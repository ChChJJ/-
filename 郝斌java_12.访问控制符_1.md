# 访问控制符_1

> 一般只向外部提供一些按钮（类似于黑匣子）

```java
class Triangle
{
	private int a, b, c;  //如果不加访问控制符，默认是protected 

	int zhouchang() {
		return a + b + c;
	}

	double area() {
		double p = 1.0*(a + b + c) / 2;
		return Math.sqrt( p * (p-a) * (p-b) * (p-c));
	}

	void set(int i, int j, int k) {
		a = 3;
		b = 4;
		c = 5;
	}
}

class TestTriangle 
{
	public static void main(String[] args) 
	{
		Triangle t = new Triangle();
		//t.a = 3;
		//t.b = 4;
		//t.c = 5;

		t.set(3, 4, 5);

		System.out.println("zhouchang = " + t.zhouchang() + "\n" + "area = " + t.area());
	}
}
```



> 在一个类的内部，所有的成员可以相互访问，访问控制符是透明的；访问控制符是针对外部访问而言的

![类的访问控制符](./java截图/类的访问控制符.png)



![private修饰符(重点)](./Java截图/private修饰符(重点).png)