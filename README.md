# Отчёт о тестировании функциональности Credit Card Number Validator для карт VISA, MasterCard

## Краткое описание

30.09.2021 - 30.09.2021 было проведено тестирование белого ящика функциональности валидации номера банковской карты.

На тестирование затрачено: 3.0

В результате тестирования выявлены следующие дефекты:
* [https://github.com/npetyaeva/javaLesson_1_2/issues/1](https://github.com/npetyaeva/javaLesson_1_2/issues/1)

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты*:
* Тестовые данные
* Тестовый скрипт

В качестве тестовых данных использовались данные:
1. Валидные номера банковских карт (сгенерированы на [freeformatter.com](https://www.freeformatter.com/credit-card-number-generator-validator.html)):

| VISA | |
|:---|:---|
| 4485459330150768 | Result is OK |
| 4539875413606291 | Result is OK |
| 4539173131015421966 | Result is FAIL |

| MasterCard ||
|:---|:---|
| 5353037262171253 | Result is OK |
| 5386945579386946 | Result is OK |
| 5523040032521398 | Result is OK |

2. Пустое поле (Result is FAIL)
3. Пробел (Result is FAIL)
4. Количесиво числовых символов меньше 16: 44854593 (Result is FAIL)
5. 16 символов кирилица: номеркартыбуквам (Result is FAIL)
6. 16 символов латиница: numbercardletter (Result is FAIL)
7. Специальные символы: &*%#(^$@/\\|&><:; (Result is FAIL)
8. 16 символов - цифры и буквы кириллицей: 4485но330мер768 (Result is FAIL)
9. 16 символов - цифры и буквы латиницей: 4485num30ber768 (Result is FAIL)

Тестирование производилось в следующем окружении:
* Windows 7 Professional
* Java 11
* IntelliJ IDEA Community
