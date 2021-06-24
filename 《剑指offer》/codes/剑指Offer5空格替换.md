

常规做法

```java
class Solution {
    public String replaceSpace(String s) {
        char[] chars = s.toCharArray();
        StringBuilder newstr = new StringBuilder();
        for (int i = 0; i < chars.length; i++) {
            if (chars[i] != ' ') {
                newstr.append(chars[i]);
            } else {
                newstr.append("%20");
            } 
        }
        return newstr.toString();
    }
}
```

使用库函数

```java
class Solution {
    public String replaceSpace(String s) {
        return s.replaceAll("\\s", "%20");
    }
}
```

