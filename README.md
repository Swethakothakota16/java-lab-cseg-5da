# java-lab-cseg-5da
experiments
## Experiment 1
## Title 1a(Implement Default Primitive Datatype):
```
class  DefaultPrim
{
   byte Byte;
   short Short;
  int Int;
    long Long;
    float Float;
     double Double;
  char Char;
  boolean bool;
  public static void main(String[] args)
  {
    DefaultPrim dp=new  DefaultPrim();
    System.out.println("default byte is:"+dp.Byte);
    System.out.println("default short  is:"+ dp.Short);
    System.out.println("default int is:"+ dp.Int);
    System.out.println("default long is:"+ dp.Long);
    System.out.println("default float is:"+ dp.Float);
    System.out.println("default double is:"+ dp.Double);
    System.out.println("default char is:"+ dp.Char);
    System.out.println("default boolean is:"+ dp.bool);

    }
}
```
## output:
![output for 1a](https://github.com/Swethakothakota16/java-lab-cseg-5da/blob/27894ba7f8495fc905382b7df84f45d62c482ce3/1a.png)
## Title 1b(Quadratic Equation):
```
import java.util.Scanner;
class Quadraticeqn
{
  public static void main(String[] args)
  {
   Scanner sc =new Scanner(System.in);
   System.out.println("enter value of a:");
   double a= sc.nextDouble();
    System.out.println("enter value of b:");
       double b= sc.nextDouble();
      System.out.println("enter value of c:");
     double  c= sc.nextDouble();
     double D=b*b-4*a*c;
     if(D>0)
     {
        System.out.println("roots are real and distinct ");
        double root1=(-b+Math.sqrt(D))/2*a;
        double root2=(-b-Math.sqrt(D))/2*a;
        System.out.println("root1:"+root1);
        System.out.println("root2:"+root2);
        }
        else if(D==0)
        {
        System.out.println("roots are real and equal");
        double root=-b/(2*a);
        System.out.println("root:"+root);
        }

        else{
        System.out.println("roots are imaginary ");
        double real=-b/(2*a);
        double imag=Math.sqrt(-D)/(2*a);
       System.out.println("root1:"+real +"+"+imag+"i");
       System.out.println("root2:"+real +"-"+imag+"i");
       }
       sc.close();
     }
}
```
## output:
![output for 1b](https://github.com/Swethakothakota16/java-lab-cseg-5da/blob/954a4159ba8ff6d9c7c8ce76d31044a9d0624c74/1b.png)
## Experiment 2
## Title 2a(Class Mechanism):
```
class Rectangle {
    double length;
    double breadth;
    double area()
    {
        return length * breadth;
    }
   double perimeter()
    {
     return 2*(length+breadth);
    }
}

class main {
    public static void main(String[] args) {


        Rectangle rect = new Rectangle();
        rect.length=6;
        rect.breadth=12;
        double area=rect.area();
        double  perimeter=rect.perimeter();
        System.out.println("Area of rectangle : " + area);
        System.out.println("perimeter of rectangle : " + perimeter);
    }
}
```
## output:
![output for 1b](https://github.com/Swethakothakota16/java-lab-cseg-5da/blob/3b4766284bbee7c11caba4e86677fa95c2cd0e7b/2a.png)
## Title 2b(Method Overload):
```
class main {
    public static void main(String[] args) {

        sum s = new sum();

        System.out.println("Sum of 2 integers: " + s.sum(30, 40));
        System.out.println("Sum of 3 integers: " + s.sum(20, 50, 70));
        System.out.println("Sum of real numbers: " + s.sum(20.45, 22.56));
    }
}
class sum {

    int sum(int a, int b) {
        return a + b;
    }

    int sum(int a, int b, int c) {
        return a + b + c;
    }

    double sum(double a, double b) {
        return a + b;
    }
}
```
## output:
![output for 1b]

## Title 2c(Implement Constructor):
```
class Student{
    String sname;
   int sage;
   double smarks;
   Student(String name,int age,double marks)//constructor
   {
     sname=name;
     sage=age;
     smarks=marks;
    }
     void display()
    {
      System.out.println("stu name:"+sname);
      System.out.println("stu age:"+sage);
      System.out.println("stu marks:"+smarks);
    }

}



class main
{
  public static void main(String[] args)
   {

    Student stu=new Student("swetha",19,99);
    stu.display();
   }
}
```
## Additional Experiment 2:
```
import java.util.Scanner;

class Fibonacci {

    int firstnumber;
    int secondnumber;
    int thirdnumber;
    int sum;
    int sizeOfFibsequence;

    // Constructor
    Fibonacci(int size) {
        firstnumber = 0;
        secondnumber = 1;
        thirdnumber = 0;
        sum = 0;
        sizeOfFibsequence = size;
    }

    void generateFibsequence() {

        while (sizeOfFibsequence > 0) {

            if (sizeOfFibsequence == 1)
                System.out.print(firstnumber + ".");
            else
                System.out.print(firstnumber + ", ");

            sizeOfFibsequence--;

            sum += firstnumber;

            thirdnumber = firstnumber + secondnumber;
            firstnumber = secondnumber;
            secondnumber = thirdnumber;
        }
    }

    int getFibsum() {
        return sum;
    }
}

public class Main {
    public static void main(String[] args) {

        System.out.print("Enter size of FibSequence: ");
        Scanner sc = new Scanner(System.in);

        int size = sc.nextInt();

        if (size > 0) {

            Fibonacci fib = new Fibonacci(size);

            System.out.println("\nFibonacci Series are:");
            fib.generateFibsequence();

            System.out.println("\nThe sum of Fibonacci Series: " + fib.getFibsum());
        } else {
            System.out.println("Fibonacci Sequence & sum cannot be calculated");
        }

        sc.close();
    }
}
```
## output:
![output for Additional Experiment](https://github.com/Swethakothakota16/java-lab-cseg-5da/blob/e15fa05e021be60faed590c8c04b7fd18c0d69e6/addexp2.png)

## Title 3a(Constructor Overloading):
```
class Student {
    String name;
    int age;
    double marks;

    Student() {
    }

    Student(String name, int age, double marks) {
        this.name = name;
        this.age = age;
        this.marks = marks;
    }

    void display() {
        System.out.println("name : " + name);
        System.out.println("age : " + age);
        System.out.println("marks : " + marks);
    }
}

class Main {
    public static void main(String args[]) {
        Student std1 = new Student();
        std1.display();

        Student std2 = new Student("Alice", 19, 92);
        std2.display();
    }
}
```
## Title 3b(Binary Search):
```
import java.util.Scanner;

class Binarysearch {
    int list[];
    int size;

    Binarysearch(int size) {
        list = new int[size];
        this.size = size;
    }

    void SetList() {
        Scanner sc = new Scanner(System.in);
        System.out.println("enter the list items in ascending order");
        for (int i = 0; i < size; i++) {
            System.out.println("enter value of " + (i + 1) + ":");
            list[i] = sc.nextInt();
        }
    }

    void GetList() {
        System.out.println("list elements :");
        for (int i = 0; i < size; i++) {
            System.out.println(list[i] + " ");
        }
        System.out.println();
    }

    int Binarysearch(int key) {
        int low = 0;
        int high = size - 1;

        while (low <= high) {
            int mid = (low + high) / 2;

            if (list[mid] == key) {
                return mid;
            } else if (list[mid] < key) {
                low = mid + 1;
            } else {
                high = mid - 1;
            }
        }
        return -1;
    }
}

import java.util.Scanner;
class Main {
    public static void main(String args[]) {

        Scanner sc = new Scanner(System.in);

        System.out.println("Enter size of list:");
        int size = sc.nextInt();

        Binarysearch bs = new Binarysearch(size);

        bs.SetList();
        bs.GetList();

        System.out.println("Enter element to search:");
        int key = sc.nextInt();

        int result = bs.Binarysearch(key);

        if (result == -1) {
            System.out.println("Element not found.");
        } else {
            System.out.println("Element found at position: " + (result + 1));
        }
    }
}
```
## Title 3c(bubble sort):
```

class BubbleSort {
    void BubbleSort(int arr[]) {
        int n = arr.length;

        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j + 1];
                    arr[j + 1] = arr[j];
                    arr[j] = temp;
                }
            }
        }
    }
}
import java.util.Scanner;

class Main {
    public static void main(String args[]) {

        System.out.println("enter size of array");
        Scanner sc = new Scanner(System.in);

        int size = sc.nextInt();
        int integer[] = new int[size];

        for (int i = 0; i < size; i++) {
            System.out.println("enter value of integer at index " + (i + 1) + ":");
            integer[i] = sc.nextInt();
        }

        BubbleSort bs = new BubbleSort();
        bs.BubbleSort(integer);

        System.out.println("sorted array");

        for (int i = 0; i < size; i++) {
            System.out.println(integer[i] + " ");
            System.out.println("\b\b.");
        }
    }
}
```
## Title 4a(Single Inheritance):
```
class person {
    String name;
    int age;

    person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void displaypersondetails() {
        System.out.println("Name : " + name);
        System.out.println("Age : " + age);
    }
}

class Employee extends person {

    double annualsalary;
    int yearofjoining;
    String nationalInsuranceNumber;

    Employee(String name, int age, double annualsalary,
             int yearofjoining, String nationalInsuranceNumber) {

        super(name, age);
        this.annualsalary = annualsalary;
        this.yearofjoining = yearofjoining;
        this.nationalInsuranceNumber = nationalInsuranceNumber;
    }

    void displayEmployeeDetails() {
        displaypersondetails();
        System.out.println("Annual salary : " + annualsalary);
        System.out.println("Year of joining : " + yearofjoining);
        System.out.println("National Insurance Number : " + nationalInsuranceNumber);
    }
}

class TestEmployee {
    public static void main(String args[]) {

        Employee emp = new Employee("Alice", 19, 60000,
                                    2022, "NI123456A");

        emp.displayEmployeeDetails();
    }
}
```

## Title 4b(Multi-level Inheritance):
```
class Bicycle {
    String pedalType;

    void showBicycleInfo() {
        System.out.println("This is a bicycle with pedals");
        System.out.println("pedalType: " + pedalType);
    }
}

class MotorBike extends Bicycle {
    int engineCapacity;

    void showMotorBikeInfo() {
        System.out.println("This motorbike has an engine");
        System.out.println("engine capacity: " + engineCapacity + " cc");
    }
}

class ElectricBike extends MotorBike {
    int batteryCapacity;

    void showElectricBikeInfo() {
        System.out.println("This electric bike has an electric motor & battery");
        System.out.println("Battery capacity: " + batteryCapacity + " cc");
    }
}

public class TestVehicle {
    public static void main(String args[]) {
        ElectricBike eBike = new ElectricBike();

        eBike.pedalType = "Standard pedals";
        eBike.engineCapacity = 250;
        eBike.batteryCapacity = 500;

        eBike.showBicycleInfo();
        eBike.showMotorBikeInfo();
        eBike.showElectricBikeInfo();
    }
}
```
## Title 4c(To construct Abstract class):

```
abstract class Figure {
    double dim1;
    double dim2;

    Figure(double dim1, double dim2) {
        this.dim1 = dim1;
        this.dim2 = dim2;
    }

    abstract double area();
}

class Rectangle extends Figure {

    Rectangle(double length, double breadth) {
        super(length, breadth);
    }

    double area() {
        double result = dim1 * dim2;
        return result;
    }
}

class Triangle extends Figure {

    Triangle(double base, double height) {
        super(base, height);
    }

    double area() {
        double result = 0.5 * dim1 * dim2;
        return result;
    }
}

public class TestFigure {

    public static void main(String args[]) {

        Figure f1 = new Rectangle(23.4, 14.5);
        Figure f2 = new Triangle(12.3, 15.6);

        System.out.println("Area of Rectangle = " + f1.area());
        System.out.println("Area of Triangle = " + f2.area());
    }
}

```
## Title 5a(Implement Interface):
```
class Bubblesort implements Sortable
{
  public  void sort(int[] arr)
  {
    int size=arr.length;
    int temp=0;
    for(int i=0;i<size-1;i++)
    {
     for(int j=0;j<size-i-1;j++)
     {
        if(arr[j]>arr[j+1])
        {
         temp=arr[j];
        arr[j]=arr[j+1];
        arr[j+1]=temp;
        }
     }

   }
 }
}
class Selectionsort implements Sortable
{
  public void sort(int[] arr)
  {
    int size=arr.length;
     int Minindex=0;
     int min;
     for(int i=0;i<size;i++)
     {
      min=arr[i];
     for(int j=i+1;j<size;j++)
     {
      if(min>arr[j])
      {
       min=arr[j];
       Minindex=j;
      }

    }
   for(int j=Minindex;j>i;j--)
   {
     arr[j]=arr[j-1];
   }
        arr[i]=min;
  }
}
}
interface Sortable
{
  void sort(int[] arr);
}
class Testsort
{
  static void display(int arr[])
  {
   for(int ele:arr)
   {
        System.out.print(ele +" ");
   }
   System.out.println("\b\b.");
  }
public static void main(String[] args)
{
 int arr[]={9,7,4,3,6,8};
 int bar[]={8,6,3,4,7,9};
 Sortable s;
 s=new Bubblesort();
 s.sort(arr);
 System.out.println("after sorting");
 display(arr);
 s=new Selectionsort();
 s.sort(bar);
 System.out.println("after sorting");
 display(bar);
 }
}


```
## Title 5b(Runtime Polymorphism):

```
class vehicle{
    void run()
{
        System.out.println("vehicle is running");
}
}
class car extends vehicle
{
        void run()
        {
        System.out.println("car is running");
        }
}
class bike extends vehicle
{
 void run()
{
  System.out.println("bike is running");
 }
}
class poly
{
   public static void main(String[] args)
   {
        vehicle v;
        v=new car();
        v.run();
        v=new bike();
        v.run();
        v=new vehicle();
        v.run();
        }
}
```
## Title 5c(StringBuffer):
```

class Deletechar
{

 public static void main(String[] args)
{
 StringBuffer sb=new StringBuffer("java programming");
  System.out.println(sb);
 sb.deleteCharAt(4);
  System.out.println(sb);
 sb.delete(0,4);
 System.out.println(sb);
 }
}

```
## Title 6a(Exception Handling):

```
import java.util.Scanner;

class ArrayIndexException {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter size of array: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter " + n + " elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        try {
            System.out.print("Enter index to access: ");
            int index = sc.nextInt();
            System.out.println("Element at index " + index + " is " + arr[index]);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array index out of bounds!");
        }

        sc.close();
    }
}
```


## Title 6b(MultipleCatch):
```
import java.util.Scanner;

class MultipleCatch {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int[] arr = {10, 20, 30, 40, 50};

        try {
            System.out.print("Enter first number: ");
            int a = sc.nextInt();

            System.out.print("Enter second number: ");
            int b = sc.nextInt();

            int result = a / b;
            System.out.println("Result = " + result);

            System.out.print("Enter index to access array: ");
            int index = sc.nextInt();
            System.out.println("Element = " + arr[index]);
        }
        catch (ArithmeticException e) {
            System.out.println("Arithmetic Exception occurred");
        }
        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array Index Out Of Bounds Exception occurred");
        }
        catch (Exception e) {
            System.out.println("Some other exception occurred");
        }

        sc.close();
        System.out.println("Program continues...");
    }
}
```

## Title 6c(Built-in Exception):
```

import java.util.Scanner;

class BuiltInException {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        try {
            System.out.print("Enter a number to divide 100: ");
            int n = sc.nextInt();

            int result = 100 / n;
            System.out.println("Result = " + result);

            int[] arr = new int[3];
            System.out.println(arr[5]);
        }
        catch (ArithmeticException e) {
            System.out.println("Arithmetic Exception occurred");
        }
        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array Index Out Of Bounds Exception occurred");
        }
        catch (Exception e) {
            System.out.println("General Exception occurred");
        }
        finally {
            System.out.println("Program continues...");
            sc.close();
        }
    }
}

```
## Title 7a(User Defined Exception):
```
class InvalidCountryException extends Exception {

    InvalidCountryException() {
        super();
    }

    InvalidCountryException(String message) {
        super(message);
    }
}

class UserRegistration {

    void registerUser(String username, String userCountry)
            throws InvalidCountryException {

        if (!userCountry.equals("India")) {
            throw new InvalidCountryException(
                    "User Outside India cannot be registered");
        } else {
            System.out.println("User Registration Done Successfully");
        }
    }
}

public class Main {

    public static void main(String[] args) {

        UserRegistration ur = new UserRegistration();

        try {
            ur.registerUser("Swetha", "USP");
        } catch (InvalidCountryException e) {
            System.out.println(e.getMessage());
        }
    }
}
```
## Title 7b(Thread class):

```
class GoodMorningThread extends Thread {
    public void run() {
        for (int i = 0; i < 10; i++) {
            System.out.println("Thread 1: Good Morning");
            try {
                Thread.sleep(1000); // 1 second
            } catch (InterruptedException e) {
                System.out.println("Exception: " + e);
            }
        }
    }
}

class HelloThread extends Thread {
    public void run() {
        for (int i = 0; i < 10; i++) {
            System.out.println("Thread 2: Hello");
            try {
                Thread.sleep(2000); // 2 seconds
            } catch (InterruptedException e) {
                System.out.println("Exception: " + e);
            }
        }
    }
}

class WelcomeThread extends Thread {
    public void run() {
        for (int i = 0; i < 10; i++) {
            System.out.println("Thread 3: Welcome");
            try {
                Thread.sleep(3000); // 3 seconds
            } catch (InterruptedException e) {
                System.out.println("Exception: " + e);
            }
        }
    }
}

public class Testthread {
    public static void main(String[] args) {
        GoodMorningThread t1 = new GoodMorningThread();
        HelloThread t2 = new HelloThread();
        WelcomeThread t3 = new WelcomeThread();

        t1.start();
        t2.start();
        t3.start();
    }
}
```
## Title 7c(is Alive and join()):

```
class LongRunningTask extends Thread {

    public void run() {
        System.out.println("Long running task started");

        for (int i = 0; i < 5; i++) {
            System.out.println("Working... " + i + " iteration");

            try {
                Thread.sleep(1000);
            } catch (Exception e) {
                System.out.println(e);
            }
        }

        System.out.println("Long running task completed");
    }
}

class ThreadDemo {

    public static void main(String[] args) throws Exception {

        LongRunningTask task1 = new LongRunningTask();

        System.out.println("Before starting task1: " + task1.isAlive());

        task1.start();

        System.out.println("After starting task1: " + task1.isAlive());

        System.out.println("Main thread waiting for task1 to complete using join operation");

        task1.join();   // Main thread waits here until task1 finishes

        System.out.println("After join: " + task1.isAlive());

        System.out.println("Main thread continues after task1 is completed");
    }
}

```
## Title 8a(Daemon Threads):

```
class DaemonThread extends Thread {

    public void run() {
        while (true) {
              System.out.println("Daemon Thread is running");

            try {
                Thread.sleep(500);
            } catch (Exception e) {
                System.out.println("Exception occurred");
            }
        }
    }
}

class UserThread extends Thread {

    public void run() {
        for (int i = 1; i <= 5; i++) {
            System.out.println("User thread iteration: " + i);
            try {
                Thread.sleep(1000);
            } catch (Exception e) {
                System.out.println("Exception occurred");
            }
        }
    }
}

public class TestThreads {

    public static void main(String[] args) {

        DaemonThread dt = new DaemonThread();
        UserThread ut = new UserThread();

        dt.setDaemon(true);

        dt.start();
        ut.start();
    }
}

```

## Title 8b(producerConsumer):

```

class SharedBuffer {

    private int[] buffer;
    private int count = 0;
    private int in = 0;
    private int out = 0;

    SharedBuffer(int size) {
        buffer = new int[size];
    }

    synchronized void produce(int item) {
        while (count == buffer.length) {
            try {
                wait();
            } catch (InterruptedException e) {
                System.out.println(e);
            }
        }

        buffer[in] = item;
        in = (in + 1) % buffer.length;
        count++;

        notify();
    }

    synchronized int consume() throws InterruptedException {
        while (count == 0) {
            wait();
        }

        int item = buffer[out];
        out = (out + 1) % buffer.length;
        count--;

        notify();
        return item;
    }
}

class Producer extends Thread {

    private SharedBuffer buffer;

    Producer(SharedBuffer buffer) {
        this.buffer = buffer;
    }

    public void run() {
        for (int i = 1; i <= 10; i++) {
            buffer.produce(i);
            System.out.println("Produced: " + i);
        }
    }
}

class Consumer extends Thread {

    private SharedBuffer buffer;

    Consumer(SharedBuffer buffer) {
        this.buffer = buffer;
    }

    public void run() {
        try {
            for (int i = 1; i <= 10; i++) {
                int item = buffer.consume();
                System.out.println("Consumed item: " + item);
            }
        } catch (InterruptedException e) {
            System.out.println(e);
        }
    }
}

public class ProducerConsumerDemo {

    public static void main(String[] args) {

        SharedBuffer buffer = new SharedBuffer(5);

        Producer p = new Producer(buffer);
        Consumer c = new Consumer(buffer);

        p.start();
        c.start();
    }
}

```


