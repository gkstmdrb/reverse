# reverse

### 문제
![image](https://github.com/gkstmdrb/reverse/assets/114748816/d4501c47-f12d-48d2-bee9-9f43bfbdf488)
### 분석
T 변수에는 총 case 수를 입력 받는다. <br>
T번 반복하면서 수를 입력받고, 해당 수와 그 수를 뒤집은 값을 합한 결과를 구한다. <br>
결과값과 뒤집은 수가 같은지 비교를 한다. <br><br> 

### 설계
1. case 수 입력 받기
2. case 수 만큼 반복	
	1. 수 받기
	2. 입력 받은 수 + 뒤집은 수
	3. 앞뒤가 똑같은지 비교 후 출력

### 구현

``` java
	public static void main(String[] args) {
		
		        Scanner scanner = new Scanner(System.in);
		        
		        int T = scanner.nextInt();      // case 수 입력 받기
		        
		        for (int i = 0; i < T; i++) {		// case 수 만큼 반복
		        	int num = scanner.nextInt();	// 수 받기
		        	int result = num + reverseDigits(num);	// 입력 받은 수 + 뒤집은 수

		        	System.out.println(result == reverseDigits(result) ? "YES" : "NO");	// 앞뒤가 똑같은지 비교 후 출력
		        }
		    }
	
	public static int reverseDigits(int num) {
		int reversedNumber = 0;
		while (num != 0) {
			int digit = num % 10;
			reversedNumber = reversedNumber * 10 + digit;
			num /= 10;
		} 
		return reversedNumber;
	}	

```
