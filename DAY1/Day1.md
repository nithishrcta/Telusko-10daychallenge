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
## Factorial of a given num using Recursion

```
public class main{
    public static void main(String args[])
    {
        int num = 0;
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



