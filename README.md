# Return Values from Functions

Most functions, by default, return the value of undefined.
An example is the console.log() function.

If I run:
~~~
console.log('Hello');
~~~
The output in the console will be:
~~~
Hello
undefined
~~~

Because the console.log() function is built so as to not have the explicitly set return value, it gets the default return value of undefined.

A code implementation of console.log() which doesn't return the value of undefined:

~~~
function consoleLog(val) {
    console.log(val)
    return val
}
~~~

When you run the consoleLog() function:

~~~
consoleLog("Hello")
~~~

You get the following output:

~~~
Hello
'Hello'
~~~

The value is output in  the console and it is also returned. 

Why is this useful?

This is because you can use return values from one function inside another function.

Example: A function that returns a double of a number that it received:

~~~
function doubleIt(num) {
    return num * 2
}
~~~

Writing another function that builds an object with a specific value:

~~~
function objectMaker(val) {
    return {
        prop: val
    }
}
~~~

You can call the objectMaker() function with any value such as:

~~~
objectMaker(20);
~~~

The returned value will be an object with a single prop key set to 20:

~~~
{prop: 20}
~~~

Considering the following code:
~~~
doubleIt(10).toString()
~~~

The above code returns the number 20 as a string.

Combining the custom function calls:

~~~
objectMaker( doubleIt(100) );
~~~

This will now return the following value:

~~~
{prop: 200}
~~~

JavaScript allows one to use the return keyword as described above. You can have multiple function calls, returning data and manipulating values, based on whatever coding challenge.

Being able to return custom values is one of the foundations that makes functional programming possible.