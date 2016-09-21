---
title: 同一行输入三个数字 java
categories:
    - java基础
tags:
    - java基础
---


---
```
  package com.jisuanke;

import java.io.*;

public class first {
	public static void main(String args[])
		throws IOException 
		{
			BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
			String str;
			String [] str1 = new String[3];
			int [] data = new int[3];
			str = br.readLine();
			str1 = str.split(" ");
			for(int i=0; i < 3; i++) {
				data[i] = Integer.parseInt(str1[i]);
			}
			int b = data[0] + data[1] + data[2];
			System.out.println(b);
			
		
	}
}
```

**更简单的方法**
```
package com.lanqiaobie;

import java.util.*;

public class One

{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();
        System.out.println(a + b + c);
    }
}
```
>样例输入：12 3 4
>样例输出：19



