# 📚 YAML Tutorial

## Table of Contents 📑

- [📚 YAML Tutorial](#-yaml-tutorial)
  - [Table of Contents 📑](#table-of-contents-)
  - [What is YAML? 🤔](#what-is-yaml-)
  - [Why Use YAML? 🌟](#why-use-yaml-)
  - [Compare YAML, JSON, and XML 🔍](#compare-yaml-json-and-xml-)
  - [YAML - Use Cases 🚀](#yaml---use-cases-)
  - [YAML Examples with Small Explanations 📝](#yaml-examples-with-small-explanations-)
    - [YAML - Data Structures](#yaml---data-structures)
    - [YAML - Structure and Comments 🗒️](#yaml---structure-and-comments-️)
    - [YAML - Document Start and End 🏁](#yaml---document-start-and-end-)
    - [YAML - Key/Value Pairs ⚙️](#yaml---keyvalue-pairs-️)
    - [YAML - String and Quotes 📝](#yaml---string-and-quotes-)
    - [YAML - Dictionaries/Mapping/Hashes 🗂️](#yaml---dictionariesmappinghashes-️)
    - [YAML - Block Collections: Use of Indentation - Spaces 🛠️](#yaml---block-collections-use-of-indentation---spaces-️)
    - [YAML is a Superset of JSON 📊](#yaml-is-a-superset-of-json-)
    - [YAML - Lists/Arrays 📋](#yaml---listsarrays-)
    - [YAML - Nesting/Mixing Structures 🧩](#yaml---nestingmixing-structures-)
      - [Dictionary in List](#dictionary-in-list)
      - [Map in List (Way 1)](#map-in-list-way-1)
      - [Map in List (Way 2)](#map-in-list-way-2)
      - [List in List](#list-in-list)
    - [YAML - Advanced Features 🌟](#yaml---advanced-features-)
      - [Multi-line Strings 📜](#multi-line-strings-)
      - [YAML - Complex Keys 🔑](#yaml---complex-keys-)
      - [YAML - Aliases and Anchors 🔗](#yaml---aliases-and-anchors-)
      - [YAML - Custom Data Types 🎨](#yaml---custom-data-types-)
      - [YAML - Directives 📜](#yaml---directives-)
      - [YAML - Embedded Comments 💬](#yaml---embedded-comments-)
      - [YAML - Conditional and Scalar Values](#yaml---conditional-and-scalar-values)
  - [Introduction to API 🌐](#introduction-to-api-)
  - [Kubernetes YAML Definition File Example 📜](#kubernetes-yaml-definition-file-example-)

---

## What is YAML? 🤔

- **YAML** stands for **YAML Ain't Markup Language**.
- It is a **data serialization language** designed for human readability and ease of use in configuration files and data exchange.

---

## Why Use YAML? 🌟

- YAML provides a standardized, easy-to-read format for configuration and data exchange.
- Compared to XML and JSON, YAML is more human-friendly due to its concise syntax and readability.

---

## Compare YAML, JSON, and XML 🔍

**Example: `hostname: App-1, manufacturer: HP, tire: Backend`**

| Feature         | YAML                             | JSON                            | XML                                  |
| --------------- | -------------------------------- | ------------------------------- | ------------------------------------ |
| **Syntax**      | Human-readable, uses indentation | Bracketed, uses key-value pairs | Tag-based, more verbose              |
| **Usage**       | Config files, data serialization | Data interchange, API responses | Document storage, complex structures |
| **Readability** | High, intuitive                  | Moderate, less human-readable   | Low, verbose                         |

---

## YAML - Use Cases 🚀

- **Configuration Files**: Defining settings for applications and systems.
- **Log Files**: Structured format for logging information.
- **Inter-process Messaging**: Communicating between services and processes.
- **Cross-Language Data Sharing**: Exchanging data between different programming languages.
- **Object Persistence**: Saving and retrieving complex objects.

---

## YAML Examples with Small Explanations 📝

### YAML - Data Structures

- **Scalars**: Basic data types like strings, numbers, and booleans.
- **Mappings**: Key-value pairs, similar to dictionaries or hashes.
- **Sequences**: Lists or arrays, ordered collections of items.

### YAML - Structure and Comments 🗒️

```yaml
# This is a comment
person:
  name: ali
  age: 3
  gender: male
```

### YAML - Document Start and End 🏁

```yaml
---
time: 01:01:10
```

### YAML - Key/Value Pairs ⚙️

```yaml
personName: ali
person_name: hassan
person-name: mohamed
person name: Ali
date: yyyy-mm-dd HH:MM:SS
```

**Note:** Variable names must be consistent within the same key.

### YAML - String and Quotes 📝

- **Special Characters**: Use quotes for strings containing special characters (e.g., `:`, `{}`, `&`).
- **URLs**: Enclose URLs in quotes to avoid issues.

### YAML - Dictionaries/Mapping/Hashes 🗂️

```yaml
# This is an object
person:
  name:
    fname: ali
    lname: hassan
  age: 12
  grade: 23
```

### YAML - Block Collections: Use of Indentation - Spaces 🛠️

**Important:** YAML uses spaces for indentation. Proper alignment is crucial to avoid errors.

```yaml
students:
  - name: Mohamed Salah
  - name: Amit Gupta
  - name: John Smith
  - name: Ali
    age: 23
```

### YAML is a Superset of JSON 📊

```yaml
person: { name: "Hassan", gender: "female", age: 33 }
```

### YAML - Lists/Arrays 📋

```yaml
students:
  - Mohamed Salah
  - Amit Gupta
  - John Smith
  - name: Ali
    age: 23
car_parts: ["tires", "engine", "gas tank"]
```

### YAML - Nesting/Mixing Structures 🧩

#### Dictionary in List

```yaml
play_games:
  - name: Ali
    game: 10
  - name: Hassan
    games: 15
```

#### Map in List (Way 1)

```yaml
play_games:
  - name: Ali
    age: 10
  - name: Hassan
    age: 3
```

#### Map in List (Way 2)

```yaml
play_games:
  name: Hassan
  games_played: 100
  years_played:
    - 1998
    - 2002
    - 2020
  teams: ["a", "b"]
```

#### List in List

```yaml
player_games:
  - name: Ali
  - age: 23
  - injuries:
      - knee
      - shoulder
      - shin
```

### YAML - Advanced Features 🌟

#### Multi-line Strings 📜

YAML supports multi-line strings with two styles:

**Literal Block Style (`|`)**: Preserves newlines and whitespace.

```yaml
bash:
  - |
    #!/bin/bash
    dnf update -y
    dnf install httpd -y
    systemctl start httpd
    echo "This is server *2*" > /var/www/html/index.html
```

**Folded Block Style (`>`)**: Collapses newlines into spaces.

```yaml
accomplishment: >
  Ali was the president of 
  Kid's World Bank from 
  1919 through 2020.
```

#### YAML - Complex Keys 🔑

YAML allows complex keys that can span multiple lines and include various data structures.

```yaml
? - line one
  - line two
: value
? this is key for us
  this content
: some_value
```

#### YAML - Aliases and Anchors 🔗

Aliases and anchors help with reusing and merging parts of YAML documents.

> **Basic Example**

```yaml
defaults: &defaults
  color: blue
  size: medium

item1:
  <<: *defaults
  name: "Item 1"

item2:
  <<: *defaults
  name: "Item 2"
  size: large
```

> **Merging and Overriding**

```yaml
base: &base
  name: Base Item
  price: 100

item:
  <<: *base
  price: 150
  description: "Updated price for item"
```

#### YAML - Custom Data Types 🎨

You can define custom data types using YAML tags.

```yaml
!!python/tuple
- 1
- 2
- 3

!!python/complex '3.14+2.71j'
```

#### YAML - Directives 📜

Directives provide instructions to the YAML processor.

> **Example of a Directive**

```yaml
%YAML 1.2
---
# This is a YAML document
```

#### YAML - Embedded Comments 💬

YAML supports comments within lists and mappings to describe or annotate parts of the document.

```yaml
items:
  - name: Item 1 # This is a comment
    price: 100
  - name: Item 2
    price: 150
    # End of item 2
```

#### YAML - Conditional and Scalar Values

While YAML itself doesn’t have built-in conditionals, it can be used with templating engines or preprocessors to include conditional logic.

> **Example Using Preprocessor**

```yaml
# In a preprocessed file
items:
  - name: Item 1
    price: ${PRICE_1}
  - name: Item 2
    price: ${PRICE_2}
```

---

## Introduction to API 🌐

- **API** (Application Programming Interface) facilitates communication between different software systems.
- **YAML** is commonly used in API definitions (e.g., OpenAPI Specification) to describe endpoints, request/response formats, and other API details.

---

## Kubernetes YAML Definition File Example 📜

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: static-web
  labels:
    role: myrole
spec:
  containers:
    - name: web
      image: nginx
      ports:
        - name: web
          containerPort: 80
          protocol: TCP
```

---
