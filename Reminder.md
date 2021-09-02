- OOP (object oriented programming) 
  - It consists of 4 pillars:
    - Encapsulation  
      Encapsulation is accomplished when each object maintains a private state, inside a class. Other objects can not access this state directly, instead, they can only invoke a list of public functions. The object manages its own state via these functions and no other class can alter it unless explicitly allowed 
    - Abstraction  
      Abstraction is an extension of encapsulation. It is the process of selecting data from a larger pool to show only the relevant details to the object.
    - Inheritance  
      Inheritance is the ability of one object to acquire some/all properties of another object. For example, a child inherits the traits of his/her parents. With inheritance, reusability is a major advantage. You can reuse the fields and methods of the existing class. 
    - Polymorphism  
      Polymorphism gives us a way to use a class exactly like its parent so there is no confusion with mixing types. This being said, each child sub-class keeps its own functions/methods as they are. If we had a superclass called Mammal that has a method called mammalSound(). The sub-classes of Mammals could be Dogs, whales, elephants, and horses. Each of these would have their own iteration of a mammal sound

- SOLID
  - S - Single responsibility principle
    A class should have one and only one reason to change, meaning that a class should have only one job.
  - O - Open/closed principle
    Objects or entities should be open for extension but closed for modification.
  - L - Liskov substitution principle
    This means that every subclass or derived class should be substitutable for their base or parent class.
  - I - Interface segregation principle
    A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use.
  - D - Dependency invertion principle
    Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions.

- REST  
  REST is acronym for REpresentational State Transfer. It is architectural style for distributed hypermedia systems
  Like any other architectural style, REST also does have it’s own 6 guiding constraints which must be satisfied if an interface needs to be referred as RESTful. These principles are listed below.
  - Client–server – By separating the user interface concerns from the data storage concerns, we improve the portability of the user interface across multiple platforms and improve scalability by simplifying the server components.
  - Stateless – Each request from client to server must contain all of the information necessary to understand the request, and cannot take advantage of any stored context on the server. Session state is therefore kept entirely on the client.
  - Cacheable – Cache constraints require that the data within a response to a request be implicitly or explicitly labeled as cacheable or non-cacheable. If a response is cacheable, then a client cache is given the right to reuse that response data for later, equivalent requests.
  - Uniform interface – By applying the software engineering principle of generality to the component interface, the overall system architecture is simplified and the visibility of interactions is improved. In order to obtain a uniform interface, multiple architectural constraints are needed to guide the behavior of components. REST is defined by four interface constraints: identification of resources; manipulation of resources through representations; self-descriptive messages; and, hypermedia as the engine of application state.
  - Layered system – The layered system style allows an architecture to be composed of hierarchical layers by constraining component behavior such that each component cannot “see” beyond the immediate layer with which they are interacting.
  - Code on demand (optional) – REST allows client functionality to be extended by downloading and executing code in the form of applets or scripts. This simplifies clients by reducing the number of features required to be pre-implemented.


- Что такое REST?
  - REST API — это прикладной программный интерфейс (API), 
который использует HTTP-запросы для получения, извлечения, 
размещения и удаления данных. Аббревиатура REST в контексте API 
расшифровывается как «передача состояния представления» 
(Representational State Transfer).
- Принципы REST
  - 1. единый интерфейс;
  - 2. разграничение клиента и сервера;
  - 3. нет сохранения состояния;
  - 4. кэширование всегда разрешено;
  - 5. многоуровневая система;
  - 6. код предоставляется по запросу.
- HTTP структура
  - 1. Starting line
  - 2. Headers
  - 3. Body

- DML/DDL
  - Data Manipulation Language (DML) – 
это группа операторов для манипуляции данными. 
С помощью этих операторов мы можем добавлять, изменять, 
удалять и выгружать данные из базы, т.е. манипулировать ими.
В эту группу входят самые распространённые операторы языка SQL:
SELECT – осуществляет выборку данных;
INSERT – добавляет новые данные;
UPDATE – изменяет существующие данные;
DELETE – удаляет данные.

  - Data Definition Language (DDL) – это группа 
операторов определения данных. Другими словами, 
с помощью операторов, входящих в эту группы, мы 
определяем структуру базы данных и работаем с 
объектами этой базы, т.е. создаем, изменяем и удаляем их.
В эту группу входят следующие операторы:
CREATE – используется для создания объектов базы данных;
ALTER – используется для изменения объектов базы данных;
DROP – используется для удаления объектов базы данных.

- KEYS
  - Первичный ключ
  - Столбец, который в базе данных должен быть 
уникальным помечают первичным ключом. Первичный 
ключ или primary key означает, что в таблице 
значение колонки primary key не может повторяться. 

  - Есть еще внешний ключ (foreign key).  Его еще называют 
ссылочным. Он нужен для связывания таблиц между собой.

  - Что касается составного ключа — это несколько 
первичных ключей в таблице. Таким образом, создав 
composite key, уникальность записи будет проверяться 
по полям, которые объединенные в этот ключ.

- INDEX
  - Индексы – это специальные таблицы, которые 
могут быть использованы поисковым двигателем базы 
данных (далее – БД), для ускорения получения данных. 
Необходимо просто добавить указатель индекса в таблицу.
CREATE INDEX name ON table(cols);

- TRANSACTIONS
  - Транзакция является рабочей единицей работы с 
базой данных (далее – БД). Это последовательность 
операций, выполняемых в логическом порядке пользователем, 
либо программой, которая работает с БД.
Основные концепции транзакции описываются 
аббревиатурой ACID – Atomicity, Consistency, 
Isolation, Durability (Атомарность, Согласованность, 
Изолированность, Долговечность).

- Уровни транзакций  
The transaction isolation level cannot be changed after the first query or data-modification statement (SELECT, INSERT, DELETE, UPDATE, FETCH, or COPY) of a transaction has been executed  
The isolation level of a transaction determines what data the transaction can see when other transactions are running concurrently:

- READ COMMITTED  
A statement can only see rows committed before it began. This is the default.

- REPEATABLE READ  
All statements of the current transaction can only see rows committed before the first query or data-modification statement was executed in this transaction.

- SERIALIZABLE  
All statements of the current transaction can only see rows committed before the first query or data-modification statement was executed in this transaction. If a pattern of reads and writes among concurrent serializable transactions would create a situation which could not have occurred for any serial (one-at-a-time) execution of those transactions, one of them will be rolled back with a serialization_failure error.

  - Атомарность
  - Атомарность гарантирует, что любая транзакция 
будет зафиксирована только целиком (полностью). 
Если одна из операций в последовательности не 
будет выполнена, то вся транзакция будет отменена. 
Тут вводится понятие “отката” (rollback). 
Т.е. внутри последовательности будут происходить 
определённые изменения, но по итогу все они будут 
отменены (“откачены”) и по итогу пользователь не 
увидит никаких изменений.

  - Согласованность
  - Это означает, что любая завершённая транзакция 
(транзакция, которая достигла завершения транзакции – end
 of transaction) фиксирует только допустимые результаты. 
Например, при переводе денег с одного счёта на другой, 
в случае, если деньги ушли с одного счёта, они должны 
прийти на другой (это и есть согласованность системы). 
Списание и зачисление  – это две разные транзакции, 
поэтому первая транзакция пройдёт без ошибок, а второй 
просто не будет.

  - Изолированность
  - Каждая транзакция должна быть изолирована от других, 
т.е. её результат не должен зависеть от выполнения 
других параллельных транзакций. На практике, 
изолированность крайне труднодостижимая вещь, поэтому 
здесь вводится понятие “уровни изолированности” 
(транзакция изолируется не полностью).

  - Долговечность
  - Эта концепция гарантирует, что если мы получили 
подтверждение о выполнении транзакции, то изменения, 
вызванные этой транзакцией не должны быть отменены из-за 
сбоя системы (например, отключение электропитания).

  - Для управления транзакциями используются следующие команды:
  - COMMIT - Сохраняет изменения
  - ROLLBACK - Откатывает (отменяет) изменения
  - SAVEPOINT - Создаёт точку к которой группа транзакций может откатиться
  - SET TRANSACTION - Размещает имя транзакции.

- 1NF
  - Все атрибуты простые и поля содержат скалярные значения, 
таблица описывает сущность.

- 2NF
  - Поля одной таблицы зависят от первичного ключа 
другой таблицы и находится в 1NF.
Если просто, то это когда вторая таблица не является частью сущности,
но существенно её дополняет.

- 3NF
  - Вынос всех не ключевых полей, которые могут 
относиться к нескольким записям таблицы

- NFBK
  - Требования нормальной формы Бойса-Кодда следующие:
  - Таблица должна находиться в третьей нормальной форме. 
    - Здесь все как обычно, т.е. как и у всех остальных 
нормальных форм, первое требование заключается в том, 
чтобы таблица находилась в предыдущей нормальной форме, 
в данном случае в третьей нормальной форме;
    - Ключевые атрибуты составного ключа не должны 
зависеть от неключевых атрибутов.

  - Отсюда следует, что требования нормальной формы 
Бойса-Кодда предъявляются только к таблицам, у 
которых первичный ключ составной. Таблицы, у которых 
первичный ключ простой, и они находятся в третьей 
нормальной форме, автоматически находятся и в 
нормальной форме Бойса-Кодда.

  - Часть составного первичного ключа не должна 
зависеть от неключевого столбца.

  - Т.е. неключевой столбец нужно сделать ключевым!

- Constraint
  - Используется для задания ограничений после того, как 
таблица была создана.
  - NOT NULL
  - INIQUE
  - PRIMARY KEY
  - FOREIGN KEY
  - CHECK
  - INDEX
