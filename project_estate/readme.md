## Исследование объявлений о продаже квартир
[ipynb](https://github.com/splin-post/Portfolio/blob/main/project_estate/project_estate_pub.ipynb)    [html](https://github.com/splin-post/Portfolio/blob/main/project_estate/project_estate_pub.html)   [pdf](https://github.com/splin-post/Portfolio/blob/main/project_estate/project_estate_pub.pdf)

### Описание проекта
Анализ архива объявлений недвижимости в С-Петербурге за несколько лет для определения рыночной стоимости объектов недвижимости
и построения в дальнейшем автоматизированной системы контроля аномалий и мошеннических действий


### Навыки и инструменты
- python
- pandas
- numpy


### Общие выводы

Во время работы с данными были произведены следующие действия:
1. проверены на наличие дубликатов
2. проверены на аномальные значения и при их наличии заменены на медианные
значения для соответствующей группы данных
3. найдены и заменены все пропущенные значения либо на соответствующие логике,
либо на медианные по соответствующей группе данных. Также часть данных была
замена на 333333, значение, которое легко в дальнейшем заменить на корректные
данны при появлении таковых и которое легко исключить из анализа понимая, что
это нереальные данные.
4. Проанализированы такие характеристики как:
- общая площадь;
- жилая площадь;
- площадь кухни;
- цена объекта;
- количество комнат;
- высота потолков;
- этаж квартиры;
- тип этажа квартиры («первый», «последний», «другой»);
- общее количество этажей в доме;
- расстояние до центра города в метрах;
- расстояние до ближайшего аэропорта;
- расстояние до ближайшего парка;
- день и месяц публикации объявления.
5. Проанализированы зависимости стоимости жилья от:
- общей площади
- жилой площади
-площади кухни
- кол-ва комнат в квартире
-типа этажа (первый, другой, последний) -дня, месяца и года публикации
объявления
6. Проанализирована взаимосвязь стоимости каждого километра от центра СПб и
стоимостью жилья.

В ходе анализа предложенных данных были выявлены следующие моменты
объявлений о продаже квартир:
1. Кол-во населенных пунктов где предлагаются квартиры на продажу составляет 308
2. Общая площадь квартир в 94% размещенных объявлений не превышает 110 кв.м.
3. Жилая площадь квартир в 94% не превышает 63 кв.м.
4. Площадь кухни квартир в 94% не превышает 18 кв.м.
5. Полная стоимость жилья в 94% не превышает 14 млн. руб.
6. Кол-во комнат в квартирах в 94% не превышает 5.
7. Высота потолоков в 93% не превышает 2.65 м оставшиеся квартиры имеют высоту
потолка выше 2.65 и не выше 3 м.
8. Этажность квартиры в 94% не превышает 16 этажей, в 50% не превышает - 9
этажей
9. Тип этажа квартиры 73% - другой (не крайние этажи), 13% - первый этаж, 14% -
последний этаж
10. Расстояние до центра города - все квартиры, объявления которые имеют
информацию о расстоянии до центра города рапологаются не далее 31 км. Все что
дальше информация отсутствует.
11. Расстояние до ближайшего аэропорта также приналичии информации
располагаются не далее 51 км. Во всех остальных случаях информация отсутствует.
12. Расстояние до ближайшего парка в 62.5% не превышает 677 метров, во всех
остальных информация отсутвует.
13. День недели публикации объявления в 75% это рабочие дни, причем вторник и
четверг более активные, с максимаьлной активностью в четверг. Люди публикуют
объявления для показа в выходные дни.
14. Месяц публикации - в первую половину года объявления публикуются более
активно, чем во вторую. С пиком в первой половине года в феврале и
последующим спадом к июню. Провал мая объясняется длинными выходными
днями, в которые как мы видели ранее, объявления публикуются наименее
активно. Низкая активность в июне, июле, августе также связана с отпусками. Во
второй половине года происходит рост активности публикаций, с ежемесячным
ростом до ноября (пик второй половины года) и резким падением до январких
уровней в декабре (в январе длинные новогодние праздники, а в декабре люди
заняты подготовкой к "Новому Году".
15. Сроки продажи - в 50% срок не превысил 94 дня, 75% - 237 дней. Также мы
оценили как быстрые продажи, продажи срок которых не превысил 43 дня и очень
долгими - со сроком более 237 дней.ю
16. В ходе анализа были проверены возможные взаимосвязи стомости жилья и
нескольких атрибутов: общая площадь, жилая площадь, площадь кухни, кол-во
комнат в квартире, а также дня недели, месфца и года публикации и типа этажа.
Как результат, имеем наличие связи между стоимостью жилья и общей площадью,
жилой площадью, площадью кухни и кол-вом комнат. Связь ослабевает
соответственно. Наличие какой-либо связи между стоимостью жилья и днем,
месяцем и годом публикации не наблюдается. Также нет связи между стоимостью
жилья и типом этажа квартиры.
17. Средняя стоимость квадратного метра в 10 населенных пунктов с максимальным
кол-вом объявлений - самая высокая стоимость в Санкт-Петербурге 114812.0
рублей за кв.м., а самая низкая в Выборге 58257.0 рублей за кв.м.
18. В ходе анализа была выялена связь между средней стоимостью расстояния от
центра города. Чем ближе к центру города, тем стоимость жилья выше, а чем
дальше от центра города, тем стоимость жилья ниже.

Также можно предоставить характеристику среднейстатистической квартиры, которую
предлагают к приобретению: Квартира общей площадью 52 кв.м., жилая площадь
составляет 30 кв.м., площадь кухни 9.6 кв.м., стоимость квартиры примерно 4.65 млн.
рублей, с 2 комнатами и высотой потолков 2.65 м., расоложена на 4 этаже, в 9 этажном
доме, на расстоянии 15 км. от центра и 33 км. от аэропорта, расстояние до ближайшего
парка 460 м. Публикация объявления сделана в четверг, в марте, срок продажи 3
месяца.
