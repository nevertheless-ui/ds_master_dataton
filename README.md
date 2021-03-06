# Торговые точки вблизи ТПУ, г.Москва

<img align="right" width="100" height="100" src="https://i.ibb.co/TbyCPm8/logoza-ru-1.png">

## Команда «Data SkyScrapers»

\
ФИЛИППЕНКО Артем, ГАБИТОВ Ильдар, КАНДЫБИН Вячеслав,  КОМПАНИЕЦ Юлия, ПЕТРОВ Егор


## Описание датасета

В датасете содержится информация о торговых точках и их принадлежность к зоне охвата размещенных вблизи транспортно-пересадочных узлов в городе Москва.

Датасет может быть использован для выбора места расположения новой торговой точки по критерию "наиболее благоприятные условия (низкая плотность конкурентов и высокий уровень пассажиропотока)".

## Источники

В датасете были использованы следующие данные с сайта [Портал открытых данных](https://data.mos.ru):

* [Транспортно-пересадочные узлы](https://data.mos.ru/opendata/7704786030-transportno-peresadochnye-uzly?pageNumber=1&versionNumber=4&releaseNumber=27)
* [Стационарные торговые объекты](https://data.mos.ru/opendata/7710881420-statsionarnye-torgovye-obekty?pageNumber=1&versionNumber=1&releaseNumber=22)
* [Бытовые услуги на территории Москвы](https://data.mos.ru/opendata/7710881420-bytovye-uslugi-na-territorii-moskvy/data/table?versionNumber=2&releaseNumber=30)

Расчет торговой зоны и зоны охвата магазина был произведен на основе статьи ["Расчет торговой зоны и зоны охвата магазина"](http://www.arhitrade.com/education.php?Id=43).

## Методы сбора и обработки

Здесь скоро будет текст

## Структура репозитория


    .
    ├── data                    # датасеты из открытых источников
    ├── test                    # просто пример структуры
    │   ├── benchmarks          
    │   ├── integration         
    │   └── unit                
    ├── middle_results.json     # структура датасета в формате json
    └── README.md



## Структура датасета



| Название | Описание | Тип | Значения |
| ------ | ------ | ------ | ------ |
| global_id | id торгового объекта | int |  |
| Name | Название торгового объекта | str | |
| IsNetObject | Является ли объект сетевым | str | да, нет|
| OperatingCompany | Управляющая компания | str | |
| TypeService| Тип предоставляемой услуги | str | |
| TypeObject | Тип объекта | str | |
| AdmArea | Административный округ | str | |
| District | Район | str| |
| PublicPhone | Номер телефона | str | |
| WorkingHours | Время работы | str | |
| ClarificationOfWorkingHours | Уточнение времени работы | str | |
| PlaceSize | Размер объекта | int | |
| tpu_TPUName | Название транспортно-пересадочного узла (ТПУ)| str | |
| tpu_global_id | id ТПУ| int | |
| tpu_AdmArea | Административный округ, в котором находится ТПУ| str | |
| tpu_District | Район, в котором находится ТПУ | str | |
| tpu_NearStation | Ближайшая к ТПУ станция| str | |
| tpu_YearOfComissioning | Год сдачи ТПУ в эксплуатацию | int | |
| tpu_Status | Стасус ТПУ | str | проект, построен, строится |
| tpu_AvailableTransfer| Доступные виды трансфера | str | |
| tpu_CarCapacity | Количество машино-мест возле ТПУ| float | |
| latitude | Координаты расположения торгового объекта: широта | float | |
| longitude | Координаты расположения торгового объекта: долгота | float | |
| tpu_latitude | Координаты расположения ТПУ: широта| float | |
| tpu_longitude | Координаты расположения ТПУ: долгота| float | |



