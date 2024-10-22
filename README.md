# py-recall

## Environment Setup

### Использование pyenv

1. **Установите pyenv через Homebrew:**
   ```bash
   brew install pyenv
   ```

2. **Добавьте pyenv в ваш `.bash_profile` или `.zshrc`:**
   ```bash
   echo 'export PATH="$HOME/.pyenv/bin:$PATH"' >> ~/.zshrc
   echo 'eval "$(pyenv init --path)"' >> ~/.zshrc
   ```

3. **Перезагрузите терминал:**
   ```bash
   source ~/.zshrc
   ```

4. **Установите нужную версию Python:**
   ```bash
   pyenv install 3.x.x  # Замените 3.x.x на нужную версию
   ```

5. **Установите версию по умолчанию:**
   ```bash
   pyenv global 3.x.x
   ```

5. **Установите локальную версию:**
   ```bash
   pyenv local 3.x.x
   ```

6. **Проверьте версию Python:**
   ```bash
   python --version
   ```

### Установка `pyenv-virtualenv`

1. **Установите `pyenv-virtualenv`:**
   ```bash
   brew install pyenv-virtualenv
   ```

2. **Добавьте настройки в ваш конфигурационный файл:**
   ```bash
   export PATH="$HOME/.pyenv/bin:$PATH"
   eval "$(pyenv init --path)"
   eval "$(pyenv init -)"
   eval "$(pyenv virtualenv-init -)"
   ```

3. **Перезагрузите терминал:**
   ```bash
   source ~/.zshrc
   ```

### Основные команды `pyenv-virtualenv`

1. **Создание виртуального окружения:**
   ```bash
   pyenv virtualenv 3.9.17 myenv
   ```
2. **Просмотр доступных виртуальных окружений:**
   ```bash
   pyenv virtualenvs
   ```

3. **Активировать виртуальное окружение:**
   ```bash
   pyenv activate myenv
   ```

4. **Деактивировать виртуальное окружение:**
   ```bash
   pyenv deactivate
   ```

5. **Удаление виртуального окружения:**
   ```bash
   pyenv uninstall myenv
   ```

### Создание файла `requirements.txt`

1. **Создание вручную**: Вы можете создать файл `requirements.txt` вручную и указать в нем необходимые пакеты. Формат записи:
   ```
   numpy==1.21.2
   requests>=2.25.1
   ```

2. **Автоматическое создание**
 Если у вас уже установлен ряд библиотек, вы можете автоматически создать файл с помощью команды:
   ```bash
   pip freeze > requirements.txt
   ```

### Установка зависимостей

Чтобы установить все зависимости, указанные в `requirements.txt`, выполните команду:
```bash
pip install -r requirements.txt
```

### Обновление зависимостей
Чтобы обновить пакет, можно изменить версию в `requirements.txt` и снова запустить команду установки. Также можно использовать:
```bash
pip install --upgrade -r requirements.txt
```

### Проверка зависимостей

Для проверки установленных пакетов и их версий используйте:
```bash
pip list
```