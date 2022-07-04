
1. 사용자 설정을 한다. git 설치 후 최초 한번만 하면 된다.
<br>

```
git config --global user.name "사용자이름" 
git config --global user.email "이메일 주소"
```
![0  confing username](https://user-images.githubusercontent.com/96712990/176862340-9a573d3c-707e-4396-a8a8-f7d748c328d9.JPG)
<br>
*적용 모습*
<br>
<br>
2. local 저장소를 생성하자.
<br>
```
git init
```

![1  git init](https://user-images.githubusercontent.com/96712990/176862727-0384f82e-09e7-47be-b74a-d7d3dbd862ec.JPG)
<br>
<br>
3. 생성 후 현재 상태를 확인하려면 git status를 입력한다.<br>
```
git status
```
![2  git status_nocommityet](https://user-images.githubusercontent.com/96712990/176862834-2da08539-41a3-4f59-a453-75adbfb8a844.JPG)<br>
*현재는 아무것도 하지 않은 상태여서 no commit yet이라고 출력된다.*
<br>
<br>
4. add 로 파일을 git에 업데이트해보자.<br>
```
git add 파일명.확장자
```
하나의 특정한 파일이 아닌 전부 올리고 싶다면
```
git add .
```

![3  git add(only onefile)](https://user-images.githubusercontent.com/96712990/176862984-ac44a14c-d341-4bde-923a-87cc8215077b.JPG)<br>
*우선 파일 하나만 업로드(보통은 git add .를 쓰긴 함)*
<br>
<br>
5. add 후 status 해보면 파일이 add된 것을 확인할 수 있다.
<br>
![4  status_after_add)](https://user-images.githubusercontent.com/96712990/176863150-0dec50d1-5e79-4429-a89c-1e0c35132b75.JPG)
<br>
<br>
6. add 후 해당 파일을 commit해보자.
<br>
```
git commit -m "commit 메세지"
```
*메세지 부분에는 변경 내역이나 체크해두어야 할 내용을 기록한다.*
<br>
![5  git commit -m](https://user-images.githubusercontent.com/96712990/176863393-fd3f50f1-1ce0-4552-8c0a-b49fe05b7ed1.JPG)<br>
*index.html 이라는 파일을 추가했음을 기록하였다.*
<br>
<br>
7. commit 후 status를 다시 확인하면 working tree 가 clean 한 것을 확인할 수 있다.
<br>
![7 git status(after modifying file)](https://user-images.githubusercontent.com/96712990/176863818-4f13f532-15b9-4abc-a432-df1cb0cb9a05.JPG)
<br>
*수정내역이 없음을 의미한다.*
<br>
<br>
8. 파일 추가 / 수정 후 add 없이 commit 을 진행하려고 하면 오류가 발생한다. add > commit 순서를 기억하자.
<br>
![8  add 없이 commit 했을 경우 오류](https://user-images.githubusercontent.com/96712990/177077528-ee15a4cf-53be-4bbd-a084-fe83775bba6c.JPG)
<br>
*수정내역이 있음을 빨간 글씨로 알려주고 있다.
<br>
9. add 후 다시 commit 을 진행하면 정상적으로 진행되는 것을 확인할 수 있다.
<br>
[9  add 후 다시 commit 결과](https://user-images.githubusercontent.com/96712990/177077714-69124697-47ba-4bbc-bd1b-00f76344bfc9.JPG)
<br>
<br>
10. git log 커맨드를 입력하면 commit의 기록을 확인할 수 있다.
<br>
![10  git log](https://user-images.githubusercontent.com/96712990/177078142-b8e18c77-ad9c-4499-903f-26a2f7627ed2.JPG)
<br>
*그동안 수정했던 파일의 기록 확인 가능
<br>
![11  log에서 각 commit의 식별자  보통 너무 길어서 앞의 7자리만 씀](https://user-images.githubusercontent.com/96712990/177078760-a83fcb3c-8332-4ab8-a1cd-be3fe0add7c6.JPG)
<br>
*각 commit 의 식별자를 확인할 수 있다. 보통 길어서 앞의 7자리만 쓴다.


