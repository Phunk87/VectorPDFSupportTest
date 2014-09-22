# VectorPDFSupportTest

在 iOS App 中，图片一直是展现 App 细节的主要元素，它至关重要。当我们去开发一款 App 时，我们需要不同分辨率的图片以保证在不同分辨率的屏幕下均可得到精致的展示。随着 iPhone 设备迭出新，不同尺寸的分辨率需要适配，直到 iPhone 6 及 iPhone 6 Plus 发布前单启动时的 Default 图片就已经有 @1x, @2x, 568h@2x 三种尺寸需要适配了。iPhone 6 Plus 发布后，又多了一种尺寸，即 @3x 图片。

为了保证 App 的精致，不断为不同尺寸的屏幕提供相应的图片是必不可少的，但是却让开发者头疼。对于责任心稍稍差一点的程序员，很容易就出现因未添加相应尺寸图片而导致的问题：

- 因某个尺寸图片为添加出现模糊
- 因不确定图片是否添加而导致的图片模糊（因为每张图有不同尺寸管理起来会很伤神）

索性，从 Xcode 6 开始，苹果提供了一种更为优雅、高效、清晰的方式来管理工程内的图片资源。那就是 **矢量化 PDF (vectorized PDF)**。从此你不必再为单个分辨率导入 png 到你的工程内，而是通过导入 PDF 的方式，Xcode 6 会在 **编译时 (build-time)** 时根据 PDF 图片产生不同分辨率的 png 图片。这样既为开发者节省了时间，又让开发者减少了犯错的可能性。

## 工具 | Tools

现在可以导出 vector PDF 的工具有

- Photoshop
- Illustrtor
- Sketch 3

## 导入 PDF 到工程 | Import PDF to project

为了能使用这一特性，你需要使用一个 Xcode Asset Catalog 来管理你的图片。如下图，你需要将 Type 设置为 Vectors, 然后将你的 PDF 文件拖拽过去，Done!

![project image]()

## 示例工程运行后的效果

![iPhone 6 Plus]()
![iPad Retina]()
![iPhone 4s]()


## 更多资源 | More resources

- [USING VECTOR IMAGES IN XCODE 6](http://martiancraft.com/blog/2014/09/vector-images-xcode6/)
- WWDC 2014 [Session 411](https://developer.apple.com/videos/wwdc/2014/#411)
- Apple Developer [Asset Catalog Guide](https://developer.apple.com/library/ios/recipes/xcode_help-image_catalog-1.0/Recipe.html)
- Apple Developer [Interface Builder Guide](https://developer.apple.com/library/prerelease/ios/recipes/xcode_help-interface_builder/chapters/AboutInterfaceBuilder.html#//apple_ref/doc/uid/TP40009971-CH38-SW1)