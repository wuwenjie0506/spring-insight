## 1. Type

java.lang.reflect.Type: 是Java所有类型的superinterface，包含普通类型、泛型、数组类型、和primitive等。
在Gson、fastjson等框架中国都有使用到，需要深入的理解。

- TypeVariable
- WildcardType
- GenericArrayType
- Class

## 2. ResolvableType

使用方法:

``` 

	private HashMap<Integer, List<String>> myMap;

    public void example() {
        ResolvableType t = ResolvableType.forField(getClass().getDeclaredField("myMap"));
        t.getSuperType(); // AbstractMap<Integer, List<String>>
        t.asMap(); // Map<Integer, List<String>>
        t.getGeneric(0).resolve(); // Integer
        t.getGeneric(1).resolve(); // List
        t.getGeneric(1); // List<String>
        t.resolveGeneric(1, 0); // String
    }

```

