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
