# Array-Challenge
Hackerrank Problem Solution in java
import java.util.Scanner;

public class ArrayChallenge {
	static String arrayChallenge(int ar[]) {
		int Fmax = 0;
		int Smax = 0;
		if(ar[0] > ar[1]) {
			Fmax = ar[0];
			Smax = ar[1];
		}
		else {
			Fmax = ar[1];
			Smax = ar[0];
		}
		for (int i = 0; i < ar.length; i++) {
			if (ar[i] > Fmax) {
				Smax = Fmax;
				Fmax = ar[i];
			}
		}
		int sum = 0;
		for (int i = 0; i < ar.length; i++) {
			sum = sum + ar[i];
		}
			sum = sum * 2;
			
			if ((Fmax * Smax) > sum) {
				return "True";
			}
			else {
				return "False";
			}
		
	}

	public static void main(String[] args) {
       Scanner scan = new Scanner(System.in);
	int n = scan.nextInt();
	int ar[] = new int[n];
	for (int i = 0; i < ar.length; i++) {
		ar[i] = scan.nextInt();
	}
	
	System.out.println(arrayChallenge(ar));
	}

}
