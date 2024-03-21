# What is Recursion in Java Script?
## Recursion is like a function that keeps calling itself. When a function does this, it's called a recursievly function. But, there is a rule it has to follow: it must have a way to stop calling itself, or it will go on forever. This stopping rule is called the base case.

#### ___Что такое рекурсия в Java Script?___
 #### ___Рекурсия - это как функция, которая продолжает вызывать сама себя. Когда функция делает это, она называется рекурсивной. Но есть правило, которому она должна следовать: у нее должен быть способ прекратить вызов самой себя, иначе она будет продолжаться вечно. Это правило остановки называется базовым случаем.___

 ___

 ## A Recursive function must have condition to stop itself. Otherwise the function is called indefinitely.
 ## Once the condition is met, the function stops calling itself. This is called the base condition

 #### ___(Рекурсивная функция должна иметь условие для самоостановки. В противном случае функция будет вызываться бесконечно. Как только условие выполняется, функция перестает вызывать себя. Это называется базовым условием)___
.
 ___

 ```
 // function to find the factorial of a number
function factorial(n) {
  // base case: if n is 0, return 1
  if (n === 0) {
    return 1;
  }
  // recursive case: return n times the factorial of n-1
  else {
    return n * factorial(n - 1);
  }
}

// test the function
console.log(factorial(5)); // 120
console.log(factorial(3)); // 6
console.log(factorial(0)); // 1
```

___


# What is Closure in Java Script?

## A **Closure** in JavaScript is a function that can access the variables and functions of its outer scope, even after the outer function has finished executing. This allows the function to remember its environment and use it later.

#### *****(Closure в JavaScript - это функция, которая может обращаться к переменным и функциям своей внешней области видимости даже после завершения выполнения внешней функции. Это позволяет функции запомнить свое окружение и использовать его в дальнейшем.)*****

___

```
// define a function that returns another function

function makeGreeting(name) {
  // name is a variable in the outer scope
  return function() {
    // this function is a closure
    console.log("Hello, " + name);
  };
}

// create a greeting function for Alice
let greetAlice = makeGreeting("Alice");

// call the greeting function

greetAlice(); // Hello, Alice

```
___

### In this example, the function `makeGreeting` returns another function that uses the parameter `name`. When we call `makeGreeting` with the argument `"Alice"`, we create a closure that remembers `"Alice"` as the value of `name`. Even after `makeGreeting` has finished, the closure can still access the variable `name` and use it in the `console.log` statement. This is how closures work in JavaScript.

#### ***(В этом примере функция `makeGreeting` возвращает другую функцию, которая использует параметр `name`. Когда мы вызываем `makeGreeting` с аргументом `"Alice"`, мы создаем closure, которое запоминает `"Alice"` как значение параметра `name`. Даже после завершения `makeGreeting` closure все еще может обращаться к переменной `name` и использовать ее в операторе `console.log`. Вот как работают замыкания в JavaScript.)***

```
function outerFunction(x) {
    return function innerFunction(y) {
        return x + y;
    };
}

var closureExample = outerFunction(5);
console.log(closureExample(3)); // Выводит: 8

```
#### ***(Здесь innerFunction - это замыкание, она сохраняет значение x, переданное во внешнюю функцию outerFunction. Таким образом, даже после завершения работы outerFunction, innerFunction может продолжать использовать значение x.)***
___


