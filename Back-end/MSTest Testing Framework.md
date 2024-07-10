MSTest uses the `[TestClass]` and `[TestMethod]` attributes to denote a class as a test class and, a method as a test method, respectively.

## Example:
~~~
[TestClass]
public class MSTestUserServiceTests
{
    private const string _useName = "admin";
    private const string _password = "password";
    private const string _otherPassword = "other_password";

    private UserService? userService;

    [TestInitialize]
    public void TestInitialize()
    {
        userService = new UserService();
        userService.AddUser(new User(_useName, _password));
    }

    [TestCleanup]
    public void TestCleanup()
    {
        userService?.RemoveUser(_useName);
    }

    [TestMethod]
    public void ValidCredentials_WhenAuthenticate_ThenShouldReturnTrue()
    {
        var isAuthenticated = userService?.Authenticate(_useName, _password);

        Assert.IsTrue(isAuthenticated);
    }

    [TestMethod]
    public void InvalidCredentials_WhenAuthenticate_ThenShouldReturnFalse()
    {
        var isAuthenticated = userService?.Authenticate(_useName, _otherPassword);

        Assert.IsFalse(isAuthenticated);
    }
}
~~~

## Note: 
It is important to note that in MSTest all the methods used to initialize and cleanup the tests follow strict naming conventions.** MSTest can only recognize these methods as part of the test setup if we follow the convention.

## Reference
https://code-maze.com/csharp-testing-framework-differences-between-nunit-xunit-and-mstest/?ref=dailydev
