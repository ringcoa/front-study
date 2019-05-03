자바스크립트에서 변수를var 키워드로 정의한다.

## 값초기화

    var num = 1; //정수를 담기 위한 메모리 할당
    var string = 'hi :D' //문자열을 담기위한 메모리 할당
    var obj = {
	    name : 'ringco',
	    gender : 'female'
    } //오브젝트와 오브젝트의 값을 담기위한 메모리
    var arr = ['봄','여름','가을','겨울'] //배열을 담기 위한 메모리
    function fun(){} // 함수를 위한 할당 - 함수는 호출가능한 오브젝트이다.
    var date = new Date() // 데이터 개체를 위해 메모리 할당


var 키워드를 사용하면 문제점이 발생한다. 
변수를 실제 사용하기 전까지 변수의 정의 여부를 확인하지 않는 것이다.
정의 되지 않았거나 값을 할당하지 않은 변수는 의도하지 않은 의외의 동작을 할 수 있게된다.

그래서 **let**키워드를 도입했다.
let의 장점은 정의하지 않은 변수 이름은 사용하지 못한다는 것이다

var 키워드를 사용할 경우

	
    console.log(letValue);
    var  letValue  =  1;
    console.log(letValue)
의 결과 값은
> undefined 
> 1

이 된다.

let 키워드를 사용 할 경우
	

    console.log(letValue);
    let  letValue  =  1;
    console.log(letValue)

> ReferenceError: letValue is not defined

와 같은 오류가 발생한다.

## 블록 범위

let 키워드는 블록범위 안에서만 유효하다.
예를 들어

    let  value  =  1;
    
    console.log(value);
   
    if(value  ==  1 ){
	    let  value  =  100;
	    console.log(value)
    }
    console.log(value)
와 같은 식이 있다면 결과값은 다음과 같다.

> 1
> 100
> 1

같은 변수 이름을 사용했지만 if문 안에 들어가 있는 변수 value는 if문 안에만 유효하다.
