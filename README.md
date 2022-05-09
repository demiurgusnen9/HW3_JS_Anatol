# HW3_JS_Anatol
This is an educational repository that contains homeworks, completed as part of Vadim Ksendzov's training course on software testing. Here I am learning how to work in JS. Below is my homework and solution

### 1. Написать скриптик, который сосчитает и выведет результат от возведения 2 в степень 10, начиная со степени 1
```
 let a = 1
 while(a <=10)  {
     console.log(2 ** a)
     a++
 }
```
### 1*. Преобразовать 1 задачу в функцию, принимающую на вход степень, в которую будет возводиться число 2
```
 let a = 1
 function step (a) {
     while(a <=10)  {
             console.log(2 ** a)
             a++
         }
 }
 step(1)
```
### 2. Написать скрипт, который выведет 5 строк в консоль таким образом, чтобы в первой строчке выводилось :), во второй :):) и так далее
 Пример в консоли:
 :)
 :):)
 :):):)
 :):):):)
 :):):):):)
```
 let stroka = ':)'
 let numberOfRows = 1
 while (numberOfRows <= 5) {
     console.log(stroka)
     stroka+=':)'
     numberOfRows++
 }
```
### 2*. Преобразовать 2 задачу в функцию, принимающую на вход строку, которая и будет выводиться в консоль (как в условии смайлик), а также количество строк для вывода e.g. function printSmile(stroka, numberOfRows)
```
 let stroka = '(^)'
 let numberOfRows = 1
 function printSmile(stroka, numberOfRows) {
     while (numberOfRows <= 5) {
     console.log(stroka)
     stroka+='(^)'
     numberOfRows++
 }
 }
 printSmile('(^)', 1)
```
### 3**.  Написать функцию, которая принимает на вход слово. Задача функции посчитать и вывести в консоль, сколько в слове гласных, и сколько согласных букв.
 e.g. function getWordStructure(word)
 В консоли: 
 Слово (word) состоит из  (число) гласных и (число) согласных букв
 Проверки: 'case', 'Case', 'Check-list'
```
 function getWordStructure(word) {
     let count_gl = 0
     let count_sogl = 0
     const gl = ['a', 'e', 'i', 'o', 'u']
     const sogl = ['b', 'c', 'd', 'f', 'g', 'h', 'j', 'k', 'l', 'm', 'n', 'p', 'q', 'r', 's', 't', 'v', 'w', 'x', 'y', 'z']

     for(let char of word.toLowerCase()) {
         if (gl.includes(char)) {
             count_gl++
         } else if (sogl.includes(char)) {
             count_sogl++
         }
         }
        
         console.log('Слово ' + word + ' состоит из ' + count_gl + ' гласных и ' + count_sogl + ' согласных букв')
     }
 getWordStructure('case')
 getWordStructure('Case')
 getWordStructure('Check-list')
```
### 4**. Написать функцию, которая проверяет, является ли слово палиндромом
 e.g. function isPalindrom(word)
 Проверки: 'abba', 'Abba'
```
function Findpalindrome(TestStr) {
    let PlainStr = TestStr.toLowerCase().split("")
    let b
    for(var i=0; i < (PlainStr.length)/2; i++) {
    if(PlainStr[i] == PlainStr[PlainStr.length-i-1]) {
        b = 1
    }

    else {
        b = 0
        break
 }
}
if(b==1) {
    console.log('It is a palindrome')
} else {console.log('It is not a palindrome')}
}

Findpalindrome("abba")
Findpalindrome("Abba")
Findpalindrome("gjgjf")
```
