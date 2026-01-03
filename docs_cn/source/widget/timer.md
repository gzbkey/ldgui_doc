# 软件定时器

## 说明
ldgui内置的软件定时器

|函数名称|说明|
|---|---|
|bool ldTimeOut(uint16_t ms, bool isReset)|简化调用版本|
|bool ldTimeOut(uint16_t ms, bool isReset, ldTimer_t *pTimer)|自定义变量版；</br>*pTimer中，数据为0，自动开始;</br>*pTimer中，数据为1，强制停止|

## 使用方法
~~~c
//1000ms循环触发
if(ldTimeOut(1000,true))
{
}
//1000ms一次性有效触发
if(ldTimeOut(1000,false))
{
}
~~~

~~~c
//自定义定时器变量
ldTimer_t timer=0;//全局变量或局部static变量
if(ldTimeOut(1000,true,&timer))
{
}
~~~