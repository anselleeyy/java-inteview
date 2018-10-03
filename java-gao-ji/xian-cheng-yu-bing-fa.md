---
description: Thread
---

# 线程与并发

## 创建线程的几种方法

### Thread

1. 创建Thread类的子类，覆盖run方法，run方法中执行的内容就是线程执行的内容
2. 创建子类的实例
3. 调用实例的 run 方法，启动线程

```javascript
public class ThreadTest extends Thread {
    @Override
    public void run () {
        System.out.println("OK");
    }
}

public class Main {
    public static void main (String[] args) {
        ThreadTest threadTest = new ThreadTest();
        threadTest.start();
    }
}
```

### Runnable

1. 创建 Runnable 接口的实现类，覆盖run方法，run方法中执行的内容就是线程执行的内容
2. 创建实现类的实例，用这个实例作为Thread的构造器参数创建Thread实例
3. 调用 Thread 实例的 run 方法，从而启动线程

```javascript
public class ThreadTest implements Runnable {
    @Override
    public void run () {
        System.out.println("OK");
    }
}

public class Main {
    public static void main (String[] args) {
        Thread thread = new Thread(new ThreadTest());
        thread.start();
    }
}
```

### Callable

> Callable接口会返回范型V结果，比如我们想让子线程去计算从1加到100，并把算出的结果返回到主线程

```javascript
public class ThreadTest implements Callable {
    @Override
    public Integer call() throws Exception {
        System.out.println("Thread starts");
        Thread.sleep(1000);
        int sum = 0;
        for (int i = 0; i <= 100; i++) {
            sum += i;
        }
        System.out.println("Thread returns");
        return sum;
    }
}

public class Main {
    public static void main(String[] args) {
        ThreadTest threadTest = new ThreadTest();
        FutureTask<Integer> futureTask = new FutureTask<>(threadTest);
        Thread thread = new Thread(futureTask);
        thread.start();

        try {
            System.out.println("before futureTask.get()");
            System.out.println("sum:" + futureTask.get());
            System.out.println("after futureTask.get()");
        } catch (InterruptedException e) {
            e.printStackTrace();
        } catch (ExecutionException e) {
            e.printStackTrace();
        }
    }
}
```

> 主线程调用 futureTask.get\(\) 方法时阻塞主线程，然后 Callable 内部开始执行，并返回运算结果，此时futureTask.get\(\) 得到结果，主线程恢复运行；并且与Runnable接口相比，Callable有返回结构，会抛出异常

_PS:  启动线程需要调用Thread.start\(\)，调用Thread.run\(\)只会执行run方法，不会创建新线程_

## Java 中线程的几种状态

### NEW（新建）

> Thread state for a thread which has not yet started
>
> 创建后还没有启动的线程

### RUNNABLE（可运行）

> Thread state for a runnable thread
>
> 可运行的线程。（调用start\(\)后，线程可能正在运行，也可能正在等待CPU调度，都属于RUNNABLE状态）

### BLOCKED（阻塞）

> Thread state for a thread blocked waiting for a monitor lock
>
> 当线程尝试进入synchronized块/方法时，锁被其他线程占有，当前线程就会被阻塞

### WAITING（等待）

> 等待的线程，需要被其他线程唤醒，不会被分配CPU时间的线程，这种状态通常是指一个线程拥有对象锁后进入到相应的代码区域后，调用相应的“锁对象”的wait\(\)方法操作后产生的一种结果Thread state for a waiting thread

