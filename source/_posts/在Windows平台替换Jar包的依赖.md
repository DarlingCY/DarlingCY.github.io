---
title: 在Windows平台替换Jar包的依赖
date: 2023-08-18 15:16:45
tags: 
  - Java
---
- 在Jar包当前目录进行Jar拆包
    ```shell
    jar -xvf JarName.jar
    ```
- 拆包后会得到BOOT-INF、META-INF、org三个文件夹，根据需求替换BOOT-INF/lib中的Jar依赖
- 替换后重新打包
    ```shell
    jar -cfM0 JarName.jar ./BOOT-INF ./META-INF ./org
    ```