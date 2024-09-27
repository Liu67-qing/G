import java.util.Random;
import java.util.Scanner;

class GuessGame {
        public static void main(String[] args) {
                Random random = new Random();
                int targetNumber = random.nextInt(100) + 1;
                int attempts = 0;
                Scanner scanner = new Scanner(System.in);

                System.out.println("欢迎来到猜数字游戏！");
                System.out.println("我已经想好了一个 1 到 100 之间的数字，你来猜猜看。");

                while (true) {
                        System.out.print("请输入你的猜测：");
                        int guess = scanner.nextInt();
                        attempts++;

                        if (guess == targetNumber) {
                                System.out.println("恭喜你，猜对了！你用了 " + attempts + " 次尝试。");
                                break;
                        } else if (guess < targetNumber) {
                                System.out.println("你的猜测小了。");
                        } else {
                                System.out.println("你的猜测大了。");
                        }
                }

                scanner.close();
        }
}
