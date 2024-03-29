Dependency Injection (DI) is a design pattern used to implement Dependency Inversion Principle, one of the five SOLID principles of object-oriented design. It's a technique to achieve Inversion of Control (IoC) between classes and their dependencies.

### **The Basics**

1. **Dependencies**: These are the objects or services that a class needs to perform its function.
2. **Injection**: This is the process of providing those dependencies to the class. Instead of the class creating the dependency or using a factory to get it, the dependency is passed to the class (typically to a constructor, but it can also be to a method or property).

### **Types of Dependency Injection**

There are primarily three types of DI:

1. **Constructor Injection**: The dependencies are provided through the class's constructor.
2. **Setter Injection**: The dependencies are provided through setter methods (or properties in languages like C# and Java).
3. **Method Injection**: The dependencies are provided as parameters to the method that needs them.

### **Why Use Dependency Injection?**

- **Decoupling**: Classes do not create their dependencies. Instead, they receive them. This decoupling leads to more modular code and easier unit testing.
- **Ease of Testing**: When dependencies are injected, it's easy to replace them with mocks or stubs for testing.
- **Flexibility and Scalability**: Changing a dependency doesn't require changes to the class using it, provided the new dependency adheres to the expected interface.
- **Configuration and Boostrapping**: It's easier to configure the system's components in one place, often at the application's entry point.

### **How It Works**

A DI container (or an IoC container) is often used in practice, though it's not a requirement for DI. This container is responsible for the instantiation of objects and managing their lifecycles, as well as injecting dependencies where required.

### **Example**

```csharp
// Service interface
public interface ILogger
{
    void Log(string message);
}

// Concrete implementation of a service
public class ConsoleLogger : ILogger
{
    public void Log(string message)
    {
        Console.WriteLine(message);
    }
}

// Consumer class that depends on the ILogger interface
public class Processor
{
    private readonly ILogger _logger;

    // Constructor injection
    public Processor(ILogger logger)
    {
        _logger = logger ?? throw new ArgumentNullException(nameof(logger));
    }

    public void Process(string data)
    {
        _logger.Log($"Processing data: {data}");
        // Process the data
    }
}

// Composition root
class Program
{
    static void Main()
    {
        // Create a logger
        ILogger logger = new ConsoleLogger();

        // Inject the logger into the Processor
        Processor processor = new Processor(logger);

        // Use the processor
        processor.Process("Example data");
    }
}
```