# vscode-settings

Мои пользовательские настройки для **Visual Studio Code**.

- 🚀 Оптимизация
- 📦 Настройка языков, плагинов
- 🔥 Улучшение визуальной части

## ⚙️ Требования

Перед началом убедитесь, что у вас имеется:

- Шрифт [Google Sans Code](https://fonts.google.com/specimen/Google+Sans+Code)
- VSCode

## 📌 Установка

1. Клонировать репозиторий:

```bash
git clone https://github.com/darkfated/vscode-settings.git
cd vscode-settings
```

2. Установить настройки:
   - **Windows (CMD)**

   ```cmd
   copy /Y .vscode\settings.json "%APPDATA%\Code\User\settings.json"
   ```

   - **Windows (PowerShell)**

   ```ps1
   Copy-Item ".vscode\settings.json" "$env:APPDATA\Code\User\settings.json" -Force
   ```

   - **Linux**

   ```bash
   cp .vscode/settings.json ~/.config/Code/User/settings.json
   ```

   - **macOS**

   ```bash
   cp .vscode/settings.json ~/Library/Application\ Support/Code/User/settings.json
   ```

3. Установить из файла `extensions.txt` расширения:
   - **Windows (CMD)**

   ```cmd
    for /f %i in (extensions.txt) do code --install-extension %i
   ```

   - **Windows (PowerShell)**

   ```cmd
   Get-Content extensions.txt | ForEach-Object { code --install-extension $_ }
   ```

   - **Linux / macOS**

   ```bash
   cat extensions.txt | xargs -L 1 code --install-extension
   ```
