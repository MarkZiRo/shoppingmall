# 오픈 마켓 프로젝트

일반 사용자는 중고거래를, 사업자는 인터넷 쇼핑몰을 운영할 수 있게 해주는 중고거래,쇼핑몰 사이트

Postman으로 테스트완료

## 기술
- Spring Boot 3.2.3
  - Spring Boot Starter Web 
  - Spring Boot Starter Data JPA
  - Spring Boot Starter Security
  - Spring Boot Starter Mail
  - Lombok
- Java JWT 0.11.5
- Querydsl 5.1.0
- Gson 2.10.1

## 실행
1. 본 Repository를 clone 받는다.
2. Intellij IDEA를 이용해 clone 받은 폴더를 연다.
3. `MarketApplication.java`의 `main`을 실행한다.

## 기능

1. 사용자 인증은 JWT토큰 인증방식으로 JWT를 Bearer Authentication 방식으로 제시된다.
2. 회원가입이 가능하며 프로필 이미지 업로드가 가능하다.
3. 사용자의 권한은 4가지가 있다( 그냥 비활성유저, 활성유저, 사업자, 관리자)
4. 활성유저는 자신을 사업자 이용자로 신청할수있고 관리자는 신청목록을 확인후 수락, 거절을 한다.
5. 중고물품은 작성자만 수정,삭제가 가능하며, 물품을 등록한사람과 비활성유저를 제외 구매 제안이 가능하다.
6. 물품을 등록한 사용자는 구매, 또는 거절을 한다. 구매제안이 된다면 다른 제안들은 모두 거절된다
7. 사업자가 되면 쇼핑몰 운영을 할수가 있다. 관리자가 쇼핑몰목록을 확인후 수락, 거절을 한다.
8. 쇼핑몰은 검색이 가능하며 조회되는 상품은 정보가 함께 제공된다.
9. Toss 결제시스템. 사용자가 구매요청을 할때 결제를 진행한다. 주인은 수락 또는 거절을한다.
10. NCP Maps를 통해 두 사용자가 수락시 서로의 위치를 바탕으로 거래위치를 확인후 이동방법을 볼수있다.
11. email(jakartamial) 통해 회원가입시 이메일인증, 중고거래시 구매제안 알림등을 보낸다.
12. NCP Captcha를 활용해 로그인을 시도하면 캡차사진을 볼수있는 링크로 이동시킨다.

