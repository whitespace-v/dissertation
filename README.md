## Название

Программная система мониторинга состояния пациента в процессе лечения с возможностью рекомендаций для его коррекции

___
## Введение

Современная медицина стремительно развивается, предлагая всё более точные диагностические методы и эффективные терапевтические подходы. Однако, для достижения оптимальных результатов лечения, необходимо не только своевременно диагностировать заболевание, но и непрерывно мониторить состояние пациента и вносить коррективы в план лечения в случае необходимости. 

В России, как и в остальных странах мира, наблюдается острая нехватка в стабильности мониторинга состояния пациентов. Отсутствие стабильного качественного мониторинга приводит к ряду проблем, включая:

-  Задержку в обнаружении ухудшения состояния пациента, что может привести к осложнениям и ухудшению прогноза заболевания.
-  Нерациональное использование медицинских ресурсов, обусловленное отсутствием объективной информации о состоянии пациента.
-  Увеличение времени госпитализации и конечной себестоимости курса лечения, из-за необходимости постоянного наблюдения за пациентом медицинским персоналом.
- Полное отсутствие и невозможность предоставления должного, полного мониторинга при амбулаторном лечении пациента.

Данная работа посвящена разработке такой системы, которая позволит:

-  Обеспечить непрерывный мониторинг состояния пациента и своевременно выявлять изменения в его состоянии.
- Предоставлять врачам рекомендации по корректировке лечения на основе анализа данных мониторинга.
-  Снизить риск осложнений и улучшить прогноз заболевания.
- Оптимизировать использование медицинских ресурсов и повысить эффективность лечения.
- Снизить нагрузку на медицинский персонал и освободить его для решения более сложных задач. 
- Существенно снизить себестоимость стационарного лечения
- Значительно повысить эффективность амбулаторного лечения

Целью данной работы является разработка модели мониторинга состояния пациента с использованием машинного обучения, позволяющая предоставлять данные и  рекомендации для его коррекции. Результатом работы будет являться модель, способная составлять рекомендации, необходимые для улучшения текущего состояния пациента.

## Материалы

Основными источниками данных являлись ресурсы, предоставляющие данные о заболеваниях и их проявлениях на человека.
В их число входили такие ресурсы как:
- Крупные датасеты с информацией о более чем 245 заболеваниях data.world [data.world], 
- Публичная база данных MalaCards: The Human Disease Database, с огромным количеством информации, центрированной с 75 ресурсов по всему миру  [malacards.org], 
Также, в качестве дополнительных источников данных использовался 
- сайт университета Stanford [stanford.edu], с датасетами *Classification of diseases into disease categories* и  *Disease categories and symptomatics*.
Данные из этих источников предоставлялись в различных форматах, в том числе и в виде форматов csv и xlsx, поэтому они были предварительно приведены к одному формату csv для дальнейшей обработки и анализа. Данные состоят из значения времени, которое является промежутком времени с начала наблюдения за пациентом, а также значений общего состояния, симптомы, проведенные тесты и процедуры, симптоматика во время приема различных препаратов, а также  некоторые данные о пациенте

## Методы

Для анализа данных применялся коэффициент корреляции Пирсона и Кендалла, функция автокорреляции, а также функция частной автокорреляции, тест Дикки-Фуллера, а также была построена линия тренда со сглаживанием для определения выбросов и аномалий в выборке. Для релизации анализа и обработки данных использовалась IDE R Studio
Для разработки модели и системы использовался язык Python, в качестве среды использовалась IDE PyСharm. В качестве методов машинного обучения использовались модели линейной регрессии и модели градиентного бустинга. Для оценки качества полученной модели использовались следующие метрики качества:

1. MAE
2. RMSE
3. R2 Score

В качестве функции потерь использовался MSE. Для обучения и валидации модели использовался k-fold.

## Результаты

В ходе работы была произведена предобработка данных о пациентах и выбранном методе лечения.  
Для составления рекомендаций выполнено построение двух ансамблей моделей машинного обучения на основе линейной регрессии и градиентного бустинга.  
Результаты моделирования показали неудовлетворительные результаты, а именно R-2 score, равный 0.6. Такого коэффициента недостаточно для решения поставленной задачи.
