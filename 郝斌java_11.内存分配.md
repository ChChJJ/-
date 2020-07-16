# 内存分配

> ​    

### 程序执行过程

![程序执行过程](./Java截图/程序执行过程.png)

```java

class A
{
	int i;
	int j;
}

class TestDemo 
{
	public static void main(String[] args) 
	{
		A aa = new A();	// 相当于C语言中的 (A *)malloc(sizeof(A));
			// new A();  在堆内存中动态分布一块区域，被当作了 A的对象
			// aa本身的内存是在栈内存中静态分配的（因为aa是以数据类型和变量名的方式）
			// aa指向堆中的内存，aa 代表了堆中的内存
			// aa.i代表：aa这个静态引用（指针）变量所指向的动态内存中的 A对象的 i这个成员
			// aa.j代表：aa这个静态引用（指针）变量所指向的动态内存中的 A对象的 j这个成员
		aa.i = 20;
		aa.j = 8;
		System.out.println("aa.i = " + aa.i);  //  aa.i = 20
		System.out.println("aa.j = " + aa.j);  //  aa.j = 8
	}
}

```



###### 单个对象实例(1)内存分配图

![](./Java截图/单个对象实例(1)内存分配图.png)



###### 类对象实例2

![类对象实例2](./Java截图/类对象实例2.png)



###### 类对象实例2内存分析图

![类对象实例2内存分析图](./java截图/类对象实例2内存分析图.png)

```java
class A{
    int i = 10;
    int j = 20;
}
class TSC{
    public static void main(String() args){
        A aa1 = new A();
        A aa2 = aa1;
        aa1.j = 30;
        System.out.println(" aa2.j = " + aaj.2);
    }
}
    
```