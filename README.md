- **사용 스택** : Android(Java), Key-Value DB(SharedPreferences)
- **개발 기간** : 2019년 8월 22일 ~ 9월 1일
- **시연 영상** : [https://youtu.be/qo-RsOIHnPQ](https://youtu.be/qo-RsOIHnPQ)
- **프로젝트 내용 요약**
    - 캘린더의 날짜를 클릭하여, 해당 날짜에 여러 개의 메모를 생성/조회/수정/삭제 할 수 있습니다.
    - 각 메모마다 To-do-list 처럼 체크박스가 존재하여, 완료 여부를 마킹할 수 있습니다.
    - '전체 보기', '완료한 메모만 보기', '완료하지 않은 메모만 보기'와 같이 3가지로 필터링할 수 있습니다.
    - UI/UX와 외적 디자인에 신경을 많이 썼습니다.
    - DB는 단순 Key-Value 저장 객체인 SharedPreferences를 사용하였습니다.
    - Play 스토어에 출시 및 버전 업데이트를 하였습니다. (누적 사용자 : 9명)
        
        [Play Console](https://www.notion.so/Play-Console-221a3093d4aa42a3bd8144d38199358e)
        
    - 출시 7일 만에 게시 취소를 하였습니다. 그 이유는 DB에 치명적 버그가 발견되었고, SharedPreferences가 감당할 수 있는 데이터의 용량의 한계가 불명확해서, 불안정성이 우려되어 출시를 취소하였습니다. 코드도 매우 복잡하고 확장 불가능한 코드가 되어 유지 보수가 어려울 것 같았습니다.
- **제작 문서**
    
    [캘린더 메모 어플 문서](https://www.notion.so/6eed79f07b2a4fa49861f754bf4b801b)
    
- **어려웠던 점 /** **느낀 점**
    - DB를 사용해본 경험이 적어서 사용 방법이 쉬운 Key-Value 기반의 SharedPreferences를 사용하였습니다. 대신 SharedPreferences와 앱 메모리 데이터 간의 Sequential ID 매핑이 필요했는데, 이 때문에 응용 레벨에서 DB를 위한 CRUD 알고리즘을 직접 짜야 했습니다. 이 과정에서 엄청난 시행착오와 디버깅 비용이 들었습니다. 이러한 경험을 통해 Key-Value 기반 DB가 아닌, MySql과 같이 많은 기능을 지원하는 DB 시스템을 이용하는 것이 훨씬 효율적이고 안정적이라는 것을 느낄 수 있었습니다.
