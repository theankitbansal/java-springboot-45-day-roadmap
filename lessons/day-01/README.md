# Day 1 — Java Foundations

**Status:** Not started  
**Goal:** Understand how Java is compiled and run, then practise variables, data types, operators, conditions, loops, methods, and a first look at OOP.

## Suggested 2-hour session
- 30 minutes: read and run the examples.
- 60 minutes: complete exercises without copying a solution.
- 30 minutes: answer the knowledge check and explain your reasoning.

## 1. JDK, JRE, JVM, source code, and bytecode
- **JVM (Java Virtual Machine):** runs Java bytecode.
- **JRE (Java Runtime Environment):** traditionally refers to the JVM plus runtime libraries.
- **JDK (Java Development Kit):** includes development tools such as the Java compiler, plus runtime components.
- **Source code:** the human-readable .java file.
- **Bytecode:** the compiled .class file executed by the JVM.

Typical flow:
1. Write HelloLoan.java.
2. Compile it with javac HelloLoan.java.
3. Run it with java HelloLoan.

For Java 8, check versions with javac -version and java -version.

## 2. First program

Create HelloLoan.java:

~~~java
public class HelloLoan {
    public static void main(String[] args) {
        System.out.println("Loan application learning project");
    }
}
~~~

Compile and run:

~~~bash
javac HelloLoan.java
java HelloLoan
~~~

Expected output:

~~~text
Loan application learning project
~~~

The public class name must match the filename: HelloLoan belongs in HelloLoan.java.

## 3. Variables and data types

A variable stores a value that a program can use.

~~~java
public class LoanDetails {
    public static void main(String[] args) {
        String applicantReference = "APP-1001";
        double requestedAmount = 250000.00;
        int tenureMonths = 36;
        boolean eligibleForInitialReview = true;

        System.out.println(applicantReference);
        System.out.println(requestedAmount);
        System.out.println(tenureMonths);
        System.out.println(eligibleForInitialReview);
    }
}
~~~

For financial calculations, use BigDecimal rather than double when exact decimal arithmetic and explicit rounding are required. We will cover this more deeply later.

Common primitive types include int, long, double, float, boolean, char, byte, and short. String is a reference type, not a primitive.

## 4. Operators and conditions

~~~java
int tenureMonths = 36;
double requestedAmount = 250000.00;

if (requestedAmount > 0 && tenureMonths >= 6 && tenureMonths <= 360) {
    System.out.println("Input passes basic checks");
} else {
    System.out.println("Input needs correction");
}
~~~

- && means both conditions must be true.
- || means at least one condition must be true.
- == compares primitive values; for object values such as strings, use equals() when comparing content.
- = assigns a value; it does not test equality.

## 5. Loops

~~~java
for (int month = 1; month <= 3; month++) {
    System.out.println("Processing month " + month);
}
~~~

A for loop is useful when the number of iterations is known. A while loop is useful when repetition depends on a condition.

## 6. Methods

A method groups behaviour under a name and can accept parameters and return a value.

~~~java
public class LoanChecks {
    public static boolean isValidTenure(int tenureMonths) {
        return tenureMonths >= 6 && tenureMonths <= 360;
    }

    public static void main(String[] args) {
        System.out.println(isValidTenure(36));
        System.out.println(isValidTenure(2));
    }
}
~~~

Expected output:

~~~text
true
false
~~~

static lets this method be called from main without creating a LoanChecks object. We will examine static and object-oriented design in more detail later.

## 7. OOP preview
- **Class:** a definition describing state and behaviour.
- **Object:** an instance of a class.
- **Encapsulation:** keeping data and related behaviour together while controlling access.
- **Inheritance:** defining a class in terms of another class.
- **Polymorphism:** using a common type or contract with different implementations.
- **Abstraction:** exposing essential behaviour while hiding implementation details.

Focus on examples rather than memorising definitions.

## Practice exercises
1. Print the project title and today's learning goal.
2. Create variables for a synthetic application reference, loan amount, tenure, and status. Print them.
3. Write isValidTenure(int months) that returns true for values from 6 through 360 inclusive.
4. Print the numbers 1 through 12 using a loop.
5. Print only the even numbers between 2 and 20.
6. Write a method that accepts a loan amount and returns whether it is greater than zero.
7. Explain why a monetary amount should generally not be represented by double in financial calculations.

Use synthetic data only. Do not use real customer information.

## Knowledge check — answer before looking up explanations
Reply in your own words and include code for coding questions.

1. What is the difference between the JDK and JVM?
2. What happens between compiling a .java file and running the class?
3. Why must a public class named LoanChecks be saved as LoanChecks.java?
4. What is the difference between a primitive type and a reference type? Give one example of each.
5. What is the difference between = and ==?
6. When comparing two strings by content, why is equals() normally preferred over ==?
7. What is the difference between for and while loops?
8. Write isValidTenure(int months) for a range of 6 to 360 inclusive.
9. If a loan amount is 0, should isPositiveAmount return true or false? Explain.
10. Interview question: what are the four main OOP principles? Give a simple example of one.

## Completion criteria
- [ ] Compiled and ran at least one Java program.
- [ ] Completed at least five exercises.
- [ ] Answered the knowledge check.
- [ ] Reviewed mistakes and completed a retest if needed.
- [ ] Confirmed that the topic is understood.

**Do not mark Day 1 complete until the assessment has been reviewed and you confirm readiness.**

## Official references
- [Dev.java — Learn Java](https://dev.java/learn/)
- [Java SE 8 documentation](https://docs.oracle.com/javase/8/docs/)
