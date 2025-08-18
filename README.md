# insight-13th
25년도 하반기 13기, 14기 활동 레포입니다.

## 목표
- git 툴에 익숙해집니다.
- pandas를 자유롭게 다룰 수 있습니다.
- 통계 기법에 대해 배우고, 적용합니다.
- 기본적인 ml 툴을 다루며, 적용할 수 있습니다.

## 진행 기간 및 내용
| 회차 | 세션일자 - 과제 마감일 | 내용 |
| --- | --- | --- |
| 0 | 9/1 - 9/3 | OT jupyter&vscode&github |
| 1 | 9/4 - 9/7 | Pandas |
| 2 | 9/8 - 9/10 | EDA&전처리 |
| 3 | 9/11 - 9/14 | 통계 |
| 4 | 9/15 - 9/17 | 회귀 기초 |
| 5 | 9/18 - 9/21 | 회귀 심화 |
| 6 | 9/22 - 9/24 | 분류 |
| 7 | 9/25 - 9/28 | 군집화 |
| 8 | 9/29 - 10/1 | 추천 시스템&연관분석 기초 |
| 9 | 10/2 - 10/5 | 경영으로 보는 데이터사이언스 |

## 진행 방식
- 매 회차별로 "사전 학습", "과제" 두 가지의 과제가 있습니다.
- 사전 학습의 마감일은 해당 세션의 진행일 전날입니다.
- 과제 마감일은 다음 세션의 진행일 전날입니다.

>예시
9/4 Pandas 세션일 기준, 9/7 자정까지 제출해야 하는 과제는 
**"Pandas 과제"** 와 **"EDA 사전 학습"** 두 가지 입니다.

## 진행 방식 상세
### 한 번만 하면 되는 과정
  - 해당 insight 레포지토리(원격)를 본인의 컴퓨터(로컬)로 clone합니다.
    ```bash
    git clone https://github.com/Insight-Sogang-Univ/insight-14th.git
    ```
  
### 과제 제출마다 거쳐야 하는 과정
  - 본인의 브랜치로 전환해 과제를 진행합니다.
    ```bash
    # (0) 현재 브랜치 상태 및 브랜치 위치 확인하기 (원격, 로컬 모두)
    git branch -a

    # (1) 원격 저장소에서 최신 커밋 및 브랜치를 로컬 저장소로 가져오기
    git fetch

    # (2) 원격 브랜치와 동일한 이름으로 로컬 브랜치를 생성하여 해당 로컬 브랜치로 전환하기
    git checkout -t origin/<원격 브랜치 이름>
    ## 예시
    git checkout -t origin/neulbokim-basic-00
    ```
  - `basic/template/`에서 필요한 파일을 복사하여 `basic/<본인 아이디>/` 디렉토리에 옮깁니다.
    ```plain text
    insight-14th
        ㄴ basic
            ㄴ template                 // 미리 업로드 되어 있는 과제 양식
                ㄴ session00
                    ㄴ example.ipynb    // OT 과제 제출 파일
                ㄴ session01
                    ㄴ example.ipynb    // 과제 제출 파일
                    ㄴ example_사전과제.ipynb     // 세션 전 사전 학습 내용 공부 정리 파일
                ㄴ session02
                    ㄴ example.ipynb    // 과제 제출 파일
                    ㄴ example_사전과제.ipynb     // 세션 전 사전 학습 내용 공부 정리 파일
                ...
            ㄴ neulbokim                // 본인 git 아이디
                ㄴ session00
                    ㄴ example.ipynb    // OT 과제 제출 파일
                ㄴ session01
                    ㄴ example.ipynb    // 과제 제출 파일
                    ㄴ example_사전과제.ipynb     // 세션 전 사전 학습 내용 공부 정리 파일
                ㄴ session02
                    ㄴ example.ipynb    // 과제 제출 파일
                    ㄴ example_사전과제.ipynb     // 세션 전 사전 학습 내용 공부 정리 파일
                ...
      ```
  - `basic/<본인 아이디>` 디렉토리 안에서 과제를 진행하고 add, commit, push합니다.
    ```git bash
    # (1) 임시 저장 공간(staging area)에 add
    git add basic/<본인 아이디>/session00/example.ipynb
    ## 예시
    git add basic/neulbokim/session00/example.ipynb

    # (2) 로컬 저장소에 commit: 본인에게 할당된 이슈 번호 확인 후 커밋 메시지 작성
    git commit -m "#3 김현서 Pandas 과제 제출합니다."

    # (3) 원격 저장소에 push
    git push
    ```
  - 과제 마감일까지 본인의 브랜치에서 develop 브랜치로 PR을 보내주세요.


## 폴더 구조
```
insight-14th
ㄴ  README.md
ㄴ  .gitignore
ㄴ  basic                       // 교육 세션
    ㄴ template                 // 미리 업로드 되어 있는 과제 양식
        ㄴ session00
            ㄴ example.ipynb    // OT 과제 제출 파일
        ㄴ session01
            ㄴ example.ipynb    // 과제 제출 파일
            ㄴ example_사전과제.ipynb     // 세션 전 사전 학습 내용 공부 정리 파일
        ㄴ session02
            ㄴ example.ipynb    // 과제 제출 파일
            ㄴ example_사전과제.ipynb     // 세션 전 사전 학습 내용 공부 정리 파일
        ...
    ㄴ neulbokim                // 본인 git 아이디
        ㄴ session00
            ㄴ example.ipynb    // OT 과제 제출 파일
        ㄴ session01
            ㄴ example.ipynb    // 과제 제출 파일
            ㄴ example_사전과제.ipynb     // 세션 전 사전 학습 내용 공부 정리 파일
        ㄴ session02
            ㄴ example.ipynb    // 과제 제출 파일
            ㄴ example_사전과제.ipynb     // 세션 전 사전 학습 내용 공부 정리 파일
        ...
```

## 제출 양식
**`pull request`** 를 보낼 때 아래의 양식을 지켜서 보내주세요!
```
pr 제목 : [session01] 제출자 세션내용 과제 제출합니다.

내용 : 해당 과제를 하면서 어려웠던 점이나 새로 알게 된 점 간단히 정리
```

ex)
```
[session01] 김현서 Pandas 과제 제출합니다.

titanic data를 선택하여 과제를 진행했습니다.
pandas 문법은 아직은 익숙하지 않은 것 같습니다.
하지만 기본적으로 python 문법과 비슷한 점이 많은 것 같아서 어느 정도 빠르게 배울 수 있었던 것 같습니다.

merge, concate 하는 부분이 아직 미숙한 것 같습니다.
앞으로 loc, iloc를 많이 쓸 것 같은데 많이 연습하겠습니다!

질문
titanic에서 3번째 과제를 다음과 같이 했는데, 답을 모르겠습니다ㅜㅠ
```

## 기타
- 사전 과제 필수 키워드에 대해서는 정리/리뷰 하셔야 합니다.
- 사전 학습 정리는 자유 분량입니다.