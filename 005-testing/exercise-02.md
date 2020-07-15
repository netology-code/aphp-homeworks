# Задание 2. Работа с TDD 

## Техническое задание
В рамках данного задания необходимо настроить у себя работу с PHPUnit, а также изучить на практике, что же такое TDD (можно
также почитать пример [отсюда](https://habr.com/ru/post/130086/))

Итак, у нас есть некая обертка над базой данных - искуственная таблица, которая все хранит во внутренних свойствах.
Выглядит примерно так:
```php
class UserTableWrapper
{
    private array $rows;

    /**
     * @param array|[column => row_value] $values
     */
    public function insert(array $values): void
    {
        $this->rows[] = $values;
    }
}
```

Также у нас есть интерфейс работы с таблицей:
```php
interface TableWrapperInterface
{
    public function insert(array $values): void;
    public function update(int $id, array $values): array;
    public function delete(int $id): void;
    
    public function get(): array;
}
```  

Необходимо:
1) подготовить тесты для каждого метода интерфейса, с использованием дата-провайдеров
2) написать реализацию для таблицы Users (как пример), проверяя её тестами
3) выполнить проверку покрытия кода тестами
4) при необходимости, дополнить тесты

**Обратите внимание на** [**рекомендации по сдаче домашнего задания**](../homework.md). 