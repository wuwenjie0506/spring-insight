1. ResolvableType
	(1) 参考基础Type，封装java.lang.reflect.Type。
	(2) 使用方法:
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

2. AutowireCandidateResolver

