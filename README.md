# 최종은 master


### 커밋 메세지 & 풀 리퀘스트 작성 요령
- 커밋메세지에 어느 부분 작업 했는지 간단히작성(로그인, 메인페이지, 예약페이지, etc..)
- 풀리퀘스트 요청 시(pull requests)어떤 페이지에 어떤 작업을 했는지 조금 더 자세히 작성(메인페이지 로고 변경, 로그인 모달창 작업, 폰트(굴림체)로 변경 , etc)  
### 작업 전 할 일
### 참고
 - 올리는 순서   : add -> commit -> push(원격저장소)
 - 내려받는 순서 : merge <- fetch(원격저장소) : fetch + merge = pull
 - 리모트(remote) : 원격저장소의 이름 (origin, upstream 등)
 - 브랜치(local branch) : 원격저장소의 저장되는 폴더 이름 (master, main 등)
 - [깃 구조](https://ibb.co/ZJQT936) (click!)
  
#### 깃 배쉬로 해당 프로젝트 안까지 들어온다 예) e:/폴더/.../projects/futsal
  1. 모든 파일 저장 후 커밋 할 내용 추가(stage:스테이징한다)
   -git add .　　　　　　　　　　　　　　　　　　　　　<- . 은 모든 파일을 뜻함, 명시해도 됨
  2. 커밋 메세지 작성
   - git commit -m ' '　　　　　　　　　　　　　　　　<- ' ' 안에 메세지 작성
  3. 깃허브(원격 저장소)에서 커밋 확인
   - git fetch
  4. 자료를 받으려는 브랜치로 이동
   - git checkout 브랜치이름　　　　　　　　　　　　　<- 안해도 되는 걸로 아는데 일단 이렇게 해주세요 확인해볼게요
  5. 본인 컴퓨터에 자료물을 합친다(로컬로 불러온다)
   - git merge 브랜치이름
  
  위 1,2,3번 대신  
  　 6. pull로 받는다 !조건 이전모든 작업이 푸쉬완료 되있어야 함 즉, 변경된 사항이 없어야한다
 　  - git pull 리모트이름 브랜치이름　　　　　　　　<- 예) git pull origin master 
  
 ---
  
### 깃허브에 저장(원격 저장소에 올리기)
#### 깃 배쉬로 해당 프로젝트 안까지 들어온다 예) e:/폴더/.../projects/futsal
#### 푸쉬받을 브랜치로 변경
 1. 모든 파일 저장 후 커밋 할 내용 추가(stage:스테이징한다)
  - git add .　　　　　　　　　　　　　　<- . 은 모든 파일을 뜻함, 명시해도 됨
 2. 커밋 메세지 작성
  - git commit -m ''　　　　　　　　　　<- '' 안에 메세지 작성\
 3. 원격 저장소에 올린다
  - git push 리모트이름 브랜치이름　　　<- 예) git push origin master
  
 ---
  
### 원격저장소 복제(최초 1회만 권장)
 1. 레퍼지토리 사용권한을 받는다
 2. code의 깃허브 주소 복사
 3. 깃 배쉬로 프로젝트를 저장할 위치로 이동 예) e:/폴더/.../projects
 4. 복제(git init, git remote 설정 안해도 됨)
  - git clone 원격저장소주소 프로젝트담을폴더이름
    
---
  
### 참조 명령어
 1. 브랜치 생성 및 이동
  - git checkout -b 브랜치이름
 2. 브랜치 이동(브랜치가 존재할 경우 사용)
  - git switch 브랜치 이름　　　　　　<- git checkout 브랜치이름
 3. 브랜치 확인
  - git branch -a[-v]  
#
 4. 임시저장
  - git stash　　　　　　<- 커밋이 불필요할 때 / 다른작업을 해야할 때
 5. 임시저장 목록
  - git stash list
 6. 임시저장 불러오기
  - git stash apply
  - git stash apply 임시저장이름  
#
 7. 리모트이름 변경
  - git remote set-url 변경할리모드이름 새로운원격저장소주소
 8. 리모트 추가
  - git remote add 리모트이름 원격저장소주소　　　　<- 삭제는 add 대신 remove
 9. 리모트 확인
  - git remote -v
#
 10. 받은 커밋취소
  - git reset --hard 리모트이름/브랜치이름　　　　　<- 같은 공간을 작업했을 시 충돌이 일어난다, 그때 사용
 11. 깃 상태 확인
  - git status
 12. 커밋 로그 확인
  - git log
 13. 커밋 충돌위치 확인
  - git diff
