# Functions

## The basics

### What is a function?

**_Function_** - a block of statements that perform a specific task.

Functions are useful because they allow us to repeat tasks or functions without having to rewrite code. This is the crux of modern programming. 

For example, when you use `printf`, this is not magic, it is a prewritten function that you get from the `stdio.h` library. 

> The `printf` function itself is about *2000* lines of code, which you would not want to write! 

By abstracting this functionality into a function, we can easily print something to the screen in a concise, and readable manner.

### Real life use-case

I could give you the standard example of a sum function but that's boring. I like to use GUI/graphics library's as examples. 

When creating a GUI application (i.e. any app on your computer), there are libraries that have simple function calls to do a lot of the background work for you.

For example, in a library called `QT`, I could call the `createWindow()` function, and it would run a bunch of background code to create a window for my application for me. I'm sure the code for that is immensly complex, and it allows me to focus on making my app, instead of understanding how to create an application window.

It is also useful because if I needed to create another window, I could just call the same function again. This allows us to *reuse* code instead of rewriting the same code over and over.

### Types of functions

**_Standard library functions_** - these are any functions that come from header files like `stdio.h` or `math.h`. These are written by really smart people who know how to write really efficient code for commonly used functions.

**_User defined functions_** - these are what you will be implementing in this class. They are functions that you define for your own programs.

## User Defined Functions

### Properites of functions

1. Functions can have *zero or more inputs* of varying types.
2. Functions only have *one output* of a single type.
3. Functions only accomplish one task (i.e. don't take input and then do calculations).

### Vocabulary

**_Function Declaration_** - The declaration goes at the **top** of your file under your `#include` and `#define` statements. The declaration tells the compiler (declares) the *Return Type*, *Function Name*, and *(Input) Parameters*.

**_Return Type_** - The data type of the value returned by the function

**_Function Name_** - The name of the function. Make sure this describes what the function does. (Ex. `getInput`, `calcSum`).

> You can optionally give names to the input variables, but this is not necessary _for the function declaration_.

**_Parameters_** - This is a list of variables that tells us how many variables we have, what type they are, their type..

**_Function Signature_** - The combination of the *function name* and the *parameter list*.

A function declaration can be shown in this generic form.

```c
#include <stdio.h>
#define PI 3.14

<returnType> simpleFunction(<inType> <optVarName>, <inType2> <optVarName2>, ...);

// main
```

> **Return Type** - returnType
> 
> **Function Name** - simpleFunction
> 
> **Parameters** - inType optVarName, inType2 optVarName2, ...
> 
> **Function Signature** - simpleFunction(\<inType\> \<optVarName\>, \<inType2\> \<optVarName2\>, ...)

For a more concrete example, a simple declaration for a function that takes and `int` and returns an `int` would look like this:

```c
#include <stdio.h>
#define PI 3.14

int simpleFunction(int <optVarName>);

// main
```

> **Return Type** - int
> 
> **Function Name** - simpleFunction
> 
> **Parameters** - int optVarName
> 
> **Function Signature** - simpleFunction(int \<optVarName\>)

> Notice that the function ***declaration*** does not contain any functionality, and also _ends in a semicolon_.

***

**_Function Definition_** - The definition contains a *Function Header*, and the *Function Body*, and it *defines* the behavior of the function. The function declaration will always go underneath main.

**_Function Header_** - The same thing as the function declartion, but includes variable names for the parameters in the parameter list.

**_Function Body_** - Contains a collection of statements that define what the function does. This is where all your logic will be.

So, if we used the example function above, the function definition would look something like this

```c
// main end

int simpleFunction(int inputVar) {
	// Calculations
	inputVar += 1;
	
	return inputVar;
}
```

> **Function Header** - int simpleFunction(int inputVariable)
> 
> **Function Body** - everything in the {...} brackets
>
> Notice that the function header _does NOT end in a semicolon_.

**_Function Call_** - This is the call to the function that tells your code to run the function.

It would look something like this (assuming the function is already defined):

```c
int main() {
	...
	result = simpleFunction(input);
	...
}
```

> Notice that the parameters in the function call just take a variable, but **DO NOT** annotate the type of the variable.

### Things that confuse students

1. Declarations don't need variable names, but I'd recommend it.
	> For example you can declare and define the function the following way:
	
   ```c
   int simpleFunction(int);
   
   // main
   
   int simpleFunction(int inputVar) { 
   	return inputVar + 1; 
   }
   ```
	> However, I'd recommend just keeping the variable name in the declaration
	
   ```c
   int simpleFunction(int inputVar);
   
   // main
   
   int simpleFunction(int inputVar) { 
   	return inputVar + 1; 
   }
   ```
  
2. A variable in a function with the same name as a variable in `main` is a completely different variable, i.e. they **DO NOT** affect each other. For example:
	
   ```c
   void changeX(int x);
   
   int main(void) {
      int x;
      
      x = 1;
      
      changeX(x); // cannot change the x in main
      
      // x still equals 1
      
      return 0;
   }
   
   void changeX(int x) { // This x is seperate from the one in main.
      // x equal 1
      
      x = 5; 
      
      // The value of x is changed in this function
      // to five, but this will not change the value
      // of x in main.
   }
   ```
   > You can see that the value of **x** changes only inside the `changeX` function, from 1 to 5. This is because a *copy* of **x** is passed to the function, and that value of 1 (from `main`) is manipulated using the local variable **x** in the `changeX` function.
   
   > If this seems complicated to you, you can always give different names to the function's variables, so you *know* they are different.
   
   ```c
   void changeX(int localX);
   
   int main(void) {
      int x;
      
      x = 1;
      
      changeX(x); // cannot change the x in main
      
      // x still equals 1
      
      return 0;
   }
   
   void changeX(int localX) { // localX recieves the value passed to it
      // localX equal 1
      
      localX = 5; 
      
      // The value of localX is changed in this function
      // to five, but this will not change the value
      // of x in main.
   }
   ```

3. You do not have to declare variables in the parameter list.

   > It is unnecessary, but more importantly **WRONG** to declare variables that are already in your parameters list. 
   
   > For example:
   
   ```c
   int simpleFunction(int a) {
      int a; // THIS IS WRONG
   }
   ```
   
   > It is wrong because the `int a` in the declarations has already declared that variable for the function (your compiler's essentially doing `int a = inputValue;` in the background already). So by declaring the variable again, you will confused the compiler and your program won't compile :)
   
4. `void` does not reutrn a value.

   > When using void as the return type for your function, either don't include a return statement, or just include a simple return. **DO NOT return 0, or any other value!**
   
	```c
	void exampleVoid1(/* doesn't matter */) {
	   // Some calculations
	}  // No return
	
	void exampleVoid2(/* doesn't matter */) {
	   // Some calculations
	   return;
	}
	
	void exampleVoid3(/* doesn't matter */) {
	   // Some calculations
	   return 0; // THIS IS WRONG, DON'T DO THIS!!!
	}
	```

5. I'm writing two functions, but they look almost exactly the same.

	> If you are writing two functions that look almost the same, but have slightly different functionality, there's most likely a way to combine them together.
	
	> For example:
	
	```c
	int addNums(int a, int b) {
		return a + b;
	}
	
	int subNums(int a, int b) {
		return a - b;
	}
	```
	
	> We could combine these functions by passing another parameter:
	
	```c
   # define ADD  1
   # define SUB -1
	
	int combNums(int a, int b, int sign);
	
	int main(void) {
		sum  = combNums(2, 2, ADD); // sum  = 4
		diff = combNums(2, 2, SUB); // diff = 0
	}
	
	int combNums(int a, int b, int sign) {
		return a + sign * b;
	}
	```
