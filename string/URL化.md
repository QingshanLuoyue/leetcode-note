## URL化

### 题目

>URL化。<br>
编写一种方法，将字符串中的空格全部替换为%20。<br>

>假定该字符串尾部有足够的空间存放新增字符，并且知道字符串的“真实”长度。<br>
（注：用Java实现的话，请使用字符数组实现，以便直接在数组上操作。）

>提示：<br>
字符串长度在[0, 500000]范围内。

<br>

### 示例
```
示例 1：

输入："Mr John Smith    ", 13
输出："Mr%20John%20Smith"
```

```
示例 2：

输入："               ", 5
输出："%20%20%20%20%20"
```

>来源：力扣（LeetCode）<br>
链接：https://leetcode-cn.com/problems/string-to-url-lcci<br>
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

<br>

### 解题思路
```javascript
1、直接截取 0 到 length 长度的字符串
   使用 正则 全局替换 空格 成 %20
```

力扣较好题解
```javascript
1、直接截取 0 到 length 长度的字符串
   使用 浏览器 encodeURIComponent/encodeURI 直接转换
```
<br>

### 题解
```javascript
// 用时较长，内存消耗较大
执行用时: 108 ms
内存消耗: 67.6 MB

let replaceSpaces = function(S, length) {
    // 直接截取 0 到 length 长度的字符串
    // 使用 正则 全局替换 空格 成 %20
    return S.slice(0, length).replace(/\s/g, '%20')
}
```

力扣较好题解
```javascript
// 用时较好，内存消耗较好
执行用时: 88 ms
内存消耗: 43.4 MB

let replaceSpaces = function(S, length) {
    // 直接截取 0 到 length 长度的字符串
    // 使用 浏览器 encodeURIComponent/encodeURI 直接转换
    return encodeURIComponent(S.slice(0, length));
    return encodeURI(S.slice(0, length));
}
```

<br>