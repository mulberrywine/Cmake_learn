# Cmake_learn
- Cmake编译源文件时CMakelists.txt的编写原则
--------------------
**修改时间为2021/4/12**
**好好经营**  
[百度](http://www.baidu.com)  
<font size =7 color = "blue">链表</font>
---------------------
pthread_create()在创建线程的时候如果有用到  
```C++
pthread_t tid;
int err;
err = pthread_create(&tid,NULL,A::b,this);
//this是A::b的参数，一般指的是本类；传入到函数中进行使用
//如果有用到其他的类就可以对this强制转化
void* A::b(void *arg)
{
  C.d = (( A*)arg)->e;
}
```
