# Изучение воронки продаж и анализ A/B эксперимента  

## Описание проекта  

Данный проект посвящен изучению воронки продаж в приложении по продаже продуктов питания, а также анализу результатов A/B эксперимента, проведенного на пользователях. Основная цель проекта - выявить ключевые этапы взаимодействия пользователей с приложением, оценить эффективность различных методов продажи и определить, как изменение некоторых факторов может повлиять на конверсию и продажи.  

## Этапы выполнения проекта  

### Шаг 1. Определение целей и задач  

На данном этапе мы сформулировали основные цели исследования:  
- Определить ключевые этапы воронки продаж.  
- Проанализировать влияние A/B эксперимента на поведение пользователей приложения.  

### Шаг 2. Подготовка данных  

Следующим шагом будет сбор и предварительная обработка данных, необходимых для анализа. Здесь мы сосредоточимся на:  
- Сборе данных о действиях пользователей в приложении.  
- Обработке данных для удаления дубликатов и устранения пропусков.  
- Подготовке данных для визуализации и дальнейшего анализа.  

### Шаг 3. Изучение и проверка данных  

На данном этапе мы проведем анализ собранных данных для:  
- Оценки их качества и полноты.  
- Проведения предварительных статистических проверок.  
- Выявления возможных аномалий и закономерностей в данных.  

### Шаг 4. Изучение воронки событий  

В этом шаге мы проанализируем воронку событий, чтобы определить, на каких этапах пользователи теряют интерес или прекращают взаимодействие с приложением. Мы будем использовать:  
- Визуализации, которые помогут отследить конверсию на каждом этапе воронки.  
- Метрики, такие как средняя продолжительность сессии и количество действий пользователей.  

### Шаг 5. Изучение результатов эксперимента  

На заключительном этапе анализа мы сосредоточимся на результатах A/B эксперимента:  
- Сравнении ключевых показателей между контрольной и тестовой группами.  
- Оценке статистической значимости полученных результатов.  
- Выявлении факторов, способствующих улучшению показателей продаж.  

# Выводы и рекомендации  

На этапе предобработки данных в датасетах events, ab_events и new_users мы преобразовали типы данных в колонках с датами, а также обнаружили пропуски в колонке details датасета ab_events, которые был решено оставить без изменений. 
Проведение A/B теста во время новогодней промо-акции под question делает его результаты сомнительными из-за повышенной покупательской активности в этот период.   

Аудитория теста была сформирована не по ТЗ, и хотя количество пользователей достигло 6000, доля пользователей из ЕС составила менее 15%. 
Разделение групп также было некорректным, так как группа A составила 57% от общего числа пользователей, что нарушает правило о максимальном превышении 51%. 
Однако тест на статистическую значимость показал, что разница в размерах групп не случайна.  

### На этапе EDA  

**Группа A:**  
- Количество событий: 19,304  
- Количество пользователей: 2,747  
- 65% пользователей перешли с этапа логина на страницу продукта, 49% из них совершили покупку.  
- Пик событий наблюдается с 14 по 23 декабря, после чего наблюдается спад.  

**Группа B:**  
- Количество событий: 5,394  
- Количество пользователей: 928  
- 56% пользователей перешли с этапа логина на страницу продукта, также 49% совершили покупку.  

Анализ воронок показал, что просмотр корзины не является обязательным этапом и по числу событий уступает даже покупкам.   

### После проверки гипотез  

Нулевая гипотеза была отвергнута по всем конверсиям (покупка, корзина, логин, страница товара), однако результаты A/B теста не показательны из-за временных обстоятельств. 
Различия в выборках между группами превышают допустимые 1-2% и составили более 7%. Конверсии в группе B оказались ниже, что вывело результаты теста за пределы ожидаемого.   

### Рекомендации  

Тест был проведен неудачно и не может считаться успешным. Рекомендуется повторить тест при подходящих условиях или не внедрять нововведения на основании текущих результатов.