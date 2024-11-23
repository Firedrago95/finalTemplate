1. fork -> clone -> initial 커밋
2. 기능구현 목록 작성
3. controller,service,domain,view,util,constants 패키지 생성

## public class Controller
---java
    private 1Service service = new 1Service();

    public void run() {

    }
---

## public enum ErrorMessage 
```java

    EMPTY_VALUE("빈 값을 입력하셨습니다. 값을 입력해주세요");
    
    private final String PREFIX = "[ERROR] ";
    private String message;

    ErrorMessage(String message) {
        this.message = message;
    }

    public String getMessage() {
        return PREFIX + message;
    }
```
