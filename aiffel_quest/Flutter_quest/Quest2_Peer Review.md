
AIFFEL Campus Code Peer Review Templete
코더 : 김원영님
리뷰어 : 소다흰

<aside>
💡 **PRT(Peer Review Template)**

- [O]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 기능이 정상적으로 작동하는지?
        - 해당 조건을 만족하는 부분의 코드 및 결과물을 근거로 첨부
        -- **네 완벽하게 구현하는 결과물이 제출되었습니다.**
    
- [O]  **2. 핵심적이거나 복잡하고 이해하기 어려운 부분에 작성된 설명을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭에 doc string/annotation/markdown이 달려 있는지 확인
    - 해당 코드가 무슨 기능을 하는지, 왜 그렇게 짜여진건지, 작동 메커니즘이 뭔지 기술.
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 잘 작성되었다고 생각되는 부분을 근거로 첨부합니다.
        -- 개인적으로 코딩을 잘 모르는 사람도 이해가 쉽도록 자세히 주석을 달아주셨습니다.
```dart class MyHomePage extends StatelessWidget { // StatelessWidget을 상속받는 MyHomePage 클래스를 정의
  @override
  Widget build(BuildContext context) { // 위젯을 빌드하는 메서드
    return Scaffold( // Scaffold 위젯을 반환
      appBar: AppBar( // 상단 앱바를 정의
        leading: Icon(Icons.location_city), // 앱바 왼쪽에 자주 사용했던 city 아이콘을 추가
        title: Text('플러터 앱 만들기'), // 앱바 중앙에 텍스트를 추가
        backgroundColor: Colors.blue, // 앱바의 배경색을 파란색으로 설정
      ),
      body: Column( // 본문을 열 방향으로 배열하는 Column 위젯을 사용
        children: <Widget>[ // Column의 자식 위젯들을 정의
          Expanded( // Expanded 위젯을 사용하여 남은 공간을 채움
            flex: 1, // flex 속성을 사용하여 공간을 얼마나 차지할지 지정
            child: Column( // Column 위젯을 자식으로 추가
              mainAxisAlignment: MainAxisAlignment.center, // 자식 위젯들을 중앙에 배치
              children: [
                ElevatedButton( // 누르면 동작하는 버튼을 추가
                  onPressed: (){ // 버튼이 눌렸을 때 실행할 동작을 정의
                    print('버튼이 눌렸습니다.'); // 콘솔에 메시지를 출력
                  },
                  child: Text('Text') // 버튼의 내용으로 'Text' 텍스트를 추가
                )
              ]
            )
          ), 
```
        
        
- [O]  **3.** 에러가 난 부분을 디버깅하여 “문제를 해결한 기록”을 남겼나요? 또는
   “새로운 시도 및 추가 실험”을 해봤나요? ****
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인 또는
    - 문제에서 요구하는 조건에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 잘 작성되었다고 생각되는 부분을 근거로 첨부합니다.
        -- 회고 부분에 잘 기술되었습니다.
        
        // 이번 프로젝트를 통해 Flutter의 Stack 위젯과 Align 위젯을 활용하여 컨테이너를 특정 위치에 배치하는 방법을 깊이 이해하게 되었습니다. 처음에는 Align 위젯의 alignment 속성을 사용해 컨테이너를 원하는 위치에 배치하려 했으나, 예상대로 작동하지 않아 많은 시간을 소비했습니다.그러나, 학습교재 233 페이지에 겹쳐서 모두 보이기 - Stack을 다시 읽으면서 방향 전환을 고려하던 찰나에 같이 협업하던 재이님께서 처음부터 Stack의 children 속성을 사용해 컨테이너를 구현하셨다는 말을 듣고 과감하게 수정을 하게 되었습니다. 
        
        // 재이님과 전체적인 코드를 서로 살펴보면서 Flutter의 레이아웃 메커니즘을 더 깊이 이해하게 되었고, 재이님은 Text 구현에 저는 Stack 위젯의 children 속성을 사용해 위젯을 순서대로 겹치게 배치하는 방법을 찾는 시너지 효과를 얻을 수 있었습니다.  이 방법을 사용하니, 컨테이너들이 원하는 대로 중첩되어 잘 출력되었고 각 컨테이너마도 색깔을 다르게 선정하여 더 나은 시각화를 꾀하였습니다. 

      // 이 경험을 통해 문제 해결에 있어 고정관념에 사로잡혀 한 접근방식을 고수하는 대신 다양한 접근 방식들에 늘 열려있어야 하며 더군다나 Flutter와 같은 프레임워크를 사용할 때 그 동작 원리와 메커니즘을 최우선적으로 이해하고 코드를 작성하는 것이 매우 중요하다는 것을 다시 한번 느꼈습니다.


        
        
- [O]  **4. 회고를 잘 작성했나요?**
    - 프로젝트 결과물에 대해 배운점과 아쉬운점, 느낀점 등이 상세히 기록 되어 있나요?
    -- 네 상세히 기술하셨습니다.

- [O]  **5. 코드가 간결하고 효율적인가요?**
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 모듈화(함수화) 했는지
        - 잘 작성되었다고 생각되는 부분을 근거로 첨부합니다.
        -- Stack 위젯 사용 시도
  ```
  Expanded( // Expanded 위젯을 사용하여 남은 공간을 채움
            flex: 1, // flex 속성을 사용하여 공간을 얼마나 차지할지 지정
            child: Center( // 중앙에 위젯을 배치하는 Center 위젯을 사용
              child: Container( // Container 위젯을 추가
                child: Stack( // 위젯을 겹쳐서 배치하는 Stack 위젯을 사용
        
![image](https://github.com/timothy2077/1st-Rep/assets/168173100/c9f82be8-4170-41b5-a345-2c47d0ea4c4e)

