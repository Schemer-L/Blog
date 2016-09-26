---
title: java 小数点后面位数的输出
categories: 
- java基础
tags: 
- java基础
---
```
import java.text.DecimalFormat;
import java.math.*;
import java.util.*;

public class Three {
	public static void main(String args[]) {
		DecimalFormat df = new DecimalFormat("0.0000000");
		Scanner sc = new Scanner(System.in);
		int r;
		double s;
		r = sc.nextInt();
		s = Math.PI * r *r;
		System.out.println(df.format(s));
	}
}

```

