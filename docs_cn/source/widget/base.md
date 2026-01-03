# 通用函数

## 说明
在ldBase.h中定义了一些通用函数，所有控件都可以直接使用这些函数

|函数名称|说明|
|---|---|
|ldWidgetType_t ldBaseGetWidgetType(ldBase_t *ptWidget)|获取控件类型|
|uint16_t ldBaseGetNameId(ldBase_t *ptWidget)|获取控件名称ID|
|ldBase_t* ldBaseGetParent(ldBase_t* ptWidget)|获取父控件|
|void* ldBaseGetWidgetById(uint16_t nameId)|通过名称ID获取控件|
|void ldBaseSetCenter(ldBase_t *ptWidget)|设置控件居中|
|bool ldBaseIsHidden(ldBase_t* ptWidget)|获取控件是否隐藏|
|uint16_t ldBaseGetOpacity(ldBase_t *ptWidget)|获取控件透明度|
|bool ldBaseIsSelectable(ldBase_t *ptWidget)|获取控件是否可被选中|
|bool ldBaseIsSelected(ldBase_t *ptWidget)|获取控件是否被选中|
|bool ldBaseIsCorner(ldBase_t *ptWidget)|获取控件是否圆角|
|void ldBaseSetHidden(ldBase_t* ptWidget,bool isHidden)|设置控件是否隐藏|
|void ldBaseSetOpacity(ldBase_t *ptWidget, uint8_t opacity)|设置控件透明度|
|void ldBaseSetSelectable(ldBase_t* ptWidget,bool isSelectable)|设置控件是否可被选中|
|void ldBaseSetSelect(ldBase_t* ptWidget,bool isSelect)|设置控件是否被选中|
|void ldBaseSetCorner(ldBase_t* ptWidget,bool isCorner)|设置控件是否圆角|
|void ldBaseSetRegion(ldBase_t* ptWidget,arm_2d_region_t region)|设置控件区域|
|void ldBaseMove(ldBase_t* ptWidget,int16_t x,int16_t y)|移动控件|
|void ldBaseResize(ldBase_t* ptWidget,arm_2d_size_t size)|设置控件大小|
|void ldBaseSetX(ldBase_t* ptWidget,int16_t x)|设置控件X坐标|
|void ldBaseSetY(ldBase_t* ptWidget,int16_t y)|设置控件Y坐标|
|void ldBaseSetWidth(ldBase_t* ptWidget,int16_t width)|设置控件宽度|
|void ldBaseSetHeight(ldBase_t* ptWidget,int16_t height)|设置控件高度|
|arm_2d_region_t ldBaseGetRegion(ldBase_t* ptWidget)|获取控件区域|
|arm_2d_location_t ldBaseGetLocation(ldBase_t* ptWidget)|获取控件位置|
|arm_2d_size_t ldBaseGetSize(ldBase_t* ptWidget)|获取控件大小|
|int16_t ldBaseGetX(ldBase_t* ptWidget)|获取控件X坐标|
|int16_t ldBaseGetY(ldBase_t* ptWidget)|获取控件Y坐标|
|int16_t ldBaseGetWidth(ldBase_t* ptWidget)|获取控件宽度|
|int16_t ldBaseGetHeight(ldBase_t* ptWidget)|获取控件高度|
