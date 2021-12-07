## Introduction

 DBeaver has the functionality to add and edit artifacts in existing drivers.

## How to open

> Database -> Driver Manager -> `Select driver`-> Libraries

### How to edit

    Double click on the library

### How to add

    Click `Add Artifact`

## How to use

For add mode, **DBeaver** supports two modes **Dependency Declaration** and **Declare Artifacts Manually**. The editing mode only supports the second **Declare Artifacts Manually**.

### Dependency Declaration

Mode parses the inputted text and creates artifacts out of the results of parsing. It supports the multiple input formats written below.

![Dependency Declaration](images/edit-maven-artifacts-dependency-declaration.png)

#### Supported formats

* Short Gradle

    ```
    group:artifact_name:version
    ```

* Maven
  * For a single artifact

    ``` XML
    <dependency>
        <groupId>group</groupid>
        <artifactId>artifact</artifactId>
        <version>version</version>
    </dependency>
    ```

  * For multiple artifacts
  
    ```XML
    <dependencies>
        <dependency>
            <groupId>group</groupid>
            <artifactId>artifact</artifactId>
            <version>version</version>
        </dependency>
        <dependency>
            <groupId>group</groupid>
            <artifactId>artifact</artifactId>
            <version>version</version>
        </dependency>
        <dependency>
            <groupId>group</groupid>
            <artifactId>artifact</artifactId>
            <version>version</version>
        </dependency>
    <dependencies>
    ```

### Declare Artifacts Manually

It allows you to manually set up parameters. It allows you to add only one item per dialog.  

![Declare artifacts manually](images/edit-maven-artifacts-manual.png)