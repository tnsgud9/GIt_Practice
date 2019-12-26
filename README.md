# GIt_Practice
-----
### Git 사용 연습용

의도 : GITHUB와 Git을 통해 어떻게 깃을 사용하고 
부가기능까지 실습.

시작 : 2019-12-26    8:50 PM


![](http://m.quickmeme.com/img/75/7509f68823389e4af3777ca6d3744c632cc32ab3547bc56e319126aa29ab149a.jpg)

----
## 시작 전 준비
터미널 방식의 Git을 처음 사용할 때는 처음의 사용자 정보를 입력해야 합니다.
<code>
  git config --global user.email "you@example.com"
  
  git config --global user.name "내 이름"
</code>
계정의 기본 신원 정보를 설정합니다.
--global 옵션을 빼면 이 저장소서만 신원 정보를 설정합니다.


----

## 기본 명령 이해하기
출처 : midas@jehun.com
### git init

- git을 사용하는 초기 환경을 만들어줍니다
- 이 명령이 실행되면 git의 시작점으로 인식합니다

### git status

- 현재 로컬 저장소의 상태를 확인합니다
- 변경된 파일과, 관리되지 않는 파일의 목록을 확인할 수 있습니다
- 커밋이 안 된 경우에 메시지들이 표시되고, 아닌 경우 메시지를 표시하지 않습니다

### git add

- git이 관리하는 파일을 추가합니다
- 파일의 경로를 정확하게 입력해야 하기 때문에 보통 git add * 로 모든 파일을 포함하게 합니다
- 포함하지 않아야 하는 파일들(node_modules 등)은 .gitignore에 추가해야 합니다
- git add -f 파일명 -> gitignore 무시
### git diff

- 변경된 내역을 표시합니다

### git clone

- 다른 사람이 만든 repository의 내용을 받아올 때 사용됩니다

### git pull

- 현재 내 코드를 기준으로 변경된 내용을 받아 옵니다
- 반드시 commit 전에 먼저 사용합니다
    - 안그러면 conflict가 발생할 확률이 높습니다

### git commit

- 작업 내역을 저장합니다
- 습관적으로 git commit -a -m "작성할 메시지" 의 형태를 사용하도록 합니다
- 이 명령어 전에는 반드시 git pull명령을 실행합니다

### git push

- 코드를 repository에 전송합니다
- conflict가 있는 경우에 전송되지 않기 때문에 주의합니다
- git push origin master

### git reset

- 특정한 브랜치로 코드를 동일하게 세팅
- 