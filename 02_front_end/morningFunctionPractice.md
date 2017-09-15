## Function and Object Practice

Given, the following object, log the third element from the array

```javascript
const fun = {
    asdf: ["afd", "matt", 'sweet']
}
```

Given, the following object, log the elbow property

```javascript
const body = {
    arm: {
        elbow: 'pointy'
    }
};
```

Given, the following object, call the jump method

```javascript
const person = {
    jump(){
        console.log('fly!');
    }
};
```

Create a data structure such that the following code logs the value "blue"

```javascript
console.log(myList[0].eyeColor);
```

Create a data structure such that the following code logs the value "buy supplies"

```javascript
console.log(myArrays[2][4]);
```

Call the function in the given code:

```javascript
const awesome = [
    {
        asdf:'true'
    },
    3456.245,
    ()=>{
        console.log('fun');
    },
    "buddy"
];
```

Loops over the following array, and print its values:

```javascript
const refrigerator = {
    fruits: ['apple', 'pear', 'banana']
}
```

Use two loops to loop over each array in the given "container" array

```javascript
const container = [
    [1,5,7],
    ['bear', 'dog', 'cat'],
    [true, false, true]
];
```

Create a data structure such that the following logs `4`

```javascript
console.log(createCar().tires);
```

Create a data structure such that the following logs `pears`

```javascript
console.log(generateShoppingList()[3]);
```

Create a data structure such that the following logs `20lbs`

```javascript
console.log(createRobot().stats.weight);
```

Call the drive method

```javascript
const generateCar = ()=>{
    return {
        drive(){
            console.log("Vroom");
        }
    }
}
```


Log the message attribute

```javascript
const account = {
    tweet(){
        return {
            message: "fun"
        }
    }
}
```

Log the second element in the array

```javascript
const me = {
    foo(){
        return {
            array: [2.5, 7, true]
        }
    }
}
```


1. Write a JavaScript function that will find the largest of five numbers. Display an alert box to show the result. 
Sample numbers : -5, -2, -6, 0, -1 
Output : 0 

2.  Write a JavaScript conditional statement to sort three numbers. Display an alert box to show the result. 
Sample numbers : 0, -1, 4 
Output : 4, 0, -1 

3. Write a JavaScript function to get the first element of an array. Passing a parameter 'n' will return the first 'n' elements of the array. 
Test Data : 
```
console.log(first([7, 9, 0, -2])); 
console.log(first([],3));
console.log(first([7, 9, 0, -2],3));
console.log(first([7, 9, 0, -2],6));
console.log(first([7, 9, 0, -2],-3));
```
Expected Output : 
```
7
[] 
[7, 9, 0] 
[7, 9, 0, -2] 
```

4. Write a simple JavaScript program to join all elements of the following array into a string. 
Sample array : ```myColor = ["Red", "Green", "White", "Black"];```
Expected Output : 
```"Red,Green,White,Black"```

5.  Write a JavaScript program which accept a number as input and insert dashes (-) between each two even numbers. For example if you accept 025468 the output should be 0-254-6-8.

6. Write a JavaScript program to find the most frequent item of an array. 
Sample array : ```const arr1=[3, 'a', 'a', 'a', 2, 3, 'a', 3, 'a', 2, 4, 9, 3];```
Sample Output : a ( 5 times ) 
