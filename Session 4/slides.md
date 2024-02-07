---
marp: true
backgroundColor: #cce3ee
color: #455a64

style: |
  .columns {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1rem;
  }
---

![bg right height:4.5in](imgs/dockerLogo.png)

<!--_fontSize:13px-->>

# <!--fit--> Get to Docker

## Session 4

---

## Agenda

- Introduction to yaml
- Docker Compose

---

#  <!--fit--> Introduction to yaml

---

## Introduction to yaml

- YAML stands for "YAML Ain't Markup Language" or "Yet Another Markup Language"

- YAML is a human-readable data serialization standard that can be used in conjunction with all programming languages and is often used to write configuration files.

- YAML is a superset of JSON, which means that any valid JSON file is also a valid YAML file.

---

## Introduction to yaml - key-value pairs

- Keys are separated from their values by a colon followed by a space.

- Key-value pairs are separated by a new line.

- Example

  ```yaml
  name: John
  age: 30
  ```

---

## Introduction to yaml - Data Types

- Scalars

  - Strings
  - Numbers
  - Booleans
  - Nulls

- Collections
  - Arrays
  - Dictionaries

---

## Introduction to yaml - Scalars

- Strings `may be plain or quoted`

  ```yaml
  name: John
  ```

- Numbers

  ```yaml
  age: 30
  grade: 9.5
  ```

- Booleans

  ```yaml
  isStudent: true
  ```

- Nulls

  ```yaml
  address: null
  ```

---

## Introduction to yaml - Collections

- Arrays

  ```yaml
  fruits:
    - Apple
    - Banana
    - Orange
  ```

  ```yaml
  fruits: [Apple, Banana, Orange]
  ```

- Dictionaries

  ```yaml
  person:
    name: John
    age: 30
  ```

  ```yaml
  person: { name: John, age: 30 }
  ```

---

## Introduction to yaml - Syntax

- Indentation

  - YAML uses indentation to indicate nesting of elements.

  - The number of spaces is not fixed, but it should be consistent throughout the file.

---

## Introduction to yaml - Syntax

- Example 1

  ```yaml
  person:
    name: John
    age: 30
    address:
      city: New York
      state: NY
  ```

---

## Introduction to yaml - Syntax

- Example 2

  ```yaml
  person:
    - name: John
      age: 30
      address:
        city: New York
        state: NY
    - name: Jane
      age: 25
      address:
        city: Los Angeles
        state: CA
  ```

---

## Introduction to yaml - Complex Example

- Suppose we have a car that may have a

  - color
  - model
  - price
  - transmission

- If we want to store information about single car, we will use dictionaries

  ```yaml
  car:
    color: red
    model: 2021
    price: 20000
    transmission: automatic
  ```

---

## Introduction to yaml - Complex Example

- If the model consists of `year` and `name` then we will represent it as nested dictionaries

  ```yaml
  color: red
  car:
    model:
      year: 2021
      name: corolla
  price: 20000
  transmission: automatic
  ```

---

## Introduction to yaml - Complex Example

- If we want to store the name of 5 cars `store data of same type` we will use `list of strings`

  ```yaml
  cars:
    - corolla
    - civic
    - city
    - vitz
    - prius
  ```

- If we want to store all information of 5 cars `store data of different type` we will use `list of dictionaries`


---

## Introduction to yaml - Complex Example

```yaml
cars:
  - color: red
    model:
      year: 2021
      name: corolla
    price: 20000
    transmission: automatic
  - color: blue
    model:
      year: 2020
      name: civic
    price: 18000
    transmission: manual
  - color: white
    model:
      year: 2019
      name: city
    price: 15000
    transmission: automatic
  - color: black
    model:
      year: 2018
      name: vitz
    price: 17000
    transmission: manual
  - color: silver
    model:
      year: 2017
      name: prius
    price: 16000
    transmission: automatic
```

---


# <!--fit--> Docker Compose

---

## Docker Compose

