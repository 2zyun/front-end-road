- 关于jQuery事件委托，目标元素不熟悉
    + e.target
    + $(e.target)
- 关于节点的操作不熟悉
- 第一个子节点的前兄弟节点是什么
- 最后一个节点的后兄弟节点是什么

- && and ||
    + 用途1 条件判断，分别表示与/或
    如果&&的第一个运算数是false，就不再考虑第二个运算数，直接返回false；如果||的第一个运算数是true，也不再考虑第二个运算数，直接返回true
    ```js
    if((a == null) && (b++ >10)) stop(); //b++递增运算可能不被执行
    if((b++ >10) && (a == null)) stop(); //保证b++递增运算都被执行
    ```
    + 用途2 简化选择性执行语句的操作
    **a() && b()** :如果执行a()后返回true，则执行b()并返回b的值；如果执行a()后返回false，则整个表达式返回a()的值，b()不执行； 
    **a() || b()** :如果执行a()后返回true，则整个表达式返回a()的值，b()不执行；如果执行a()后返回false，则执行b()并返回b()的值； 
    > && 优先级高于 || 
    ```js
    var a = function() { return true; }
    var b = function() { return false; }
    var c = function(a, b) { 
        return a + b;
    }

    a() && c(10, 20); // 30
    b() && c(10, 20); // false
    a() || c(10, 20); // true
    b() || c(10, 20); // 30
    ```

