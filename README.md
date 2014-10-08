suggestions_prestashop
======================

Описание модуля
---------------

Модуль выводит подсказки по ФИО/почтовому адресу и автоматически определяет индекс на странице заказа в PrestaShop при помощи сервиса "Подсказки" [DaData.ru] (https://dadata.ru).

По отзывам интернет-магазинов, модуль значительно повышает качество получаемых от пользователей данных. Клиенты начинают указывать почтовые адреса для доставки, разбитые по КЛАДР, без опечаток и с квартирами, индекс определяется автоматически. ФИО вводят без опечаток и с полом.
 
UPDATE: отзыв нашего пользователя про модуль:
просто, удобно, бесплатно. Время установки с получением ключа- минут 5. Получаем читаемый адрес, автоматическое определение индекса, при наборе в латинице предлагает читаемый адрес на кириллице, есть геотаргетинг- в поля адреса автоматически подставляется город и много что еще может. Это отличная система, которая активно развивается. Пробежался по сайту: уже сейчас- по наименованию фирмы или ИП автоматически заполняются остальные реквизиты (ИНН, расчетные счета итп). И все это- (до какого-то безумного количества запросов)- бесплатно. Совет- поставьте модуль на Престу, хотя бы просто- попробовать. 5+

Совместимость
-------------

Данный модуль совместим с версиями PrestaShop 1.5 и выше.

Дистрибутив
-----------

Последняя версия дистрибутива находится [тут] (https://github.com/hflabs/suggestions_prestashop/archive/v1.4.zip)

Установка
---------
### Распаковка модуля
Распаковать дистрибутив в папку modules рабочей директории prestashop и переименовать suggestions_prestashop-версия в suggestions_prestashop.
### Проверка корректности
В консоли администрирования prestashop выбрать пункт меню "Модули", модуль будет расположен в категории "Оформление заказа".

![](doc/dadata-prestashop-admin.png)

![](doc/dadata-prestashop-plugins.png)

![](doc/dadata-prestashop-plugins-install.png)

### Получение API токена DaData
Для этого нужно перейти на сайт [DaData] (https://dadata.ru)

![](doc/dadata-home.png)

Нажать кнопку "Войти".

![](doc/dadata-login.png)

В случае, если у вас уже есть учетная запись, необходимо ввести данные в форме, либо войти через учетную запись любой из предложенных социальных сетей.
В случае, если вы хотите зарегистрироваться с помощью e-mail адреса перейдите по ссылке "Это недолго" в верхней части формы и заполните предлагаемые поля.

![](doc/dadata-new.png)

Далее в правом-верхнем углу необходимо нажать кнопку профиля и выбрать пункт "Настройки"

![](doc/dadata-menu.png)

В появившейся форме нажать на ссылку сгенерировать.

![](doc/dadata-settings-initial.png)

Полученный токен необходимо скопировать.

![](doc/dadata-settings-token.png)

### Включение и настройка плагина
В консоли администрирования нужно нажать кнопку установить напротив модуля "Подсказки DaData.ru"

![](doc/dadata-prestashop-plugins-install.png)

Вы попадете на страницу настроек плагина

![](doc/dadata-prestashop-plugins-settings-edited.png)

Далее необходимо ввести токен полученный ранее и нажать кнопку "Сохранить"

Плагин готов к работе.

Настройка
---------

Плагин имеет следующие настройки:
* Максимальное количество подсказок в списке - количество строк в выпадающем списке при заполнении.
* Автоматическое исправление по мере ввода - необходимо-ли пытаться исправить слова с опечатками.
* Включить подсказки по ФИО - использовать модуль подсказки для подсказок по ФИО.
* Включить подсказки по адресу - использовать модуль подсказки для подсказок по адресу.
* Версия подсказок - какой сервис использовать при работе (подробнее см. [Версии подсказок] (https://dadata.ru/suggestions/#pricing)).
* Идентификатор поля, хранящего регионы - в каком выпадающем списке заполнены регионы. (id_state - регионы добавлены как штаты России, id_country - регионы указаны как страны)


Использование
-------------

После включения модуля на странице ввода имени и адреса поля гранулярные поля заменяются на единое. При вводе данных выпадает список с наиболее релевантными вариантами заполнения. 

История изменений
-----------------

* 1.4
 * Исправлены ошибки при работе с Firefox и PrestaShop 1.6
* 1.3
 * Добавлена возможность работы со стандартным заказом (5 шагов)
 * Функциональность подсказок теперь работает на всех формах (в т. ч. и на редактировании адреса)
 * Добавлена настройка идентификатора поля, из которого выбираются регионы России
* 1.2
 * Добавлена возможность выборочно включать подсказки для ФИО или Адреса.
 * Добавлена возможность использования платной версии подсказок (подробнее см. [Версии подсказок] (https://dadata.ru/suggestions/#pricing))
 * Обновлена версия API подсказок
* 1.1
 * Добавлена функциональность отключения подсказок при выборе страны отличной от россии.
* 1.0
 * Первый релиз

Скриншоты
---------
![](doc/dadata-prestashop-demo-1.png)
![](doc/dadata-prestashop-demo-2.png)
![](doc/dadata-prestashop-demo-3.png)
