### Публикация сайтов на GitHub  

1. Зарегистрируйтесь на github и установите на компьютер git с терминалом gitbash, введите начальные значения (имя и емейл) для git. 

2. Создайте на сайте githab новый  репозиторий (репо )

3. Склонируйте это репо на свою рабочую машину

   - Чтобы получить адрес жмем зеленую кнопку справа *Clone or download*

   - в открывшемся окне видим текст *Clone with HTTP* - значит все ок

   - жмем на безымянную иконку справа

   - должно быть что-то вроде такого текста https://github.com/gennadiy1970/FE-13.git т.е. в начале *https*, в конце *.git*

   - открываем терминал *gitbash* - клонируем репо и переходим в папку (директорию) проекта

     ```bash
     git clone https://github.com/ВАШЕ_ИМЯ_НА_ГИТХАБЕ/ИМЯ_РЕПОЗИТОРИЯ.git
     cd ИМЯ_РЕПОЗИТОРИЯ
     ```

4. поработали с домашним заданием - сохраняем правки локально

```bash
git add .
git commit -m "init"
```



5. отправим на сервер в единственную пока ветку master

```bash
git push
```



6.  создаем на сервере ветку gh-pages - кнопка *Branch*
![gh-pages](https://i.ibb.co/pdQwJyw/gh-page.png)
7. вводим текст _gh-pages_ и жмем кнопку ниже *Create branch: gh-page*

   

8. страница создана. Увидить ссылку на эту веб-страницу можно в разделе *Settings -> Git Hub Page*
   - приблизительно такая ссылка https://USER_NAME.github.io/ИМЯ_РЕПОЗИТОРИЯ/index.html
   -  увидить страницу по ссылке можно минут через 5-10, а до того буде ошибка 404,  это нормально, ждем 

9. закачаем эту ветку с сервера к себе на рабочу машину

```bash
git pull
```





10. Когда закончим работу в master, то сохраним в git изменения

    ```bash
    git add .
    git commit -m "add next"
    ```



11.  Переключимся на ветку gh-pages

```bash
git checkout gh-pages
```



12. git status покажет что мы в ветке gh-pages

    ```bash
    git status
    ```

    

13. Зальем в эту ветку изменения, созданные в  master

```bash
git rebase master
```



14. Отправим ветку gh-pages на сервер git

```bash
git push origin gh-pages
```



15. Переключимся на ветку master 

    ```bash
    git checkout master
    ```

    

16. git status покажет что мы в ветке master см. пп. 12



17.  Отправим ветку master на сервер git

```bash
git push master
