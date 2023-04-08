## Отток клиентов

Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.
Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Вам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком. 
Постройте модель с предельно большим значением *F1*-меры. Чтобы сдать проект успешно, нужно довести метрику до 0.59. Проверьте *F1*-меру на тестовой выборке самостоятельно.
Дополнительно измеряйте *AUC-ROC*, сравнивайте её значение с *F1*-мерой.

Источник данных: [https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling](https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling)

Целью данного проекта является - прогнозирование того, уйдёт клиент из банка в ближайшее время или нет.
Для достижения данной цели в ходе реализации проекта требуется:
1. Подготовить данные. Рассмотреть их на наличение аномалий, пропущенных значений или дубликатов. 
2. Рассмотреть являются ли все столбцы информативными для обучения модели, если нет - удалить лишнии столбцы.
3. Рассмотреть баланс классов.
4. Определить target.Разделить данные на тренировочные, тестовые и валидационные.
5. Рассмотреть различные значения класов, определить, какие преобразования к ним более корректно применить.Преобразовать данные с помощью One-Hot Encoding и standardScaler.
6. Обучить несколько моделей на неуравновешенных данных. Подобрать гиперпараметры.
7. Уравновесить классы с использованием апсемплинга и даунсемплинга.
8. Обучить несколько моделей на уравновешенных данных, получить точность больше 0.59
9. Измерить AUC-ROC и сравнить с F1-мерой.

В ходе выполнения данных мы прогнозировали то, уйдёт клиент из банка в ближайшее время или нет. 
Для решений этой задачи были подготовлены данные, рассмотрены и устранены проблемы с дисбалансом классов, рассмотрены и преобразованы данные с использованием One-Hot Encoding и Scaler, данные были подготовлены для обучения моделей.
Далее были обучены три модели(DecisionTreeClassifier, RandomForestClassifier, LogisticRegression), которые показали неплохие результаты даже на несбалансированных данных, после чего данные были сбалансированы и модели были обучены снова. 
По результатом обучения всех моделей были выбраны две модели с лучшими и худшими результатами и для них были построены roc-кривык и посчитан auc.
Лучший результат был получен с помощью RandomForestClassifier и составил AUC=0.83 и F1=0.6