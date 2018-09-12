## 개인용으로 사용

개인용
* 2018-09-12 커밋

## 내장함수

- [1.0](#1.0) intval : 변수의 정수값을 얻습니다

  ```PHP 4, PHP 5, PHP 7
  // PHP
  int intval ( mixed $var [, int $base ] );
  
  //예제
  echo intval(42);                      // 42
  echo intval(4.2);                     // 4
  echo intval('42');                    // 42
  echo intval('+42');                   // 42
  echo intval('-42');                   // -42
  ```