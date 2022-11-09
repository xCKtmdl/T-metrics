# T-metrics Technical Interview

The first technical interview will consist of questions like this:

```
What is the static keyword?

What is a static class?

What is a static method?

What is an abstract class?

What is the difference between an abstract class an interface?

What makes an abstract class more useful than an interface?
A: If you don't like something in a abstract class you can override it.

What is Lipsuv principle?
What is Single Responsibility principle?
(be able to explain SOLID)

What is the private keyword?

What is the protected keyword?

What is a deadlock?

He will ask about the UI thread and how to lock the GUI in WinForms applications.

What is the sealed keyword?

What is a Dictionary and why is it useful?

What is MVC and why do people want to use it?
(be able to explain concept of routes and controller and what a Model is,
 how it gets passed to the View etc
 I used the example of a Product/Detail/{id} page for a store website)

What is a singleton?

What is a INNER JOIN (SQL)?
Basically contrast with a left join.

What is an anonymous method?
It's a method without a name, usually invoked with parentheses and arrow notation such as
await Task.Run(() => myTask.MyAsync(1, ConsoleColor.Red));

What is the return type of an anonymous method?
It is inferred by the return statement in the code block.
```

Basically questions about GoF design patterns, and SOLID. Also some specific
questions pertaining to how UI in WinForms works because that is one of their
primary applications.

For the second technical interview, T-metrics uses a REPL code exercise site
similar to leetcode, hackerrank, etc.

The site they use is [codewars](https://www.codewars.com/).

## You're a square!
kyu 7

A square of squares
You like building blocks. You especially like building blocks that are squares. And what you even like more, is to arrange them into a square of square building blocks!

However, sometimes, you can't arrange them into a square. Instead, you end up with an ordinary rectangle! Those blasted things! If you just had a way to know, whether you're currently working in vain… Wait! That's it! You just have to check if your number of building blocks is a perfect square.


Task
Given an integral number, determine if it's a square number:

"In mathematics, a square number or perfect square is an integer that is the square of an integer; in other words, it is the product of some integer with itself."

The tests will always use some integral number, so don't worry about that in dynamic typed languages.

Examples
```
-1  =>  false
 0  =>  true
 3  =>  false
 4  =>  true
25  =>  true
26  =>  false
```

```csharp
        public static bool IsSquare(int n)
        {
            bool retval = false;
            try
            {
                double sqrt = Math.Sqrt(n);
                var canParse = Int32.Parse(sqrt.ToString());

                // will only be set true if the square root
                // is an integer
                // otherwise it will throw an Exception
                retval = true;
            }
            catch 
            {
               return retval;
            }
            return retval;
            

        }
```