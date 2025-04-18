ПРОЕКТ: Прогнозирование страховых случаев и выявление групп повышенного риска

Цель: Провести комплексный анализ датасета медицинских страховых случаев для выявления ключевых закономерностей и разработки новых признаков.

1. Исследовательский анализ данных (EDA)
Анализ числовых (age, bmi, children, charges) и категориальных (sex, smoker, region) признаков.

Поиск аномалий, корреляций и взаимосвязей между переменными.

Визуализация распределений, box-plot’ов и матрицы корреляций.

2. Создание новых признаков
emergency_care (экстренная помощь):

Логика: charges > среднее + 3 * стандартное отклонение → 1, иначе 0.

regional_outlier (аномалия региона):

Логика: charges значительно отклоняются от медианы по региону → 1.

health_risk_behavior (рискованное поведение):

Логика: BMI > 30 И smoker = yes И charges < медиана → 1.

3. Проверка гипотез
Гипотеза 1: Пациенты с health_risk_behavior = 1 чаще нуждаются в emergency_care.

Гипотеза 2: Регионы с большим числом regional_outlier имеют более высокий средний возраст населения.

4. Дополнительно (по желанию)
Сегментация клиентов (например, по возрасту, курению, BMI) для выявления групп риска.

Вывод: Анализ поможет страховой компании выявить ключевые факторы риска, оптимизировать тарифы и разработать превентивные меры.
