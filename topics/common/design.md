# OOP

## Что такое ООП?

ООП (объектно-ориентированное программирование) - это парадигма программирования, которая основана на использовании
объектов, классов и принципах инкапсуляции, наследования, полиморфизма и абстракции. ООП моделирует реальный мир с
помощью объектов, которые имеют свое состояние и поведение, а классы определяют их свойства и методы.
Принципы ООП обеспечивают модульность, гибкость и повторное использование кода.

## Опишите основные принципы ООП

1. **Инкапсуляция**: объединение данных и методов, работающих с этими данными, внутри классов для обеспечения скрытия
   деталей реализации и предоставления интерфейса доступа.
2. **Наследование**: создание новых классов на основе существующих, позволяющее наследовать свойства и методы
   родительских классов и расширять их функциональность.
3. **Полиморфизм**: способность объектов с одним и тем же интерфейсом иметь различную реализацию методов, позволяющая
   использовать их без необходимости знать конкретный тип объекта.
4. **Абстракция**: выделение общих характеристик и функциональности объектов в абстрактные классы или интерфейсы,
   скрывающие детали реализации и позволяющие сосредоточиться на существенных аспектах системы.

## Что такое объект, класс, интерфейс, абстрактный класс?

1. **Объект**: экземпляр класса, имеющий свои уникальные данные и способность выполнять определенные действия.
2. **Класс**: шаблон или описание, определяющее структуру, свойства и методы объектов одного типа. Он является основой
   для создания объектов.
3. **Интерфейс**: контракт, определяющий набор методов, которые должны быть реализованы классами, чтобы соответствовать
   интерфейсу. Интерфейс определяет только сигнатуры методов без их реализации.
4. **Абстрактный класс**: класс, который не может быть создан в виде объекта, но может содержать как абстрактные
   методы (без реализации), так и конкретные методы с реализацией. Абстрактный класс может служить базовым классом для
   других классов и определять общую функциональность.

## Когда следует применять интерфейс, а когда абстрактный класс?

Интерфейс следует применять, когда нужно определить контракт для классов, независимо от их иерархии, и различные классы
могут реализовывать его по-разному.

Абстрактный класс следует использовать, когда есть общая функциональность, которая может быть использована в нескольких
классах, и требуется предоставить базовую реализацию для методов с возможностью их переопределения в производных
классах. Также абстрактный класс может ограничивать создание экземпляров и использоваться в качестве базового класса для
наследования.

## Что такое композиция и агрегация? В чем их отличие?

Композиция и агрегация относятся к отношениям между объектами в ООП:

Композиция:

1. Композиция представляет собой отношение "часть-целое", где объекты одного класса являются составными частями другого
   объекта.
2. Жизненный цикл составной части связан с жизненным циклом целого объекта.
3. Удаление целого объекта приводит к автоматическому удалению его составных частей.

Агрегация:

1. Агрегация также представляет отношение "часть-целое", но составные части могут существовать независимо от целого
   объекта.
2. Жизненный цикл составной части не зависит от жизненного цикла целого объекта.
3. Удаление целого объекта не влияет на существование его составных частей.

Композиция представляет собой отношение "часть-целое", где составные части объекта тесно связаны и зависят от его
жизненного цикла. Агрегация также является отношением "часть-целое", но составные части могут существовать независимо от
целого объекта. Вот основные отличия между композицией и агрегацией: связь, жизненный цикл и удаление.

## Что такое статическое и динамическое связывание?

Статическое связывание происходит на этапе компиляции, когда метод или функция определяются на основе типа переменной.
Динамическое связывание происходит во время выполнения программы, когда метод или функция выбираются на основе
фактического типа объекта или переменной.
Статическое связывание обеспечивает более быстрое выполнение программы, в то время как динамическое связывание
обеспечивает гибкость и полиморфизм.

## Что такое обмен сообщениями?

Обмен сообщениями в ООП представляет собой механизм взаимодействия между объектами, основанный на передаче запросов и
команд через сообщения. Вот основные аспекты обмена сообщениями:

1. Сообщение: запрос или команда, отправляемая от одного объекта к другому.
2. Отправитель: объект, инициирующий отправку сообщения.
3. Получатель: объект, который получает сообщение и обрабатывает его.
4. Метод: операция, которую получатель выполняет в ответ на полученное сообщение.
5. Время выполнения: обмен сообщениями происходит во время выполнения программы.

Преимущества обмена сообщениями в ООП:

- Модульность: объекты взаимодействуют только через сообщения, что способствует локализации логики и состояния объектов.
- Инкапсуляция: объекты скрывают свою внутреннюю реализацию, предоставляя только интерфейс для взаимодействия через
  сообщения.
- Полиморфизм: различные объекты могут отвечать на одинаковые сообщения, позволяя заменять объекты разных типов без
  изменения кода, работающего с сообщениями.

# SOLID

## Что такое принципы SOLID?

Принципы SOLID представляют собой набор принципов объектно-ориентированного программирования, разработанных для создания
гибкого, расширяемого и поддерживаемого кода. Вот основные принципы SOLID:

1. Принцип единственной ответственности (Single Responsibility Principle): Каждый класс должен иметь только одну
   ответственность.
2. Принцип открытости/закрытости (Open-Closed Principle): Код должен быть открыт для расширения, но закрыт для
   модификации.
3. Принцип подстановки Лисков (Liskov Substitution Principle): Объекты должны быть заменяемыми своими подтипами без
   изменения корректности программы.
4. Принцип разделения интерфейса (Interface Segregation Principle): Клиенты не должны зависеть от интерфейсов, которые
   они не используют полностью.
5. Принцип инверсии зависимостей (Dependency Inversion Principle): Модули верхнего уровня не должны зависеть от модулей
   нижнего уровня, оба должны зависеть от абстракций.

## В чем разница между принципами Single Responsibility и Separation of Concerns? Предоставьте примеры, которые иллюстрируют эти принципы.

Принципы Single Responsibility (SRP) и Separation of Concerns (SoC) являются взаимосвязанными, но имеют некоторые
различия. Вот их различия и примеры для иллюстрации:

Single Responsibility Principle (SRP):

1. Класс должен иметь только одну ответственность.
2. Класс должен быть изменен только по одной причине.

Пример: Рассмотрим класс "Order", который отвечает за обработку заказов и отправку уведомлений клиентам. Этот класс
нарушает принцип SRP, так как он имеет две ответственности: обработку заказов и отправку уведомлений. Чтобы соблюсти
принцип SRP, можно разделить этот класс на два отдельных класса: "OrderProcessor" для обработки заказов и "
NotificationSender" для отправки уведомлений.

Separation of Concerns (SoC):

1. Разделение функциональности на отдельные модули или компоненты.
2. Каждый модуль должен заниматься только одной сферой ответственности.

Пример: Рассмотрим веб-приложение для онлайн-магазина. При применении принципа SoC мы можем разделить функциональность
на отдельные компоненты, такие как "User Management" для управления пользователями, "Product Catalog" для управления
каталогом товаров, "Order Management" для управления заказами и т. д. Каждый компонент будет заниматься только своей
сферой ответственности, что упрощает поддержку и изменение системы.

Вывод:
Принцип SRP фокусируется на классах и требует, чтобы каждый класс имел только одну ответственность. Принцип SoC шире и
фокусируется на разделении функциональности на отдельные модули или компоненты для достижения более четкой и логической
структуры кода. Оба принципа направлены на создание более гибкого, модульного и поддерживаемого кода.

## Как принцип Open-Closed связан с возможностью расширения и невозможностью изменения кода? Предоставьте пример, который демонстрирует применение этого принципа.

Принцип Open-Closed обеспечивает гибкость и расширяемость кода, позволяя добавлять новую функциональность без изменения
существующего кода.
Это достигается путем создания абстракций, интерфейсов и использования наследования.
Принцип OCP способствует созданию более поддерживаемого и масштабируемого кода.

Пример: Рассмотрим систему управления транспортными средствами, где есть базовый класс "Vehicle" с методом "
startEngine".
Согласно принципу OCP, мы можем расширить функциональность системы, добавив новые типы транспортных средств (например,
автомобиль и мотоцикл), не изменяя базовый класс "Vehicle".
Мы создаем новые классы, наследующие от "Vehicle" и реализующие свою специфическую логику запуска двигателя.
Таким образом, мы расширяем функциональность системы без изменения базового класса, что обеспечивает соблюдение принципа
OCP.

## Почему принцип Liskov Substitution является важным для поддержки полиморфизма в объектно-ориентированных системах? Приведите пример, который показывает нарушение этого принципа и его последствия.

Принцип Liskov Substitution (LSP) является важным для поддержки полиморфизма в объектно-ориентированных системах по
следующим причинам:

1. Гарантирует согласованное поведение: Если классы не соблюдают принцип LSP, то код, который использует полиморфизм,
   может работать некорректно или даже вызывать ошибки. Соблюдение принципа LSP позволяет гарантировать, что все подтипы
   класса будут вести себя согласованно.

2. Обеспечивает безопасность типов: Принцип LSP помогает поддерживать безопасность типов в системе. Если классы не
   соблюдают принцип LSP, это может привести к неправильному использованию и непредсказуемому поведению при работе с
   типами.

3. Упрощает разработку и поддержку: Принцип LSP способствует созданию четкой и последовательной иерархии классов, что
   упрощает разработку и понимание кода. Кроме того, он облегчает поддержку системы, так как добавление новых подтипов
   не требует изменения существующего кода, который использует полиморфизм.

Пример нарушения принципа LSP и его последствий:

Предположим, у нас есть иерархия классов "Фигура" (Shape), включающая классы "Прямоугольник" (Rectangle) и "Круг" (
Circle). Класс "Фигура" имеет метод `getArea()`, который возвращает площадь фигуры.

Нарушение принципа LSP:
Если мы нарушим принцип LSP и переопределим метод "получитьПлощадь" в классе "Прямоугольник" таким образом, что он будет
возвращать, например, длину стороны, то это приведет к нарушению ожидаемого поведения.
Если код, использующий полиморфизм, ожидает получить площадь, то вызов метода на объекте "Прямоугольник" приведет к
неправильному результату.

Последствия нарушения принципа LSP:

- Неправильные результаты и непредсказуемое поведение при использовании полиморфизма.
- Нарушение принципа согласованности и ожидаемого поведения объектов.
- Усложнение понимания и поддержки кода.

## Что такое принцип Dependency Inversion и как он способствует достижению слабой связности между модулями? Как можно применить этот принцип в практическом программировании?

Принцип Dependency Inversion (инверсия зависимостей) в объектно-ориентированном программировании означает следующее:

1. Зависимости должны быть относительно абстракций, а не конкретных реализаций. Вместо того, чтобы модули зависели от
   конкретных классов или объектов, они должны зависеть от общих интерфейсов или абстрактных классов. Это позволяет
   более гибко управлять зависимостями и облегчает замену реализации.

2. Высокоуровневые модули не должны зависеть от низкоуровневых модулей. Оба должны зависеть от абстракций. Это означает,
   что модули разных уровней должны общаться друг с другом через общие абстракции, а не напрямую.

3. Абстракции не должны зависеть от деталей реализации. Детали реализации должны зависеть от абстракций. Это означает,
   что абстракции должны определять только общие контракты и не должны содержать конкретных деталей, которые могут
   меняться.

Применение принципа Dependency Inversion в практическом программировании может осуществляться следующими способами:

1. Введение интерфейсов или абстрактных классов:
    - Определите интерфейсы или абстрактные классы, которые представляют абстракции для модулей.
    - Высокоуровневые модули должны зависеть от этих абстракций, а не от конкретных реализаций.

2. Инверсия зависимостей через внедрение зависимостей (Dependency Injection):
    - Внедрение зависимостей позволяет передавать зависимости в модуль извне, вместо того чтобы модуль самостоятельно
      создавать и управлять своими зависимостями.
    - Зависимости передаются через конструкторы, методы или свойства объекта.

3. Использование фабрик или контейнеров внедрения зависимостей:
    - Фабрики или контейнеры внедрения зависимостей облегчают создание и предоставление объектов с правильными
      зависимостями.
    - Они позволяют централизованно управлять зависимостями и их конфигурацией.

## Как принципы SOLID взаимодействуют с другими практиками разработки, такими как TDD (Test-Driven Development) и DI (Dependency Injection)? Какие преимущества получаются при использовании этих подходов вместе?

Принципы SOLID, Test-Driven Development (TDD) и Dependency Injection (DI) взаимодействуют и дополняют друг друга,
обеспечивая более гибкую и поддерживаемую разработку программного обеспечения. Вот как они связаны и какие преимущества
получаются при их использовании вместе:

1. SOLID и TDD:
    - SOLID принципы обеспечивают принципы хорошего проектирования, которые упрощают тестирование кода.
    - TDD предлагает разрабатывать тесты перед написанием кода, что позволяет обеспечить высокую степень покрытия
      тестами.
    - Вместе они способствуют разработке модульного, гибкого и тестируемого кода.

2. SOLID и DI:
    - SOLID принципы поддерживают инверсию зависимостей и использование интерфейсов или абстракций для описания
      зависимостей модулей.
    - DI предоставляет механизм внедрения зависимостей, позволяющий легко заменять конкретные реализации зависимостей и
      управлять ими извне.
    - Вместе они обеспечивают слабую связность и управляемость зависимостей, что упрощает тестирование и поддержку кода.

Преимущества использования этих подходов вместе:

- Улучшенная тестируемость: SOLID и TDD совместно позволяют создавать модули, которые легко тестируются в изоляции,
  благодаря инверсии зависимостей и разработке тестов заранее.
- Гибкость и масштабируемость: SOLID и DI позволяют легко вносить изменения в код, добавлять новые функциональности и
  поддерживать код при росте проекта.
- Улучшенная поддерживаемость: Хорошая архитектура, основанная на принципах SOLID, совместно с TDD и DI, делает код
  более понятным, структурированным и легко поддерживаемым.
- Возможность параллельной разработки: SOLID и DI позволяют разработчикам независимо работать над модулями и их тестами,
  что улучшает параллельную разработку и интеграцию кода.

# Design Patterns

## Что такое паттерны проектирования и для чего они нужны?

Паттерны проектирования (Design Patterns) - это повторно используемые архитектурные шаблоны для решения типичных
проблем, возникающих при проектировании программных систем. Они представляют собой bewährte Lösungskonzepte, die dazu
beitragen, Best Practices und bewährte Methoden in der Softwareentwicklung zu etablieren.

Паттерны проектирования имеют следующие цели и преимущества:

1. **Общий язык**: Паттерны предоставляют общий язык и терминологию для коммуникации между разработчиками. Это упрощает
   обсуждение и понимание архитектурных решений.

2. **Повторное использование кода**: Паттерны предоставляют готовые архитектурные шаблоны, которые можно применять в
   различных проектах. Это способствует повторному использованию кода и сокращению разработки "с нуля".

3. **Улучшение поддерживаемости**: Паттерны позволяют создавать код, который более понятен и поддерживаем. Они соблюдают
   принципы SOLID (Single Responsibility, Open-Closed, Liskov Substitution, Interface Segregation, Dependency
   Inversion), что делает код более гибким и менее подверженным ошибкам.

4. **Повышение расширяемости**: Паттерны позволяют легко вносить изменения в систему, не нарушая ее основной структуры.
   Это особенно полезно при добавлении новых функций или компонентов.

## Какие паттерны проектирования вы знаете?

Существует множество паттернов проектирования, которые используются разработчиками для решения типичных задач в
проектировании программных систем. Вот некоторые из наиболее известных видов паттернов проектирования:

**Порождающие паттерны (Creational Patterns):**

1. **Одиночка (Singleton)**: Гарантирует, что класс имеет только один экземпляр и предоставляет глобальную точку доступа
   к этому экземпляру.

2. **Фабричный метод (Factory Method)**: Определяет интерфейс для создания объекта, но оставляет подклассам решение,
   какой класс инстанцировать.

3. **Абстрактная фабрика (Abstract Factory)**: Предоставляет интерфейс для создания семейств взаимосвязанных или
   зависимых объектов без указания их конкретных классов.

4. **Строитель (Builder)**: Позволяет создавать сложные объекты пошагово. Разделяет процесс создания объекта на
   различные шаги.

5. **Прототип (Prototype)**: Позволяет создавать новые объекты, копируя существующие, без привязки к их конкретным
   классам.

**Структурные паттерны (Structural Patterns):**

1. **Адаптер (Adapter)**: Позволяет объектам с несовместимыми интерфейсами работать вместе.

2. **Мост (Bridge)**: Отделяет абстракцию от ее реализации, чтобы они могли изменяться независимо друг от друга.

3. **Компоновщик (Composite)**: Позволяет строить деревья объектов одного типа так же, как и отдельные объекты.

4. **Декоратор (Decorator)**: Позволяет добавлять объектам новые функциональные возможности динамически, не изменяя их
   структуры.

5. **Фасад (Facade)**: Предоставляет унифицированный интерфейс для группы интерфейсов в подсистеме, облегчая
   использование этой подсистемы.

**Поведенческие паттерны (Behavioral Patterns):**

1. **Цепочка обязанностей (Chain of Responsibility)**: Позволяет передавать запросы последовательно по цепочке
   обработчиков, избегая жесткой привязки отправителя запроса к его получателю.

2. **Команда (Command)**: Инкапсулирует запрос как объект, позволяя параметризовать клиентов с запросами, ставить
   запросы в очередь, а также поддерживать отмену операций.

3. **Итератор (Iterator)**: Предоставляет способ последовательного доступа к элементам коллекции, не раскрывая ее
   внутреннего представления.

4. **Наблюдатель (Observer)**: Определяет зависимость "один ко многим" между объектами так, чтобы при изменении
   состояния одного объекта все зависящие от него объекты уведомлялись и обновлялись автоматически.

5. **Стратегия (Strategy)**: Определяет семейство алгоритмов, инкапсулирует их и делает их взаимозаменяемыми. Позволяет
   клиенту выбирать подходящий алгоритм во время выполнения.

6. **Состояние (State)**: Позволяет объекту изменять свое поведение при изменении его внутреннего состояния. Объект
   кажется изменяющим свой класс.

7. **Шаблонный метод (Template Method)**: Определяет структуру алгоритма, но позволяет подклассам переопределить
   определенные шаги алгоритма без изменения его структуры.

## Что такое антипаттерны? Какие антипаттерны вы знаете?

Антипаттерны (Anti-Patterns) - это архитектурные или проектировочные решения, которые, хотя они могут казаться вначале
привлекательными, в конечном итоге приводят к нежелательным последствиям, таким как плохая производительность, плохая
поддерживаемость, сложность кода и другие проблемы. Это противоположность паттернам проектирования, которые представляют
собой bewährte Lösungskonzepte. Антипаттерны предостерегают разработчиков от использования неправильных подходов к
проектированию и разработке программных систем.

Вот некоторые из наиболее известных антипаттернов:

1. **Антипаттерн "Косвенное наследование" (Blob)**: Этот антипаттерн возникает, когда класс становится "косвенным
   наследником" множества других классов, что приводит к созданию большого и сложного класса, содержащего множество
   функций.

2. **Антипаттерн "Магические строки" (Magic Strings/Numbers)**: Использование магических строк и чисел в коде без
   объяснения их значения и предназначения делает код менее читаемым и поддерживаемым.

3. **Антипаттерн "Повторяющийся код" (Copy-Paste Programming)**: Копирование и вставка кода в разные части программы
   приводит к дублированию кода и увеличению сложности его поддержки.

4. **Антипаттерн "Слишком большой класс" (God Object)**: Этот антипаттерн возникает, когда один класс содержит слишком
   много функциональности и становится слишком сложным для понимания и изменения.

5. **Антипаттерн "Ненужная сложность" (Needless Complexity)**: Добавление избыточной сложности в код, которая не
   приносит никакой дополнительной ценности, делает код менее читаемым и поддерживаемым.

6. **Антипаттерн "Использование глобальных переменных" (Global Variable)**: Использование глобальных переменных делает
   код менее предсказуемым и усложняет отслеживание зависимостей между компонентами программы.

7. **Антипаттерн "Программирование на уровне железа" (Spaghetti Code)**: Этот антипаттерн описывает код, в котором
   логика смешана с низкоуровневыми деталями, что делает его трудным для понимания и поддержки.

8. **Антипаттерн "Золотой молоток" (Golden Hammer)**: Использование одного и того же инструмента или технологии для всех
   задач, даже если они не подходят для него, может привести к ненужной сложности и ограничениям.

9. **Антипаттерн "Операции, ожидающие операции" (Dead End)**: Создание функциональности, которая не используется в
   реальных сценариях, может быть ненужным и усложнять код.

10. **Антипаттерн "Проектирование на бумаге" (Analysis Paralysis)**: Бесконечное анализирование и проектирование без
    фактической реализации может привести к задержкам в разработке и ненужной сложности.

## Что такое Singleton? Какие есть виды?

[Singleton](https://refactoring.guru/ru/design-patterns/singleton)

Singleton - это паттерн проектирования, который гарантирует, что у класса есть только один экземпляр, и предоставляет
глобальную точку доступа к этому экземпляру. Это полезно, когда необходимо убедиться, что в системе существует только
один объект определенного типа, который координирует действия в приложении, обеспечивает доступ к ресурсам или выполняет
другие глобальные задачи.

Основные характеристики Singleton:

1. **Один экземпляр**: Существует только один экземпляр класса Singleton в рамках приложения.

2. **Глобальный доступ**: Класс Singleton предоставляет глобальную точку доступа к своему экземпляру, обычно через
   статический метод.

3. **Ленивая инициализация (при необходимости)**: Экземпляр Singleton создается только тогда, когда он действительно
   нужен, а не заранее.

4. **Защита от множественных потоков (по необходимости)**: Singleton должен быть потокобезопасным, чтобы избежать
   создания нескольких экземпляров в многопоточной среде.

5. **Простой доступ**: Singleton может предоставлять доступ к своему экземпляру через геттер или метод getInstance().

Виды Singleton:

1. **Eager Singleton (Инициализация при загрузке)**:
    - Экземпляр создается заранее, при загрузке класса.
    - Прост в реализации, но может вызвать нежелательную задержку при запуске приложения, если экземпляр не используется
      сразу.
    - Пример на Java:
   ```java
   public class EagerSingleton {
       private static final EagerSingleton instance = new EagerSingleton();
   
       private EagerSingleton() {}
   
       public static EagerSingleton getInstance() {
           return instance;
       }
   }
   ```

2. **Lazy Singleton (Ленивая инициализация)**:
    - Экземпляр создается только при первом обращении.
    - Потокобезопасный вариант может потребовать использования двойной проверки блокировки (Double-Checked Locking).
    - Пример на Java:
   ```java
   public class LazySingleton {
       private static volatile LazySingleton instance;
   
       private LazySingleton() {}
   
       public static LazySingleton getInstance() {
           if (instance == null) {
               synchronized (LazySingleton.class) {
                   if (instance == null) {
                       instance = new LazySingleton();
                   }
               }
           }
           return instance;
       }
   }
   ```

3. **Enum Singleton (Перечисление)**:
    - Использует перечисление для определения Singleton.
    - Гарантирует создание единственного экземпляра вне зависимости от потоков и сериализации.
    - Пример на Java:
   ```java
   public enum EnumSingleton {
       INSTANCE;
   
       // Дополнительные методы и поля
   }
   ```

## Что такое фабричный метод?

[Factory Method](https://refactoring.guru/ru/design-patterns/factory-method)

Паттерн "Фабричный метод" - это паттерн проектирования, который относится к категории порождающих паттернов. Его
основная идея заключается в создании интерфейса для создания объектов, но оставлении решения о конкретном типе объекта
на подклассы, которые реализуют этот интерфейс.

Вот ключевые компоненты паттерна "Фабричный метод":

1. **Интерфейс фабрики (Creator)**: Это абстрактный класс или интерфейс, который объявляет метод (фабричный метод),
   используемый для создания объекта. Этот метод возвращает абстрактный тип или интерфейс продукта.

2. **Конкретные фабрики (Concrete Creators)**: Это подклассы интерфейса фабрики, которые реализуют фабричный метод и
   конкретно определяют, какой тип продукта будет создан.

3. **Интерфейс продукта (Product)**: Это абстрактный класс или интерфейс, который объявляет интерфейс для объектов,
   создаваемых фабрикой.

4. **Конкретные продукты (Concrete Products)**: Это подклассы интерфейса продукта, реализующие конкретную логику
   создания и поведения объектов.

Паттерн "Фабричный метод" позволяет создавать объекты, не привязываясь к конкретным классам продуктов. Вместо этого
клиентский код работает с абстрактными типами, определенными интерфейсом фабрики и интерфейсом продукта. Это делает
систему более гибкой и легко расширяемой, так как можно добавлять новые типы продуктов и соответствующие им фабрики, не
изменяя существующий код.

```java
// Интерфейс продукта - Транспорт
interface Transport {
    String deliver();
}

// Конкретный продукт - Доставка по суше
class LandTransport implements Transport {

    @Override
    public String deliver() {
        return "Доставка по суше";
    }
}

// Конкретный продукт - Доставка по воде
class SeaTransport implements Transport {

    @Override
    public String deliver() {
        return "Доставка по воде";
    }
}

// Интерфейс фабрики - Фабрика транспорта
interface TransportFactory {
    Transport createTransport();
}

// Конкретная фабрика - Фабрика для создания транспорта по суше
class LandTransportFactory implements TransportFactory {

    @Override
    public Transport createTransport() {
        return new LandTransport();
    }
}

// Конкретная фабрика - Фабрика для создания транспорта по воде
class SeaTransportFactory implements TransportFactory {

    @Override
    public Transport createTransport() {
        return new SeaTransport();
    }
}

public class Main {
    public static void main(String[] args) {
        // Создание фабрики для доставки по суше
        TransportFactory landTransportFactory = new LandTransportFactory();
        // Создание транспорта для доставки по суше
        Transport landTransport = landTransportFactory.createTransport();

        // Создание фабрики для доставки по воде
        TransportFactory seaTransportFactory = new SeaTransportFactory();
        // Создание транспорта для доставки по воде
        Transport seaTransport = seaTransportFactory.createTransport();

        // Вывод результата
        System.out.println(landTransport.deliver());
        System.out.println(seaTransport.deliver());
    }
}
```
