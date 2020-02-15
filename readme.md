### Изучение Vue.js

1. Ставим CLI
    $ npm install --global @vue/cli
    @vue/cli@4.2.2
2. Ставим плагин для браузера vue-devtools
    https://github.com/vuejs/vue-devtools
3. Простой пример ToDo
    $ vue create todo --default
    или можно через Web: 
    $ vue ui
4. Запуск
    $ cd todo
    $ npm run serve
    при этом собирается сборка и теперь доступно на 
    http://localhost:8080/
    или запуск через npx
    $ npx vue-cli-service serve
5. Для VSCode - поставил расширение Vetur
6. Для сборки для прода 
    $ run npm run build
    при этом создается папка dist с пожатым кодом - готово к выкатке
7. Проверка на ошибки:
    $ npm run lint [options]
        Options:
        --format [formatter] specify formatter (default: codeframe)
        --no-fix             do not fix errors
        --max-errors         specify number of errors to make build failed (default: 0)
        --max-warnings       specify number of warnings to make build failed (default: Infinity)
8. Запуск тестов:
    - можно Jest подрубить
    - при создании нового проекта можно выбрать еще Unit и E2E
9. Устанавливаем так же и bootstrap
    $ npm install bootstrap@4.0.0
10. В main.js добавляем 
    import "bootstrap/dist/css/bootstrap.min.css";
11. VSCode - ставим Debugger for Chrome
12. Создать файл конфигурации vue.config.js
```
module.exports = {
  configureWebpack: {
    devtool: 'sorce-map'
  }
}
```
13. VSCode выбирае слева Run&Debug -> F5 -> Chrome
```
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "chrome",
            "request": "launch",
            "name": "vuejs: chrome",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}/src",
            "breakOnLoad": true,
            "sourceMapPathOverrides": {
                "webpack:///./*": "${webRoot}/*"
            }
        }
    ]
}
```  
14. Запускаем сервер
    $ npm run serve  
    идем в код и в режим дебагинга - на методе ставим брекпоинт
    теперь в вверху нажимаем RUN
    необходимо все запускать в той же папке с проектом - иначе пути к файлам не пройдут
    

 



