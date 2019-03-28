В виде идеи:
Предсказывать по тексту отзыва и его оценке является ли он фейковым (тоесть преподносит банк или принижает его не заслужено) или он честный отзыв. 

### 0. Разобратся в структуре файлов (все)
  Описание данных лежит в файле data_description
### 1. Препроцессинг данных (<username> ответственный).
1. Удаление неинформативных слов
2. Токениазация
3. Лемматизация 
4. Эмбединги 
Пункты 1-3 уже реализованы в данных, поэтому основной поинт препроцессинга - это построение эмбедингов, в наибольшей степени подходящих для моделей из пункта 3 (эксперименты с моделями); с этой целью эмбединги будут сроиться возможно разные (для каждой модели), кроме того, для построения новых эмбедингов, возможно, нужно будет обращаться к пунктам 1-3 и делать там что-то уже другое.
### 2. Поиск тематик (<username> ответственный)
  Разбиение сообщения по темам: карты, кредиты, депозиты, страховки и т.д.
  
  A:С помощью ключевых слов: подобрать темы -> подобрать базовые опорные слова -> расширить тематики за счет словарей синонимов или других штук (например, https://wordstat.yandex.ru/) -> кластеризовать данные.
 
  Б: Если получится шаг А, то попытатся построить более продвинутую модель -> найти в кластерах ярких представителей тематик -> потом через Baf of Words или embedding сделать semi-supervised clustering.
  
  ### 3. Построение моделей семантического анализа и эксперименты с ними (<username> ответственный)

Построить на основе оценок пользователей модель тональности сообщений.

Или построить модель тональностей на другом корпусе данных и попытаться его применить к моделям банки ру. Оценить тональность отзывов пользователей, сравнить с выставляемми оценками.
Архитектуры:
1. cnn
2. rnn
3. birnn
4. cnn+rnn / birnn
5. другие сети (сиамские какие-нибудь)
6. другие алогоритмы (вдруг сработает)
7. state-of-the-art в области semantic analysis
  
### 4. Подготовка аналитики (---)
  Создание красивых тыкабельных графиков и извлечение возможных удивительных фактов 
  
