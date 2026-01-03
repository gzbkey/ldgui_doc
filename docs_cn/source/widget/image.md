# image

## 说明
|函数名称|说明|
|---|---|
|ldImage_t* ldImageInit(uint16_t nameId, uint16_t parentNameId, int16_t x, int16_t y, int16_t width, int16_t height, arm_2d_tile_t* ptImgTile, arm_2d_tile_t* ptMaskTile, bool isWindow)|创建image控件|
|void ldImageSetBackgroundColor(ldImage_t *ptWidget,ldColor bgColor)|设置image背景颜色|
|void ldImageSetImage(ldImage_t *ptWidget, arm_2d_tile_t* ptImgTile, arm_2d_tile_t* ptMaskTile)|设置image图片|
|ldColor ldImageGetBackgroundColor(ldImage_t *ptWidget)|获取image背景颜色|

### 使用方法

~~~c
#define ID_BG 0
#define ID_IMAGE_0 1
ldImage_t *obj=ldImageInit(ID_IMAGE_0,ID_BG,ID_WINDOW_0,10,10,200,200,&g_tImage,NULL,false);
ldBaseSetCorner(obj,true);
ldBaseSetSelectable(obj,true);
~~~