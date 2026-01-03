# window

## 说明
|函数名称|说明|
|---|---|
|ldWindow *ldWindowInit(nameId,parentNameId,x,y,width,height)|创建window控件|
|ldWindowSetColor|设置window背景颜色|
|ldWindowSetImage|设置window背景图片|

## 使用方法
ldgui中页面背景和window控件实际为image控件，但只能设置背景颜色或者背景图片

~~~c
#define ID_BG 0
#define ID_WINDOW_0 1
ldWindow *obj=ldWindowInit(ID_WINDOW_0,ID_BG,10,10,200,200);
ldWindowSetColor(obj,ldColor(0xff,0xff,0xff));
~~~
