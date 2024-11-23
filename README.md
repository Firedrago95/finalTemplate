1. fork -> clone -> initial 커밋
2. 기능구현 목록 작성
3. controller,service,domain,view,util,constants 패키지 생성

- 에러 메시지 enum 클래스
```java
public enum ErrorMessage {

    private final String PREFIX = "[ERROR] ";
    private String message;

    ErrorMessage(String message) {
        this.message = message;
    }

    public String getMessage() {
        return PREFIX + message;
    }
}
```
