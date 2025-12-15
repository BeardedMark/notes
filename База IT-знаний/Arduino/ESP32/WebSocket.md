``` c++
#include <WebSocketsClient.h>

WebSocketsClient ws;  

void handleIncomingMessage(const char* message) {
  String msg = String(message);
  msg.trim();

  if (msg == "on") { on(); }
  if (msg == "off") { off(); }
  if (msg == "play") { play(); }
}  

void onWebSocketEvent(WStype_t type, uint8_t* payload, size_t length) {
  switch (type) {
    case WStype_CONNECTED:
      ws.sendTXT("/register/ghost");
      break;
    case WStype_TEXT:
      handleIncomingMessage((char*)payload);
      break;
    case WStype_DISCONNECTED:
      break;
  }
}

void setupWebSocket(const char* ip, const int port, const int interval = 2000) {
  ws.begin(ip, port, "/");
  ws.onEvent(onWebSocketEvent);
  ws.setReconnectInterval(interval);
}

void setup() {
  setupWebSocket("192.168.0.30", 8080);
}

void loop() {
  ws.loop();
}  
```