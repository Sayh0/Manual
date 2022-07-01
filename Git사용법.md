git 설치
https://git-scm.com/



2. git 사용자 설정 (git 설치후 최초 한번만 설정하면 된다)


>git config --global user.name "사용자이름"
>git config --global user.email "이메일 주소"
3. local 저장소 생성

>git init 

4. 현재 저장소의 상태 알아보기

>git status

5. 변경 사항을 staging area (Index) 에 올리기

>git add .

 6. staging area 에 있는 내용을 commit 하기 
   (변경 사항의 snap shot 이 있는 staging area 의 내용을 local 저장소에 snap shot 으로 저장하기 )

>git commit -m "commit 메세지"

7. 새로운 branch 만들기

>git branch 브랜치명

8. branch 목록 보기

>git branch

9. branch 이동

>git checkout 브랜치명
or
>git switch 브랜치명 

10. branch 합치기(merge)
브랜치를 합치고 싶은 브랜치로 checkout 한 다음 합칠 브랜치를 merge 한다.  

>git merge 브랜치명 

- 합칠때 충돌이 나면 자동 merge 가 안된다.
- 충돌나면 충돌을 해결후  다시  add , commit 을 하면 merge 완성된다. 


11. branch 삭제

>git branch -d 브랜치명 

12. 커서(HEAD) 를 이전 commit 으로 이동하기 ( ~ 갯수만큼 뒤로 간다. )

>git  checkout  HEAD~

13. commit 취소 하기

옵션 : --hard , --soft , --mixed

--hard : working dir, staging area, commit 모두 취소
--soft : commit 취소
--mixed: staging area, commit 취소


>git reset 옵션 HEAD~

14. 작업하던 내용 임시 저장 및 관리

- 추적되지 않는 파일을 제외하고 변경사항 저장
>git  stash  save

- 추적되지 않는 파일도 포함해서 변경사항 저장
>git  stash  save  -u

- 저장된 변경사항을 지우면서 적용 시키기
>git  stash  pop 


- 저장된 변경사항을 유지하면서 적용 시키기
>git  stash  apply  [ stash id ]

- 저장된 변경사항을 삭제하기
>git  stash  drop  [ stash id ]

- 저장된 변경사항 목록 보기 
>git  stash  list

15.  추적하고 있는(commit 한적이 있는 파일) 파일에 대한 변경 사항 복구(취소)하기

-특정 파일만 복구 (add 된 파일은 복구가 안된다)
>git  restore  파일명

-모든 파일 복구  (add 된 파일은 복구가 안된다)
>git  restore  .

-특정 파일 add 취소 
>git  restore --staged  파일명



16. untracked file 과 directory 를 모두 삭제하기

>git  clean  -fd

17. reset 하기 바로 이전 상태로 돌아가기
ORIG_HEAD : reset 바로 직전의 HEAD 가 가리키던 commit 

>git reset --hard ORIG_HEAD

18. add 된 모든 내용 취소

>git reset
or
>git  restore  --staged   .


19. 최근 commit 을 취소하는 commit 

>git revert HEAD


20. remote 저장소 목록 보기

>git remote -v

21. remote 저장소 등록

>git remote add  저장소이름   저장소주소

예)
>git remote add origin https://github.com/oli999/test14.git

22. 등록된 remote 저장소에 업로드 하기

>git push -u  저장소이름  브랜치명

예)
>git push -u origin master




23. remote 저장소 복사하기

>git clone  저장소주소 

예)
>git clone https://github.com/oli999/test14.git


24. remote 저장소의  특정 branch 의 최근 commit 내려받아서 병합하기

>git  pull  origin  브랜치명

예)
>git  pull  origin  master

25. local 에 등록된 remote 저장소 정보 삭제

>git  remote  remove   저장소 이름

예)
>git  remote  remove  upstream

26. local 에 등록된 remote 저장소 이름 바꾸기 

>git  remote  rename  원래이름   바꿀이름

예)
>git  remote rename  upsteam   upstream
  
27. remote 저장소에 있는 특정 브랜치 commit 내려 받기

>git fetch  저장소이름   브랜치명

예)
>git  fetch  origin  master 

28. remote 저장소에 있는 모든 브랜치  commit 내려 받기

>git  fetch  --all   저장소이름

예)
>git  fetch  --all  origin

29.  remote 저장소에서 내려받은 브랜치에서  시작하는 수정할수 있는 새 브랜치 만들기

>git  checkout  -b    새브랜치명    트래킹브랜치명

예)
>git  checkout -b  lab1    origin/lab1






30.  remote 브랜치 삭제( git hub 에 존재하는 브랜치 삭제 )

>git   push   저장소이름   :삭제할브랜치명

예)
>git  push  origin   :lab1



