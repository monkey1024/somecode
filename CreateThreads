/*
    测试看能创建多少线程
*/
public class CreateThreads {
    private static Object obj = new Object();
    private static int count = 0;

    public static void main(String[] args) {
        for (; ; ) {
            new Thread(() -> {
                synchronized (obj) {
                    count += 1;
                    System.err.println("创建线程" + count);
                }
                for (; ; ) {
                    try {
                        Thread.sleep(1000);
                    } catch (Exception e) {
                        System.err.println(e);
                    }
                }
            }
            ).start();
        }
    }
}
