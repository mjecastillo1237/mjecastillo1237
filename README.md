package activity1;
import java.util.Scanner;
public class activity1 {
	 public static void main(String[] args) {
	        Scanner sc = new Scanner(System.in);
	        System.out.print("String input: ");
	        validateString(sc.next());
	    }

	    public static void validateString(String input) {
	        boolean isValid = input.length() >= 8 && input.matches("^[A-Za-z0-9]+$");

	        int count = 0;
	        for (int i = 0; i < input.length(); i++) {
	            if (Character.isDigit(input.charAt(i))) {
	                count++;
	            }

	        }

	        String result;
	        if (count >=3 && isValid) {
	            result = "valid";
	        } else {
	            result = "invalid";
	        }
	        System.out.println("String is " + result);
	    }

}
