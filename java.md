# Various Java cheats
## Change value of final static private field with Reflection (for testing)<br>
```java
Field field = data.getClass().getDeclaredField("type");
field.setAccessible(true);
Field modifiersField = Field.class.getDeclaredField("modifiers");
modifiersField.setAccessible(true);
modifiersField.setInt(field, field.getModifiers() & ~Modifier.FINAL);
field.set(data, null);
```
**For Android**
```java
Field field = data.getClass().getDeclaredField("type");
field.setAccessible(true);
field.set(data, null);
```

**NOTE:** cannot change *primitive* fields

