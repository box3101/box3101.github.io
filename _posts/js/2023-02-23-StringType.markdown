---
layout: post
title: "StringType"
date: 2023-02-22 17:53:32 +0900
author: Jeffrey
categories: JavaScript(Es6)
---

## 문자열에 대한 조작

# · 문자열 이어 붙이기

console.log( "이찬용"+"입니다." ); <br>
var intro = "이찬용"; <br>
intro = intro+"입니다."; <br>
var intro = "이찬용"; <br>
intro += "입니다.";

# · 문자열의 길이(= 글자 수)를 구하기

문자열.length => Number타입의 결과가 도출

# · 문자열에서 부분 문자열(substring)을 찾아서 등장하는 위치 구하기

문자열.indexOf( 찾고자 하는 부분문자열 ) <br>
위치: 문자열의 맨 첫글자를 0 으로 보고 그 이후부터 한글자당 1씩 증가하는 숫자 <br>
전체 문자열에서 찾고자 하는 부분문자열이 존재하지 않으면 -1 이 도출된다.

# 문자열에서 일부 구간을 잘라내서 부분 문자열을 뽑아내기

4-1) 문자열.substr( 시작위치, 길이 ) <br>
전체 문자열에서 시작위치부터 시작해서 길이만큼의 부분문자열을 뽑아낸다. <br>
<br>
4-2) 문자열.substring( 시작위치, 끝위치 ) <br>
전체 문자열에서 시작위치부터 (끝위치-1)까지 뽑아낸다. <br>
<br>
4-3) 문자열.slice( 시작위치, 끝위치 ) <br>
전체 문자열에서 시작위치부터 (끝위치-1)까지 뽑아낸다. <br>
끝위치를 생략할 수 있다. 그 경우, 시작위치부터 문자열의 끝까지를 추출. <br>
끝위치가 생략되고 시작위치로 음수가 주어지면, 문자열의 끝에서부터 (시작위치)길이만큼의 문자열을 추출

# · 문자열에서 부분문자열을 찾아서 다른 문자열로 치환하기

문자열.replace( 찾을 부분문자열, 치환할 새 부분문자열 ) <br>
     <br>
5-1) 전체 문자열에서 부분문자열이 여러번 등장하더라도 치환은 맨 앞의 1번만 일어난다. <br>
5-2) 문자열 자체를 바꿔버리는건 아니고, 치환된 상태로 새 문자열을 만들어준다.

## 사용자로부터 키보드를 통해 문자열을 입력받기
var name = prompt( 사용자에게 보여줄 질문 문자열 ); <br>
사용자로부터 숫자를 입력받을 방법은 없다.

## 묵시적 형 변환 (Implicitly type casting)
서로 다른 타입의 데이터끼리 연산을 시도하면, 어느 한 쪽의 데이터타입이 일시적으로 변화하는 현상.

# · String타입과 Number타입간에 +연산을 하는 경우 <br>
= Number타입 데이터가 String타입으로 바뀌어서 결과적으로 String타입 데이터간의 문자열 이어붙이기 동작으로 작동한다.

# · String타입과 Number타입간에 -,*,/,%연산을 하는 경우 <br>
원칙적으로는 NaN 이 도출되어야 하나..<br>
단, String타입 데이터가 마치 숫자로 바꿀 수 있을것처럼 생긴 경우에 한해서 String타입 데이터가 Number타입으로 바뀌어서 결과적으로 산술연산이 이뤄진다.

