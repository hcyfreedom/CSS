## 布局模式包括：
* 块布局：侧重垂直方向
* 行内布局：侧重水平方向
* 表格布局
* 定位布局
* 弹性盒子布局：方向无关
* 网格布局

弹性布局是指通过调整其内元素的宽高，从而在任何显示设备上实现对可用显示空间最佳填充的能力。弹性容器扩展其内元素来填充可用空间，或将其收缩来避免溢出。
<br>
flex布局已经得到了包括IE10+在内的所有浏览器的支持。

## 相关词汇
![图片](img/flexbox.png)
* flex container: 包含着弹性项目的父元素，定义：` .box{display : flex}`或者`.box{display:inline-flex}`;
这样做将元素定义为弹性容器，其子元素则成为弹性项目。值 flex 使弹性容器成为块级元素。值 inline-flex 使弹性容器成为单个不可分的行内级元素。
* flex item: flex container的每个子元素都称为弹性项目。弹性容器直接包含的文本将被包覆成匿名弹性单元。
* 轴(Axis):每个弹性框布局包含两个轴。弹性项目沿其依次排列的那根轴称为主轴(main axis)。垂直于主轴的那根轴称为侧轴(cross axis)。
    * flex-direction 确立主轴。
    * justify-content 定义了在当前行上，弹性项目沿主轴如何排布。
    * align-items 定义了在当前行上，弹性项目沿侧轴默认如何排布。
    * align-self 定义了单个弹性项目在侧轴上应当如何对齐，这个定义会覆盖由 align-items 所确立的默认值。
    
* 方向(Direction): 弹性容器的主轴起点(main start)/主轴终点(main end)和侧轴起点(cross start)/侧轴终点(cross end)描述了弹性项目排布的起点与终点。它们具体取决于弹性容器的主轴与侧轴中，由 writing-mode 确立的方向（从左到右、从右到左，等等）。
    * order 属性将元素与序号关联起来，以此决定哪些元素先出现。
    * flex-flow 属性是 flex-direction 和 flex-wrap 属性的简写，决定弹性项目如何排布。

* 行(Line): 根据 flex-wrap 属性，弹性项目可以排布在单个行或者多个行中。此属性控制侧轴的方向和新行排列的方向。             
* 尺寸(Dimension): 根据弹性容器的主轴与侧轴，弹性项目的宽和高中，对应主轴的称为主轴尺寸(main size) ，对应侧轴的称为 侧轴尺寸(cross size)。
    * min-height 与 min-width 属性初始值将为 0。
    * flex 属性是 flex-grow、flex-shrink 和 flex-basis 属性的简写，描述弹性项目的整体的伸缩性。


## 设置在容器上的属性
* flex-direction:决定主轴的方向，可取值：
    * row 水平方向，起点正在左端
    * row-reverse 主轴为水平方向，起点在右端
    * column 主轴为垂直方向，起点在上沿
    * column-reverse 主抽为垂直方向，起点在下沿
    
* flex-wrap：默认情况下，项目都排在一条线上（轴线），这个属性定义，如果一条轴线排不下，如何换行。取值：
   * nowrap：不换行，默认
   * wrap：换行，第一行在上方
   * wrap-reverse：换行，第一行在下方
   
* flex-flow：flex-direction和flex-wrap的简写形式，默认值row nowrap

* justify-content：定义了item在主轴上的对齐方式
   * flex-start：默认值，左对齐
   * flex-end：右对齐
   * center：居中
   * space-between：两端对齐，项目之间的间隔相等
   * space-around：每个项目两侧的间隔相等（所以项目之间的间隔会比项目与边框的间隔大一倍）

* align-items属性定义项目在交叉轴上如何对齐，具体对齐方式和轴的方向有关，取值：
   * flex-start：交叉轴（侧轴）的起点对齐
   * flex-end：交叉轴的终点对齐
   * center：交叉轴的中点对齐
   * baseline：项目的第一行文字的基线对齐
   * stretch：默认值，如果项目没有设置高度或者设为auto，将占满整个容器的高度
   
* align-content属性定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用。
   * flex-start：与交叉轴的起点对齐。
   * flex-end：与交叉轴的终点对齐。
   * center：与交叉轴的中点对齐。
   * space-between：与交叉轴两端对齐，轴线之间的间隔平均分布。
   * space-around：每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
   * stretch（默认值）：轴线占满整个交叉轴。
   
   
## 设置在项目上的属性
  * order：定义项目的排列顺序。数值越小，排列越靠前，默认为0。order:<integer>;
  * flex-grow:定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大。如果所有项目的flex-grow属性都为1，则它们将等分剩余空间（如果有的话）。如果一个项目的flex-grow属性为2，其他项目都为1，则前者占据的剩余空间将比其他项多一倍。
  * flex-shrink:定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。如果所有项目的flex-shrink属性都为1，当空间不足时，都将等比例缩小。如果一个项目的flex-shrink属性为0，其他项目都为1，则空间不足时，前者不缩小。负值对该属性无效。
  * flex-basis:flex-basis属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。
它可以设为跟width或height属性一样的值（比如350px），则项目将占据固定空间。
  * flex:flex属性是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。后两个属性可选。
  * align-self :align-self属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。   