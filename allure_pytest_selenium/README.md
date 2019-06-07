PyTest + Selenium + Allure Reports
---
Здесь вы можете найти пример того, как можно 
интегрировать PyTest, Selenium и Allure Reports.

Необходимые шаги:
---

1. Установка Allure. 
Для Mac 

    brew install allure
    
2. Установка плагина для pytest

    pip3 install allure-pytest
    
3. Запуск тестов с опцией --alluredir, указав директорию для размещения сырых результатов

    pytest --alluredir ./allure_result 
    
4. Генерация HTML отчета и последующее его открытие

    allure generate ./allure_result -c -o ./allure_report  &&  allure open


Как получить Allure Report
--------------------------

Для генерации красивого Allure отчета вам нужно:

1) Установить NodeJS (https://nodejs.org/en/download/)
2) Установить Allure Console (https://www.npmjs.com/package/allure-commandline)
3) Запустить тесты, указав в качестве дирректории с результатами
папку ./allure_report
4) Сгененировать HTML отчет и открыть его:


    allure generate ./allure_report  &&  allure open allure-report


После выполнения всех 5ти шагов в браузере должен открыться Allure отчет.

Конечно, вы так же можете сгенерировать HTML Allure отчет
используя плагины для Jenkins / TeamCity.


Как установить Allure на MacOS
------------------------------

Для установки Allure на MacOS нужно выполнить следующие команды:

    brew install node
    npm install -g allure-commandline --save-dev
Или

    brew install allure
    

Как запустить
-------------
    
Можно запускать тесты:

    pytest --alluredir ./allure_result
или

    pytest test.py --alluredir ./allure_result    

Затем сгененировать HTML отчет и открыть его:


    allure generate ./allure_result -c -o ./allure_report  &&  allure open


