# Отчёт о тестировании приложения BonusService

## Краткое описание

11.05.2020 - 11.05.2020 было проведено функциональное тестирование методом «белого ящика» приложения BonusService.

На тестирование затрачено: 1 час

В результате тестирования выявлены следующие дефекты:
* [При запуске приложения ошибка Error: java: RV_RETURN_VALUE_IGNORED_NO_SIDE_EFFECT](https://github.com/Oleg2394/BonusService2/issues/1#issue-615842116)

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты:
 * Набор тест кейсов:
1. Взять проект, который прикреплён в архиве [bonus-service.zip](https://github.com/netology-code/javaqa-homeworks/blob/master/maven-junit/artifacts/bonus-service.zip)
2. Открыть его как Maven проект в IDEA.
3. Запустить следующую команду Maven*: mvn clean compile spotbugs:check

Ожидаемый результат: Запуск приложения пройдет корректно

Фактический результат: Появляется ошибка RV_RETURN_VALUE_IGNORED_NO_SIDE_EFFECT
[INFO] --- spotbugs-maven-plugin:3.1.12.2:check (default-cli) @ bonus-calculator --- [INFO] BugInstance size is 1 [INFO] Error size is 0 [INFO] Total bugs: 1 [ERROR] Return value of BonusService.calculate(long, boolean) ignored, but method has no side effect [Main] At Main.java:[line 8] RV_RETURN_VALUE_IGNORED_NO_SIDE_EFFECT

Тестирование производилось в следующем окружении:
* <Windows 64-bit версия 1909>
* <Java 11.0.7>

