- [Switch](#switch)

- [Loops](#loops)
    - [for loop](#for-loop)
        - [Infinte for loop](#infinite-for-loop)
    - [while Loop](#while-loop)
        - [Infinite while Loop](#infinite-while-loop)
    - [do while loop](#do-while-loop)
        - [Infinite do while loop](#infinite-do-while-loop)
    - [for vs while loop](#for-vs-while-loop)
  - [break](#break)
  - [continue](#continue)



## Switch

Switch  is an alternative for **if else if else else**.
The switch statement starts with a *switch* keyword followed by a parenthesis and code block. Inside the code block we will have different cases. Case block runs if the value in the switch statement parenthesis matches with the case value. The break statement is to terminate execution so the code execution  does not go down after the condition is satisfied.  The default block runs if all the cases don't satisfy the condition.

```js
switch(caseValue){
  case 1:
    // code
    break
  case 2:
   // code
   break
  case 3:
   // code
   break
  default:
   // code
}
```

```js
let weather = 'cloudy'
switch (weather) {
  case 'rainy':
    console.log('You need a rain coat.')
    break
  case 'cloudy':
    console.log('It might be cold, you need a jacket.')
    break
  case 'sunny':
    console.log('Go out freely.')
    break
  default:
    console.log(' No need for rain coat.')
}
```
// Examples to use conditions in the cases

```js
let num = prompt('Enter number');
switch (true) {
  case num > 0:
    console.log('Number is positive');
    break;
  case num == 0:
    console.log('Numbers is zero');
    break;
  case num < 0:
    console.log('Number is negative');
    break;
  default:
    console.log('Entered value was not a number');
}
```

  
# Loops

In programming, loops are used to repeat a block of code.

For example, if you want to show a message 100 times, then you can use a loop. It's just a simple example; you can achieve much more with loops.

## for loop

The syntax of the for loop is:

```js
for (initialExpression; condition; updateExpression) {
    // for loop body
}
```

Here

1. The initialExpression initializes and/or declares variables and executes only once.
2. The condition is evaluated.
    1. If the condition is false, the for loop is terminated.
    2. If the condition is true, the block of code inside of the for loop is executed.
3. The updateExpression updates the value of initialExpression when the condition is true.
4. The condition is evaluated again. This process continues until the condition is false.

**Example**

Display a Text Five Times

```js
// program to display text 5 times
const n = 5;

// looping from i = 1 to 5
for (let i = 1; i <= n; i++) {
    console.log(`I love JavaScript.`);
}
```

**Output**

```
I love JavaScript.
I love JavaScript.
I love JavaScript.
I love JavaScript.
I love JavaScript.
```

### Infinite for loop

If the test condition in a for loop is always true, it runs forever (until memory is full).

```js
// infinite for loop
for(let i = 1; i > 0; i++) {
    // block of code
}
```

## while Loop

The syntax of the while loop is:

```js
while (condition) {
    // body of loop
}
```

Here ,

1. A while loop evaluates the condition inside the parenthesis ().
2. If the condition evaluates to true, the code inside the while loop is executed.
3. The condition is evaluated again.
4. This process continues until the condition is false.
5. When the condition evaluates to false, the loop stops.

**Example**

Display Numbers from 1 to 5

```js
// program to display numbers from 1 to 5
// initialize the variable
let i = 1, n = 5;

// while loop from i = 1 to 5
while (i <= n) {
    console.log(i);
    i += 1;
}
```

**Output**
```
1
2
3
4
5
```

### Infinite while Loop

If the condition of a loop is always true, the loop runs for infinite times (until the memory is full).

```js
// infinite while loop
while(true){
    // body of loop
}
```

## do while loop

The syntax of do...while loop is:

```js
do {
    // body of loop
} while(condition)
```

Here, 
1. The body of the loop is executed at first. Then the condition is evaluated.
2. If the condition evaluates to true, the body of the loop inside the do statement is executed again.
3. The condition is evaluated once again.
4. If the condition evaluates to true, the body of the loop inside the do statement is executed again.
5. This process continues until the condition evaluates to false. Then the loop stops.

**Note:** do-while loop is similar to the while loop. The only difference is that in do…while loop, the body of loop is executed at least once.


### Infinite do while Loop

```js
// infinite do...while loop
const count = 1;
do {
   // body of loop
} while(count == 1)
```

## for Vs while Loop

A for loop is usually used when the number of iterations is known. For example,

```js
// this loop is iterated 5 times
for (let i = 1; i <=5; ++i) {
   // body of loop
}
```
And while and do...while loops are usually used when the number of iterations are unknown. For example,

```js
while (condition) {
    // body of loop
}
```

## break

Break is used to interrupt a loop.

```js
for(let i = 0; i <= 5; i++){
  if(i == 3){
    break
  }
  console.log(i)
}

// 0 1 2
```

The above code stops if 3 found in the iteration process.

## continue

We use the keyword *continue* to skip a certain iterations. 

```js
for(let i = 0; i <= 5; i++){
  if(i == 3){
    continue
  }
  console.log(i)
}

// 0 1 2 4 5
```