# 此文件用于记录 solidity 学习中从不同资料里获得的零星知识

## internal、private、external、public 区别

public 修饰的变量和函数，任何用户或者合约都能调用和访问。  
private 修饰的变量和函数，只能在其所在的合约中调用和访问，即使是其子合约也没有权限访问。  
internal 和 private 类似，不过， 如果某个合约继承自其父合约，这个合约即可以访问父合约中定义的“内部”函数。  
external 与 public 类似，只不过这些函数只能在合约之外调用 - 它们不能被合约内的其他函数调用。

## function 的修饰词，如 payable,view 等，如果没写，则是默认值 non-payable.

## constant view pure 关键字的区别与联系

![](./img/2022-03-20-10-37-32.png)  
如果函数使用了函数外的状态变量，只能用 view 修饰，使用 pure 修饰会报错。如果没有，则都可以修饰，但用 view 会有 warnning。

## 16 进制 big number 转 10 进制。合约里是 10 进制，但是前端返回确是 16 进制的 bignumber，所以需要转换下

parseInt(hex, 16)
其中 hex 代表 16 进制值。

---

(add,以上可能是错误的，需要将 16 改为 10)  
或者可以使用如下方法：  
![](./img/2022-03-22-16-39-56.png)

```
const { ethers } require("ethers")
var a = "0x03"
var b = ethers.BigNumber.from(a)
var c = b.toNumber()
console.log(c)
```