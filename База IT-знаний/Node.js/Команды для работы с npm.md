### **1. Основные команды**

```bash
npm -v          # версия npm
node -v         # версия node.js
npm init         # создание package.json (с вопросами)
npm init -y      # создание package.json по умолчанию
npm help <cmd>   # справка по команде
```

---

### **2. Установка пакетов**

```bash
npm install <package>          # локально в проект
npm i <package>                # короткая запись
npm install -g <package>       # глобально
npm install <package>@<ver>    # конкретная версия
npm install --save-dev <pkg>   # как devDependency
npm install --save-peer <pkg>  # как peerDependency
npm install --legacy-peer-deps # игнор зависимостей peer
```

---

### **3. Удаление и обновление**

```bash
npm uninstall <package>       # удалить пакет
npm update <package>          # обновить пакет до последней версии
npm outdated                  # проверить устаревшие пакеты
```

---

### **4. Работа с проектом**

```bash
npm init                     # создать package.json
npm list                     # список установленных пакетов
npm list --depth=0           # только верхний уровень
npm run <script>             # запуск скрипта из package.json
npm start                    # запуск скрипта "start"
npm test                     # запуск скрипта "test"
npm audit                    # проверка безопасности пакетов
npm audit fix                # авто-исправление уязвимостей
```

---

### **5. Кэш и очистка**

```bash
npm cache verify             # проверить кэш
npm cache clean --force      # очистить кэш
```

---

### **6. Работа с глобальными пакетами**

```bash
npm list -g --depth=0        # список глобальных пакетов
npm uninstall -g <package>   # удалить глобально
```

---

### **7. Полезные флаги**

- `--save-dev` — добавить в devDependencies
    
- `--save-prod` — добавить в dependencies
    
- `--global` / `-g` — глобальная установка
    
- `--force` — форсированное действие
    
- `--legacy-peer-deps` — игнор конфликтов peer
    

---

Если хочешь, я могу сделать **суперкороткую версию на одну страницу**, прямо в виде шпаргалки с командами и флагами, чтобы распечатать и держать рядом.

Хочешь, чтобы я так сделал?