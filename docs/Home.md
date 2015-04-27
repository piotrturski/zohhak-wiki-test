# Zohhak - JUnit parameterized made simple

#### Clean & DRY parameterized tests
Zohhak lets you write flexible parameterized JUnit tests without boilerplate. No need for data providers or custom constructors. Each test has its own set of parameters and you can use any types you want:
```java
@TestWith({
    "clerk,      45'000 USD, GOLD",
    "supervisor, 60'000 GBP, PLATINUM"
})
public void canAcceptDebit(Employee employee, Money money, ClientType clientType) {
    assertTrue(   employee.canAcceptDebit(money, clientType)   );
}
```
No plugin needed. Just run and you'll see:<br />

![http://wiki.zohhak.googlecode.com/git/img/eclipse_run.gif](http://wiki.zohhak.googlecode.com/git/img/eclipse_run.gif)
#### Start using Zohhak
Get Java 5+, JUnit 4.5+ and read 3 minute [Quick Start](Quick-Start) or [Full Guide](Full-Guide)
```xml
<dependency>
    <groupId>com.googlecode.zohhak</groupId>
    <artifactId>zohhak</artifactId>
    <version>1.1.0</version>
    <scope>test</scope>
</dependency>
```
Or download jar from [maven central repo](http://search.maven.org/#search|gav|1|g%3A%22com.googlecode.zohhak%22%20AND%20a%3A%22zohhak%22) and add the dependency: org.apache.commons:commons-lang3:3.1
#### Credits
Zohhak was inspired by [JUnitParams](https://github.com/Pragmatists/junitparams), [Tapestry 5](http://tapestry.apache.org) and [Spring](http://spring.io). Thanks guys!