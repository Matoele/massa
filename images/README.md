# Massa公司网站图片

## 图片文件夹结构

本网站使用以下图片文件夹结构：

- `slider/`: 轮播图片
  - `craft-beer-equipment.jpg`: 精酿啤酒设备轮播图
  - `cold-brew-coffee.jpg`: 冷萃咖啡设备轮播图
  - `extraction-system.jpg`: 冷水萃取系统轮播图
  - `hero-background.jpg`: 主页背景图

- `products/`: 产品图片
  - `craft-beer-equipment.jpg`: 精酿啤酒设备
  - `cold-brew-equipment.jpg`: 冷萃咖啡设备
  - `extraction-system.jpg`: 冷水萃取系统
  - `cold-brew-process.jpg`: 冷萃咖啡流程
  - `microbrewery-system.jpg`: 微型啤酒酿造系统
  - `commercial-brewing-system.jpg`: 商用啤酒酿造系统

- `about/`: 关于我们页面图片
  - `production-facility.jpg`: 生产设施
  - `massa-history.jpg`: 公司历史
  - `massa-mission.jpg`: 公司使命
  - `david-chen.jpg`: 团队成员 - David Chen
  - `sarah-johnson.jpg`: 团队成员 - Sarah Johnson
  - `michael-rodriguez.jpg`: 团队成员 - Michael Rodriguez

- `process/`: 冷萃咖啡流程页面图片
  - `bean-grinding.jpg`: 咖啡豆研磨
  - `water-preparation.jpg`: 水的准备
  - `coffee-immersion.jpg`: 咖啡浸泡
  - `coffee-filtration.jpg`: 咖啡过滤
  - `cold-brew-storage.jpg`: 冷萃咖啡存储
  - `cold-brew-finishing.jpg`: 冷萃咖啡完成

- `testimonials/`: 客户评价头像
  - `john-roberts.jpg`: John Roberts头像
  - `emily-wong.jpg`: Emily Wong头像
  - `sarah-chen.jpg`: Sarah Chen头像
  - `michael-torres.jpg`: Michael Torres头像

## 如何替换图片

1. 请准备好与原图片尺寸相同的图片：
   - 轮播图片：1500 x 800像素
   - 产品图片：1000 x 600像素
   - 关于我们图片：1000 x 600像素（团队成员图片为500 x 300像素）
   - 流程图片：600 x 400像素
   - 客户评价头像：100 x 100像素

2. 为获得最佳显示效果，建议使用PNG或JPG格式的图片。

3. 将您的图片替换到对应的文件夹中，保持相同的文件名。

4. 如果您想使用不同的文件名，请同时更新HTML文件中的图片引用路径。

## 自定义样本图片

您也可以使用我们提供的`sample-image.html`工具来生成临时占位图：

访问 `images/sample-image.html` 并添加以下参数：
- `?bg=颜色代码`：设置背景颜色（十六进制，不含#符号）
- `&color=颜色代码`：设置文字颜色（十六进制，不含#符号）
- `&title=标题文本`：设置图片标题
- `&subtitle=副标题文本`：设置图片副标题

示例：`sample-image.html?bg=1a3c6e&color=ffffff&title=精酿啤酒&subtitle=Massa专业设备`

## 图片要求

- 所有图片应当是高质量、专业相关的内容
- 推荐格式: JPG或PNG
- 请优化图片以适合网页使用（在不明显损失质量的情况下压缩）
- 在每个部分内保持一致的宽高比
- 遵循建议的尺寸以确保布局正确显示

## 当前图片状态

目前网站使用的是空白图片文件，您需要替换这些文件以显示实际内容。可以使用以下方法获取适合的图片：

1. 使用专业摄影师拍摄您的实际设备和产品
2. 从图片库网站购买专业图片
3. 使用免费图片资源网站，如Unsplash、Pexels或Pixabay

## Placeholder Images

Until you add your own images, you can use placeholder images from services like:
- [Unsplash](https://unsplash.com) (search for relevant terms like "coffee", "brewing", "factory")
- [Pexels](https://pexels.com)
- [Pixabay](https://pixabay.com)

Or you can use placeholder image generators:
- [Placeholder.com](https://placeholder.com)
- [PlaceImg](https://placeimg.com)

## 重要说明：目前使用在线占位图

目前，网站使用的是通过Placeholder.com服务生成的在线占位图像。这是一个临时解决方案，以确保网站能够正常显示，直到您添加实际的图片。

这些在线占位图使用以下格式的URL：
```
https://via.placeholder.com/尺寸/背景色/文字色?text=显示文本
```

例如：
```
https://via.placeholder.com/1500x800/1a3c6e/ffffff?text=Craft+Beer+Equipment
```

### 如何替换为实际图片

要用实际图片替换占位图，请按照以下步骤操作：

1. 准备所需尺寸的实际图片（遵循上面的推荐尺寸）
2. 将图片文件放入相应的文件夹（slider、products、about、process等）
3. 在HTML或CSS文件中，将在线占位图URL更改为相对路径，例如：
   - 从: `src="https://via.placeholder.com/1500x800/1a3c6e/ffffff?text=Craft+Beer+Equipment"`
   - 改为: `src="images/slider/craft-beer-equipment.jpg"`

### 离线开发注意事项

如果您在离线环境中开发，或者想避免依赖外部服务，建议尽快用实际图片替换这些在线占位图。 