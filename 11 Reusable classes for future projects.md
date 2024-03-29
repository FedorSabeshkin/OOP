# Классы для повторного использования в грядущих проектах
## Идея
Необходимо выбрать классы, которые я использовал бы в будущих проектах.

## Метод поиска
Для выделения повторно используемых классов классов применял *абстрагирование*.  
*Факторизацию* не применяю, т.к. соответственно рекомендации не применял наследование на этапе проектирования.  
На этапе формирования классов, не выделил те, что представимы в виде свойств, то есть не использовал *структурное наследование*. 

## Решение
Очевидно, что это будет зависеть от того, какую систему я буду создавать в будущем :).  
*Logger* и *ErrorHandler* понадобятся в любом случае, но будут лишь отличаться в реализации от игрового проекта.  
*Storage* - так же может быть типизирован под конкретный тип.  
*Timer* - может быть переиспользован, при переопределении соответствующих методов *checkInterrupt()* и *interrupt()*.  
*Formatter* - фактически функциональный интерфейс и тоже может быть переиспользован.  
Остальные классы можно добавлять в подходящие им по тематике проекты, с допущением, что *Money* все таки игровой тип денег для одиночной игры.  

## Анализ прошлых решений
Теперь вижу, что мог применить структурное наследование для классов Health, Power, Money - где требовались операции увеличения и уменьшения.  
Мог выделить интерфейс *Decreaseable/Increaseable* и некий общий интерфейс от них.  
Тем не менее, в моем случае названия у методов у каждого из классов ближе к его предметной области, чем были бы при простом преопределении родителя.

