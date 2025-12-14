
```java
package org.example;  

class Teacher {

    Teacher(int i) {

        this("doctor");

        System.out.println("The teacher teaches " + i + " years ");

    }

    Teacher(String s) {

        System.out.println("The teacher's degree is" + s);

    }

    void teach() {//`void teach()`就是老师的一个​**​动作​**​或​**​行为**

        System.out.println("teacher teaches very good");

    }

}

public class OverloadedConstructors {

    public static void main(String[] args) {

        new Teacher(8).teach();

    }

}
```

***代码解释

```
步骤1: 程序开始执行 main 方法
步骤2: 遇到 new Teacher(8) → 调用第一个构造方法
步骤3: 在第一个构造方法中，立即遇到 this("doctor")
步骤4: 暂停当前方法，先执行 Teacher("doctor") 方法
步骤5: 打印 "The teacher's degree doctor"
步骤6: 回到第一个构造方法继续执行
步骤7: 打印 "The teacher teaches 8 years"
步骤8: 对象创建完成，调用 teach() 方法
步骤9: 打印 "teacher teaches very good"
步骤10: 程序结束

```

遇到: this("doctor")
↓
检查参数类型: 字符串 "doctor"
↓
在Teacher类中搜索: 有没有接受字符串参数的构造方法？
↓
找到: Teacher(String s) { ... }
↓
跳转到这个方法并执行
↓
执行完后回到原来的位置继续