## Validation 로직 모음

- 중복검사 : Set을 활용한 중복검사
  ```java
  private static void checkDuplicate(String input) {
        String[] names = input.split(COMMA);
        Set<String> _Names  = new HashSet<>();
        for (String name : names) {
            if (!_Names.add(name)) {
                throw new IllegalArgumentException(ErrorMessage.DUPLICATION.getMessage());
            }
        }
    }
  ```
- 💡 여러 구분자 처리 및 동적 구분자 활용
  ```java
  private static void checkDuplicate(String input) {
    // 여러 구분자를 지원 (콤마, 세미콜론, 콜론)
    String[] names = input.split("[,;:]");
    // 동적 구분자를 정규표현식으로 변환 String regex = "[" + delimiters + "]"
    Set<String> uniqueNames = new HashSet<>();
    for (String name : names) {
        if (!uniqueNames.add(name)) {
            throw new IllegalArgumentException("중복된 이름: " + name);
        }
    }
  }
  ```
