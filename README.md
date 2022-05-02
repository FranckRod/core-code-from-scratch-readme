# core-code-from-scratch-readme

### Week 1 challenge (April 5th Tuesday) 
Interpreted And Compiled Programming Languages

1. Interpreted languages are processed line by line of code by the program and Compiled languages are processed in human language first and then proceseed by the machine.

2. Is Java compiled or interpreted, or both?. Java is both because it gets first converted into machine code and then the code gets interpred by the JVM.

3. pseudocode currency converter

-START 
- Quantity -- GET
- btcvalue -- GET from https://coinmarketcap.com/currencies/bitcoin/
- Conversation -- quantity * btcvalue
- TOTAL conversation 
- END


4.  High and Low level languages

- Low level languages are more complex for us to learn but give us more control and is executed direcly by the cpu.

- High level languages are easier for us to read and write.


              Week 1 challenge (April 6th Wednesday) 

Year of birth in binary, year 1993

(1993) decimal = (11111001001) binary

subtraction method 
1993 ->1024 + 512 + 256 + 128 +64 +8 

1993 - 1024 = 969      969-512= 457    457-256= 201   201-128= 73   73-64= 9   9-8= 1  

 1,024 512 256 128 64 32 16 8 4 2 1
 
 11111001001
 
 


MIPS Exercise, suma de 2 numeros

```js
.data
	number1: .asciiz "\nIngresar el primer numero: "
	number2: .asciiz "\nIngresar el segundo numero: "
	add_numbers: .asciiz "\nEl resultado de la suma sera: "
	
.text 
	main:
	li $v0, 4
	la $a0, number1
	syscall
	
	li $v0, 5
	syscall
	
	move $t0, $v0
	
	li $v0, 4
	la $a0, number2
	syscall 
	
	li $v0, 5
	syscall 
	
	move $t1, $v0
	
	add $t2, $t0, $t1
	
	li $v0, 4
	la $a0, add_numbers
	syscall 
	
	li $v0, 1
	move $a0, $t2
	syscall
  ```
  
  Mostrar mi nombre
  
  ```js
	.data
	      my_name: .asciiz "\nAntonio\n"
  .text
	      main:
              li $v0, 4
              la $a0, my_name
              syscall
  ```
	
   

### Week 1 challenge (April 7th Thursday) 
 
PRINTS SPECIAL NUMBES 


```js 
for (let a = 0; a < 101; a++) {
  if (a % 2 === 0) 
    
    console.log(a);
}
```


BAD CODE 1

The error is that the value of cod was changed using the = assignment operator instead of the == equality operator  

```js 
var cond = false;

if ((cond == true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```

BAD CODE 2

```js
var n = 100;

if (n == 100) {
  console.log('This is a special number!');
}
if (n < 1000 && n % 10 === 0) {
  console.log('This number is almost special');
} else {
  console.log('Just a regular number');
}

```
 
 
 ### Week 2 challenge (April 19th Tuesday)
 
 CODEWARS EXERCISES 
 
1. Multiply exercise

```js
function multiply(a, b){
 return a * b;
}
```

2. ASCII

```js
function uniTotal (string) {
  let total = 0;
  let totalcaracters = string.length;
  
  for (let i = 0; i < totalcaracters; i++) {
    let chr = string[i];
    total = total + chr.charCodeAt();
  }
  return total;
}
```

3. Get character from ASCII Value

```js
function getChar(c){
  return String.fromCharCode(c);
}
```

4. Binary addition

```js
function addBinary(a,b){

let result = (a + b).toString(2);

return result;
}
addBinary(1,2);
```

5. Student's final grade

```js
const finalGrade = (exam, projects) => {
  if (exam > 90 || projects > 10) return 100
  if (exam > 75 && projects >= 5) return 90
  if (exam > 50 && projects >= 2) return 75

  return 0
}
```

#### Week 2 challenge (April 20th Wednesday)

Holiday- Duty Free

```js
function dutyFree(normPrice, discount, hol) {

  let discPrice = (normPrice * discount) /100; 

  let bottleswithdisc = hol / discPrice;
  
  let finalResult = Math.floor(bottleswithdisc);
  return finalResult;
}
```

Twice as old 
```js
function twiceAsOld(dadYearsOld, sonYearsOld) {
return Math.abs(2 * sonYearsOld - dadYearsOld);
}
```

Valid Spacing (resolved in the Stand Up session)

```js
function validSpacing(s) {
  if(s.charAt(0) === ' ' || s.charAt(s.length - 1) === ' ') { 
     return false;
  }
  
  for(let i = 0; i < s.length; i++) {
    if(s.charAt(i) === ' '){ 
      if(i != 0 && s.charAt(i-1) === ' ') {
        return false;
      }
      if(i != (s.length - 1) && s.charAt(i+1) === ' ') {
        return false;
      }
    }
  }
  
  return true; 
}
```
Fake Binary 

```js
function fakeBin(x){
return x.split("").map( i => i < 5 ? 0 : 1).join("")
}
```

### Week 3 challenge (April 25th Monday)


April 26th Tuesday

 Simple Pig Latin



```js
function pigIt(str) {
  const firstletter = str.split(' ')
  return firstletter
  
 .map((word) => {

     return word.match(/[A-z]/i)
        ? `${word.substr(1)}${word.substr(0, 1)}ay`
        : word
    })
    .join(' ')
```
