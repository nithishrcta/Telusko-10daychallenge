# DAY - 1
## Recursion
A Function which is calling itself is known as Recursion  
  
Example : 

```
fun add(int n)
{
  if(n == 0) break;
  print(n);
  add(n-1);  // Recursion
}
```
## Factorial of a given number using Recursion
   The product of all positive integers less than or equal to a given positive integer and denoted by that integer and an exclamation point.
```
public class main{
    public static void main(String args[])
    {
        Scanner sn = new Scanner(System.in):
        int num = 0;
        num = sc.nextInt();
        int res = 0;
        res = fact(num);
        System.out.println(res);
    }
    public static int fact(int num)
    {
      if(num == 0 || num == 1)
      {
        return 1;
      }
      return num*fact(n-1);
    }
}

```
## Fibonacci Series
The Fibonacci sequence is a set of integers (the Fibonacci numbers) that starts with a zero, followed by a one, then by another one, and then by a series of steadily increasing numbers.
```
public class main{
    public static void main(String args[])
    {
        Scanner sn = new Scanner(System.in):
        int pos = 0;
        pos = sc.nextInt();
        int res = fib(num);
        System.out.println(res);
    }
    public static int fib(int pos)
    {
      if(pos == 0))
      {
        return 0;
      }
      if(pos == 1 || pos == 2)
      {
        return 1;
      }
      return fib(pos-1)+fact(pos-2);
    }
}

```


