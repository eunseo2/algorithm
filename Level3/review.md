# 간단한 완전탐색(Simple Brute-Force Algorithm)- 1
* 가능한 모든 경우를 모두 시도해본다.
* ex) 약수의 개수가 홀수인 수  입력:10 출력 :3
* 1-1개o 2-2개 3-2개 4-3개o 5-2개 6-4개 7-2개 8-4개 9-3개o 10-4개 -> 약수의 개수가 홀수인 수 : 3개

-----------------------------------------------------
<img width="500" src="https://user-images.githubusercontent.com/70589857/103610145-c2e35600-4f62-11eb-910c-59f3fd079be3.PNG">
 b[i][j] = a[i][M-j-1] point! 이 코드가 좌우를 바꿔줌
 
 -----------------------------------------------------
 <img width="500" src="https://user-images.githubusercontent.com/70589857/103618662-ae5b8980-4f73-11eb-8deb-9675d105f9b0.PNG">
새로운 2차원 배열 만들고 거기에 입력값 받아서 1,1~5,5에 값 복사하기! 

 -----------------------------------------------------
 # 최대공약수
 *  유클리드 호제법
 ```
gcd(a,b) = gcd(b,a%b)
ex) gcd(24,18) = gcd(18,6)
while(1) {
 c= a%b
 if(c==0) break;
 a=b;
 b=c;
}
int GCD= b
``` 
--------------------------------------------------------
# rook
```
ry,rx=3
for(i=rx+1; i<=8; i++)
if(arr[ry][i]== king)
else if(arr[ry][i]== 장애물)
break;
```
# attackrange
### 문제
윤성이는 어렸을 적부터 수없이 몰려오는 적으로부터 기지를 방어하는 디펜스 유형의 게임을 플레이하는 것을 좋아했다.
그래서 간단한 디펜스 게임을 만들어 보려고 한다.
당신은 윤성이를 도와, 디펜스 게임 내에서 플레이어가 설치하는 유닛의 사거리를 나타내는 기능을 구현하면 된다.  

### 입력
입력 첫째 줄에는 디펜스 게임의 맵 크기 N이 주어딘다. 맵은 N×N 크기의 2차원 형태이다. (N은 6이상 100이하의 짝수)
둘째 줄에는 유닛이 설치될 위치 X, Y와 유닛의 사거리 R이 주어진다. X는 행의 번호, Y는 열의 번호를 의미한다.
(X, Y는 1이상 N이하의 자연수, R은 N/2이하의 자연수)

---------------------------------------------------
# class president
### 문제
오민식 선생님은 올해 형택초등학교 6학년 1반 담임을 맡게 되었다. 
오민식 선생님은 우선 임시로 반장을 정하고 학생들이 서로 친숙해진 후에 정식으로 선거를 통해 반장을 선출하려고 한다. 
그는 자기반 학생 중에서 1학년부터 5학년까지 지내오면서 한번이라도 같은 반이었던 사람이 가장 많은 학생을 임시 반장으로 정하려 한다.

-----------------------------------------------------
# 행렬 뒤집기
### 문제
뒤집기 게임의 룰은 다음과 같다.
뒤집기 게임을 진행할 맵과 뒤집기 횟수 N이 주어진다. 이때 맵은 10×10정삭각형 모양의 2차원 배열 형태이면 모든 원소들이 0으로 되어있는 상태이다.
뒤집기 행위는 뒤집을 원소가 1이면 0으로 만들고, 0이면 1로 만든다는 뜻이다.
첫번째 뒤집을 때는 1행의 원소들과 1열의 원소들을 모두 뒤집는다. 두번째 뒤집을 때는 2행의 원소들과 2열의 원소들을 모두 뒤집는다.
마찬가지로 i번째 뒤집을 때는 i행의 원소들과 i열의 원소들을 모두 뒤집는다. 이렇게 총 N번의 뒤집기를 한다. (행과 열의 번호는 1번부터 시작한다.)
N이 주어졌을 때 뒤집기 게임을 모두 시행하고 난 뒤의 맵을 출력하는 프로그램을 작성해보자  


