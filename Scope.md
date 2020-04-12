# Scope

Scope is the accessibility of variables, functions, and objects in some particular part of your code during runtime.

## Examples
### Example : 1
```js
var userName = "Ameen ALam";
function modifyUserName() {
        userName = "Daniyal Nagori"; 
    };

function showUserName() {
        alert(userName);
    };

alert(userName); // Output =  Ameen Alam

modifyUserName();
showUserName();// display Daniyal Nagori
``` 
 
### Example : 2

```js 
function createUserName() {
    userName = "Ameen Alam";
}

function modifyUserName() {
    if(userName)
        userName = "Daniyal Nagori";
};

function showUserName() {
    alert(userName);  
}

createUserName();
showUserName(); // Output = Ameen Alam 

modifyUserName();
showUserName(); // Output = Daniyal Nagori 

 ```



### Example : 3

```js

function createUserName() {
    var userName = "Ameen Alam";
}

function showUserName() {
    alert(userName);
}

createUserName();
showUserName(); // Uncaught ReferenceError: userName is not defined
    // at showUserName (<anonymous>:6:11)
    // at <anonymous>:10:1

```





### Example : 4


```js
var userName = "Ameen Alam";

function ShowUserName()
{
    var userName = "Daniyal Nagori";

    alert(userName); // "Daniyal Nagori"
}

ShowUserName();

alert(userName); // Ameen Alam

```



### Example : 5

```js
function NoBlockLevelScope(){
    
    if (1 > 0)
    {
        var myVar = 22;

    }

    alert(myVar);
}

NoBlockLevelScope(); // Ouput = 22 
```



### Example : 6

```js 
var age = 100;
function go(){
 var age = 200;
 var hair =  'black';
 console.log(age);
 console.log(hair);
}
go();
console.log(age);

// OUTPUT  200 
// OUTPUT  black 
// OUTPUT  100 
```



### Example : 7
```js

if (true) {
   // userName is in the global scope because of the 'var' keyword
   var userName = 'Ameen Alam';
   console.log(userName); // output 'Ameen Alam'
   // age is in the local scope because of the 'let' keyword
   let age = 20;
   console.log(age); // output 20
   // skills is in the local scope because of the 'const' keyword
   const skills = 'JavaScript';
   console.log(skills); // output 'JavaScript'
}
console.log(userName); // output 'Ameen Alam'
console.log(age); // Uncaught ReferenceError: age is not defined // Becase let is block level  
console.log(skills); // Uncaught ReferenceError: skills is not defined // const is also block level
```


// --------------------------
