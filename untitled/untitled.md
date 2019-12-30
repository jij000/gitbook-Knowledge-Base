# 17. Letter Combinations of a Phone Number

{% embed url="https://leetcode.com/problems/letter-combinations-of-a-phone-number/submissions/" %}

## Solution

```java
class Solution {
    Map<String, String> phone = new HashMap<String, String>() {{
        put("2", "abc");
        put("3", "def");
        put("4", "ghi");
        put("5", "jkl");
        put("6", "mno");
        put("7", "pqrs");
        put("8", "tuv");
        put("9", "wxyz");
    }};
    List<String> saveList;
    
    public List<String> letterCombinations(String digits) {
        
        saveList = new ArrayList<>();
        if (digits.length()>0) {
            letterCombinations_helper(digits, -1, "");
        }
        return saveList;
    }
    // save = digits(0...index-1) combination
    public void letterCombinations_helper(String digits, int index, String save ) {
        if (digits.length() == index + 1) {
            saveList.add(save);
            return;
        }
        String strLetter = phone.get(String.valueOf(digits.charAt(index + 1)));
        for (int i = 0; i<strLetter.length(); i++ ) {
            letterCombinations_helper(digits, index + 1, save + String.valueOf(strLetter.charAt(i)));
        }
    }
}
```

