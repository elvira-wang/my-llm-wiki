---
title: " CHITUBOX V1.4.0：从分色拆件到堆叠打印"
language:
  - zh-Hans
  - en
status: draft
created: 2026-10-23
source: 用户提供的中文更新日志、功能说明及共同修订稿
---

# CHITUBOX V1.4.0：从分色拆件到堆叠打印

# CHITUBOX 1.4.0: From splitting models to stacking prints

拿到一个完整模型，不代表立刻就要完整地打印出来。有些部位拆开才方便上色，有些连接需要多切几处，有些小件您想一次多打几个。这次更新，我们从这些具体的打印准备开始。

Your model comes in one piece. That doesn't mean you have to print it that way. Some parts are easier to paint separately. Some need more than one cut to come apart. And sometimes, you just want to print a few more small parts in one go. CHITUBOX 1.4.0 brings new ways to get those jobs ready. Let's take a look.

## 有些部位，拆开来才方便上色

## Some parts are easier to paint on their own

新增的“拆件”功能会先为模型智能分色。您可以根据需要调整、合并分色区域，再按区域拆分模型。如果准备在上色后重新装配，还可以选择为切割面添加榫卯。

The new Part tool starts by automatically dividing your model into color-coded regions. Adjust or merge those regions to suit the parts you want, then split the model along their boundaries. Planning to put everything back together after painting? You can add mortise-and-tenon joints to the cut surfaces, too.

拆件效果受模型质量影响。内部结构存在问题，或区域划分较多且模型质量不佳时，可能出现切割失败或破面。

Results depend on the quality of your model. Problems with its internal geometry can cause cuts to fail or leave broken surfaces. Dividing a poor-quality model into many regions can also lead to these issues.

## 把图案，变成凹凸

## Give your artwork a little depth

想给模型加上自己的 Logo，或做出浮雕效果？“标签”新增了“图片”功能。导入黑白灰度图，用图像的明暗控制表面的凸起与凹陷，再根据需要调整大小和高度，选择阳刻或阴刻。想进一步调整图案的凹凸效果，还可以修改黑阶、白阶和 Gamma 值。

Want to add your own logo to a model, or turn an image into a relief? You can now add an image label. Import a grayscale image and use its light and dark areas to create raised or recessed details on the surface. Adjust the size and height, then choose an embossed or engraved effect. For more control over the result, you can adjust the black point, white point, and gamma.

如果准备制作印章，文字标签和图片标签现在都支持翻转，可以在打印前调整图案方向。

Making a stamp? Both text and image labels now support flipping, so you can get the artwork facing the right way before you print.

建议使用对比鲜明、背景干净的图片，让图案细节更容易呈现。

Start with a high-contrast image and a clean background to help the details come through.

## 批量打印，也可以向上安排

## No room left? Think up.

士兵模型已经列好队，平台却站不下？您可以在“复制”中勾选“在Z方向复制”，将模型沿高度方向排列。软件会自动添加可调整的保护框架，帮助您准备堆叠打印任务，充分利用平台上方的空间。

Got a whole squad of miniatures ready to print, but not enough room on the build plate? In the copy tool, enable copying along the Z axis to arrange models vertically. CHITUBOX automatically adds an adjustable protective frame to help you prepare a stacked print and make use of the space above the plate.

较大的模型不建议采用堆叠打印。

Stacked printing isn't recommended for large models.

## 多个切面，一次完成

## More than one cut. All in one go.

把茶杯把手拆下来，切开一端还不够。自由切割现在支持同时绘制多个切割面，让需要切开多处连接的部件也能在一次操作中完成拆分。遇到曲折的切割路径，还可以开启光滑处理，形成更顺滑的切割面。

Taking the handle off a cup? Cutting through one end won't quite do it. Free cutting now lets you draw multiple cutting surfaces at once, so parts attached in more than one place can be separated in a single operation. If your cutting path has a few too many twists and turns, you can also enable smoothing for a smoother cut surface.

需要添加榫卯时，新增的自适应功能会根据切割面尺寸，自动生成大小合适的榫卯。

Adding joints? The new adaptive option automatically sizes mortise-and-tenon joints to fit the cut surface.

切割效果受模型质量影响。如果原模型存在质量问题，可能出现切割失败、破面或碎面。

Cutting results depend on model quality. Issues in the original model can cause cuts to fail, leave broken surfaces, or produce small fragments.

## 加完你的，加你的，节奏尽在掌握中

## One island at a time. At your own pace.

给悬空点添加支撑后，该点会从黄色变为水蓝色，保留在视图中，也不再自动跳回首个未处理的悬空点。您可以留在当前位置，继续检查和添加支撑。

Add a support to an island and its marker now turns from yellow to light blue, staying visible instead of disappearing. The view no longer jumps back to the first untreated island, either. Stay where you are and keep checking or adding supports.

希望自动加支撑时跳过某个悬空点？给它添加标记，该点就会变为紫色，并在自动加支撑时被忽略。需要回头检查时，可以用新增的筛选器查找未处理或已标记的悬空点。

Want automatic supports to skip an island? Mark it manually. Its marker turns purple, and automatic support generation leaves it alone. When you want to take another look, the new filter helps you find untreated or marked islands.

## 还有这些改进

## A few more things

开始页新增了自动保存标签页，您可以通过缩略图辨认自动保存文件。保存目录、间隔、文件数量上限和保留期，也可以在设置中调整。

The start page now has an autosave tab, with thumbnails to help you recognize your saved projects. In settings, you can choose where autosaves go, how often they're created, how many to keep, and how long to keep them.

处理模型时，您可以自由选择要填充的空腔，切换全局或局部坐标系，或在拖动模型时按住 `Alt` 创建副本。

You can also choose which cavities to fill, switch between global and local coordinate systems, or hold `Alt` while dragging a model to make a copy.

全局工具栏整合了选择、测量等工具，并新增套索、刷选等选择方式。使用多显卡电脑的用户，也可以在设置中指定运行 CHITUBOX 的显卡。

The new global toolbar brings together tools for selection and measurement, with lasso and brush selection options. And if your computer has more than one graphics card, you can choose which one CHITUBOX uses in settings.

此外，我们修复了带支撑模型进行 3D 碰撞检测时移动卡顿，以及像素尺寸不大于 0.025 mm 时切片过程中像素丢失等问题。

We've also fixed lag when moving supported models during 3D collision detection, along with an issue that caused pixels to go missing during slicing at pixel sizes of 0.025 mm or smaller.

[查看 CHITUBOX 1.4.0 完整更新日志](https://www.chitubox.com/zh-Hans/product/changelog)

[See the full CHITUBOX 1.4.0 changelog](https://www.chitubox.com/en/product/changelog)

最后，祝您打印顺利。希望这次打出来的模型，是您舍不得收进柜子里的那一个。

Here's to a good print, and a model you'll want to leave out on display.
