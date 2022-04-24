# 게임 프로젝트

## 목차
 1) 게임 소개

 2) 게임 개발 환경

 3) 주차별 실행 현황

 4) 게임 관련 아이템 및 함정

 5) 미구현, 추가 구현 이유 설명
 
 6) 주차별 계획
 
### 게임 소개

 게임 이름: Run Slime

 게임 장르: 플랫포머, 퍼즐

 플랫포머: 점프와 이동기를 사용하는 게임을 말한다. 플랫폼이란 발판을 의미하는데 구체적으로 플레이어가 
       캐릭터를 조종하면서 발판 위를 뛰어다니는 점프 컨트롤이 중요한 게임이다.

 퍼즐: 어떠한 규칙 내에서 정해진 행위를 통해 주어진 조건을 완료해 클리어하는 단순한 게임을 지칭한다. 
       게임의 특성상 변수가 전혀 없거나 극히 드물다는 특성이 있다.

#### 플레이 방법:

  1. 이동기 점프(W), 좌우 이동키(A, D)를 이용하여 플레이어 자신을 이동시킨다.

  2. 아이템을 먹고 마우스 좌클릭과, 우클릭를 이용한다.

  3. Space키는 특수키로 이동하는 방향으로 짧게 대쉬를 한다.

  4. 여러 개의 장애물을 피하면서 여럿 문제를 풀어서 목표 지점으로 간다.

  5. 하나믜 맵으로 이루어져 있는 것이 아닌 여러 개의 맵(스테이지)가 있어 여러 맵을 플레이 할 수 있다.

#### 에셋 소개(출처):
  ● 타일맵에 사용 할 에셋 (FREE Pixel Art kit)      
       사이트: https://assetstore.unity.com/
     
  ● 아이템으로 사용 할 에셋 (Jelly Icons)    
       사이트: https://assetstore.unity.com/
     
  ● 플레이어로 사용 할 에셋 (2D Pixel Slime Set)    
       사이트: https://www.gamedevmarket.net/category/2d/
     
  ● 플레이어 대쉬 사운드    
       사이트: https://www.sellbuymusic.com/
     
  ● 인게임 배경 음악 사운드    
       사이트: https://pixabay.com/ko/sound-effects/

<hr>

### 게임 개발 환경

 개발할 엔진: 유니티
 2D 게임 제작이 처음이더라도 다양한 툴을 자유롭게 사용할 수 있고 2D 게임 제작에 중요한 기능의 대부분은 즉시 사용할 수 있거나
 에디터 창에서 쉽게 설치할 수 있기 때문

 게임 관련 에셋: 유니티 에셋 스토어
 여러 종류의 에셋을 무료와 유로로 구매하여 사운드와 이미지파일을 이용하여 게임 에셋을 구할 예정
 원하는 사운드 파일이 없을 경우 freesound.org 같은 저작권 없고 무료로 제공하는 사이트에서 자신에게 맞는 사운드를 사용할 예정

 사용할 언어: 유니티가 기본적으로 C#을 제공하기 때문에 C#을 이용하여 사용함

<hr>

### 주차별 실행 현황

#### 1주차
##### 1) 게임 계획서 작성    
유니티와 언리얼엔진에서 한 가지를 생각하여 자신이 원하는 게임을 만들기 적합한지 알아보고
어떤 장르의 게임을 개발 할지와 모티브, 방법, 개발 환경을 생각한 다음
PPT와 깃허브를 이용하여 게임 개발과 관련된 정보를 정리하였음

#### 2주차
##### 1) 플레이어 이동    
플레이어가 점프키인 W와 좌우 이동키인 A,D를 이용하여 이동하는 것을 구현
![슬라임 움직임과 점프 구현-min](https://user-images.githubusercontent.com/101154683/164979952-f664191d-e3aa-4ec3-b2cc-1b517d17af87.gif)

##### 2) 긴 점프와 짧은 점프    
플레이어가 점프인 W키를 누르면 점프를 하는데    
점프를 살짝 누를 때와 길게 누를 때의 중력 크기를 다르게 하여 구현
![슬라임 낮은 점프와 높은 점프-min](https://user-images.githubusercontent.com/101154683/164979927-4f15dda7-818e-4e11-a2f1-e90694ec944a.gif)

#### 3) 타일맵 추가 후 플레이아와 충돌 처리    
여러개의 타일을 그린 후 플레이어가 해당하는 타일에 충돌시 이동을 하지 못하도록 구현

#### 3주차

##### 1) 플레이어가 움직일때의 애니메이션 추가    
플레이어가 정지하거나 좌우로 이동할때, 점프할 때의 애니메이션을 구현
![슬라임 애니메이션 구현-min](https://user-images.githubusercontent.com/101154683/164979940-3b053033-cbc1-49dd-a11f-5ad1d2fb3b81.gif)

##### 2) 플레이어의 특수키(대쉬)를 구현    
플레이어가 스페이스 바를 누를시 현재 가고 있는 방향으로 대쉬 하는것을 구현
![슬라임 대쉬 구현-min](https://user-images.githubusercontent.com/101154683/164979931-5bf9181d-4c65-4a6f-b58e-6107e3aa4239.gif)

#### 4주차

##### 1) 플레이어가 가시에 충돌 시 뒤로 넉백    
플레이어가 가시에 충돌을 한다면 현재 가고 있는 방향의 반대 방향으로 이동을 하며    
그 동안에는 플레이어가 대쉬나 이동 및 아이템을 사용하지 못하도록 구현    
![슬라임 가시 충돌 넉백 구현-min](https://user-images.githubusercontent.com/101154683/164979925-23d37d32-013c-4e0e-9331-f2a22506a405.gif)

##### 2) 특수 키(대쉬)를 사용 한 후 딜레이를 알리는 UI    
플레이어가 특수 키(대쉬)를 사용을 하면 플레이어의 위에 딜레이 바를 구현    
자신의 특수 키의 재사용하기 까지의 가시성을 부여하였음

##### 3) 아이템 상자 ( 점프 1회 추가)    
플레이어가 해당하는 아이템 상자를 획득(충돌)을 한다면 점프 횟수를 1번 증가시키게 구현    
하지만 아이템 획득 후 바닥과 충돌을 한다면 획득한 후의 점프 횟수는 초기화 됨
![슬라임 아이템 상자 1회성 점프 추가 구현-min](https://user-images.githubusercontent.com/101154683/164979933-406a522c-b98f-4e62-a44b-ed95a792a0bb.gif)

#### 5주차

##### 1) 아이템 상자 스포너    
플레이어가 아이템 상자를 획득 해도 다시 아이템 상자가 생성될 수 있도록 구현    
![아이템 상자 스포너 구현-min](https://user-images.githubusercontent.com/101154683/164979963-5d203e75-8e5d-40cb-a5ca-af3b60c4ac87.gif)

##### 2) 아이템 상자 ( 순간 이동 )    
플레이어가 해당 하는 아이템을 획득 하면 자기 중심으로 8방향으로 순간이동을 하도록 구현      
![순간 이동 아이템 구현-min](https://user-images.githubusercontent.com/101154683/164979920-146ad286-091a-4440-b93d-1a157a109765.gif)

##### 3) 플레이어가 열쇠를 획득 후 문과 충돌    
플레이어가 처음에는 문과 충돌을 하면 문과 부딪혀 이동을 할 수 없지만     
열쇠를 획득한 후 다시 문과 충돌을 하면 문이 사라지면서 이동을 할 수 있게 구현
![슬라임 열쇠 획득 후 문 삭제 구현-min](https://user-images.githubusercontent.com/101154683/164979949-1f2c0bf6-2108-48a6-922b-65838579101e.gif)

##### 4) 플레이어가 폭포와 물에 닿으면 이동속도 감소
플레이어가 해당하는 물에 충돌시 이동속도 감소 구현    
<미구현 사유: 살펴보기>

#### 6주차

##### 1) 배경음악, 대쉬 사운드    
게임을 시작하면 바로 실행이 되며 무한으로 반복하는 배경음악을 설정    
플레이어가 특수 키(대쉬)를 사용하면 나오는 사운드 설정

##### 2) 플레이어의 좌우 이동시 파티클 추가
플레이어가 좌우로 이동할 시 슬라임의 뒷바닥에 달리는 듯한 파티클을 구현
![슬라임 움직일 때 파티클 구현-min](https://user-images.githubusercontent.com/101154683/164979951-1bfeea47-9f16-4f92-91f5-013b15892492.gif)    

##### 3) 움직이는 발판
플레이어가 올라탈수 있고 다른 장소로 이동하기 위해 사용하는 발판 구현
![움직이는 발판 구현-min](https://user-images.githubusercontent.com/101154683/164979967-245495e3-7e16-425d-b920-6d4b371441ec.gif)    
<추가 구현 필요 사유: 살펴보기>

#### 7주차

##### 1) 갈고리 이동    
플레이어가 좌클릭 시 갈고리에 맞는 Tag에 충돌시 갈고리가 걸려 플레이어가     
그 방향을 중심으로 U자로 이동 구현    
![갈고리 구현-min](https://user-images.githubusercontent.com/101154683/164983824-c52d0a21-ebfa-43c7-b2c6-1a91f2f0e9df.gif)    

##### 2) 아이템 상자 ( 갈고리 )    
플레이어가 해당 아이템 획득 시 갈고리를 1회 사용 가능하도록 구현
<미구현 사유: 살펴보기>

<hr>

### 게임 관련 아이템 및 함정 및 발판

#### 1) 아이템
● 점프 아이템: 점프의 횟수를 1회 더 늘려준다. (바닥에 착지하면 횟수는 사라진다.) 
![점프 1회](https://user-images.githubusercontent.com/101154683/164984545-5734f6d6-b618-4079-b67c-c8ea3f1eaecb.png)
    
● 순간이동 아이템: 자신을 기준으로 8방향에서 원하는 위치로 순간이동이 가능하다. 
![순간이동](https://user-images.githubusercontent.com/101154683/164984542-ca872bb5-26c3-4f5d-80ec-8e71a1baa6ea.png)
    
● 열쇠: 문으로 인해 가지 못하는 구간을 열수 있다. 
![열쇠](https://user-images.githubusercontent.com/101154683/164984543-7b34637d-54b3-4d45-8dae-6faef93d5d7e.png)
    
#### 2) 함정 및 발판
● 가시: 플레이어가 충돌한다면 자신이 가고 있던 방향의 정반대로 넉백하며    
    바닥에 착지를 할 동안 아이템 및 이동을 할 수 없다. 
    ![가시](https://user-images.githubusercontent.com/101154683/164985020-e31e0cac-445a-438f-99f0-1a9efa3a1359.png)
    
● 발판: x축과 y축으로 이동하는 발판으로 가지 못하는 구간을 움직이는 발판으로 이동 할 수 있다. 
![발판1](https://user-images.githubusercontent.com/101154683/164985022-e1022c66-3e4d-4fbc-8b3a-d5df215e0d4d.png)  ![발판2](https://user-images.githubusercontent.com/101154683/164985023-b062222d-0f43-403b-a28e-68212d311f8f.png)
    
<hr>

### 미구현, 추가 구현 이유 설명

<hr>


### 주차별 계획 
#### (주차별 실행 현황에 자세히 있으므로 간략하게 생략하였음)

1주차: 게임프로젝트 계획서 작성

2주차: 플레이어 이동 구현, 길고 짧은 점프 구현, 타일맵 추가 후 충돌 처리

3주차: 플레이어 애니메이션 추가, 대쉬 키 구현

4주차: 가시 구현, 대쉬 딜레이 UI 구현, 점프 1회 아이템 구현

5주차: 아이템 스포너 구현, 순간이동 아이템 구현, 문과 열쇠 구현

6주차: 배경음악과 대쉬 사운드 구현, 이동 파티클 구현, 발판 구현

7주차: 갈고리 구현, 갈고리 아이템 구현

8주차: 중간고사

9주차: 

10주차: 

11주차: 

12주차: 

13주차: 

14주차: 

15주차: 기말고사

