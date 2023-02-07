# -3
Пользователь с клавиатуры вводит 3 числа, необходимо создать функцию, которая определяет максимальное значение среди этих чисел

function maxNum(num1, num2, num3){
        var max = 0;
        if(num1 > num2){
            if(num1 > num3){
                num1 = max;
            }
            else{
                num3 = max;
            }
        }
        else{
            if(num2 > num3){
                num2 = max;
            }
        }
    return max;
    }

    for(i=0;i<3;i++){
        parseInt(prompt("Enter a number"));
    }
    document.write(maxNum());
    
    */Необходимо реализовать четыре функции, каждая функция должна принимать по два числа и выполнять одну из операций (каждая функция выполняет одну из них):
1. Сложение
2. Разность
3. Умножение
4. Деление
Необходимо сделать так, чтобы функция вернула число, например выражение console.log(sum(2, 6)); должно вывести число 8 в консоль (sum - функция сложения в данном примере, ваши названия функций могут отличаться). Округлять значения, которые возвращают функции не нужно, однако, обратите внимание на разность, функция должна вычесть из большего числа меньшее, либо вернуть 0, если числа равны. Функциям всегда передаются корректные числа, проверки на NaN, Infinity делать не нужно./*

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Homework</title>
</head>

<body>
    
    <script>
        "use strict";

        /**
        * Функция сложения двух чисел
        * @param {number} a - число А
        * @param {number} b - число В
        * @return {number} - сумма чисел 
         */
        function sum(a, b) {
            return a + b;
        }

        /**
        * Функция разности двух чисел
        * Из большего вычитается меньшее число, если числа одинаковые -
        * функция возвращает ноль.
        * @param {number} a - число А
        * @param {number} b - число В
        * @return {number} - разность чисел 
         */
        function diff(a, b) {
            if (a > b) {
                return a - b;
            }
            return b - a;
        }

        /**
        * Функция умножения двух чисел
        * @param {number} a - число А
        * @param {number} b - число В
        * @return {number} - произведение чисел 
         */
        function mul(a, b) {
            return a * b;
        }

        /**
        * Функция деления двух чисел
        * @param {number} a - число А
        * @param {number} b - число В
        * @return {number} - деление чисел 
         */
        function div(a, b) {
            return a / b;
        }

        const numberA = +prompt(`Введите число А: `);
        const numberB = +prompt(`Введите число B: `);
        alert(`Сумма числел А и В: ${sum(numberA, numberB)}`);
        alert(`Разность числел А и В: ${diff(numberA, numberB)}`);
        alert(`Произведение числел А и В: ${mul(numberA, numberB)}`);
        alert(`Деление числел А и В: ${div(numberA, numberB)}`);
    </script>
</body>

</html>
