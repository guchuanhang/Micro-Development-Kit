# Micro-Development-Kit
微量级的软件开发包，目前版本提供一些基础类，和一个tcp的网络引擎

使用c++开发，是一个跨平台的开发包，支持linux32/linux64/win32/win64的类库。

mdk服务器引擎，提出面向业务的服务器开发模式，根据服务器业务层最关心的3件事，抽象出连接发生（OnConnect），消息到达（OnMsg），连接关闭（OnClose）3个接口，让服务器端开发者可以全身心的投入业务逻辑的开发中。

特点：

       提供分布式支持，自身是一个server-client的结合体（即做服务器使用的同时，也可以像client一样去连接别的服务器，组成分布式系统），并且io接口统一到onconnect onmsg onclose中，不必区别对待

       事件轮巡使用的是原生epoll iocp实现，确保了对io响应速度的完全掌控

       几乎等同于lock free的并发算法，保证并发效率                                    引用自OSChina.
