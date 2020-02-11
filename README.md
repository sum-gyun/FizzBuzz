# FizzBuzz??

"Fizzbuzz questions"는 영국의 아이들이 학교에서 하게되는 일종의 놀이다(를 통한 동기 또는 흥미 유발을 위한). 해외의 학교에서는 놀이식으로 수업을 진행하는 경우가 많은 편인데, 우리 것과 궂이 비교하자면 일종의 369 게임과 비슷할까?

어쨌든 Fizzbuzz 문제를 프로그래머 채용 인터뷰시에 내 보았더니 대다수의 우수한 프로그래머의 경우 2분 이내로 답을 내어야 함에도 대부분의 컴퓨터과학 전공학과 졸업생들이 문제 자체를 제대로 풀지 못했고, 심지어 좀 한다는 시니어 프로그래머들도 솔루션을 내는데 10~15분이 걸렸다고 한다.


## How?

[문제(영어 원문)]

Write a program that prints the numbers from 1 to 100. But for multiples of three print "Fizz" instead of the number and for the multiples of five print "Buzz". For numbers which are multiples of both three and five print "FizzBuzz".

우리 말로 풀어서 쓰면, 1부터 100사이의 숫자를 프린트하는 프로그램을 작성하는데 3의 배수이면 "Fizz"를, 5의 배수이면 "Buzz"를, 둘 모두의 배수 즉 15의 배수이면 "FizzBuzz" 를 프린트하도록 하라.

문제는 한마디로 간단하고 명확하다. 인터뷰시에 해당되는 중요한 얘기인데, 만약 문제에 구체적인 제약사항이 필요하다면 적극적으로 면접관에게 질문하고 상의하라. 문제가 요구하는 답은 다음과 같은 모양일 것이다.

1
2
Fizz
4
Buzz
.
.
또는
1 2 Fizz 4 Buzz Fizz 7 ...


### Prerequisites

알고리즘을 구현하기 위해 보통 IF-ELSE문으로 구현할 것이다

fun FizzBuzz(input: Int): Array<String?> {
    val array: Array<String?> = arrayOfNulls(input)

    for (i in 0 until input) {
        val index = i + 1

        if ((index % 3 == 0) and (index % 5 == 0)) {
            array[i] = "FizzBuzz"
        } else if (index % 3 == 0) {
            array[i] = "Fizz"
        } else if (index % 5 == 0) {
            array[i] = "Buzz"
        } else {
            array[i] = index.toString()
        }
        Log.e("FizzBuzz", "index : $index  array = ${array[i]}")
    }
    return array
}

하지만... 이번시간은 딥러닝의 세계를 맛보기 위한 순서이기 때문에 딥러닝에 관련된 생각으로 들어가보자.


### Installing

딥러닝을 하기 위해 여러가지 언어와 라이브러리가 있지만, 딥러닝의 대표적인 언어인 "Python"으로 시작한다.
딥러닝 환경 구성을 하기 위해서는 Python 설치, Tensorflow 환경 설치(그래픽카드 혹은 CPU 환경의 Cuda, Cudnn 설치, Tensorflow library 설치)가 필요하다.
그러나 Amazon SageMaker를 이용하여 쉽게 Demo를 접근한다.
https://console.aws.amazon.com/sagemaker?p=sgm&cp=bn&ad=c

노트북(Notebook) → 노트북 인스턴스(Notebook Instance) → 생성 → 작업(Jupyter 열기)

## Running the tests

New(conda_tensorflow_p36) 파일로 생성
Demo를 넣어가며 test!!!
