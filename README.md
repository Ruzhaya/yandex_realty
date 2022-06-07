# [Проект Исследование объявлений о продаже квартир](https://github.com/Ruzhaya/Data_analysis_projects/blob/main/Project_3.ipynb)
В распоряжении данные сервиса Яндекс.Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктах за несколько лет. Нужно научиться определять рыночную стоимость объектов недвижимости. Задача — установить параметры. Это позволит построить автоматизированную систему: она отследит аномалии и мошенническую деятельность.

По каждой квартире на продажу доступны два вида данных. Первые вписаны пользователем, вторые получены автоматически на основе картографических данных. Например, расстояние до центра, аэропорта, ближайшего парка и водоёма.

## Описание данных

- `airports_nearest` — расстояние до ближайшего аэропорта в метрах (м)
- `balcony` — число балконов
- `ceiling_height` — высота потолков (м)
- `cityCenters_nearest` — расстояние до центра города (м)
- `days_exposition` — сколько дней было размещено объявление (от публикации до снятия)
- `first_day_exposition` — дата публикации
- `floor` — этаж
- `floors_total` — всего этажей в доме
- `is_apartment` — апартаменты (булев тип)
- `kitchen_area` — площадь кухни в квадратных метрах (м²)
- `last_price` — цена на момент снятия с публикации
- `living_area` — жилая площадь в квадратных метрах (м²)
- `locality_name` — название населённого пункта
- `open_plan` — свободная планировка (булев тип)
- `parks_around3000` — число парков в радиусе 3 км
- `parks_nearest` — расстояние до ближайшего парка (м)
- `ponds_around3000` — число водоёмов в радиусе 3 км
- `ponds_nearest` — расстояние до ближайшего водоёма (м)
- `rooms` — число комнат
- `studio` — квартира-студия (булев тип)
- `total_area` — площадь квартиры в квадратных метрах (м²)
- `total_images` — число фотографий квартиры в объявлении

# [Проект Исследование тарифов мобильной связи](https://github.com/Ruzhaya/Data_analysis_projects/blob/main/Project_4.ipynb)
Необходимо было проанализировать данные 500 пользователей оператора связи, чтобы определить какой тариф приносит больше денег и в какую рекламу стоит вкладывать рекламный бюджет.

## Описание тарифов
 
**Тариф «Смарт»**

1. Ежемесячная плата: 550 рублей
2. Включено 500 минут разговора, 50 сообщений и 15 Гб интернет-трафика
3. Стоимость услуг сверх тарифного пакета: 1. минута разговора: 3 рубля («Мегалайн» всегда округляет вверх значения минут и мегабайтов. Если пользователь проговорил всего 1 секунду, в тарифе засчитывается целая минута); 2. сообщение: 3 рубля; 3. 1 Гб интернет-трафика: 200 рублей.
**Тариф «Ультра»**

1. Ежемесячная плата: 1950 рублей
2. Включено 3000 минут разговора, 1000 сообщений и 30 Гб интернет-трафика
3. Стоимость услуг сверх тарифного пакета: 1. минута разговора: 1 рубль; 2. сообщение: 1 рубль; 3. 1 Гб интернет-трафика: 150 рублей.

## Описание данных 
Таблица `users` (информация о пользователях):<br>
* *user_id* — уникальный идентификатор пользователя
* *first_name* — имя пользователя
* *last_name* — фамилия пользователя
* *age* — возраст пользователя (годы)
* *reg_date* — дата подключения тарифа (день, месяц, год)
* *churn_date* — дата прекращения пользования тарифом (если значение пропущено, то тариф ещё действовал на момент выгрузки данных)
* *city* — город проживания пользователя
* *tarif* — название тарифного плана <br>

Таблица `calls` (информация о звонках):<br>
* *id* — уникальный номер звонка
* *call_date* — дата звонка
* *duration* — длительность звонка в минутах
* *user_id* — идентификатор пользователя, сделавшего звонок <br>

Таблица `messages` (информация о сообщениях): <br>
* *id* — уникальный номер звонка
* *message_date* — дата сообщения
* *user_id* — идентификатор пользователя, отправившего сообщение <br>

Таблица `internet` (информация об интернет-сессиях): <br>
* *id* — уникальный номер сессии
* *mb_used* — объём потраченного за сессию интернет-трафика (в мегабайтах)
* *session_date* — дата интернет-сессии
* *user_id* — идентификатор пользователя <br>

Таблица `tariffs` (информация о тарифах): <br>
* *tariff_name* — название тарифа
* *rub_monthly_fee* — ежемесячная абонентская плата в рублях
* *minutes_included* — количество минут разговора в месяц, включённых в абонентскую плату
* *messages_included* — количество сообщений в месяц, включённых в абонентскую плату
* *mb_per_month_included* — объём интернет-трафика, включённого в абонентскую плату (в мегабайтах)
* *rub_per_minute* — стоимость минуты разговора сверх тарифного пакета (например, если в тарифе 100 минут разговора в месяц, то со 101 минуты будет взиматься плата)
* *rub_per_message* — стоимость отправки сообщения сверх тарифного пакета
* *rub_per_gb* — стоимость дополнительного гигабайта интернет-трафика сверх тарифного пакета (1 гигабайт = 1024 мегабайта)

# [Проект исследование рынка компьютерных игр](https://github.com/Ruzhaya/Data_analysis_projects/blob/main/Project_5.ipynb)
Из открытых источников доступны исторические данные о продажах игр, оценки пользователей и экспертов, жанры и платформы (например, Xbox или PlayStation). Необходимо выявить определяющие успешность игры закономерности. Это позволит магазину компьютерных игр сделать ставку на потенциально популярный продукт и спланировать рекламные кампании.

## Описание данных¶
* `Name` — название игры
* `Platform` — платформа
* `Year_of_Release` — год выпуска
* `Genre` — жанр игры
* `NA_sales` — продажи в Северной Америке (миллионы проданных копий)
* `EU_sales` — продажи в Европе (миллионы проданных копий)
* `JP_sales` — продажи в Японии (миллионы проданных копий)
* `Other_sales` — продажи в других странах (миллионы проданных копий)
* `Critic_Score` — оценка критиков (максимум 100)
* `User_Score` — оценка пользователей (максимум 10)
* `Rating` — рейтинг от организации ESRB (англ. Entertainment Software Rating Board). Эта ассоциация определяет рейтинг компьютерных игр и присваивает им подходящую возрастную категорию.

# [Проект маркетинговое исследование поведения пользователей приложения](https://github.com/Ruzhaya/Data_analysis_projects/blob/main/Project_7.ipynb)
В распоряжении был лог сервера с данными о посещениях приложения новыми пользователями, зарегистрировавшимися в период с 2019-05-01 по 2019-10-27, выгрузка их покупок за этот период, а также статистика рекламных расходов. Предстояло изучить, как люди пользуются продуктом, когда они начинают покупать, сколько денег приносит каждый клиент, когда он окупается и какие факторы отрицательно влияют на привлечение пользователей.

## Описание данных 
Таблица `visits_log_short` (лог сервера с информацией о посещениях сайта):

* *User Id* — уникальный идентификатор пользователя
* *Device* — категория устройства пользователя
* *Session start* — дата и время начала сессии
* *Session End* — дата и время окончания сессии
* *Channel* — идентификатор рекламного источника, из которого пришел пользователь
* *Region* - страна пользователя

Таблица `orders_log_short` (информация о заказах):

* *User Id* — уникальный id пользователя, который сделал заказ
* *Event Dt* — дата и время покупки
* *Revenue* — выручка

Таблица `costs_short` (информация о затратах на маркетинг):

* *Channel* — идентификатор рекламного источника
* *Dt* — дата
* *Costs* — затраты на этот рекламный источник в этот день
