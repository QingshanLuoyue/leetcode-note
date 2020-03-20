## IP 地址无效化

### 题目
> 给你一个有效的 IPv4 地址 address，返回这个 IP 地址的无效化版本。<br>
所谓无效化 IP 地址，其实就是用 "[.]" 代替了每个 "."。

<br>

### 示例
```
示例 1：

输入：address = "1.1.1.1"
输出："1[.]1[.]1[.]1"
```

```
示例 2：

输入：address = "255.100.50.0"
输出："255[.]100[.]50[.]0"
```

>来源：力扣（LeetCode）<br>
链接：https://leetcode-cn.com/problems/defanging-an-ip-address/<br>
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

<br>

### 解题思路
```javascript
1、
使用正则匹配，简单，明了
在给出的字符串 IP 地址中，匹配到全局每个 `.` ，最后使用 `[.]` 进行替换
```

或者

```javascript
1、
使用字符串切割
切割字符串 IP 地址中每个 `.` ，得到数组
最后使用 join 方法， `[.]` 作为连接符，组成字符串
```

<br>

### 题解
```javascript
// 推荐使用正则
let defangIPaddr = function(address) {
    return address.replace(/\./g, '[.]')
}
```

或者

```javascript
let defangIPaddr = function(address) {
    return address.split('.').join('[.]')
}
```
<br>
