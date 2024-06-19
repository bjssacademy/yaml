# YAML



## What is YAML?

- YAML stands for "YAML Ain't Markup Language".
- It is a human-readable data serialization standard.
- Commonly used for configuration files and data exchange between languages with different data structures.

## Why Use YAML?

- Simple and easy to read.
- Widely used in various applications such as configuration files (e.g., Docker Compose, Ansible) and data serialization (e.g., Kubernetes manifests).


## Basic Syntax and Structure 

### Scalars

Scalars in YAML represent the simplest data types, such as strings, numbers, and booleans. They form the basic building blocks for more complex YAML structures.

Examples:

```yaml
string: "Hello, World!"
integer: 25
float: 3.14
boolean: true
```

#### Plain Strings

```yaml
greeting: Hello, World!
```

#### Quoted Strings

```yaml
path: "C:\\Users\\JohnDoe"
message: 'Don''t forget to escape single quotes'
```

#### Multi-line Strings

```yaml
description: |
  This is a multi-line string
  that maintains line breaks.

summary: >
  This is a multi-line string
  that folds line breaks into spaces.
  ```

#### Numbers and Booleans

```yaml
integer: 25
float: 3.14159
is_admin: true
is_guest: no
```

#### Null Values

```yaml
first_name: John
middle_name: ~
last_name: Doe
```

### Key-Value Pairs

Key-value pairs are separated by a colon and a space.

Example:

```yaml
name: John Doe
age: 30
```

### Collections

**Lists**: Use a dash and a space to indicate items.

```yaml
- Apple
- Banana
- Orange
```

**Dictionaries**: Key-value pairs grouped together.

```yaml
person:
  name: John Doe
  age: 30
  occupation: Developer
```

### Nested Structures

Combining lists and dictionaries.

Example:

```yaml
people:
  - name: John Doe
    age: 30
    occupation: Developer
  - name: Jane Smith
    age: 25
    occupation: Designer
```

## Common Features

### Comments

Use the # symbol to add comments.

Example:
```yaml
# This is a comment
name: John Doe
```

### Multi-line Strings

Use `|` for literal block style.

Use `>` for folded block style.

Example:

```yaml
literal_block: |
  This is a multi-line
  string in literal block style.

folded_block: >
  This is a multi-line
  string in folded block style.
```

### Anchors and Aliases

Use `&` to define an anchor and `*` to reference it.

Example:

```yaml
default: &default
  name: John Doe
  age: 30

person:
  <<: *default
  occupation: Developer
  ```


## Hands-on Practice 

### Exercise 1: Simple Key-Value Pairs

Create a YAML file with personal details (name, age, profession).

Example:
```yaml
name: Jane Doe
age: 28
profession: Engineer
```
### Exercise 2: Lists and Nested Structures

Create a YAML file with a list of hobbies and a nested structure for address.

Example:
```yaml
hobbies:
  - Reading
  - Hiking
  - Cooking

address:
  street: 123 Main St
  city: Anytown
  state: CA
  zip: 12345
  ```

### Exercise 3: Multi-line Strings and Comments

Create a YAML file with a description using multi-line strings and add comments.

Example:
```yaml
description: |
  This is a detailed
  description that spans
  multiple lines.

# Remember to include comments
```