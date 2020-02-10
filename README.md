# Установка зависимостей

Установить в проект следующие пакеты.

```bash
npm install --save-dev prettier husky lint-staged
```

## Интерграция плагинов

Ссылки на документацию по интеграции плагинов в популярные редакторы.

- [Prettier editor integration](https://prettier.io/docs/en/editors.html)
- [ESLint editor integration](https://eslint.org/docs/user-guide/integrations)

## Настройки VSCode

Для комфортной работы, после установки плагинов, нужно добавить несколько
настроек редактора для автосохранения и форматирования файлов.

```json
{
  "files.autoSave": "onFocusChange",
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
```