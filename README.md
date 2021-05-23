# Настройка pre-commit хуков

## 1 - Установка зависимостей

Установить в проект следующие пакеты.

```bash
npm install --save-dev prettier eslint
```

## 2 - Инициализация lint-staged и husky

Выполнить в терминале следующую команду. Она установит и настроит `husky` и
`lint-staged` в зависимости от инструментов качества кода из зависимостей
проекта в `package.json`.

При выполнении будут просканированы файлы проекта, это может занять какое-то
время. После сканирования создастся папка `.husky` с pre-commit хуком, а в файле
`package.json` будут автоматически добавлены настройки форматирования и
исправления кода измененёных файлов перед коммитом.

```bash
npx mrm lint-staged
```

## 3 - Интерграция плагинов

Ссылки на документацию по интеграции плагинов в популярные редакторы.

- [Prettier editor integration](https://prettier.io/docs/en/editors.html)
- [ESLint editor integration](https://eslint.org/docs/user-guide/integrations)

## 4 - Настройки VSCode

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
