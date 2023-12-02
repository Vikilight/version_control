#Домашняя работа1

## Как работать с Git?

### Подготовка к работе

При первом запуске нужно познакомится с программрй и вввести свое имя и емаил командами: *git config --globai user.name <Ваше Имя>*
и *git config --global user.email <Ваша почта>*

Для того чтобы начать работу необходимо инициализировать программу с помощью команды: *git init* после этого появится в выбранной папке для сохранения скрытая папка *.git*

### Просмотр состояния репозитория 

для того чтобы просмореть текущий статус ващего файла используем команду: *git status*

Чтобы созлать коммит(сохранение) необходимо выполнить команду: *git commit*

### Списки

#### Ненумерованный список

* первый 
* второй
* третий

#### Нумерованый список
1. первый
2. второй

### Добавление WEB ссылок
чтобы добавить ссылку нужно обрамить ее квадратными скобками и в круглых скобках и ковычках вставить саму ссылку

* перейди [по ссылке](https://gb.ru "Всплывающая подсказка")

## Основные команды для GIT

```sh
git add
```
добавить файл к коммиту

```sh
git status
```
получить информацию от git о его текущем состоянии

```sh
git commit -m
```
создание коммита
```sh
git checkout
```
переход от одного комиита к другому

```sh
git log
```
вывод на экран истории всех коммитов с их кодами

```sh
git diff
```
увидеть разницу между текущим файлом и сохраненным файлом


## Создание веток
Для создания веток истользуется команда git branch

Чтобы перейти на ветку нужно ввести команду git checkout branch_name (имя созданной ветки)
### Чтобы переключится на другую ветку необходимо набрать команду git checkaout branch_name

# Добавление изображения в Git
Чтобы добавить картинку необходимо перенести ее в папку с репозиторием, затем поставить "! [имя картинки] (путь картинки)"

вот так:
![Лошадка](horse.jpeg)

## Слияние веток
для того чтобы соеденить ветки нужно ввести git marge branch_name
## Удаление слитых веток
git branch -d branch_name

# Связка с удаленным репозиторием

Для начала регестрируемся на https://github.com/ и создаем в своем аккаунте новый репозиторий. затем гит сам даст подсказку что необходимо сделать. 

Нужно связать наш локальный репозиторий и удаленный для этого используем команды: 
Для начала корипуем ссылку на гитхаб (с удаленным репозиторием) и командой:

```sh
git clone (ссылка)
``````

далее нужно пепеименовать ветку master на main
командой:
```sh
git branch -M main
```
Затем связываем репозитории
```sh
git git remote add origin (ссылка)
```
Если про прошло успешно то выбрасываем изменения на удаленный репозиторий
```sh
 git push -u origin main
 ```
 Проветить можно командой
 ```sh
 git remote -v
 ```
 что бы проверить изменения в уданенном репозитоиии ( загрузить изменения на локальный реп если были изменения в удаленном)

 ```sh
 git pull
 ```
  вылалнкуть на удаленный реп новую ветку нужно командой 
  ```sh
  git push --set-upstrem origin имя ветки
  ```
  слить ветки с конфликтом ( если произошел конфликн на ветках локального и удаленного реп, то нужно залить удаленную версию и решить конфликт в редакторе)
  ```sh
  git pull --rebase
  ```
  зафиксировать изменения после конфликта 
  ```sh
  git rebase --continue
  ```
  