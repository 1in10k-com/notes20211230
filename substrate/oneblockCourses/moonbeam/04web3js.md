![](./img/2022-04-29-13-48-52.png)

![](./img/2022-04-29-13-54-52.png)

![](./img/2022-04-29-13-56-20.png)

本课内容

课程脚本：
https://github.com/hyd628/moonbeam-intro-course-scripts

---

---

![](./img/2022-04-29-13-57-49.png)  
安装 web3

---

---

![](./img/2022-04-29-15-06-25.png)  
新建 transaction.js 文件，代码解释看视频

---

---

![](./img/2022-04-29-15-21-06.png)  
回到上节课目录，用 truffle 启动一个 docker moonbeam 节点。docker logs ID 查看运行状态

---

---

![](./img/2022-04-29-15-24-14.png)  
设置发款账户私钥和地址，以及收款账户地址。

---

---

![](./img/2022-04-29-15-25-18.png)  
执行，看到结果。

---

---

![](./img/2022-04-29-15-26-41.png)  
本地链和测试链只用替换这里就行

---

---

npm install solc@0.8.0

部署智能合约 solc=solidity compiler.

![](./img/2022-04-29-15-35-50.png)  
智能合约代码

![](./img/2022-04-29-15-36-23.png)  
编译文件，compiler.js

![](./img/2022-04-29-15-37-11.png)  
部署文件，deploy.js

之后 node deploy.js 部署

---

---

![](./img/2022-04-29-15-48-37.png)

使用 web3，读取智能合约

---

---

![](./img/2022-04-29-15-51-04.png)  
web3，修改合约数据

---

---

![](./img/2022-04-29-15-53-06.png)  
web3，监听事件

---

---

![](./img/2022-04-29-15-55-30.png)  
wb3，监听智能合约事件。topics 接空数组代表监听所有事件，如果只监听某事件，则需提供 event hash。

---

---

![](./img/2022-04-29-15-57-08.png)

![](./img/2022-04-29-15-57-46.png)

![](./img/2022-04-29-15-58-22.png)
得到 event hash 的方法

![](./img/2022-04-29-16-02-26.png)  
事件里的参数隐藏在 data 字段里。

![](./img/2022-04-29-16-03-15.png)  
常见错误
