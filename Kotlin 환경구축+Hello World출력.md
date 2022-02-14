# 구축 순서
1. 자바JAVA JDK 설치<br>
1-1. 안정성을 위해선 JAVA 8 버전이 권장된다고 함. 인터넷 친구들 거의 모두 zulu 설치를 권장하므로 따라가보도록 한다.<br>
1-2. https://www.azul.com/downloads/?package=jdk 에서 자바 8 윈도우용 버전에 해당하는 8u322b06 설치.<br>
1-3. **중요** : 설치 경로를 메모해 두어야 한다. 이후에 경로를 환경변수에 추가해야 하기 때문이라고 함. 나는 `C:\Program Files\Zulu\zulu-8\` 에 설치.<br>
1-4. 설치 후 `제어판\모든 제어판 항목\시스템` 으로 이동해서 왼쪽 위 `고급 시스템 설정\고급\환경변수` 클릭. 시스템 변수 아래에 있는 새로 만들기 클릭. 변수 이름은 `JAVA_HOME`, 변수 값은 메모해둔 설치 경로인 `C:\Program Files\Zulu\zulu-8\` 기입 후 확인 클릭. <sup id="a1">[1](#f1)</sup><br>
1-5. 시스템 변수 목록에 있는 Path 변수를 선택하고 편집을 클릭. 이후 새로 만들기 버튼 클릭 후 ` %JAVA_HOME%\bin` 입력<sup id="a1">[2](#f1)</sup> 하면 환경변수 추가 작업 완료.<br>
<br><br>
2. IntelliJ IDEA 설치   
이미 설치되어 있으므로 넘어간다. Community 버전으로도 Kotlin을 이용한 개발엔 문제가 없다고 함. 이미 Ultimate 버전이 설치되어 있음.<br>
Community 버전 설치는 www.jetbrains.com/idea/download/#section=windows 에서 가능함.<br>
<br><br>
3. IntelliJ 실행 후 New project 생성 시 코틀린 설정 후 실행.<br>
<br><br>
*****
### IntelliJ에서 Kotlin으로 프로젝트를 생성하여, "Hello Kotlin" 출력해보기
*****

1. IntelliJ에서 File > New > Project 선택.<br>
2. 왼쪽 메뉴에서 Java 선택. Project SDK는 위에서 설치한 1.8 ver 선택. 아마 맨 밑에 Detected SDK 해서 C:\Program Files\Zulu\zulu-8\ 경로를 선택할 수 있을 것<sup id="a1">[3](#f1)</sup>.<br>
3. 프로젝트 이름 입력 후 Finish. 우선 프로젝트 이름은 HelloWorld로 기입.
4. 프로젝트 빌드 후 `HelloWorld\src` 위치에 마우스 오른쪽 클릭 new > Kotlin Class/File 선택. File 선택, 상단에 HelloWorld 입력<sup id="a1">[4](#f1)</sup>.
5. 아래 소스 코드 입력.
```
fun main(args: Array<String>){
    println("Hello World")
}
```
6. 상단 메뉴에서 Run > Run > HelloWorldKt 선택.
7. 하단 Run에 Hello World가 출력된 것 확인 가능.
![kt3](https://user-images.githubusercontent.com/96712990/153898543-c6ef6fee-9909-4b5e-8d9d-9fc73426305f.JPG)
<br><br><br><br>
*****
*각주*<br>
<b id="f1"><sup>1</sup></b>  ![systemvariables](https://user-images.githubusercontent.com/96712990/153868239-dd11be08-f9b7-44f8-8dd1-7223ffc796fb.JPG)[↩](#a1)   
<b id="f1"><sup>2</sup></b>  ![systemvariables2](https://user-images.githubusercontent.com/96712990/153885532-9d879694-269e-4ff6-a533-61fbf2cb648b.JPG)[↩](#a1)<br>
<b id="f1"><sup>3</sup></b>  ![kt1](https://user-images.githubusercontent.com/96712990/153892997-a93f6c26-94fc-4a6d-b1d0-6700e7717e97.JPG)[↩](#a1)<br>
<b id="f1"><sup>4</sup></b>  ![kt2](https://user-images.githubusercontent.com/96712990/153897901-85047bbe-eed3-48eb-9174-0462dcefe2ae.JPG)[↩](#a1)<br>

