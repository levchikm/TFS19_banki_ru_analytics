### 0. Разобратся в структуре файлов (все)
### 1. Препроцессинг данных (<username> ответственный).
### <краткое описание что входит в препроцессинг данных>
### 2. Создание архитектуры проекта (<username> ответственный)
### <снова описание>
### 3. Эксперимент с моделью 1. (<username> ответственный)
### <описание архитектуры модели 1>
  
    
#### Структура данных
Для каждого банка создано 3 таблицы:
1. branches
  * index - id ветки ???
  * sentence_id - id предложения из базы sentences_replies
  * branch_id - ???
  * branch - ???

2. replies - надо понять идут ли сообщения в том же порядке что и на форуме
  * index - id сообщения
  * author - имя пользователя
  * bank - имя банка
  * bank_response - текст ответа банка. None - если ответа не было.
  * comment_page - страница на форуме ????
  * comments_n - ???
  * rating - оценка ответа на банки.ру
  * text - текст сообщения
  * time - время сообщения
  * title - тема
  * mark - числовое значение поля rating. Число от 1 до 5. Если оценки нет, то -1.

3.sentences_replies - сообщение разбито на отдельные предложения
  * index - id предложения
  * sentence - текст предложения из соотбщения
  * reply_id - номер сообщения
  * data_extra_symbols - предложение без знаков пунктуации
  * lemmatized - лемматизированное предложение
  * covab_only - оставлены только слова из словаря ????
  * vw - ???
