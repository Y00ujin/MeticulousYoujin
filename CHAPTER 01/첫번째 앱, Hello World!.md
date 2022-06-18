## 1.1 첫번째 앱, Hello World!
##### 화면에 버튼을 두고 이것을 터치하면 Hello World!가 표시되는 단순한 앱을 만들어 보겠습니다.

<br>
<br>

## 1.1.1 Xcode 프로젝트 생성
##### 앱을 클릭하면 나타나는 시작화면에서 신규 프로젝트 생성(Create a new Xcode project)을 선택합니다.


<p align="center"> 
<img width="514" alt="스크린샷 2022-06-08 오후 3 05 03" src="https://user-images.githubusercontent.com/71479613/172543875-1f653939-f6f3-4e16-b375-244cf2c7e226.png">

<p align="center">
<font size="2em">
Xcode 앱 클릭 시 프로젝트 창이 켜지고 위와 같은 창이 안나온다면, <br>프로젝트 창을 끈 후 Xcode 앱을 한번 더 클릭하면 시작 창이 나타나요!
</font>
</p>
</p>

<br>
<br>

##### 이미 Xcode가 실행되어 있는 상태라면 Xcode의 컨텍스트 메뉴에서 File, New, Project를 선택하면 위의 방법 대신 프로젝트를 생성할 수 있습니다.
<br>

<p align="center"> 
<img width="452" alt="스크린샷 2022-06-08 오후 3 35 03" src="https://user-images.githubusercontent.com/71479613/172548244-25681a4b-03c5-43a2-8d81-2bb734f2a631.png">
</p>

<br>
<br>


##### 그 다음으로는 프로젝트와 템플릿을 선택해야합니다. <br>이를 위한 화면은 상단과 하단으로 나누어져있으며 상단에서는 제작할 어플리케이션의 OS환경을 선택하고, 하단에서는 애플리케이션에 적용할 템플릿을 선택할 수 있습니다.

##### 상단의 OS목록에는 애플에서 제공하고있는 기기들의 OS가 나열되어있습니다. 아이폰용 프로그램은 iOS를, macOS용 프로그램은 macOS를 선택하면 됩니다.

##### 우리는 아이폰용 앱을 만들 것이기 때문에 iOS와 App을 선택한 후 Next 버튼 또는 엔터를 클릭합니다.
<p align="center"> 
<img width="578" alt="스크린샷 2022-06-08 오후 3 55 00" src="https://user-images.githubusercontent.com/71479613/172551628-0451e900-54ac-4f05-b8d1-4bc84fbd4bf7.png">
</p>

<br>
<br>

##### 이번에는 프로젝트의 정보를 입력할 차례입니다. 프로젝트 생성을 위한 정보 몇 가지를 입력해야 합니다. 아래는 현재 화면에 표시된 항목들입니다.

- ###### Product Name : 우리가 만들 프로젝트 이름, 이 이름은 앱의 고유 식별 코드인 Bundle Identifier(번들 아이디)를 만드는 요소로 사용되므로, 적절한 이름을 입력해주어야 합니다.
- ###### Product Name : 애플 개발자 계정으로 생성된 인증서를 선택하는 부분입니다. 앱 스토어에 앱을 등록하거나, 인하우스 방식으로 배포할 앱을 빌드하기 위해서는 그에 맞는 인증서가 필요합니다. 이 항목에서 애플 개발자 사이트에서 발급받은 인증서를 선택할 수 있습니다. 개발자 계정이 없다면 우선은 'None'을 선택하도록 합니다.
- ###### Organization Name : 본인이 소속된 조직명 이름, 원하는 이름으로 작성하면 됩니다.
- ###### Organization Identifier : 프로젝트 운영 기관 또는 조직의 식별값을 입력합니다. 대체로 소속 회사나 해당 프로젝트의 도메인에서 www를 뺀 나머지를 역순으로 사용합니다. 예로 www.youjin.com라면, Organization Identifier는 com.youjin과 같은 형식으로 작성합니다. 이 값은 앞선 Product Name 과 연결되어 Bundle Identifier가 됩니다.
- ###### Bundle Identifier : 앱의 고유 식별 코드입니다. 이 항목은 Organizaiton Identifier + Product Name 항목으로 자동 구성되기 때문에 우리가 편집할 수 없습니다. 
- ###### Language : 앱을 제작할 개발 언어를 선택하는 항목입니다. Objective-C와 Swift 두 가지 옵션이 있습니다. 저희는 Swift를 선택합니다.
- ###### Use Core Data : 최근엔 서버에 데이터를 저장해두고 네트워크를 통해 데이터를 받아오는 방식이 일반화되어있지만, 때에 따라서는 기기 내부의 저장소에 데이터를 저장해야 할 경우도 있습니다. 이 때 데이터 저장을 지원하는 객체인 코어 데이터를 사용할지를 선택하는 옵션입니다. 이 옵션을 선택할 시 코어 데이터를 사용하기 위한 기본 템플릿이 프로젝트에 추가되므로 좀더 편리합니다. 하지만 소스 코드의 복잡도를 높이는 문제가 있으므로 여기에서는 선택을 해제합니다.
- ###### Include Unit Tests : 소프트웨어의 품질 관리를 위해 최근 프로그래밍에서는 애플리케이션에 대한 반복적이고 단조로운 기능 테스트 과정을 줄이는 대신, 자동으로 테스트하고 결과를 검사해볼 수 있는 단위 테스트(Unit Tests) 기능을 제공하빈다. Xcode에서도 단위 테스트를 사용할 수 있으며 이 옵션을 선택하면 XXXTests라는 폴더와, 기능 단위별 테스트 케이스를 직접 정의할 수 있도록 XCTestCase를 상속받은 클래스가 추가됩니다.
- ###### Include UI Tests : 앞에서 설명했던 Include Unit Tests와 비슷한 목적의 테스트 옵션입니다. 다른 점은 Include Unit Tests가 기능 단위 테스트인 데 비해 이 옵션은 화면 요소에 대한 자동 테스트라는 점입니다. 이 옵션을 선택하면 XXXUITests라는 폴더와, 화면 요소를 테스트하는 스크립트를 작성할 수 잇도록 XCTestCase를 상속받은 클래스가 추가됩니다.


<p align="center"> 
<img width="578" alt="스크린샷 2022-06-08 오후 4 01 05" src="https://user-images.githubusercontent.com/71479613/172552620-f67a854c-5a70-4a08-a409-de92b4e1d99e.png">
</p>

<p align="center">
<font size="2em">
    책에선 Include Unit Tests와 Include UI Tests 두개가 있는데 현재는 Include Tests 한개만 존재해요. 두 개가 합쳐진 것일까요..?
</font> 
</p>


<br>
<br>

##### 정보를 모두 입력한 후엔 프로젝트 파일이 어디에 저장될지 선택해주어야 합니다. 원하는 위치를 선택한 후 
<p align="center"> 
<img width="578" alt="스크린샷 2022-06-08 오후 4 29 05" src="https://user-images.githubusercontent.com/71479613/172557766-6dd72d1b-e6d4-4bbd-9199-e0ea44729514.png">
</p>


<br>
<br>

##### 위치를 선택한 후 마지막으로 Create 버튼을 클릭하면 드디어!!!! 프로젝트가 생성됩니다. 아래 그림은 프로젝트 생성 후 워크스페이스 상에서 프로젝트 정보가 표시된 모습입니다.

<p align="center"> 
<img width="560" alt="스크린샷 2022-06-08 오후 4 32 33" src="https://user-images.githubusercontent.com/71479613/172558538-84e3a63b-6ec9-4ce3-9b45-2dde40330e43.png">
</p>

<br>
<br>
<br>
<br>

## 1.1.2 프로젝트 설정
##### 프로젝트 생성버튼을 클릭하면 보이는 창이 설정 정보창입니다. 이 창에서는 다양한 설정 정보를 확인할 수 있으며 주요 속성을 설정할 수도 있습니다. 이 창을 열고싶다면 왼쪽 프로젝트 네비게이터에서 프로젝트명을 클릭하면 됩니다.

##### 설정 창은 몇 개의 영역으로 나누어져 있습니다. 먼저 Identity 영역입니다.
- ###### Display Name : 모바일 기기에 설치된 앱의 이름을 설정하는 역할을 합니다. 프로젝트 이름과 상관없이 우리가 원하는 앱 이름을 입력해주면 됩니다. 대부분 프로젝트명은 영어로 설정하지만 앱의 이름은 한글로 표시해야 할 때가 많습니다. 이때 이 항목을 이용하여 이름을 설정해주면 됩니다.
- ###### Bundle Identifier : 이거는~ 앱 스토어가 앱을 식별하는 고유 코드입니다. 프로젝트 생성할 때 본 그거!임  프로젝트 이름과 조직명이 합해져 자동 생성되는 값으로 우리가 수정할 수 없습니다.


<p align="center"> 
<img width="658" alt="스크린샷 2022-06-08 오후 4 55 36" src="https://user-images.githubusercontent.com/71479613/172563115-31d28514-05ab-400f-9f0d-a478cf9d9e13.png">
</p>

<br>

##### 다음은 앱이 배포될 때 필요한 항목을 설정하는 Deplyment Info 영역입니다. 
- ###### Deplyment Target : 배포를 허용할 iOS 버전의 하한선을 지정하는 항목으로, 여기서 지정한 항목보다 낮은 버전의 iOS에는 앱 설치가 제한됩니다. 하지만 버전을 낮게 설정한 상태에서 상위 버전을 충분히 대응하지 않으면 최신 iOS에서는 원하는 기능이 제대로 동작하지 않을 수 있으므로 주의해야합니다.

- ###### Device : 아이폰용, 아이패드용, 그리고 둘 모두를 지원하는 유니버설 세 값 중에서 선택할 수 있습니다. 유니버설로 선택할 경우 스토리보드가 자칫 매우 복잡해질 수 있으므로, 특별히 아이폰이나 아이패드 양쪽을 모두 지원할 분명한 목적이 있는 경우가 아니라면 아이폰이나 아이패드 중 하나를 선택하는 것이 좋습니다. 여기서는 iPhone으로 선택합니다.

- ###### Main Interface : 앱이 처음 실행될 때 기본 인터페이스 파일을 무엇으로 할 것인지 설정하는 항목입니다. Main으로 작성 시 Main.storyboard파일을 처음 실행하겠다는 소리입니다.

- ###### Device Orientation : 모바일 기기의 가로, 세로에 대한 회전 여부를 설정하는 항목입니다. 각각의 방향을 결정하는 체크박스 중에서 체크된 것만 지원합니다. Portrait는 세로모드, Upside Down은 디바이스의 위아래를 180도 회전한 상태, Landscape Left는 디바이스를 왼쪽으로 90도 회전시켜 눕힌 상태, Landscape Right는 디바이스를 오른쪽으로 90도 회전시켜 눕힌 상태입니다.

<Br>


<p align="center"> 
<img width="554" alt="스크린샷 2022-06-08 오후 5 22 10" src="https://user-images.githubusercontent.com/71479613/172568568-f0049bca-d918-42c4-aec0-d6aff7a1c946.png">
</p>

<br>

##### 다음은 App icons and Launch Images 영역입니다. 영역은 기기에 설치되는 앱의 아이콘에 대한 설정과, 초기 로딩 페이지 설정을 관리합니다.

<br>

<p align="center"> 
<img width="566" alt="스크린샷 2022-06-08 오후 5 34 10" src="https://user-images.githubusercontent.com/71479613/172571038-f005fc78-1774-4b7d-826a-9b80bfe0dd5c.png">
</p>


<br>

##### 다음 영역인 Frameworks, Libraries, and Embedded Content 부분입니다. 이곳에선 프레임워크나 라이브러리를 등록할 수 있습니다.

<br>

<p align="center"> 
<img width="566" alt="스크린샷 2022-06-17 오전 9 38 21" src="https://user-images.githubusercontent.com/71479613/174199947-d800b62b-1767-44de-a193-d28d865b4967.png">
</p>

<br>
<br>
<br>
<br>

## 1.1.3 프로젝트 구성과 스토리보드
##### 프로젝트의 구성을 살펴봅시다. 우리가 만든 프로젝트는 기본적으로 클래스 파일인 AppDelegate.swift와 ViewController.swift, 그리고 화면을 담당하는 Main.storyboard파일과 LaunchScreen.storyboard 파일, 이미지 등 리소스를 관리하는 Assets.xcassets, 프로젝트의 설정을 담당하는 info.plist파일로 구성됩니다. 옵션 설정에 따라 XXXTests 폴더와 XXXUITests 폴더가 추가되어 있을 수도 있습니다.

- ###### .swift 파일 : .swift 확장자로 이루어진 클래스 파일은 앱의 소스 코드를 구성하는 역할을 합니다. 
- ###### AppDelegate.swift : 기본 프로젝트에 포함되어 있는 클래스 파일은 두 개인데, 이 중 AppDelegate.swift는 앱 전체의 생명 주기 관리를 위임받은 객체인 앱 델리케이트를 구현한 클래스 입니다. 쉽게 말해 앱 전체에 적용해야 할 기능을 담당하는 클래스라고 할 수 있습니다. 앱이 실행되고 종료될 때, 그리고 활성화 상태가 되거나 비활성화 상태가 될 때, 백그라운드 상태로 들어가는 등의 다양한 상태 변화를 감지하고 이에 대한 처리를 해주어야 할 때 이 클래스를 이용합니다.

- ###### Viewcontroller.swift : 앱은 하나 이상의 화면을 가지는데, 이를 관리하기 위해 사용되는 것이 뷰 컨트롤러입니다. 일반적으로는 화면의 개수만큼 뷰 컨트롤러가 필요합니다.

- ###### .storyboard 파일 : 스토리보드 파일은 유저 인터페이스를 종합적으로 구현하는 역할을 합니다. 

- ###### Main.storyboard : 이 파일은 앱의 사용자 인터페이스 설계를 담당합니다.
- ###### LunchScreen.storyboard : 이 파일은 앱을 실행하면 처음 나타나는 시작 화면(앱 키면 바로 잠깐 뜨고 사라지는 하면)을 구성하는 데에 사용됩니다. 시작화면은 다른 말로 스플래시라고도 불립니다.

<br>

<p align="center"> 
<img width="268" alt="스크린샷 2022-06-17 오전 10 06 35" src="https://user-images.githubusercontent.com/71479613/174202185-5901805b-5559-41b9-a019-c2c39d55dc47.png">
<p align="center">
<font size="2em">
프로젝트 생성 시 프로젝트 구조
</font>
</p>
</p>

<br>
<br>

##### 스토리보드 파일은 기존의 nib나 안드로이드의 xml 방식 화면 구성과 달리, 앱에 사용되는 여러 화면을 하나의 파일에 모아 설계할 수 있도록 지원하는 UI 설계용 파일 형식입니다. 기존에는 앱의 화면 하나당 하나의 nib, xml 파일과 대응하는 방식이었다면, 스토리보드 방식은 서로 연결되는 여러 화면이 하나의 스토리보드 파일로 구성되는 방식이라고 할 수 있습니다.

<br>

<p align="center"> 
<img width="668" alt="스크린샷 2022-06-17 오전 10 51 12" src="https://user-images.githubusercontent.com/71479613/174206522-b0dfb900-c67a-4653-9e51-e8e6ea00a01d.png">
<p align="center">
<font size="2em">
Main.storyboard를 클릭한 상태입니다.
</font>
</p>
</p>


<br>

##### 보이는 것만으로는 이 앱이 어떤 기능을 수행하는지까진 알 수 없겠지만, 앱이 어떤 흐름으로 진행되는지, 이 페이지 다음은 어떤 페이지가 오는지는 한눈에 알 수 있습니다. 이것이 스토리보드를 사용하는 이유입니다. 다음은 스토리보드를 사용할 때에 발생하는 이점을 입니다.
- ###### 1. 전체 설계가 파일 하나에 모두 들어있기 때문에 앱의 화면 전체와 화면 사이 관계를 쉽게 파악할 수 있습니다.
- ###### 2. 스토리보드에서는 다양한 화면 사이의 전환을 손쉽게 처리합니다. 이러한 전환 방식을 세그웨이라고 부르는데, 하나의 뷰 컨트롤러에서 전환하고자 하는 뷰 컨트롤러를 향해 Ctrl 키를 누른 상태로 마우스를 드래그하기만 하면 세그웨이가 자동으로 만들어집니다. 덕분에 훨씬 더 짧은 코드로 UI를 다룰 수 있습니다.
- ###### 3. 테이블 뷰를 작업할 때 셀의 외형을 만드는 것이 매우 쉽습니다. 결과적으로 작성해야 하는 코드의 양이 대폭 줄어듭니다.

<br>

<p align="center"> 

<img width="683" alt="스크린샷 2022-06-17 오전 10 56 49" src="https://user-images.githubusercontent.com/71479613/174207109-24a50a89-26fb-432e-abc7-1a42c6225b90.png">

<p align="center">
<font size="2em">
Main.storyboard 사용 예시입니다.
</font>
</p>
</p>

<br>
<br>
<br>
<br>

## 1.1.4 스토리보드로 화면 구현하기
##### Main.storyboard를 클릭하면 현재 인터페이스 빌더에는 한 개의 앱 UI 화면이 추가되어 있을 것입니다. 이 화면을 스토리보드상의 용어로 씬(Scene)이라고 부르지만, 여기서는 뷰 컨트롤러라고 부르겠습니다. 

##### 마우스로 뷰 컨트롤러 위의 길죽한 네모 바 부분을 클릭하면 잘 안보이지만 파란색 테두리 표시되면서 현재 선택된 객체임을 나타냅니다. 이 부분을 도크(Dock)라고 부릅니다. ViewController를 정확히 실패없이! 선택하고싶다면 도크 내부에 존재하는 세 개의 아이콘 중 맨 왼쪽 아이콘을 클릭하셔도 ViewController가 선택됩니다.


<br>

<p align="center"> 
<img width="318" alt="스크린샷 2022-06-17 오전 11 13 12" src="https://user-images.githubusercontent.com/71479613/174210716-27b266d3-8c84-4d09-8a23-0bdf247555f0.png">
<p align="center">
<font size="2em">
ViewController가 선택되지 않은 상태입니다.
</font>
</p>
</p>

<br>

<p align="center"> 
<img width="318" alt="스크린샷 2022-06-17 오전 11 13 23" src="https://user-images.githubusercontent.com/71479613/174210775-d6b1d4dc-a5a1-4cae-9554-def1b88f4909.png">
<p align="center">
<font size="2em">
ViewController가 선택된 상태입니다. 파란색 테두리가 표시되었습니다.
</font>
</p>
</p>


<br>

##### 이 뷰 컨트롤러의 사이즈를 조절할 수 있습니다. 디바이스 종류를 선택하여 뷰 컨트롤러의 크기를 바꿀 수 있습니다. 왼쪽에서 4번째 아이콘을 클릭하면 화면이 가로로 눕습니다. 가로로 실행되는 앱은 가로로 설정한 후 개발하면 더 편리합니다.

##### 단 View as 항목에서 특정 디바이스 기기를 선택했다고 해서 앱이 그 디바이스에서만 동작하는 것은 아니며, 가로모드로 설정했다고 해서 앱이 가로 모드로 동작하는 것은 아닙니다. 단지 화면 설계 시 편의를 위해 특정 사이즈나 가로, 세로에 미리 맞춰서 작업하는 것일 뿐입니다. 특정 디바이스에서만 작동하거나 앱을 가로모드로 설정하고 싶다면 Info에서 수정해야합니다.

<br>

<p align="center"> 
<img width="393" alt="스크린샷 2022-06-17 오전 11 19 56" src="https://user-images.githubusercontent.com/71479613/174211910-a7f5324e-280c-4b7c-9aa1-2b42d10683f7.png">
<p align="center">
<font size="2em">
Xcode 화면의 왼쪽 하단 부분에서 ViewController의 Size를 조절할 수 있습니다.
</font>
</p>
</p>

<br>

<p align="center"> 
<img width="390" alt="스크린샷 2022-06-17 오전 11 21 27" src="https://user-images.githubusercontent.com/71479613/174212059-48dcd636-afcc-416e-866b-5bde44ae9cff.png">
<p align="center">
<font size="2em">
왼쪽에서 4번째 아이콘을 클릭하면 화면이 가로로 변경되거나 세로로 변경됩니다.
</font>
</p>
</p>

<br>
<br>
<br>

### 뷰 컨트롤러에 오브젝트 추가하기
##### 이제 앱 화면에 뭐라도 추가해봅시다. Xcode 우측 상단의 + 버튼을 클릭하여 오브젝트 라이브러리를 꺼냅니다.

<br>

<p align="center"> 
<img width="508" alt="스크린샷 2022-06-17 오전 11 28 25" src="https://user-images.githubusercontent.com/71479613/174212867-c137df5d-2103-4830-be2d-0c07ab491d24.png">
<p align="center">
<font size="2em">
버튼이나~ 라벨이나~ 다 여기 있었다구
</font>
</p>
</p>

<br>

##### 오브젝트 라이브러리에서 레이블과 버튼 객체를 찾아 뷰 컨트롤러로 각각 끌어다 놓습니다. 영어로 검색하세요..! 놓을때마다 라이브러리 창이 매번 닫혀서 불편하다면, Option키를 누르고 드래그 드롭 해보세요. 안닫힘!

<br>

<p align="center"> 
<img width="520" alt="스크린샷 2022-06-17 오전 11 30 30" src="https://user-images.githubusercontent.com/71479613/174213104-d951650a-6dd2-479f-8294-ff0d956815e9.png">
<p align="center">
<font size="2em">
오브젝트 라이브러리에서 라벨과 버튼을 끌어당겨 화면에 두었습니다. 귀엽당.
</font>
</p>
</p>

<br>

##### 둘 다 더블클릭해 다음과 같이 텍스트를 변경하였습니다.

<br>

<p align="center"> 
<img width="520" alt="스크린샷 2022-06-17 오전 11 33 36" src="https://user-images.githubusercontent.com/71479613/174213409-3de58743-9006-4df4-b46b-93adcac22470.png">
<p align="center">
<font size="2em">
</font>
</p>
</p>

<br>
<br>
<br>

### 앱 시뮬레이터로 앱 실행해보기
##### Xcode하면서 제일 신났을 때.. 바로 시뮬레이터를 만났을 때.. 
##### Xcode 상단의 툴바 영역에서 실행버튼을 클릭하기 전에~ 상단의 iPod Touch~ 라고 써져있는 부분을 클릭해 원하는 기기로 설정해줍니다. 하지만 가급적 뷰 컨트롤러에 설정된 디바이스 사이즈와 동일한 시뮬레이터를 실행하는 것이 좋습니다. 각 기기마다 화면 크기가 달라 이상하게 나올 수도 있어요..

<br>

<p align="center"> 
<img width="572" alt="스크린샷 2022-06-17 오전 11 40 48" src="https://user-images.githubusercontent.com/71479613/174214149-fc2a2d14-0b2c-40c8-ba5f-c7a3a9903c3b.png">
<p align="center">
<font size="2em">
</font>
</p>
</p>

<br>

##### 이제 Command + R 또는 실행버튼을 클릭하여 시뮬레이터를 실행해봅시다.

<br>

<p align="center"> 
<img width="538" alt="스크린샷 2022-06-17 오전 11 45 16" src="https://user-images.githubusercontent.com/71479613/174214652-b309fd5d-e53a-4dcf-bb53-00e85fb99e28.png">
<p align="center">
<font size="2em">
멋있당 ....
</font>
</p>
</p>

<br>
<br>
<br>
<br>

## 1.1.5 화면 전환 구현하기
##### 버튼을 눌렀을 때 화면을 전환할 것이기 때문에 버튼을 새로 한개 추가해줍니다. 또 이동될 페이지가 필요하기 때문에 ViewController를 하나 추가해주고 두번째 화면임을 알 수 있도록 두번째 ViewController에 label을 추가해줍니다.

<br>

<p align="center"> 
<img width="587" alt="스크린샷 2022-06-17 오전 11 54 39" src="https://user-images.githubusercontent.com/71479613/174215587-566cd256-faa1-4101-a307-69cdaa3919e2.png">
<p align="center">
</p>
</p>

<br>

##### 화면 전환의 하이라이트.. 첫 번째 뷰 컨트롤러의 페이지 이동 버튼을 선택하고, 마우스 오른쪽 버튼을 클릭한채로 두 번째 뷰 컨트롤러에 드래그 합니다. 아니면 Ctrl 키를 누른채로 마우스 왼쪽 버튼을 같이 눌러 오른쪽 화면으로 드래그 합니다.
##### 그럼 표시되는 팝업 메뉴 중 Present Modally를 선택해봅시다. 그럼 아래와 같이 화살표로 연결된 모습을 볼 수 있습니다.

##### 이렇게 되면 화면전환은 끝입니다. 실행해서 확인해보면 버튼 클릭 시 화면이 전환되는 것을 볼 수 있습니다.

##### 그리고 화살표 가운데 원 안에 아이콘 형식의 기호가 들어있는데, 화면 전환 방식이 달리지면 이 아이콘의 표시도 달라집니다. 즉, 화살표 안에 들어 있는 아이콘은 화면 전환 방식을 표현해 주는 것입니다.

<br>

<p align="center"> 
<img width="573" alt="스크린샷 2022-06-17 오전 11 57 30" src="https://user-images.githubusercontent.com/71479613/174215896-30b1facd-7e90-433e-a528-a3a6fd27466e.png">
<p align="center">
</p>
</p>

<br>
<br>
<br>

## 1.1.6 스위프트 코드 작성하기
##### 이번엔 버튼을 클릭하면! 글자가 바뀌는 앱을 만들어보겠습니다.
##### 앱이 사용자의 동작에 반응하기 위해선 레이블과 버튼 등을 제어하는 소스 코드를 작성해야합니다. 버튼을 누르면 텍스트를 바꿔라~와 같은 동작을 소스 코드로 작성해주어야 합니다.
##### 이때 소스 코드를 작성하는 위치는 뷰 컨트롤러에 연결된 클래스 내부입니다. 이게 무슨 말이냐 하면 UI를 표현하는 각각의 뷰 컨트롤러에는 이를 프로그래밍적으로 제어하기 위한 클래스 객체가 배정되는데, 이 클래스의 소스 코드 내부에 스위프트 코드를 작성함으로써 UI를 마음대로 조정할 수 있다는 겁니다.
##### 일반적으로 뷰 컨트롤러를 추가하고 나면 소스 코드를 작성할 클래스를 정의하고, 이어서 뷰 컨트롤러와 클래스를 서로 연결해주어야 합니다. 하지만 기본 생성된 이 첫 번째 뷰 컨트롤러는 이미 ViewController.swift파일과 연결되어 있는 상태입니다. 따라서 우리는 연결하는 과정을 건너뛰고 바로 swift파일에 소스코드를 작성해주면 되는 것 입니다!! 방금 언급된 연결 어찌고 하는 내용은 다음 장에서 다뤄보기로 하고 지금은 바로 swift 파일을 열어 코드를 작성해보겠습니다.

##### 왼쪽의 프로젝트 네비게이터에서 ViewController.swift 파일을 Option 키를 누른상태로 클릭하여 Storyobard파일과 swift파일을 동시에 볼 수 있게 해봅시다.

<br>

<p align="center"> 
<img width="573" alt="스크린샷 2022-06-17 오전 11 57 30" src="https://user-images.githubusercontent.com/71479613/174215896-30b1facd-7e90-433e-a528-a3a6fd27466e.png">
<p align="center">
<font size="2em">
Main.storyboard파일에서 Option키를 누른 상태로 ViewController.swift 파일을 클릭한 상태입니다.
</font>
</p>
</p>

<br>
<br>

### ViewController.swift
##### ViewController.swift 파일에는 ViewController 클래스가 다음과 같은 내용으로 구현되어 있습니다.

- ###### 주석입니다. 메모라고 보면 됩니다.
```Swift
//
//  ViewController.swift
//  MeticulousYoujin
//
//  Created by 김유진 on 2022/06/08.
//
```
<br>

- ###### UIKit 프레임워크를 사용하기 위해 필요한 기본 파일들을 읽어 들이는 부분입니다. import 키워드는 라이브러리나 프레임워크 등 사용하고자 하는 기능 파일들을 데려오라는 뜻입니다. UIKit은 뒤에 가서 자세히 배우겠지만 앱 화면을 구성하는 데에 필요한 모든 객체들이 포함된 프레임워크입니다.
```Swift
import UIKit
```
<br>

- ###### UIViewController라는 클래스를 상속받아 ViewController라는 이름의 새로운 클래스를 정의하는 내용입니다. 또 viewDidLoad() 메소드를 정의하는 부분입니다. 이 메소드는 부모 클래스인 UIViewController 클래스에 정의되어 있는 메소드로, 뷰의 로딩이 완료되었을 때 시스템에 의해 자동으로 호출됩니다. 초기 화면을 구성하거나 리소스를 초기화하는 등, 처음 한 번만 실행해야 하는 초기화 코드는 대부분 이 메소드 내부에 작성하면 됩니다.

```Swift
class ViewController: UIViewController {

    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.
    }

}
```

##### 방금 언급한 viewDidLoad() 메소드는 뷰의 로딩이 완료되었을 때 시스템에 의해 자동으로 호출되는 이른바 콜백 메소드입니다.

<br>
<br>
<br>

### 레이블 연결
##### 이제 화면에 있는 객체인 레이블을 소스 코드에서 컨트롤할 수 있도록 서로 연결하겠습니다. 첫번째 화면이라고 작성했던 레이블을 선택한 후에 Ctrl 키를 누른 채 마우스 왼쪽 버튼을 클릭한 채 오른쪽 swift 파일의 class 선언 아래 부분에 드래그 드롭 합니다.
##### 이 레이블의 이름을 uiTitle로 설정한 후 storage가 Weak으로 되어있는 경우 Strong으로 변경하고 Connect버튼을 클릭해 레이블과 소스코드를 연결하는 작업을 마무리합니다.
##### 이 변수는 인터페이스 빌더의 레이블을 스위프트 클래스가 참조할 수 있도록 연결된 멤버 변수로, 아울렛 변수라고 부릅니다. 특히 @IBOulet이라는 키워드는 인터페이스 빌더에 관련된 속성이라는 것을 알려주는 어노테이션입니다.

##### uiTitle 변수는 뷰 컨트롤러에 추가했던 레이블과 직접적으로 연결되어 있습니다. 우리가 이 변수의 속성을 변경하면 화면 상에 있는 레이블에도 그대로 반영됩니다. 따라서 우리는 아울렛 변수를 통해 화면상에 있는 레이블을 마음대로 다룰 수 있습니다.
<br>

<p align="center"> 
<img width="608" alt="스크린샷 2022-06-17 오후 12 20 45" src="https://user-images.githubusercontent.com/71479613/174218366-6fff1de3-1297-4497-ba8a-925d3a9360a9.png">
<p align="center">
</p>
</p>

<br>
<br>
<br>

### 버튼 연결