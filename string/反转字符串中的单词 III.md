## 反转字符串中的单词 III.md

### 题目
> 给定一个字符串，你需要反转字符串中每个单词的字符顺序<br>
同时仍保留空格和单词的初始顺序。

<br>

### 示例
```
示例 1：

输入: "Let's take LeetCode contest"
输出: "s'teL ekat edoCteeL tsetnoc" 
```

>来源：力扣（LeetCode）<br>
链接：https://leetcode-cn.com/problems/reverse-words-in-a-string-iii/<br>
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

<br>

### 解题思路
```javascript
1、使用 `空格` 切割字符串返回单词数组
["let's", "take", ...]

2、遍历单词数组，对每个单词元素，切割成 `单字符数组` 
执行反转操作，之后 join 组合成字符串
["s'tel", "ekat", ...]

3、最后拿到 map 返回的数组， join 空格，返回字符串
`s'tel ekat ...`
```

<br>

### 题解
```javascript
let reverseWords = function(s) {
    // 使用 空格 切割字符串返回单词数组
    return s.split(' ').map(item => {
        // 遍历单词数组，对每个单词元素，切割成 `单字符数组` 
        // 执行反转操作，之后 join 组合成字符串
        return item.split('').reverse().join('')         
    }).join(' ')
    // 最后拿到 map 返回的数组， join 空格，返回字符串
}
```

<br>