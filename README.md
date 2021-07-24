# JUNIT-5_Basics ❤️ 

- This module consists of Some Important and Basic Concepts of JUNIT-5 (Unit Testing) which is verymuch supportive for testing our Code with multiple test scripts in Eclipse/Spring framework.

# Introduction 👋

- This JUnit 5 tutorial talks about how it adapted java 8 style of coding and several other features as well.
- JUnit 5 is most widely used testing framework for java applications. 
- For very long time, JUnit has been doing its job perfectly. 
- In between, JDK 8 brought very exciting features in java and most notably lambda expressions. 
- JUnit 5 aims to adapt java 8 style of coding and several other features as well, that’s why java 8 is required to create and execute tests in JUnit 5 (though it is possible to execute tests written with JUnit 3 or JUnit 4 for backward compatibility).

# JUnit 5 Architecture 📺
  
     JUnit 5 = JUnit Platform + JUnit Jupiter + JUnit Vintage

## JUnit Platform

- To be able to launch junit tests, IDEs, build tools or plugins need to include and extend platform APIs. It defines the TestEngine API for developing new testing frameworks that runs on the platform.
- It also provides a Console Launcher to launch the platform from the command line and build plugins for Gradle and Maven.

## JUnit Jupiter

- It includes new programming and extension models for writing tests. 
- It has all new junit annotations and TestEngine implementation to run tests written with these annotations.

## JUnit Vintage

- It primary purpose is to support running JUnit 3 and JUnit 4 written tests on the JUnit 5 platform. 
- It’s there are backward compatibility.

# Installation 📫

You can use JUnit 5 in your maven or gradle project by including minimum two dependencies i.e. Jupiter Engine Dependency and Platform Runner Dependency.

    //pom.xml
    
    <properties>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <maven.compiler.source>1.8</maven.compiler.source>
        <maven.compiler.target>${maven.compiler.source}</maven.compiler.target>
        <junit.jupiter.version>5.5.2</junit.jupiter.version>
        <junit.platform.version>1.5.2</junit.platform.version>
    </properties>
    <dependencies>
        <dependency>
            <groupId>org.junit.jupiter</groupId>
            <artifactId>junit-jupiter-engine</artifactId>
            <version>${junit.jupiter.version}</version>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.junit.platform</groupId>
            <artifactId>junit-platform-runner</artifactId>
            <version>${junit.platform.version}</version>
            <scope>test</scope>
        </dependency>
    </dependencies>

    //build.gradle
    testRuntime("org.junit.jupiter:junit-jupiter-engine:5.5.2")
    testRuntime("org.junit.platform:junit-platform-runner:1.5.2")
    
# JUnit 5 Annotations 📌

### @BeforeEach	- The annotated method will be run before each test method in the test class.
### @AfterEach - The annotated method will be run after each test method in the test class.
### @BeforeAll - The annotated method will be run before all test methods in the test class. This method must be static.
### @AfterAll - The annotated method will be run after all test methods in the test class. This method must be static.
### @Test - It is used to mark a method as junit test
### @DisplayName - Used to provide any custom display name for a test class or test method
### @Disable	- It is used to disable or ignore a test class or method from test suite.
### @Nested -	Used to create nested test classes
### @Tag	- Mark test methods or test classes with tags for test discovering and filtering
### @TestFactory -	Mark a method is a test factory for dynamic tests


