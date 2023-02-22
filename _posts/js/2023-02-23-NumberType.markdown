---
layout: post
title: "NumberType"
date: 2023-02-22 17:53:32 +0900
author: Jeffrey
categories: JavaScript(Es6)
---

## 숫자 (Number)

var myAge = 41; // 정수 (integer, int) <br>
var catAge = 0.66; // 실수 (real number, r) <br>
부동소수점 실수 floating point number, float <br>
배수정밀도 실수 double #precision number, double <br>
var earthToAndromeda = 289712398789798547786783687123; // big integer, bigint 

## 산술연산(arithmatic operation)

숫자를 대상으로 해서 가공하면 결과도 숫자로 나오는 계산

# 사칙연산: + - \* / %

이항연산 5 나누기 3 = 몫이 1 이고, 나머지는 2

# 산술대입연산: += -= \*= /= %=

단항연산 좌항에는 반드시 이미 숫자가 들어있는 변수가 위치해야 한다.

# 증감연산: ++ --

무항연산
이미 숫자가 들어있는 변수의 내용을 1씩 증가시키거나, 1씩 감소시킨다. <br>
변수이름의 뒤에 연산기호를 적는 후위표기법과 변수이름의 앞에 연산기호를 적는 전위표기법이 존재. <br>
한 문장에 여러개의 연산기호가 등장할 때 전위표기와 후위표기가 작동하는 방식이 미묘하게 다르다.

```jsx
num3 = num1++; // num1의 값을 num3에 할당한 뒤 num1의 값을 1 증가시킴
num4 = num2--; // num2의 값을 num4에 할당한 뒤 num2의 값을 1 감소시킴
```

```실행결과
2 2
```

```jsx
num3 = ++num1; // num1의 값을 1 증가시킨 뒤 num3에 할당
num4 = --num2; // num2의 값을 1 감소시킨 뒤 num4에 할당
```

```실행결과
3 1
```

# 숫자중에 특수하게 생긴 숫자
<strong>NaN Not a Number</strong>. 산술연산의 결과로 숫자를 도출할 수 없을때 계산할 수 없다는 뜻으로 사용하는 숫자. <br>
<strong>Infinity</strong> 무한대. 자바스크립트에 취급할 수 있는 수의 범위를 벗어난 말 그대로 무한대를 의미하는 숫자.