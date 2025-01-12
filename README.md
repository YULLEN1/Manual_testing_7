# Домашнее задание к занятию «13. Инструменты тестирования. Клиент-сервер»

[Инструкции по установке Postman, JMeter и BlazeMeter и запуску Terminal](https://github.com/netology-code/iqa-homeworks/blob/iqa-12/Instruction.md)

## Задание 1    

Руководитель планирует запустить проект в закрытое бета-тестирование. В нём будут участвовать члены семьи руководителя, включая бабушку. Поэтому нам нужно проверить, выдержит ли наша анкета одновременную работу 15 человек, или кому-то придётся пить кофе, пока остальные тестируют. 

[Ссылка на анкету](https://sinsl.github.io/testing-form/) 

Мы знаем, что есть специальный инструмент, при помощи которого можно проверить нагрузку, — [JMeter](https://jmeter.apache.org/).
Обратите внимание, что Java мы ставим строго по инструкции [отсюда](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/openjdk11-manual.md) для того, чтобы далее в обучении не было конфликтов версий.

Задача
1. При помощи JMeter создайте профиль нагрузки, как было рассмотрено на лекции.

2. Запустите одновременно 15 потоков.

3. Предоставьте отчёт о результатах запуска. 

В результате задания вам необходимо прикрепить при отправке три файла-картинки со скриншотами, которые должны отображать:
* request файл
* thread файл
* listener файл


## Задание 2 

В ходе тестирования проекта разработчики бэкенда обнаружили, что данные, которые приходят на сервер при отправке [формы](https://sinsl.github.io/testing-form/), не такие, какие они должны были получить. Разработчики просят вас протестировать API самостоятельно и задокументировать проблемы для того, чтобы они их смогли исправить.

Задача

Используя инструмент Postman, попробуйте найти баги. Нашей целью необязательно будет поймать ошибку в ответе от сервера: можно, например, попробовать изменить тело запроса и посмотреть, не будет ли дефектов в содержимом ответа сервера.

Подсказка

Для отправки запроса можно использовать body(raw), где указать, что отправлять в формате JSON.
К примеру, вот так: 

```
{
"birthday": "13.06.1999",
"name": "Иван",
"passport": "4444 № 44444444",
"patronymic": "Иванович",
"phone": "+7 (999)-999-99-99",
"surname": "Иванов"
}
```

В результате задания у вас должна получиться ссылка на [Google Docs](https://docs.google.com/document/d/1pA6iung7Fbor8H7orYzy4IxGyHPUUFqfWZFJGIzx_ho/edit) или [Яндекс.Документ](https://docs.yandex.ru/) **с оформленным по стандартам, пройденным раньше баг-репортом** и скриншоты Postman.
На ваше усмотрение есть два варианта оформления задания:
1. Прикрепить скрины Jira и Postman в виде файлов-картинок при отправке.
2. Дать ссылку на табличку по шаблону, который мы использовали ранее.

В домашнем задании надо составить баг-репорт по результатам запроса в Postman. Так как это тестирование API, немного новый для вас вид тестирования, стоит в двух словах обозначить, как в этом случае составлять баг-репорт.
Что надо включить в шаги:
- URL и path запроса;
- метод HTTP, который мы используем;
- тело запроса, если оно есть.

Что надо включить в результат (ожидаемый и фактический):
- код ответа;
- тело ответа, если есть;
- описание, что не так с кодом, телом или чем-то ещё.

Что включать не стоит:
- шаги по установке и открытию Postman;
- описание действий внутри Postman: «вставить значение ... в поле ...», «нажать кнопку Send» и т. д.

## Задание 3 `*` (необязательная задача)

## Что нужно сделать
Нам надо проверить, не может ли злоумышленник обрушить наш сайт. Что будет, если он обойдёт ограничения по длине поискового запроса и всё же введёт ну очень большую строку? Надо проверить.

1. Зайдите на https://www.mos.ru/search.
2. Запустите любой поисковый запрос и посмотрите, как отреагирует приложение.
3. Исследуйте поле поиска в консоли DevTools.
4. Введите очень длинный текст в строку поиска и посмотрите, не изменится ли реакция приложения при поиске, в том числе и в DevTools.
5. Если вы нашли баг, опишите его в нашей стандартной форме баг-репорта, которую мы использовали ранее. В качестве ожидаемого результата опишите то, как, по-вашему, должна работать эта форма, а в фактическом — расскажите, что видите на самом деле. 

6*. Если у вас есть идеи или размышления на тему того, баг ли это, как его можно исправить и может ли это вызвать реальные проблемы — напишите, что вы думаете. 

В этом задании наша основная задача — тренировка работы с DevTools.

Результат задания: ссылка на [Google Docs](https://docs.google.com/document) или [Яндекс.Документ](https://docs.yandex.ru/), можно заполнить в том же документе, который вы создадите по второй части ДЗ.



## Как сдать домашнее задание

Все задания обязательны к выполнению для получения зачёта, кроме дополнительных задач, помеченных звёздочкой. 

Любые вопросы по решению задач задавайте в чате учебной группы.

# [Решение](https://docs.google.com/document/d/1I-Ms6E20vWrUd8WXZYw6UrEnRUSqaALiSfkQzBLc25M/edit?tab=t.0)
