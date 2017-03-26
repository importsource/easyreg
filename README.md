# importsource-easyreg

```java
  EasyExpression testRegex = EasyExpression.regex()
                .startOfLine().then("http").maybe("s")
                .then("://")
                .maybe("www.").anythingBut(" ")
                .then(".com")
                .endOfLine()
                .build();



        // Create an example URL
        String url = "https://www.google.com";

        // Use EasyExpression's testExact() method to test if the entire string matches the regex
        boolean is = testRegex.testExact(url); //True
        System.out.println(is);

        System.out.println(testRegex.toString()); // Outputs the regex used:
        // ^(?:http)(?:s)?(?:\:\/\/)(?:www\.)?(?:[^\ ]*)$
```