1. fork -> clone -> initial 커밋
2. 기능구현 목록 작성
3. controller,service,domain,view,util,constants 패키지 생성

## public class Application
```java
     _Controller controller = new _Controller();
    controller.run();
```

## public class Controller
```java
    private _Service service = new _Service();

    public void run() {

    }
```

## public enum ErrorMessage 
```java

    EMPTY_VALUE("빈 값을 입력하셨습니다. 값을 입력해주세요."),
    WRONG_FORM("형식에 맞지 않는 값을 입력하셨습니다. 다시 입력해주세요.");

    private final String PREFIX = "[ERROR] ";
    private String message;

    ErrorMessage(String message) {
        this.message = message;
    }

    public String getMessage() {
        return PREFIX + message;
    }
```

## public class InputValidator
```java
    
    private static final Pattern _REGEX = Pattern.compile("");

    private static void checkEmpty(String input) {
        if (input == null || input.isEmpty()) {
            throw new IllegalArgumentException(ErrorMessage.EMPTY_VALUE.getMessage());
        }
    }

    private static void check_Form(String input) {
        if (!_REGEX.matcher(input).matches()) {
            throw new IllegalArgumentException(ErrorMessage.WRONG_FORM.getMessage());
        }
    }
```
