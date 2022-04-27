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
 
 


MIPS Exercise

.data
       
        result: .asciiz "\nEl resultado es: "
        number_one_msg: .asciiz "\nIngrese el primer numero: "
        number_two_msg: .asciiz "\nIngrese el segundo numero: "
  .text
        main:
   	      # user input
              li $v0, 4
              la $a0, number_one_msg
              syscall

              li $v0, 5
              syscall

              # saving user input
              move $t0, $v0

              # user input
              li $v0, 4
              la $a0, number_two_msg
              syscall

              li $v0, 5
              syscall

              # saving user input
              move $t1, $v0

              # adding the user numbers
              add $t2, $t0, $t1

              # showing result number
              li $v0, 4
              la $a0, result
              syscall

              # printing number
              li $v0, 1
              move $a0, $t2
              syscall



### Week 1 challenge (April 7th Thursday) 
 
PRINTS SPECIAL NUMBES 


```js 
for (let a = 0; a < 101; a++) {
  if (a % 2 === 0) 
    
    console.log(a);
}
```
 
 
 ### Week 2 challenge (April 19th Tuesday)
 
 CODEWARS EXERCISES 
 
1. Multiply exercise

```js
function multiply(a, b){
 return a * b
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
