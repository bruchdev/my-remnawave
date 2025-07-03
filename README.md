# My Remnawave

## Страницы подписки

- [Моя](https://github.com/bruch-alex/cupertino-remnawave-subscription-page)

## Кастомный app-config

1. Копировать `app-config.json` в контейнер
```shell
curl -O https://raw.githubusercontent.com/bruch-alex/my-remnawave/refs/heads/main/app-config.json
```

2. Добавить файл в контейнер

```yaml
remnawave-subscription-page:
...
    volumes:
      - ./app-config.json:/opt/app/frontend/assets/app-config.json
...

```

3. Перезапустить контейнер

```shell
docker compose down remnawave-subscription-page && docker compose up -d remnawave-subscription-page
```
