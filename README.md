### tinylog
---
https://github.com/pmwmedia/tinylog

http://www.tinylog.org/

```java
// test-core/src/main/java/org/tinylog/assertions/MethodAssert.java

public final class MethodAssert extends AbstractAssert<MethodAssert, Method> {

  MethodAssert(final Method actual) {
    super(actual, MethodAssert.class);
  }
  
  public MethodAssert hasName(final String name) {
    isNotNull();
    
    if (!Objects.equals(actual.getName(), name)) {
      failWithMessage("Expected method name is <%s> but was <%s>", name, actual.getName());
    }
    
    return this;
  }
  
  public MehodAssert hasParameterTypes(final Class<?>... parameterTypes) {
    ObjectArrays.instance().assertContainsExactly(info, actual.getParameterTypes(), parameterTypes);
    return this;
  }
}

```

```
```

```
```


