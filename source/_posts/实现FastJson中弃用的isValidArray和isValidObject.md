---
title: 实现FastJson中弃用的isValidArray和isValidObject
date: 2023-08-18 15:16:45
tags:
  - Java
---

- isValidArray
    ```java
    public boolean isValidArray(String str) {
        return JSONValidator.Type.Array == JSONValidator.from(str).getType();
    }
    ```
- isValidObject
    ```java
    public boolean isValidObject(String str) {
        return JSONValidator.Type.Object == JSONValidator.from(str).getType();
    }
    ```