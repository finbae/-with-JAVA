# -with-JAVA
## 가위바위보 게임 만들기

```
package scissors;
import java.util.Random;
import java.util.Scanner;

public class paper {
	public static void main(String[]args) {
		System.out.println("가위바위보를 하자!");
		System.out.println("안내면 진다, 가위바위보!");
		
		Scanner scanner = new Scanner(System.in);
		System.out.print("무엇을 내시겠습니까?: ");
		String value = scanner.next();
		
		System.out.println("당신은 "+value+"를 냈습니다.");
		
		scanner.close();
		
		int data = 0;
		Random random = new Random();
		data = random.nextInt(3)+1;
//		System.out.println("결과는 : "+data);
		
		String computer = "";
		if (data == 1) {
			computer = "가위";
		} else if (data == 2) {
			computer = "바위";
		} else {
			computer = "보";
		}
		System.out.println("컴퓨터는 "+computer);
		
		String answer = "";
		if ((data == 1 && value.equals("가위"))||(data == 2 && value.equals("바위"))||(data == 3 && value.equals("보"))) {
			System.out.println("비겼어요!");
		} else if ((data == 1 && value.equals("보"))||(data == 2 && value.equals("가위"))||(data == 3 && value.equals("바위"))) {
			System.out.println("컴퓨터가 이겼어요!");
		} else {
			System.out.println("당신이 이겼어요!");
		}
	}

} 
