有一些约束应用于const变量。它们如下 -
const只能应用于类的不可变属性。
它不能分配给任何函数或任何类构造函数。它应该分配有原始数据类型或字符串。
const变量将在编译时初始化。

在 Kotlin 中，val也用于声明变量。“val”和“const val”都用于声明类的只读属性。声明为const的变量在运行时初始化。
val处理类的不可变属性，即只能使用val声明只读变量。
val在运行时初始化。
对于val，内容可以被静音，而对于const val，内容不能被静音。

const val 和 val 的区别:
const 关键字 不可单独使用，只能与 val 组合使用.

1. const val 只可以修饰top-level变量，val 无限制

2. const val 字节码为 public final static，可以直接访问。而 val 字节码为 private final static，并且val 会生成方法getNormalObject()，通过方法调用访问。