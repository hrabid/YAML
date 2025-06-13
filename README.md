# YAML 
Short form for **YAML Ain't Programming Language**. Previously YAML referred. to  Yet Another Markup Language. 

YAML is a human-readable [[Data Serialization Language]].

> [!NOTE]
> YAML is superset of JSON (Javascript Object Notation). That means any valid JSON file is a valid YAML file.

***Extension***: YAML use .yaml & .yml extension. Both are correct.

## Syntax Essentials 
### Indentation 
- Python style indentation defines structure.
- Space only (tabs are forbidden)
### Comments 
- Comments starts with a hash sign(#)
- Ends with the ending of line 
- Comments can be anywhere in the yaml file

### Sequences & Inline List 
***Block:***
```yaml
microservices:
 - frontend 
 - dashboard
 - shopping_cart 
 - user_auth
```
***Inline(json like)***:
```yaml
microservices: [frontend,dashboard,shopping_cart,user_auth]

```
### Mappings & Inline Maps:
***Block:***
```yaml
microservices:
 app: frontend
 port: 3000
 version: 1.25

```
***Inline (json like):***
```yaml
microservices: [app: frontend, port: 3000, version: 1.25 ]
```

### Scalars & Types 
```yaml
count: 100 # integer 
pi: 3.14 # floating point 
hex: 0xFF # hexadecimal 
flag: true # boolean 
empty: null # null value 
```

### Strings 
Quotation is not necessary in yaml but any of the quotes ("" & '') is valid.
```yaml
name: Mustasim Billah
```
- If there have any special character then Quotes are needed 

### Multi-line Strings 
***Literal Block:*** ( | preserves new line)
```yaml
yaml: |
  YAML Ain't Markup Language
  Yet Another Markup Language
```


***Folded Block:*** ( > merges line with space)
```yaml
yaml: >
  YAML Ain't 
  Markup Language
```

### Multiple Docs 
```yaml
name: app1
version: 1.0
---
name: app2 
version: 2.0
```

### Anchor / Aliases 


### Explicit Tags & Typing
```yaml
str_int: !!str 145 
int_str: !!int "15667"
comma_num: !!int +545_000 # 545,000
float: !!float 15.377
boolean: !!bool true # yes,no | on,off | 
infinite: !!float .inf 
not_a_num: .nan
null_value: !!null Null # or null, NULL, ~
~: wth # a null key 
```


## Usecase
YAML is widely used as configuration file for most of the DevOps tools. Like: 
- Automation
- Configuration file
  - docker-compose 
  - k8s manifests 
  - Ansible playbook
  - GitHub Actions 
- Data Exchange 

## Terms 
- **Scalars** : Simple Values like **strings, numbers, boolean, null** etc.  
- **Sequences:** Ordered List of items.
- **Mappings:** Key-Value Pair

## Release 
Initial Release: 11 May 2001
Latest Release: 01 October 2021 (v1.2.2)

Copyright (c) 2025 hrahmanabid. All Rights Reserved.
