# Задание 3. Итераторы, магия

## Техническое задание

Необходимо создать класс Person со свойствами и методами. Можно взять из предыдущих заданий.
Далее необходимо:
* провести работу с объектами класса Person и их сериализацией, то есть:
    * добавить работу с магическими методами __get(), __set(), __sleep() и __wakeup(); 
    * создать объект
    * сериализовать его
    * вывести в строку
    * поменять в строке какое-нибудь значение, например, логин, с помощью str_replace. Для интереса можно проверить, как оно будет
    работать со строкой такого же размера и со строкой другого размера;
    * десериализовать объект и вывести его свойства;

* создать дополнительный класс, который будет представлять собой список людей — PeopleList;
* реализовать этот класс как итерируемый, чтобы выводить объекты Person 
 приходилось не через явное обращение, а через foreach, для этого прикручиваем работу с интерфейсом Iterator. Подсказка: 
 чтобы удобнее выводить Person через echo, можно добавить тому работу с методом __toString().  


**Обратите внимание на** [**рекомендации по сдаче домашнего задания**](../homework.md). 
