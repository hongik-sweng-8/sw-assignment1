## 팀 코드 : 17050

**※ 이름 순서는 가나다 순이며 기여도와 관계 없음**

---

### 팀 내 역할 분담

| 이름   | 역할 분담 내용 |
|--------|----------------|
| 노태일 | 회원가입 기능, 회원탈퇴 기능, 로그인/로그아웃 기능, 대여소 검색 기능 Use Case 구현 및 Use Case Description 제작 |
| 이다윤 | 자전거 반납 및 식당 예약 서비스 연계 기능, 결제 및 요금 조회 기능, 통계 기능 Use Case 구현 및 Use Case Description 제작 |
| 이승찬 | 자전거 대여 정보 조회, 자전거 예약대기 정보 조회/취소 기능, 이용내역 조회/삭제 기능 Use Case 구현 및 Use Case Description 제작 |
| 조수민 | 상세정보 조회 및 자전거 즉시대여/예약대기 기능, 대여소 등록/조회/삭제 기능, 자전거 등록/조회/삭제 기능 Use Case 구현 및 Use Case Description 제작 |

- UseCaseDiagram는 각자 생각하는 바를 그려온 뒤 회의를 통해 하나로 통합했습니다. 
- Requirements List와 Description은 use case 단위로 분배하여 각자 작업 후 최종 정리를 진행했습니다. 

---

### 팀원이 실제 수행한 내용

| 이름   | 실제 수행 내용 |
|--------|----------------|
| 노태일 | 역할 분담 내용 + UML Tool 조사, Requirements List 최종 정리 |
| 이다윤 | 역할 분담 내용 + Classroom Q&A 분석, Usecase Description 최종정리 |
| 이승찬 | 역할 분담 내용 + Git Organization 구성 및 Repository 초안 제작 + UseCaseDiagram 최종 정리 + git commit 히스토리 파일|
| 조수민 | 역할 분담 내용 + 보고서 최종 취합|

## Requirement List

| No  | Requirement                                                         | Use Case(s)                      |
|-----|---------------------------------------------------------------------|----------------------------------|
| 1   | 관리자가 대여소 정보를 등록할 수 있도록 한다. 등록 시 입력되는 정보는 대여소 이름, 위치(도시, 주소), 자전거 보관 가능 수량, 운영 시간 등이다. | 대여소 등록 |
| 2   | 관리자가 등록된 대여소 리스트를 조회할 수 있도록 한다. (option) 특정 대여소 항목을 선택하여 삭제할 수 있도록 한다. | 대여소 리스트 조회, 대여소 삭제    |
| 3   | 관리자가 원하는 대여소 항목을 선택하면 등록시 입력한 상세내용을 볼 수 있게 한다. | 대여소 상세내용 조회 |
| 4   | 관리자가 자전거 정보를 등록할 수 있도록 한다. 등록 시 입력되는 정보는 자전거 ID, 자전거 제품명, 유형(일반/전기), 소속 대여소, 상태(사용 가능/수리 중) 등이다. | 자전거 등록  |
| 5   | 관리자가 등록된 자전거 리스트를 조회할 수 있도록 한다. (option) 특정 자전거 항목을 선택하여 삭제할 수 있도록 한다. | 자전거 리스트 조회, 자전거 삭제 |
| 6   | 관리자가 원하는 자전거 항목을 선택하면 등록시 입력한 상세내용을 볼 수 있게 한다. | 자전거 상세정보 조회             |
| 7   | 회원은 검색된 대여소 리스트 화면에서 특정 대여소를 선택하면 상세정보화면을 볼 수 있다. (option) 회원이 남아 있는 자전거를 즉시 대여할 수 있도록 한다. 이 경우, 회원에게 문자 알림이 전송된다. (option)회원이 자전거가 없을 때 예약대기를 신청할 수 있도록 한다. 이 경우, 회원에게 문자 알림이 전송된다. | 대여소 상세정보 조회, 자전거 즉시 대여, 자전거 예약 대기 |
| 8  | 시스템을 이용하려면 사용자는 회원 가입을 해야 한다. 회원의 필수 입력 정보는 ID, 비밀번호, 전화번호, 결제 수단, 선호 자전거 유형(일반/전기) 등이다. | 회원 가입 |
| 9  | 회원은 언제든 탈퇴할 수 있으며, 탈퇴 시 모든 이용 권한과 데이터가 삭제되어야 한다. | 회원 탈퇴 |
| 10  | 관리자와 회원은 ID와 비밀번호로 로그인할 수 있어야 한다.          | 로그인 |
| 11  | 관리자와 회원은 로그아웃 할 수 있고, 로그아웃 시 시스템 접속이 종료되어야 한다.    | 로그아웃 |
| 12  | 회원은 조건에 맞는 대여소를 검색할 수 있어야 한다. 입력값은 대여소 이름이고, 검색결과로 조건에 맞는 대여소 리스트가 출력되어야 한다. | 대여소 검색 |
| 13  | 회원이 현재 대여 중인 자전거 정보(대여소 이름, 대여소 위치, 자전거 ID, 자전거 제품명, 자전거 유형)를 조회할 수 있도록 한다. (option) 자전거를 사용하던 회원이 자전거 대여 정보 조회 화면에서 지정된 대여소에서 자전거를 반납할 수 있도록 한다. 이때 외부결제 시스템을 통해 결제가 이루어지도록 한다. 또한, 해당 자전거에 대기 예약이 존재한다면 외부 이메일 시스템을 통해 1순위 대기예약자에게 예약 되었다는 이메일을 보낸다. (option) 자전거 반납 후, 원하는 경우 사용자 위치 정보를 기반으로 근처 식당을 추천받아서 예약할 수 있는 외부 서비스와 연결된다.  | 자전거 대여 정보 조회, 대여 자전거 반납, 식당 추천 |
| 14  | 회원이 예약대기 중인 자전거 정보(대여소 이름, 대여소 위치, 자전거 ID, 자전거 제품명, 자전거 유형)를 조회할 수 있도록 한다. (option) 회원이 예약대기를 취소할 수 있도록 한다. | 자전거 예약대기 정보 조회, 자전거 예약대기 취소  |
| 15  | 회원이 과거 대여 기록을 조회할 수 있도록 한다. (option) 과거 대여 기록을 대여소별로 정렬할 수 있도록 한다. (option) 회원이 과거 대여 기록 중 특정 항목을 선택하여 삭제할 수 있도록 한다. | 이용 내역 조회, 대여소 별 정렬, 이용 내역 삭제 |
| 16  | 회원이 자신이 반납한 자전거에 대한 대여시간과 요금을 볼 수 있도록 한다 | 요금 조회 |
| 17  | 관리자는 대여 정보(대여소 이름, 대여소 위치, 자전거 ID, 자전거 제품명, 자전거 유형)를 반납 시간 기준 최근순으로 조회할 수 있도록 한다. (option) 대여 정보 방법을 지역별로 변경하여 조회 할 수 있도록 한다. | 대여정보 조회, 지역별 정렬 |
| 18  | 관리자는 대여 금액, 대여 횟수를 (option)1주일, 1달, 1년 단위로 조회 할 수 있도록 한다.  | 대여 금액&횟수 조회, 기간 단위 선택 |
