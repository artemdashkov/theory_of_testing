# Базовая теория
## Как писать код, принципы разработки программного кода
есть разные принципы SOLID, KISS, DRY
### Принцип DRY (Don't Repeat Yourself)
DRY — это принцип разработки программного обеспечения, который способствует уменьшению дублирования кода. Главная идея заключается в том, чтобы каждая часть вашей программы имела одно, единственное, и четкое представление, что способствует уменьшению ошибок и упрощению поддержки кода.

**Примеры применения DRY в Python:**
- `Функции` - Вместо повторения одного и того же кода в разных местах, выносите его в функцию.
- `Классы и наследование` - Используйте классы для группировки методов и свойств, чтобы избежать дублирования.
- `Конфигурационные файлы:` - Вместо повторения данных, храните параметры в одном месте (например, конфигурационные файлы).

### Принцип KISS (Keep It Simple, Stupid)
KISS — это принцип, который призывает к тому, чтобы системы или код были простыми. Избегайте ненужной сложности, так как она затрудняет понимание и поддержку кода.
Примеры применения KISS в Python:
- `Чистый и простой код` - Пишите функции, которые выполняют одну задачу.
- `Избегайте излишней логики:` - Если возможно, используйте встроенные функции вместо написания сложных алгоритмов.
- `Понятные имена:` - Названия переменных и функций должны отражать их суть.
- `Лаконичные конструкции:` - Используйте простые и лаконичные конструкции, такие как list comprehensions, для легкости чтения.

### Принцип SOLID
Принцип SOLID — это набор пяти основных принципов объектно-ориентированного проектирования, которые помогают создавать более гибкие и поддерживаемые программные системы. Эти принципы способствуют улучшению архитектуры кода, упрощению его тестирования и снижают риск возникновения ошибок. 
1. `S: Single Responsibility Principle (SRP)` – Принцип единственной ответственности. Каждый класс должен иметь только одну причину для изменения. Это означает, что класс должен быть сфокусирован на выполнении одной задачи.
2. `O: Open/Closed Principle (OCP)` – Принцип открытости/закрытости
Классы должны быть открыты для расширения, но закрыты для модификации. Это означает, что поведение класса можно изменять, не изменяя его исходный код.
3. `L: Liskov Substitution Principle (LSP)` – Принцип подстановки Лисков. Объекты подкласса должны быть заменяемыми на объекты суперкласса без нарушения правильности программы.
4. `I: Interface Segregation Principle (ISP)` – Принцип разделения интерфейса. Клиенты не должны зависеть от интерфейсов, которые они не используют. Это означает, что лучше иметь несколько специализированных интерфейсов, чем один общий.
5. `D: Dependency Inversion Principle (DIP)` – Принцип инверсии зависимостей. Высокоуровневые модули не должны зависеть от низкоуровневых; оба типа модулей должны зависеть от абстракций.



## Prioritize features to test based on the following factors:
- Recent—New features, new areas of code, new functionality that has been recently repaired, refactored, or otherwise modified
- Core—Your product’s unique selling propositions (USPs). The essential functions that must continue to work in order for the product to be useful
- Risk—Areas of the application that pose more risk, such as areas important to customers but not used regularly by the development team or parts that use third-party code you don’t quite trust
- Problematic—Functionality that frequently breaks or often gets defect reports against it
- Expertise—Features or algorithms understood by a limited subset of people report

### cards --help
- Usage: cards [OPTIONS] COMMAND [ARGS]...
Cards is a small command line task tracking application.
Options:
--help Show this message and exit.
**Commands**:
- `add` Add a card to db.
- `config` List the path to the Cards db.
- `count` Return number of cards in db.
- `delete` Remove card in db with given id.
- `finish` Set a card state to 'done'.
- `list` List cards in db.
- `start` Set a card state to 'in prog'.
- `update` Modify a card in db with given id with new info.
- `version` Return version of cards application

### Creating Test Cases
- Start with a non-trivial, “happy path” test case
- Then look at test cases that represent
    - interesting sets of input,
    - interesting starting states,
    - interesting end states, or
    - all possible error states.

### When writing automated tests, these are common mistakes:
- Only writing happy path test cases
- Spending too much time thinking about how things can go wrong
- Ignoring how behaviors change based on system or component state