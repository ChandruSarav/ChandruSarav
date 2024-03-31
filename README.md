import java.util.Scanner;
class NumberNames {
public static void main(String[] args) {
Scanner scanner = new Scanner(System.in);
System.out.print("Enter the number: ");
int number = scanner.nextInt();
scanner.close();
if (number < 0) {

System.out.println("Invalid number");

return;

}

printNumberNames(number);

}

private static void printNumberNames(int number) {

String[] numbers = {"zero", "one", "two", "three", "four", "five", "six",

"seven", "eight", "nine"};

if (number != 0) {

int length = (int)(Math.log10(number) + 1);

for (int i = length; i > 0; i--) {

int divisor = (int)Math.pow(10, i - 1);

int digit = number / divisor;

number = number % divisor;

System.out.print(numbers[digit] + " ");

}

} else {

System.out.println(numbers[0]);

}

}

}
