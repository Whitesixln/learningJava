# learningJava
## I am learning Java.These are my self-study exercise code.


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

练习1：给定["a","b","a","b","c","a","b","c","b"]字符串数组，然后使用Map的key来保存数组的字符串元素，value保存该字符串元素出现的次数。
代码:

```java
import java.util.Arrays;
import java.util.HashMap;
import java.util.Map;

public class Practice8_03 {
    public static void main(String[] args) {
        String[] str = new String[]{"a", "b", "a", "b", "c", "a", "b", "c", "b"};
        System.out.println("字符串数组：" + Arrays.toString(str));
        Map<String, Integer> map = new HashMap<>();
        map.put("a", 0);
        map.put("b", 0);
        map.put("c", 0);
        System.out.println(map);
        for (int i = 0, na = 0, nb = 0, nc = 0; i < str.length; i++) {
            if (str[i].equals("a")) {
                map.put("a", ++na);
            } else if (str[i].equals("b")) {
                map.put("b", ++nb);
            } else if (str[i].equals("c")) {
                map.put("c", ++nc);
            }
        }
        System.out.println(map);
    }
}
