Unit tests are a type of software testing where individual units or components of a software are tested. The purpose is to validate that each unit of the software performs as designed. A unit is the smallest testable part of any software and usually has one or a few inputs and usually a single output. In procedural programming, a unit could be an entire module, but it is more commonly an individual function or procedure. In object-oriented programming, a unit is often an entire interface, such as a class, or it might be one method within a class.

**Why Use Specialized Frameworks Like JUnit:**

Specialized frameworks like JUnit for Java, PyTest for Python, NUnit for .NET, and others provide a comprehensive testing environment for developers. They come with a host of benefits:

1. **Standardization:** They provide a standard way of writing and running tests which can be consistent across different parts of the project or even across different projects.
2. **Ease of use:** They offer user-friendly annotations and assertions to define tests and verify outcomes, making tests easier to write and understand.
3. **Integration:** They can be integrated with build tools (like Maven or Gradle for Java) and Continuous Integration (CI) systems to automatically run tests with every build or deployment.
4. **Test Isolation:** They promote the writing of tests that are independent of each other, which makes it easier to pinpoint failures.
5. **Reporting:** They offer mechanisms to generate reports that give insights into the number of tests that have passed, failed, or skipped.

**Benefits of Unit Tests:**

1. **Early Bug Detection:** Bugs can be found early in the development cycle, which can save time and cost in the long run.
2. **Code Quality:** Writing unit tests encourages better coding practices, as it requires the code to be modular to make testing feasible.
3. **Refactoring Confidence:** They allow developers to refactor code or upgrade system libraries with the confidence that the existing functionality is not broken by these changes.
4. **Documentation:** They act as a form of documentation for the code. By reading the tests, one can understand what the code is supposed to do.
5. **Design Feedback:** They can provide immediate feedback on the system design and allow the developer to make improvements continuously.

### Example Code in Java

Build with JUnit 4 and Gradle

```java
// A simple Java class
public class Calculator {
    public int add(int a, int b) {
        return a + b;
    }
    
    public int subtract(int a, int b) {
        return a - b;
    }
    
    public int multiply(int a, int b) {
        return a * b;
    }
    
    public int divide(int a, int b) {
        if (b == 0) {
            throw new IllegalArgumentException("Divider cannot be zero");
        }
        return a / b;
    }
}
```

```java
import org.junit.Assert;
import org.junit.Before;
import org.junit.Test;

// JUnit test class
public class CalculatorTest {
    
    private Calculator calculator;
    
    @Before
    public void setUp() {
        calculator = new Calculator();
    }
    
    @Test
    public void testAdd() {
        int result = calculator.add(10, 15);
        Assert.assertEquals(25, result);
    }
    
    @Test
    public void testSubtract() {
        int result = calculator.subtract(20, 10);
        Assert.assertEquals(10, result);
    }
    
    @Test
    public void testMultiply() {
        int result = calculator.multiply(10, 5);
        Assert.assertEquals(50, result);
    }
    
    @Test(expected = IllegalArgumentException.class)
    public void testDivide() {
        calculator.divide(10, 0);
    }
}
```