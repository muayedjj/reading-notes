# Unit Tests and TDD
**Unit tests** are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want.

But **Test-Driven Development** is a strategy to think (and write!) tests first.

<br/>

## **Structure** 
**A structuring convention widely used is the AAA: Arrange, Act and Assert.**

1. Arrange: you need to organize the data needed to execute that piece of code (input).
2. Act: here you will execute the code being tested (exercise the behaviour).
3. ***Assert: after executing the code, you will check if the result (output) is the same as you were expecting.***

<br/>

## **The Cycle**

The cycle is made by three steps:
1. 🆘 Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)
2. ✅ Write the feature and make the test pass! (you can dance after that)
3. 🔵 Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy).[1][1]

<br/>

# The ***`__main__`*** script and modules
- ***A module is a file containing Python definitions and statements. The file name is the module name with the suffix .py appended.***
- We can test function by calling it.
But once we want to use that module by importing we **have to comment out** our call, or use a specific python 3 code. [2]
>>***`if __name__ == "__main__":`***
>>    `my_function()`
>> 
>>`import myscript`
>> 
>>`myscript.my_function()` 


# Recursion
## What is Recursion? 
The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called a recursive function. [3]

The most popular example of recursion is the calculation of the factorial. Mathematically the factorial is defined as: n! = n * (n-1)!

We use the factorial itself to define the factorial. Hence, this is a suitable case to write a recursive function. Let us expand the above definition for the calculation of the factorial value of 5 mathmaticaly.

    5! -->  the steps that we d like the following :

      5 X 4!
      5 X 4 X 3!
      5 X 4 X 3 X 2!
      5 X 4 X 3 X 2 X 1!
      5 X 4 X 3 X 2 X 1
     = 120



<br/>

## **Takeaways:**
- The greatest advantage about TDD is to craft the software design first. [1]
- Your code will be more reliable: after a change you can run your tests and be in peace. [1]

- Beginning may be hard — and that’s fine. You just need to practice!. [1]

- If the python interpreter is running that module (the source file) as the main program, it sets the special __name__ variable to have a value “__main__”. If this file is being imported from another module, __name__ will be set to the module’s name. Module’s name is available as value to __name__ global variable. [2]

- Advantages of using tha main script include:
    - Every Python module has it’s __name__ defined and if this is ‘__main__’, it implies that the module is being run standalone by the user and we can do corresponding appropriate actions.
    - If you import this script as a module in another script, the __name__ is set to the name of the script/module.
    - Python files can act as either reusable modules, or as standalone programs.
    - if __name__ == “main”: is used to execute some code only if the file was run directly, and not imported.



[1]: https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932
[2]: https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/
[3]: https://www.geeksforgeeks.org/recursion/

