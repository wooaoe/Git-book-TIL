# Algorithm
👩‍💻 알고리즘 문제 풀이
  # Baekjoon # 2581번 # 1929번 소수 구하기 문제
  
```java
package com.baekjoon;

import java.util.Scanner;

public class Solution {

	public void BaekTest() {
		
		Scanner sc = new Scanner(System.in);
		System.out.print("M : ");
		int M = sc.nextInt();
		System.out.print("N : ");
		int N = sc.nextInt();

		int sum = 0;
		int min = 10000;
		int cnt = 0;

		if (M > N) {
			System.out.println("M은 N보다 작거나 같아야 합니다.");
		} else {
			if (M > 0 && M <= 10000 && N > 0 && N <= 10000) {
				for (int i = M; i <= N; i++) {
					for (int j = 2; j < i; j++) {
						if (i % j == 0) {
							cnt++;
						}
					}
					if (cnt == 0) {
						sum += i;
						if (min > i) {
							min = i;
						}
					}
					cnt = 0;
				}
				if (sum == 0) {
					System.out.println(-1);
				}
				System.out.println(sum);
				System.out.println(min);
			}

		}

	}
}

```
