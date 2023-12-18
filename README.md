### Репозиторий по курсу Автоматическое машинное обучение.

Ссылка на соревнование на Kaggle
https://www.kaggle.com/competitions/ventilator-pressure-prediction/overview

Ссылка на гугл диск со всеми файлами сгенерированными для сабмита

$~~~~~~~~~$

#### Описание файлов и папок:

EDA.ipynb - ноутбук с анализом данных.

LightAutoML_baseline.ipynb - ноутбук с бейзлайном на основе LAMA. Лучший скор MAE=0.6824

Свое решение.ipynb - ноутбук с вариантами своего решения. Лучший скор MAE=0.6644

logs - папка с логами

$~~~~~~~~~$

#### Таблица сравнения LightAutoML baseline и решений на основе других методов:

| Модель                                                            | MAE                 |
| :-----------------------------------------------------------------|:-------------------:|
| KNeighborsRegressor (на дополнительно сгенерированных признаках)  | 0.6671              | 
| LightAutoML baseline                                              | 0.6824              | 
| VotingRegressor (KNeighborsRegressor + CatBoostRegressor)         | 0.6863              |
| KNeighborsRegressor                                               | 0.7259              |
| VotingRegressor (KNeighborsRegressor + LGBMRegressor)             | 0.7609              |
| CatBoostRegressor (RandomizedSearchCV)                            | 0.8252              |
| VotingRegressor (LGBMRegressor + CatBoostRegressor)               | 0.8592              | 
| CatBoostRegressor                                                 | 1.3124              |
| LGBMRegressor                                                     | 1.1923              |
| LGBMRegressor (RandomizedSearchCV)                                | 1.0018              |
| LinearRegression                                                  | 5.8927              |
| Lasso                                                             | 6.8041              |
| Lasso (GridSearchCV)                                              | 6.384               |
| Ridge                                                             | 5.8927              |
| Ridge (GridSearchCV)                                              | 5.8927              |
| ElasticNet                                                        | 6.7186              | 
| ElasticNet (GridSearchCV)                                         | 6.1399              |
| LinearSVR                                                         | 6.4595              |


Также я пытался применить RandomForestRegressor, но он вылетал по памяти при обучении.




