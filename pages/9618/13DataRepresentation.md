# Data Representation

learn about:
* user-defined data types
* the definition and use of non-composite and composite data types
* the choice and design of an appropriate user-defined data type for a given problem
* methods of file organisation, such as serial, sequential and random
* methods of file access, such as sequential and direct access
* hashing algorithms
* binary floating-point real numbers
* converting binary floating-point real numbers into denary numbers
* converting denary numbers into binary floating-point real numbers
* the normalisation of binary floating-point numbers
* how underflow and overflow can occur
* how binary representation can lead to rounding errors.

---

## User Defined Data Types

### You should already know...

1. Different data types
2. How to select appropriate data types
3. How to write pseudocode
4. What a record is

Programmers use specific data types that perfectly fit the needs of a program. They can create their own data types using basic data types that are already available in the programming language. Sometimes, they also make use of data types they have created earlier in their program. These custom data types are known as user-defined data types. User-defined data types can be divided into two categories: non-composite and composite data types.

---

### Non-composite Data Types

Non-composite data types in programming are like single puzzle pieces that can hold one specific type of information. They are simple and don't contain multiple pieces or parts.

Imagine you have a box of Lego blocks, and each block represents a non-composite data type. Each block can only hold one piece of information, such as a number, a letter, or a word. For example, if you want to store someone's age, you can use a non-composite data type called "integer." It's like having a special Lego block that can only hold a single number, like 15. Similarly, if you want to store someone's name, you can use a non-composite data type called "string." It's like having another Lego block that can only hold a word or a series of letters, like "Emma" or "John."

Non-composite data types are useful because they allow programmers to work with simple pieces of information and build more complex structures using these basic building blocks.

A non-composite data type doesn't need to rely on another data type for its definition. It can be either a basic type provided by a programming language or a custom type created by the user. Non-composite user-defined data types are typically designed for specific purposes.

#### Enumerated Data Type

An enumerated data type contains no references to other data types when it is defined.

Enumerated data types, also known as enums, are a way to define a specific set of values that a variable can hold. It's like having a predefined list of options to choose from. Think of it as a menu in a restaurant. The menu lists different dishes you can order. Each dish has a unique name and description. In programming, an enumerated data type works similarly. It defines a list of named values, and a variable of that type can only be assigned one of those specific values.

In pseudocode the type definition would look like this:

`TYPE <IDENTIFIER> = (val1, val2, val3, ... )`

For example, let's say we want to represent the days of the week in a program. We can define an enumerated data type called "DaysOfWeek" with the following options: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, and Sunday. 

```pseudocode
TYPE DaysOfWeek = (Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday)
```

Now, if we declare a variable of type "DaysOfWeek", we can only assign it one of those specific values.

```pseudocode
DECLARE today : DaysOfWeek
today <- Monday
```

Here is the python:

```python
import enum
class DaysOfWeek(enum.Enum):
    MONDAY = 1
    TUESDAY = 2
    WEDNESDAY = 3
    THURSDAY = 4
    FRIDAY = 5
    SATURDAY = 6
    SUNDAY = 7

day = DaysOfWeek.MONDAY
```

Enums are useful because they provide clarity and restrict the range of possible values a variable can have. They make code more readable and help avoid errors by ensuring that variables are assigned valid values from a predefined set.

