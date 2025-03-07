# Парсер постов в социальной сети TenChat

## Использование
Данный проект использует Python 3.12

## Установка зависимостей и запуск
Для установки зависимостей, выполните команду:
```
pip install -r requirements.txt
```
Запуск парсера происходит командой:
```
python -m parser
```

### Запуск в Docker
Создайте контейнер командой:
```
docker build -t tenchat-parser .
```
Запустите его командой:
```
docker run -it --rm tenchat-parser
```

## Конфигурация парсера при запуске
После запуска парсера в терминал будет выведено сообщение:
`Выберите две цифры (1 или 2). 1 - если нужно собрать данные по всем комментариям поста; 2 - если только по последнему:` - введите необходимое значение
Если был выбран первый режим, то скрипт выведет в терминал все данные по комментариям к посту.
Далее, если был выбран второй режим, то в терминал будет выведено:
`Задайте частоту в минутах, с которой скрипт будет проверять наличие нового комментария:` - введите число от 1 до бесконечности (шутка). С данной частотой скрипт будет проверять наличие нового комментария к посту, предварительно напечатав в терминал данные по последнему комментарию в посте.
Во втором режиме результатам работы скрипта являются данные к посту:
- имя комментатора
- текст комментария
- ссылка на фото профиля комментатора
