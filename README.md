# Установка web приложения на ruby

## Предварительные настройки
Необходимо установить на controlnode приватный ключ имеющий доступ к репозитарию.
Для проброса приватного ключа на удаленный сервер необходимо перед запуском плейбука выполнить на controlnode следующие команды:

```bash
eval "$(ssh-agent -s)"
ssh-add /home/<user>/.ssh/id_rsa
# Можно проверить добавился ли ключ
# ssh-add -l
```

Выполнить установку необходимых ролей и коллекций:
```bash
ansible-galaxy install -r requirements.yml
```

При необходимости поменять переменные в файле:
`vars/vars.yml`

## Запуск плейбука
```bash
ansible-playbook playbook.yml
```

## TODO
Добавить описание переменных