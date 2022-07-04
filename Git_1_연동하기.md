
## Git 원격 저장소(GitHub)와 로컬 저장소 연동하기.
<br>

[이전 글 9번](https://github.com/Sayh0/Manual/blob/main/Git_%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0%2Ccommit.md) commit을 완료한 부분에서부터 시작.
<br>
![177078856-195d1ab0-d4f4-42cb-bccd-7df374633a53](https://user-images.githubusercontent.com/96712990/177122475-b1a1105f-c51f-4f41-b43d-8cb7c59fb03b.jpg)
<br>
*nothing to commit, working tree is clean 메세지 확인.*
<br>
<br>

1. 연동할 원격 저장소를 생성하자. 깃허브 계정의 repositories 부분을 클릭하여 new repository를 생성한다. <br>
원래 있던 repository를 사용해도 무방하다.<br>
![image](https://user-images.githubusercontent.com/96712990/177122647-5786600f-d624-46ef-adb0-fa6564abec01.png)<br>

![image](https://user-images.githubusercontent.com/96712990/177122958-aa405528-bcbc-4e9b-a8c8-5e11d37d6237.png)<br>

![image](https://user-images.githubusercontent.com/96712990/177123075-aed6ed44-158a-4e35-b9cd-0a4313d4f8b6.png)<br>
<br>
2. 생성한 repository의 주소를 복사한다.<br>
![image](https://user-images.githubusercontent.com/96712990/177123455-b6652435-c586-4b47-99b9-515b1916742d.png)

3. git 커맨드를 다음과 같이 입력한다.
```
git remote add origin https://github.com/Sayh0/test_repo.git
```
*[https://github.com/Sayh0/test_repo.git] 부분은 repository 주소를 입력한다.*<br>
<br>
![image](https://user-images.githubusercontent.com/96712990/177124179-4fe162fe-7d94-4e1b-830e-4bba9bcd4201.png)
<br>
<br>
4. 마지막으로 push 커맨드를 다음과 같이 입력하면 연동 완료.
```
git push -u origin main 
```
![image](https://user-images.githubusercontent.com/96712990/177124446-29f4cf96-8f21-4242-beb9-a0c39e00be6e.png)<br>
*연동 완료*

