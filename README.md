Базовая Gulp-сборка для вёрстки.

- Собирает и оптимизирует `html`, `sass`, `js`, изображения и шрифты
- Использует `gulp-rigger` для работы с html-chunks
- Включает файлы настроек различных линтеров
- Все ошибки логируются в консоль
- Добавляет вендорные префиксы
- Совмещает и оптимизирует медиазапросы
- Есть режим разработки и сборки в продакшн
- Автоматический деплой на GitHub Pages

### Setting up Dev

Для быстрого старта необходимо:

Установить все зависимости.

```shell
npm install
```

И запустить режим разработки.

<!-- ```shell -->
npm start
```

Во вкладке браузера перейти по адресу
[http://localhost:1234](http://localhost:1234).

### Building

Для того чтобы создать оптимизированные файлы для хостинга, необходимо выполнить
следующую команду. В корне проекта появится папка `build` со всеми
оптимизированными ресурсами.

```shell
npm run build
```

### Deploying / Publishing

Сборка может автоматически деплоить билд на GitHub Pages удаленного (remote)
репозитория. Для этого необходимо в терминале выполнить следующую команду.

```shell
npm run deploy
```

Если нет ошибок в коде и свойство `homepage` указано верно, запустится сборка
проекта в продакшен, после чего содержимое папки `build` будет помещено в ветку
`gh-pages` на удаленном (remote) репозитории. Через какое-то время живую
страницу можно будет посмотреть по адресу указанному в отредактированном
свойстве `homepage`.

## Configuration

- Все файлы стилей должны лежать в папке `src/sass` и импортироваться в
  `src/sass/main.scss`
- Изображения добавляйте в папку `src/images`
- Локальные шрифты идут в папку `src/fonts`

Пример изображения в HTML, после того как файл `picture.png` был добавлен в
папку `src/images`.

```html
<img src="./images/picture.png" />
```

Пример изображения в CSS, после того как файл `picture.png` был добавлен в папку
`src/images`.

```css
.my-class {
  background-image: url('../images/picture.png');
}
```
