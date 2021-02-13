# JavaScriptNJquery_Study
## 1. JavaScript
자바스크립트는 웹 브라우저에서 많이 사용하는 프로그래밍 언어이며 본래 넷스케이프의 브랜든 아이크에 의해 모카라는 이름으로 만들어졌다.
모카는 곧 라이브 스크립트 라는 이름으로 개발됐고 이후 넷스케이프가 썬 마이크로시스템과 함께 라이브 스크립트에 자바스크립트라는 이름을 붙이고 본격적으로 발전한다.
자바스크립트 아래와 같이 활용된다.

  1. 웹 클라이언트 애플리케이션
  2. 웹 서버 애플리케이션 (Node.js)
  3. 모바일 애플리케이션 (React Native)
  4. 데스크톱 애플리케이션 (일렉트론)
  5. 게임 개발 (액션스크립트, 유니티)
  6. 데이터베이스 관리 (NoSQL - MongoDB)

## 2. 종류
유럽 컴퓨터 제조 협회는 자바스크립트를 ECMAScript 라는 이름으로 표준화했다. 최신 브라우저들은 ECMAScript 7까지의 기능을 대부분 지원한다.
최신이 아닌 경우에는 보완 방법으로 Node.js 를 활용하기도 한다.

## 3. 기본문법
- 자바스크립트에서 자료형을 확인할때는 typeof 연산자를 사용한다.
- 변수를 초기화하지 않으면 undefined 자료형이다.
- 입력의 경우 prompt() 함수를 이용한다. confirm 함수의 경우 확인을 요구하는 메시지 창을 띄운다.
-  더하기 연산자에 숫자형 자료형과 문자열 자료형을 사용할 경우 문자형으로 변환하며 그 외 연산자는 문자열 자료형을 숫자형 자료형으로 변환한다.
- 복소수는 NaN 로 표현되며 0, NaN, '', null, undefined 자료형은 false 로 판단된다.
- 일치연산자의 경우, 자동으로 형변환이 일어나 비교된다.

- 템플릿 문자열 ( ECMAScript 6 )
ECMAScript5 까지는 문자열 내부에 표현식을 삽일할 때 + 를 사용했지만 코드가 복잡해지는 단점이 있었다.
따라서, ECMAScript6 부터는 템플릿 문자열 기능이 추가되어 \` 기호로 감싸며 문자열 내부에 ${} 기호를 사용하고 내부에 표현식을 넣으면 문자열이 만들어질때 표현식이 계산되어 들어간다.
EX> alert(\`표현식 273+52의 값은 ${52+273} 입니다 ... !\`);

- ECMAScript6 부터는 var 키워드가 아닌, let 키워드를 사용한 변수, const 키워드를 사용한 상수라는 개념이 추가되었다. <br/>
  var 키워드의 경우 전역 스코프에 선언하며 재선언이 가능하지만, let 과 const 키워드의 경우 해당 스코프에 선언하며 재선언이 불가능하다.
  전역 스코프에 선언하게 될 경우, 중복 문제가 발생할 경우 함수로 한번 감싼 후 사용할 변수를 전달하는 방법으로 해결해야했다.
  그러나 let 키워드를 선언하여 해당 스코프에서만 유효하다면 이러한 문제가 발생하지 않는다.

- JavaScript 의 경우, 숫자를 0부터 세며 indexOf() 함수의 경우에도 0부터 위치를 출력한다.

## 4. 배열
- JavaScript 에서 배열은 [] 로 생성한다. 배열 안에 입력된 요소는 자료형을 구분하지 않는다.
- 배열에는 push() 메서드를 사용하여 추가한다.
- for in 반복문을 사용하여 배열이나 객체를 더욱 쉽게 다룰 수 있다. for of 문을 사용할 경우 반복 변수에 '요소'를 넣을 수 있다.


## 5. 함수
- 함수의 경우에도 var 함수명 = function() { } 과 같은 방법으로 할당이 가능하다.
- 선언적 함수와 달리 익명 함수는 나중에 생성된다.
- 자바 스크립트의 경우, 가변 인자 함수이므로 arguments 변수를 이용해 동적인 함수를 만들 수 있다.
- 함수 내부에 내부함수를 선언하여 프로젝트 중 겹칠 수 있는 함수명의 문제를 해결할 수 있다.
- 매개변수로 전달하는 함수를 콜백함수라고 한다. 또한, 함수를 리턴하는 함수를 만들 수 있다. 리턴된 함수를 사용하려면 () 를 하나 더 사용해야한다.
- 함수를 생성하자마자 실행하는 것을 자기호출함수 라고 하며, 함수를 () 로 감싸고 끝에 () 로 호출하는 방식이다.
  cf) 내장함수 - 타이머 함수, 인코딩/디코딩 함수, eval 함수, 숫자확인함수, 숫자변환함수

  ### 클로저
  - 클로저를 사용하면 지역 변수를 스코프 밖에서 사용 할 수 있는데, 이렇게 **활용될 가능성이 있는 변수를 제거하지 않고 남겨두는 것(혹은 공간)을 클로저라고 한다.**

- 웹 브라우저에 처리를 부탁하는 함수는 다른 코드의 실행이 끝난 후에 실행되는데 일반적인 for 문과 함께 사용하게되면 반복문이 모두 끝난 이후에 실행된다.
따라서, 해당 반복문의 변수를 사용하려면 자기호출함수를 사용하여 변수를 복사해서 전달해주거나 forEach() 메서드를 활용해 클로저를 생성한다.

<pre>
  <code>
  <script>
   [0,1,2].forEach(function (i) {
              setTimeout(function(){
                  alert(i);
               }, 0);
   });
   </script>
   </code>
</pre>



- 짧은 조건문을 활용하여 b = b||52; 와 같은 형태로 기본 매개변수를 설정할 수 있다.
- ECMAScript 6 에서는 (a, b = 52, c = 273 ) 과 같은 형태로 undefined 인 변수에 대해 기본 매개변수를 세팅해준다.

  ### 화살표 함수 - ECMAScript 6
  익명함수를 간단하게 사용할 수 있는 것이 화살표 함수이다. () => {} 와 같은 형태로 사용한다.
  바벨과 같은 ECMAScript 6 를 5 코드로 변환해주는 트랜스파일도 화살표 함수를 익명 함수로 단순 변환하므로 this 키워드를 주의하지 않고 사용하면 문제가 발생한다.
  
- 함수에서의 전개 연산자는 마침표 3개 ... 를 찍어 표기하는 연산자이다.
함수 내에서 arguments 객체를 사용하여 매개변수를 배열로 사용하는 것처럼 ...numbers 와 같은 형태로 전개연산자를 사용할 수 있다.
하지만, 다른 매개변수와 조합해서 사용할 때는 가장 뒤에 딱 하나만 사용해야한다.
- 모든 함수에는 apply() 메서드가 있다. 첫번째 매개변수는 함수 내부에서 사용할 this 키워드 객체, 두번째 매개변수로는 매개변수 배열을 넣게 된다.
- 배열을 매개변수로 전달할 때도 전개 연산자를 입력하여 전달할 수 있다.

## 6. 객체
- 객체 속성은 <객체 이름>.<속성 이름> <객체 이름>['<속성 이름>'] 과 같은 방법으로 접근 가능하다.
- 객체의 키 값을 식별자가 아닌 문자열로 사용할 경우 ['속성 이름'] 으로 접근해야 한다.
- 자바스크립트 속성에 function 을 넣고 해당 객체의 다른 속성에 접근하려고 하는 경우, this. 키워드를 생략할 수 없다.
- for ~ in 문을 사용하면 객체의 키를 순차대로 뽑아낼 수 있으며 반복문에 쓰지 않을 경우 해당 속성이 있는지 확인한다.
- with 키워드를 사용할 경우, 해당 객체 이름을 명시하지 않고 블록 내에서 속성을 쉽게 사용할 수 있다.
- with 키워드 내부에 있는 속성이 외부 변수 이름과 같을 경우 자바스크립트는 객체의 속성을 우선시한다.
이를 교정하려면 with 키워드 내부에서 window 객체의 (ex. output 등) 변수를 사용하겠다고 지정해주어야 한다.
- 동적으로 객체의 속성을 제거할 때는 delete 키워드를 사용한다. 속성 입력 시에는 typeof 키워드처럼 괄호를 사용해도 되고 사용하지 않아도 된다.
- 자바스크립트에서도 값 복사가 아닌 참조 복사가 일어날 경우, 주소복사가 되어 같은 객체를 바라보게 된다.
  - 전개 연산자를 이용해 배열을 복사할 경우, 값 복사가 일어난다.
  EX> const newArray = [...originalArray];
  - 전개 연산자를 두 번 사용할 경우, 배열을 병합할 수도 있다.
  EX> const newArray = [...arrayA, ...arrayB];
  
## 7. 생성자
- 생성자 함수의 경우, 일반적으로 대문자로 시작하며 new 키워드로 객체를 생성한다.
- 프로토 타입이란 생성자 함수로 생성된 객체가 공통으로 가지는 공간이며 사용하려면 해당 생성자.prototype 으로 명시한 후 .속성명 = function(){ } ; 과 같은 방법으로 할당 가능하다.
- new 키워드를 사용하지 않고 생성자 함수를 실행하면 해당 객체를 위한 공간을 만드는 것이 아니라 window 객체에 속성을 추가한 것 처럼 작동한다.

  ### 캡슐화
  - 생성자 함수 내에 this.get/set 함수를 설정함으로써 설정 값의 제한을 둘 수 있고 만일의 상황에 대비해 특정 속성이나 메서드를 사용자가 사용할 수 없게 숨길 수 있다.
  ### 상속
  - 특정 생성자 함수 내부에 속성으로 다른 생성자 함수를 넣고 prototype 을 전달해주고 .constructor 를 재지정하는 것으로 상속으로 동작하도록 할 수 있다.
  EX>
  <pre>
    <code>
      function Square(length){
        this.base = Rectangle;
        this.base(length, length);
      }
      
      Square.prototype = Rectangle.prototype;
      Square.prototype.constructor = Square;
    </code>
  </pre>
  
  - 생성자 함수에 constructor() 메서드를 다시 넣지 않아도 정상동작하지만, square 객체의 constructor() 메서드를 출력할 경우 생성자 함수 Rectangle 을 가리키므로
  프로토타입의 생성자 함수를 재정의하였다.
  
- ECMAScript 6 의 클래스는 변수를 숨길 수 없다. 그래서 일반적으로 개발자외에 만지지 말아달라는 의미로 변수 앞에 _ 를 붙인다.
- 게터와 세터는 선언할 때 앞에 get 또는 set 을 붙여 선언한다. get 을 붙여 만든 메서드는 rectangle.width 처럼 값을 가져오는 행위를 할 때 자동으로 호출되며,
set 을 붙여 만든 행위는 = 처럼 값을 넣는 행위를 할 때 자동으로 호출된다.
그러나, 게터와 세터를 사용하면 스택 트레이스와 유지 보수가 어렵고 메서드 체이닝에 활용하기 어렵다.

- 상속은 extends 키워드로 구현할 수 있다.

  <pre>
    <code>
    class Square extends Rectangle {
      constructor(length){
        super(length, length);
        alert(this)
      }
    </code>
  </pre>

## 8. 기본 내장 객체
- 기본 자료형에 속성이나 메서드를 사용하게 될 경우, 자동으로 객체로 변환된다, 하지만 임시적인 것이므로 속성이나 메서드를 추가할 수 없다.
추가하려면 프로토타입으로 메서드를 추가하여 임시적인 객체에서 사용해야 한다.
- 생성자 함수 등을 추가한 경우에는 propertyIsEnumerable() 과 같은 메서드로 나열 가능한지 검사 후, for in 반복문으로 출력하여야한다.
- 생성자 함수로 만든 숫자와 같은 자료형은 객체가 되므로 typeof 와 같은 연산자가 아닌 constructor 메서드를 사용하는 것이 좋다.ㅏ
EX> if(numberFromLiteral.constructor == Number)...

- Object 는 모든 객체의 최상위 객체이므로 prototype 객체에 추가한 메서드는 모든 객체에서 사용 가능하다.
- Number / String / 
