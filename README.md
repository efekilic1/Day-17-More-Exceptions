# Day-17-More-Exceptions
Day 17: More Exceptions patika.dev


<img width="920" alt="Ekran Resmi 2022-05-21 20 46 05" src="https://user-images.githubusercontent.com/105243448/169663398-bb3e77b2-7164-461b-b5f4-86778e5e6deb.png">



https://www.hackerrank.com/challenges/30-more-exceptions/problem


```
using System;

//Write your code here

class Calculator{
    public int power(int n, int p){
        
        if (n<0 || p<0){
            throw new Exception("n and p should be non-negative");
        }
        
        return (int)Math.Pow(n,p);
    }
    
}

class Solution{
    static void Main(String[] args){
        Calculator myCalculator=new  Calculator();
        int T=Int32.Parse(Console.ReadLine());
        while(T-->0){
            string[] num = Console.ReadLine().Split();
            int n = int.Parse(num[0]);
            int p = int.Parse(num[1]); 
            try{
                int ans=myCalculator.power(n,p);
                Console.WriteLine(ans);
            }
            catch(Exception e){
               Console.WriteLine(e.Message);

            }
        }
        
        
        
    }
}

```
