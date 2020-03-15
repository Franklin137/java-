# Java从键盘接收字符

从键盘中输入若干成绩（double类型）并填入一个数组中，使用foreach输出。

```java
import java.util.Scanner;

class homework1 {
	public static void main(String arg[]){
		Scanner input=new Scanner(System.in);
		System.out.printf("输入成绩(空格隔开):");
		String num=input.nextLine();
		String tem[]=num.split(" ");
		double grade[]=new double[tem.length];
		for(int i=0;i<tem.length;i++) {
			grade[i]=Double.parseDouble(tem[i]);
		}
		for(double i:grade) {
			System.out.printf(i+"\t");
		}
		System.out.printf("\n");
	}
}
```

仅需先输入一个用空格隔开的数字字符串，而后切割字符串并将其转换为double类型即可。