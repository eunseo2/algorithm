# 정렬
### 선택정렬
- 최솟값을 앞으로 이동시킴 기준: 오름차순
- 최소값 찾기 위해 : o(n)걸림
- 최소값을 n번 찾아야 함.
- o(n^2)
- n이 만개까지만 가능하다!

### 삽입정렬
- 원소를 차례대로 정렬된 배열에 삽입시킴
- |뒤에 있는 원소를 앞으로 자리를 찾아서 삽입시킴.
- o(n^2)

### 버블정렬
- 인접한 원소를 비교하여 큰 수를 뒤로 보냄 
- o(n^2)
```
def BubbleSort(a):
  for i in range(len(a)-1,0,-1):
    for j in range(0,i):
      if a[j]>a[j+1]:
        a[j],a[j+1]=a[j+1],a[j]
```

# 시간복잡도
* 프로그램이 대략적으로 몇 개의 명령을 수행하는가?
* 항상 최악일 때를 가정함
* 대부분 반복문이 시간복잡도를 결정함
* 수행시간 O(n) < O(n^2) O(n)이 훨씬 빠름!!

# 수행시간을 어림짐작하기
* 대략 1억번의 연산을 수행하면 1초가 걸린다.
* O(n) n=1억 -> 1초
* O(n^2) n=1만 -> 1초  ex n=10만이면 제한시간 넘는다. n이 10만일때 n^2으로 짜면 안된다!

# 기초정수론
* 정수론
  - 정수의 성질을 연구하는 분야
  - 약수와 배수
* 소수(prime number)
  - 약수가 1과 자기 자신뿐인 정수
  - bool flag = false 이용
  
```
for i in range(2,N)
  if n%i ==0 :
    flag=true
  if flag==true:
    print('소수 아님')
  else:
    print('소수')
```
### 에라토스테네스의 체
  - 소수를 구하는 방법 중 하나
  - O(nlogn)
  - 1~N 까지 모든 소수를 구할 때 쓰는 
```
n = 123456*2+1
prime = [1]*(n)
prime[0] = 0
prime[1] = 0
for i in range(2, n):
  if prime[i]==1:
    for j in range(i*2, n, i):
      prime[j] = 0
while 1:
  x = int(input())
  if x == 0:
    break
  cnt = 0
  for i in range(x+1, x*2+1):
    if prime[i] == 1:
      cnt+=1
 
  print(cnt)
```

### 소인수분해(Prime factorization)
  * 숫자 N을 소수의 곱으로 나타냄.
  * 소수의 리스트를 꼭 알 필요 없다. 다만, 소수의 리스트를 알면 더 빠르다.
  * 모든 정수에 대해 나누는 방법 써도 됨
```
for(int i=2; n>1;){
  if(n%i==0){
  
    print(i)
    n/=i;
  }
  else i++; -> 여기서 i++을 해야 함 for문안에 쓰면 2 두번 못나누니까 ex)20 2*2*5
}
```

### 공약수와 공배수
  -최대공약수(GCD)
  -최소공배수(LCM)
  
* 유클리드 호제법
  - 최대공약수를 구하기 위한 알고리즘
  
# 파스칼의 삼각형
  - 3C2 =3 
  - 5C3=10
  - 파스칼의 삼각형은 조합이랑 동일함.
  - 20C12 = xxxxxxx123 끝에 몇자리를 알려달라고 문제에서 나왔을 때 나눗셈 없이 파스칼의 삼각형으로 구할 수 있음
  - 20C11 = 20!/11!9!
# 벌집문제 -beehive
- 1(+6) 7 (+12) 19 (+18) 37 (+24) 61 

# streetree
- 가로수의 간격들의 최대 공약수를 구하는 것이 핵심!
```
def GCDofTwoNumbers(a,b):
  while b !=0:
    a,b=b,a%b 
  return a 

GCDarr = arr[0]
for i in range(len(arr)):
  GCDarr=GCDofTwoNumbers(GCDarr,arr[i])

print(GCDarr)

```


