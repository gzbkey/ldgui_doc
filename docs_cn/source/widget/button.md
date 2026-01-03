# button

## 说明
|函数名称|说明|
|---|---|
|ldButton_t* ldButtonInit(uint16_t nameId, uint16_t parentNameId, int16_t x, int16_t y, int16_t width, int16_t height)|创建button控件|
|void ldButtonSetColor(ldButton_t* ptWidget, ldColor releaseColor, ldColor pressColor)|设置button背景颜色|
|void ldButtonSetImage(ldButton_t* ptWidget,arm_2d_tile_t* ptReleaseImgTile,arm_2d_tile_t* ptReleaseMaskTile,arm_2d_tile_t* ptPressImgTile,arm_2d_tile_t* ptPressMaskTile)|设置button图片|
|void ldButtonSetTransparent(ldButton_t* ptWidget,bool isTransparent)|设置button是否透明|
|void ldButtonSetFont(ldButton_t *ptWidget, arm_2d_font_t *ptFont)|设置button字体|
|void ldButtonSetText(ldButton_t* ptWidget,uint8_t *pStr)|设置button文字|
|void ldButtonSetTextColor(ldButton_t* ptWidget,ldColor textColor)|设置button文字颜色|
|void ldButtonSetCheckable(ldButton_t *ptWidget,bool isCheckable)|设置button是否可自锁|
|void ldButtonSetKeyValue(ldButton_t *ptWidget,uint32_t value)|设置button按键值|
|void ldButtonSetPress(ldButton_t *ptWidget,bool isPress)|设置button是否按下|
|ldColor ldButtonGetReleaseColor(ldButton_t* ptWidget)|获取button背景颜色|
|ldColor ldButtonGetPressColor(ldButton_t* ptWidget)|获取button按下背景颜色|
|bool ldButtonGetTransparent(ldButton_t *ptWidget)|获取button是否透明|
|arm_2d_font_t *ldButtonGetFont(ldButton_t *ptWidget)|获取button字体|
|uint8_t *ldButtonGetText(ldButton_t* ptWidget)|获取button文字|
|ldColor ldButtonGetTextColor(ldButton_t* ptWidget)|获取button文字颜色|
|bool ldButtonGetCheckable(ldButton_t *ptWidget)|获取button是否可自锁|
|uint32_t ldButtonGetKeyValue(ldButton_t *ptWidget)|获取button按键值|
|bool ldButtonGetPress(ldButton_t *ptWidget)|获取button是否按下|

## 使用方法

~~~c
//创建一个默认的纯色按钮
#define ID_BG 0
#define ID_BUTTON_0 1
ldButton_t *obj=ldButtonInit(ID_BUTTON_0,ID_BG,10,10,50,20);
~~~

~~~c
//创建一个图片按钮
#define ID_BG 0
#define ID_BUTTON_0 1
#define FONT_ARIAL_16_A8          (arm_2d_font_t*)&ARM_2D_FONT_arial_16_A8
#define IMAGE_KEYRELEASE_PNG          (arm_2d_tile_t*)&c_tile_keyRelease_png_RGB565
#define IMAGE_KEYRELEASE_PNG_Mask     (arm_2d_tile_t*)&c_tile_keyRelease_png_Mask
#define IMAGE_KEYPRESS_PNG          (arm_2d_tile_t*)&c_tile_keyPress_png_RGB565
#define IMAGE_KEYPRESS_PNG_Mask     (arm_2d_tile_t*)&c_tile_keyPress_png_Mask
ldButton_t *obj=ldButtonInit(ID_BUTTON_0,ID_BG,10,10,50,20);
ldButtonSetFont(obj,FONT_ARIAL_16_A8);
ldButtonSetText(obj,(uint8_t*)"123");
ldButtonSetTextColor(obj,GLCD_COLOR_WHITE);
ldButtonSetImage(obj,IMAGE_KEYRELEASE_PNG,IMAGE_KEYRELEASE_PNG_Mask,IMAGE_KEYPRESS_PNG,IMAGE_KEYPRESS_PNG_Mask);
~~~
