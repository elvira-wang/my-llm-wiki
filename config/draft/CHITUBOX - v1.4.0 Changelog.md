# CHITUBOX 1.4.0更新日志

# 简体中文

CHITUBOX v1.4.0 已上线！分色拆件让模型拆分更加便利；悬空检测支持悬空点标记和筛选；图片标签助您轻松解锁图章制作；Z 轴复制搭配保护框架实现堆叠打印；更有自由选择空腔填充、坐标系切换、显卡切换、全局工具栏等丰富功能等待您来体验！

🚀 新增功能

● 拆件：自动为模型赋予颜色区块，可自定义颜色区块范围，根据颜色区块快速创建与调整切割面与连接结构；

● 齿科模型连接：将多个配套齿科模型通过横杆进行连接；

● 切换使用显卡：针对多显卡电脑，现可在设置页面切换以指定运行CHITUBOX的显卡；

● 悬空检测：新增悬空点标记功能，标记的悬空点在自动加支撑时会自动忽略；新增筛选器功能，便于筛选未处理/已标记的悬空点；在悬空点添加支撑后，不会再自动跳回首个悬空点；

● 空腔填充：可自由选择模型空腔进行填充；

● 坐标系切换：现可切换模型坐标系为全局坐标系或局部坐标系，更灵活适用于各种场景；

● 全局工具栏：整合多种工具的全新全局工具栏——适配各个功能的选择工具，扩展套索、刷选的选择方式；能在多种功能场景下使用的测量工具；还有ChituAction、ChituGlyph等快捷入口；

● 标签：标签功能新增图片标签，可通过调整图片黑阶、白阶、Gamma值决定图片标签形态；文字标签、图片标签新增翻转功能，适用于图章模型制作；

● 模型渲染：全新模型渲染设置，现可选择显示带纹理、X光、实体线框、线框等模型渲染方式；并可开启全新边框显示；

● 堆叠复制：复制功能新增Z轴复制，搭配可调保护框架，实现堆叠打印；

💫 改进

● 自由切割：现已支持多切割面，环状结构的模型可被成功分割；新增路径光滑功能，可将曲折的路径光滑化以形成更顺滑的切割面；新增榫卯自适应，根据切割面尺寸自动生成合适的榫卯；

● 自动保存与崩溃恢复：开始页新增自动保存tab，显示带有缩略图的自动保存文件；增强自动保存逻辑，现可在设置页设置自动保存目录、自动保存间隔、自动保存文件数量上限、保留期等；

● 模型轴显示：现可自定义切换移动轴、旋转轴、缩放轴的显示/隐藏；

● 拖动复制：现可在拖动模型过程中按住alt进行复制；

● 风险区域显示：现可开启网格显示，便于直观感受支撑间距；

● 按模型切片：优化了按模型切片模型列表与软件模型列表的对应显示关系；

● 切片文件命名：优化了切片文件命名显示格式；

🔧 修复

● 修复了含异常数据的ctp文件无法导入的问题；

● 修复了当像素尺寸≤0.025mm时，切片过程中像素丢失的问题；

● 修复了执行自动打孔预览会清除手动孔预览的问题；

● 修复了带支撑模型进行3D碰撞检测，移动模型卡顿问题；

● 修复了支撑缩放后，删除支撑后无法正确撤销的问题；

● 修复了替换模型后模型框与模型位置不一致问题；

● 修复了basic权限下交叉直径未正常记忆的问题。

# 繁體中文

CHITUBOX v1.4.0 已上線！分色拆件讓模型拆分更加便利；懸空檢測支援懸空點標記和篩選；圖片標籤助您輕鬆解鎖圖章製作；Z 軸複製搭配保護框架實現堆疊列印；更有自由選擇空腔填充、座標系切換、顯示卡切換、全域工具列等豐富功能等待您來體驗！

🚀 新增功能

● 拆件： 自動為模型賦予顏色區塊，可自訂顏色區塊範圍，根據顏色區塊快速建立與調整切割面及連接結構；

● 齒科模型連接： 將多個配套齒科模型透過橫桿連接；

● 切換使用顯示卡： 針對多顯示卡電腦，現在可在設定頁面切換並指定執行 CHITUBOX 的顯示卡；

● 懸空檢測： 新增懸空點標記功能，標記的懸空點在自動加支撐時會自動忽略；新增篩選器功能，便於篩選未處理及已標記的懸空點；在懸空點新增支撐後，不會再自動跳回第一個懸空點；

● 空腔填充： 可自由選擇模型空腔進行填充；

● 座標系切換： 現在可在全域座標系與局部座標系之間切換模型座標系，更靈活地適用於各種場景；

● 全域工具列： 全新的全域工具列整合多種工具，提供適用於不同功能的選取工具，擴充套索及刷選等選取方式；新增可在多種功能場景中使用的測量工具，以及 ChituAction、ChituGlyph 等快速入口；

● 標籤： 標籤功能新增圖示標籤，可透過調整圖片黑階、白階及 Gamma 值決定圖片標籤形態；文字標籤及圖片標籤新增翻轉功能，適用於圖章模型製作；

● 模型渲染： 全新的模型渲染設定，現在可選擇顯示紋理、X 光、實體線框或線框等模型渲染方式；並可啟用全新的邊框顯示；

● 堆疊複製： 複製功能新增 Z 軸複製，搭配可調整的保護框架，實現堆疊列印；

💫 改進

● 自由切割： 現在支援多個切割面，環狀結構的模型也可成功分割；新增路徑平滑功能，可將曲折路徑平滑化，以形成更順滑的切割面；新增榫卯自適應功能，可根據切割面尺寸自動生成合適的榫卯；

● 自動儲存與崩潰恢復： 開始頁新增自動儲存分頁，顯示帶有縮圖的自動儲存檔案；強化自動儲存邏輯，現在可在設定頁面設定自動儲存目錄、自動儲存間隔、自動儲存檔案數量上限及保留期限等；

● 模型軸顯示： 現在可自訂顯示或隱藏移動軸、旋轉軸及縮放軸；

● 拖曳複製： 拖曳模型時按住 Alt 鍵即可複製模型；

● 風險區域顯示： 現在可啟用網格顯示，便於直觀了解支撐間距；

● 依模型切片： 優化依模型切片模型清單與軟體模型清單的對應顯示關係；

● 切片檔案命名： 優化切片檔案名稱的顯示格式；

🔧 修復

● 修復含有異常資料的 CTP 檔案無法匯入的問題；

● 修復像素尺寸 ≤ 0.025 mm 時，切片過程中像素遺失的問題；

● 修復執行自動打孔預覽時會清除手動孔位預覽的問題；

● 修復對帶有支撐的模型進行 3D 碰撞檢測時，移動模型卡頓的問題；

● 修復支撐縮放後刪除支撐，無法正確復原的問題；

● 修復替換模型後模型框與模型位置不一致的問題；

● 修復 Basic 權限下交叉直徑未正確記憶的問題。

# English

CHITUBOX v1.4.0 has arrived! Split models more easily with color-based Parting; mark and filter overhang points with Overhang Detection; create custom stamps effortlessly with Image Labels; and combine copying in Z direction with protective frames for stacked printing. Plus, there are even more features like freely cavity picking and filling, coordinate system switching, GPU switching, and the global toolbar waiting to explore!

🚀 New Features

● Parting: Automatically assign color regions to the model. Customize the ranges of the color regions to quickly create and adjust cutting planes and connector structures.

● Dental Model Linking: Connect multiple matching dental models with crossbars.

● GPU Switching: On computers with multiple GPUs, select the GPU used to run CHITUBOX in the Settings page.

● Overhang Detection: Added overhang point markers. Marked overhang points are automatically ignored when adding supports. Added filters for unprocessed and marked overhang points. After adding a support to an overhang point, the view no longer automatically returns to the first overhang point.

● Cavity Filling: Freely select cavities in the model to fill.

● Coordinate System Switching: Switch the model coordinate system between global and local coordinates for greater flexibility in different scenarios.

● Global Toolbar: Added a new global toolbar that integrates multiple tools. It provides selection tools for different features, expands selection methods with lasso and brush selection, includes a measurement tool available across multiple workflows, and provides quick access to ChituAction and ChituGlyph.

● Labels: Added icon labels. Adjust the image black point, white point, and Gamma value to control the appearance of image labels. Added flip functions for text and image labels, suitable for creating stamp models.

● Model Rendering: Added new model rendering settings. Choose from textured, X-ray, solid wireframe, and wireframe rendering modes. Edge display is also available.

● Stack Copy: Added Z-axis duplication with an adjustable protective frame for stacked printing.

💫 Improvements

● Freeform Cutting: Now supports multiple cutting planes, allowing models with ring-shaped structures to be successfully split. Added path smoothing to smooth jagged paths and create smoother cutting planes. Added adaptive mortise-and-tenon joints that automatically generate suitable joints based on the cutting plane size.

● Autosave and Crash Recovery: Added an Autosave tab to the Start page, displaying autosaved files with thumbnails. Improved the autosave logic. The Settings page now allows you to configure the autosave directory, interval, maximum number of autosaved files, retention period, and more.

● Model Axis Display: Customize the visibility of the move, rotate, and scale axes.

● Drag to Copy: Hold Alt while dragging a model to create a copy.

● Risk Area Display: Mesh display can now be enabled to make support spacing easier to assess.

● Slice by Model: Improved the correspondence between the model list in Slice by Model and the software model list.

● Slice File Naming: Improved the display format of slice file names.

🔧 Fixes

● Fixed an issue where CTP files containing invalid data could not be imported.

● Fixed an issue where pixels could be lost during slicing when the pixel size was ≤ 0.025 mm.

● Fixed an issue where previewing automatic hole placement cleared the manual hole preview.

● Fixed an issue that caused lag when moving a supported model during 3D collision detection.

● Fixed an issue where undo did not work correctly after deleting a support following support scaling.

● Fixed an issue where the model box and model position became inconsistent after replacing a model.

● Fixed an issue where the cross diameter was not remembered correctly under Basic permissions.