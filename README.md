# hello_world
About Me.
import java.util.Scanner;

public class HelloThere{
  public static void main(final String[] args) {
      // Scanner kb = new Scanner (System.in);
      System.out.println("Hello There. We are now going to say hello to you however many times you would like...Enter here: ");
      final int num = getInt();
      recursiveHello(num);
  }

  public static void recursiveHello(final int ntimes) {
      if (ntimes > 0) {
          System.out.println("Hello there! I am fromt the recursive method...");
          recursiveHello(ntimes - 1);
      }
  }

  public static int getInt() {
      final Scanner kb = new Scanner(System.in);
      while(!kb.hasNextInt()){
          System.out.println("Please enter an integer...");
          kb.next();
      }
      return kb.nextInt();
  }
}
