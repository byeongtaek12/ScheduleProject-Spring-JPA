## Lv 1. 일정 CRUD  

### - 일정을 생성, 조회, 수정, 삭제
### - `작성 유저명`, `할일 제목`, `할일 내용`, `작성일`, `수정일` 필드
### -  `작성일`, `수정일` 필드는 `JPA Auditing`을 활용

---

## Lv 2. 유저 CRUD

### - 유저를 생성, 조회, 수정, 삭제
### -   `유저명`, `이메일`, `작성일` , `수정일` 필드
### -  `작성일`, `수정일` 필드는 `JPA Auditing`을 활용

### -   연관관계 구현
####    -   일정은 이제 `작성 유저명` 필드 대신 `유저 고유 식별자` 필드를 가집니다.

---
## Lv 3. 회원가입

### - 유저에 비밀번호 필드를 추가

---
## Lv 4. 로그인(인증)
### - 키워드

  **인터페이스**

- HttpServletRequest / HttpServletResponse : 각 HTTP 요청에서 주고받는 값들을 담고 있습니다.

#### - Cookie/Session을 활용해 로그인 기능을 구현
#### - 필터를 활용해 인증 처리
#### - @Configuration 을 활용해 필터를 등록

#### - 이메일과 비밀번호를 활용해 로그인 기능을 구현
#### - 회원가입, 로그인 요청은 인증 처리에서 제외
#### - 로그인 시 이메일과 비밀번호가 일치하지 않을 경우 HTTP Status code 401을 반환

---
## Lv 5. 다양한 예외처리 적용하기
### - Validation을 활용해 다양한 예외처리를 적용