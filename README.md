## 개인용으로 사용

개인용
* 2018-09-12 커밋

## 숫자형 함수

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
  
## 문자열 함수

- [2.0](#2.0) str_replace : 검색된 모든 문자열을 변경 문자열로 교체

  ```PHP 4, PHP 5, PHP 7
  // PHP
  mixed str_replace ( mixed $search , mixed $replace , mixed $subject [, int &$count ] );
  
  //예제
  echo str_replace("<br />","<br>","<p>테스트 문구<br /></p>");                      
  // <p>테스트 문구<br></p>
  ```

- [2.1](#2.1) explode : 문자열을 특정 문자열로 나누어 배열에 반환

  ```PHP 4, PHP 5, PHP 7
  // PHP
  array explode ( string $delimiter , string $string [, int $limit ] );
  
  //예제
  $str = explode(" ","abc def");            //$str[0] = "abc" , $str[1] = "def"
  ```
  
- [2.2](#2.2) trim : 문자열 앞, 뒤에 있는 공백문자를 제거

  ```PHP 4, PHP 5, PHP 7
  // PHP
  string trim ( string $str [, string $character_mask = " \t\n\r\0\x0B" ] );
  
  //예제
  trim(" abc ")            //abc//
  ```
  
- [2.3](#2.3) ltrim : 문자열 앞에 들어가는 공백문자만 제거

  ```PHP 4, PHP 5, PHP 7
  // PHP
  string ltrim ( string $str [, string $character_mask ] );
  
  //예제
  ltrim(" abc ")            //abc //
  ```
  
- [2.4](#2.4) chop : 문자열 앞에 들어가는 공백문자만 제거

  ```PHP 4, PHP 5, PHP 7
  // PHP
  string chop ( string $str [, string $character_mask ] );
  
  //예제
  chop(" abc ")            // abc//
  ```
  
- [2.5](#2.5) nl2br : 문자열에 포함된 줄바꿈(\r,\n) 문자를 <br> 태그로 변환합니다. (php 버전이 4.0.6 보다 낮을경우 <br> 높을경우 <br/>)

  ```PHP 4, PHP 5, PHP 7
  // PHP
  string nl2br ( string $string [, bool $is_xhtml = TRUE ] );
  
  //예제
  nl2br("This\r\nis\n\ra\nstring\r");
  
  //위 예제 출력
  This<br />
  is<br />
  a<br />
  string<br />
  ```
  
- [2.6](#2.6) strlen : 문자열의 길이를 반환

  ```PHP 4, PHP 5, PHP 7
  // PHP
  int strlen ( string $string );
  
  //예제
  $str = ' ab cd ';  
  strlen($str)            // 7
  ```
  
- [2.7](#2.7) substr_replace : 원본문자열을 특정위치에 있는 변수로 바꾸어서 반환함

  ```PHP 4, PHP 5, PHP 7
  // PHP
  mixed substr_replace ( mixed $string , mixed $replacement , mixed $start [, mixed $length ] );
  substr_replace($원본문자열, $변수, $위치)
  
  //예제
  substr_reaplce("ABCDEF","XYZ",2);             // ABXYZDEF
  
  ```
  
## 배열 함수

- [3.0](#3.0) array_slice : 배열의 일부를 추출(주로 배열을 나눌때 사용)

  ```PHP 4, PHP 5, PHP 7
  // PHP
  array array_slice ( array $array , int $offset [, int $length [, bool $preserve_keys ]] );
  
  //예제
  $input = array ("a", "b", "c", "d", "e");
  
  $output = array_slice ($input, 2);      // ["c","d","e"]
  $output = array_slice ($input, -2, 1);  // ["d"]
  $output = array_slice ($input, 0, 3);   // ["a","b","c"]
  ```
  
- [3.1](#3.1) array_slice : 하나 이상의 배열을 합칠때 사용

  ```PHP 4, PHP 5, PHP 7
  // PHP
  array array_merge ( array $array1 [, array $array2 [, array $... ]] );
  
  //예제
  $array1 = array("color" => "red", 2, 4);
  $array2 = array("a", "b", "color" => "green", "shape" => "trapezoid", 4);
  $result = array_merge($array1, $array2);
  
  //위 예제 출력
  Array(
      [color] => green,
      [0] => 2,
      [1] => 4,
      [2] => a,
      [3] => b,
      [shape] => trapezoid,
      [4] => 4
  )
  ```
  
- [3.2](#3.2) implode : 특정 문자열로 배열내 문자를 합침

  ```PHP 4, PHP 5, PHP 7
  // PHP
  string implode ( string $glue , aray $pieces );
  string implode ( array $pieces );
  
  //예제
  $array = array('lastname', 'email', 'phone');
  $comma_separated = implode(",", $array);
  
  //위 예제 출력 lastname,email,phone
  ```
  