# 主流JDK特性

## JDK8

### Lambda 表达式
允许把函数作为一个方法的参数传递，使代码更简洁
```
List<String> list = Arrays.asList("a1", "a2", "a3");
list.forEach(s -> System.out.println(s));
```
### stream API
用于处理集合元素，提供了过滤，映射，匹配，聚合等操作
```
List<Integer> numbers = Arrays.asList(1, 2, 3);
List<Integer> list = numbers.steam().filter(n -> n > 1).collect(Collectors.toList());
```
### 接口默认方法和静态方法
接口中可以定义默认方法和静态方法，为接口增加了更多的灵活性
```
interface MyInterface {
    default void defaultMethod() {
        System.out.println("default method");
    }
    static void staticMethod() {
        System.out.println("static method");
    }
}
```
