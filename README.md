# 조사내용 README파일로 정리하기
<div style="text-align: left"> 광기술 공학과 20161682 최은창 </div>

## top, ps, jobs, kill 명령어</br>

* ### top 명령어 

top는 실시간으로 CPU 사용률을 체크해주는 명령어이다. 윈도우에서 작업관리자와 비슷한 역할을 한다고 생각하면 된다. top 명령어는 주로 리눅스를 사용하는 서버의 성능이나 현재 돌아가고 있는 상황을 볼 때 사용한다.

사용법
사용법은 간단하다. 리눅스에서 top 명령어를 치고 들어가면 된다.

` $ top `

<img width="1920" alt="그림1" src="https://user-images.githubusercontent.com/83526046/169364524-00cca6d8-3621-44db-bc6e-acb65ba53532.png" >


위 그림처럼 top명령어는 밑줄친 부분으로 나눠서 윗부분과 아랫부분으로 나누어 볼 수 있다. 

윗 부분은 주로 현재 시스템의 상태를 보여주는데, 시스템 시간이나 uptime 등을 확인 해 볼 수 있고

아랫부분은 현재 실행하고 있는 프로세스 현황을 볼 수 있다.

#### Top 정보 시스템 내용

13:47:52 : 현재 서버의 시간

9 day, 5:24 : uptime(켜져있는시간)

3 users : 유저

load average : 현재 시스템이 얼마나 일을 하고 있는지 1분, 5분, 15분 단위로 실행/대기 중인 프로세스 수를 나타내고 있음 

tasks : 프로세스 개수

CPU

%us : 유저레벨에서 사용하고 있는 CPU 비중

%sy : 시스템 레벨에서 사용하고 있는 CPU 비중

%id: 유휴 상태의 CPU 비중

%wa : 시스템이 I/O 요청을 처리하지 못한 상태에서의 CPU idle 상태인 비중

KiB Mem, Swap : 각 메모리의 상태 정보

#### 프로세스 

PID : 프로세스 ID (PID)

USER : 프로세스를 실행시킨 사용자 ID

PRI : 프로세스의 우선순위(priority)

NI : NICE 값, 일의 nice valuce값이다. 마이너스를 가지는 ncie value는 우선순위가 높음.

VIRT : 가상 메모리의 사용량(SWAP+RES)

RES : 현재 페이지가 상주하고 있는 크기(Resident Size)

SHR : 분할된 페이지, 프로세스에 의해 사용된 메모리를 나눈 메모리의 총합.

S : 프로세스의 상태 [S(sleeping), R(running), W(swapped out process), Z(zombies)]

%CPU : 프로세스가 사용하는 CPU의 사용율

%MEM : 프로세스가 사용하는 메모리의 사용율

COMMAND : 실행된 명령어

#### Top 명령어 옵션
Top 명령어 실행중에 추가 사용 가능함

shilt + p : CPU 사용률이 높은 프로세스 순서대로 표시

shift + m : 메모리 사용률이 높은 프로세스 순서대로 표시

shift + t : 프로세스가 돌아가고 있는 시간 순서대로 표시

k : 프로세스 kill - k 입력 후 종료할 PID 입력 signal을 입력하라고 하면 kill signal인 9를 입력

a : 메모리 사용량에 따라 정렬

b : batch 모드 작동

c : 명령행/프로그램 이름 토글

d : 지연 시간 간격은 다음과 같다 -d ss. tt(seconds.tenths)

h : 도움말

H :스레드 토글

i : 유휴 프로세스 토글

m : VIRT/USED 토글

M : 메모리 유닛 탐지

n :  반복 횟수 제한 : -n number

p : PID를 다음과 같이 모니터 : -pN1 0pN2 ... or -pN1, N2[,...]

s : 보안 모드 작동

S : 누적 시간 모드 토글

u : 사용자별 모니터링 : u somebody

U : 사용자별 모니터링 : U somebody

u : 입력한 유저의 프로세스만 표시 which u

숫자 1 : CPU Core별로 사용량을 보여준다.

* ### ps 명령어 

ps명령어는 현재 실행중인 프로세스 목록을 보여준다

` $ ps -[옵션] `

-e : 모든 프로세스를 출력해준다.

-f : 풀 포맷으로 보여준다(UID, PID등)

-l : 긴 포맷으로 보여준다

p, -p : 특정 PID의 프로세스를 보여준다.

-u : 특정 사용자의 프로세스를 보여준다.




## vim 에디터에서 매크로 활용방법
