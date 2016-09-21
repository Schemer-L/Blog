---
title: java Scanner类的简单用法
categories: 
- java基础
tags: 
- java基础
---

```
import java.util.*;
public class ScannerDemo {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner scan = new Scanner(System.in); // 创建Scanner实例
		int num = 0;
		float f = 0.0F;
		System.out.println("请输入int型整数：");
		if(scan.hasNextInt()) {  // 判断输入的数据是否为int型 在使用nextXxx()方法时最好用hasNextXxx()方法验证，否则容易产生异常
			num = scan.nextInt();  // 输入int型整数
		} 
		else {
			System.out.println("输入的不是整数\n程序退出");
			System.exit(0); // 退出程序
		}
		
		System.out.println("请输入float型整数：");
		if(scan.hasNextFloat()) {  // 判断输入的数据是否为float型
			f = scan.nextFloat();  // 输入float型数
		} 
		else {
			System.out.println("输入的不是小数\n程序退出");
			System.exit(0); // 退出程序
		}
		System.out.println("请输入字符串： ");
		String str = scan.next();  // 输入字符串，若输入的字符串中间有空格，那么空格之后的数据就没有了
		System.out.println("整数：" + num + "\n小数： " + f + "\n字符串： " + str);
	}

}
```
>请输入int型整数：
>32
>请输入float型整数：
>234.44
>请输入字符串： 
>asf dfsa
>整数：32
>小数： 234.44
>字符串： asf

```
/*解决上面的字符串空格问题 
		 * 使用useDelimiter()将分隔符修改为换行符"\n"
		 * Scanner扫描到分隔符就停止
		 * 例如：scan.useDelimiter(";"); for(int i=0; i<2; i++) { str = scan.next(); System.out.println(str);}
		 * 输入是: aa;bb 输出是：
		 * aa
		 * bb
		 * 
		 */
		scan.useDelimiter("\n"); 
		str = scan.next();
		System.out.println(str);
		
		// 还可以用nextLLine()
		str = scan.nextLine();
		System.out.println(str);
```




