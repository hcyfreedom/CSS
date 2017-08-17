## 盒子模型包括两种：
w3c标准盒模型+IE怪异盒模型
### 最主要的区别在于一个块的宽度的计算方式不同。
标准模式下：一个块的总宽度 = width + margin + border + padding (默认) <br>
怪异模式下：一个块的总宽度 = width + margin
也就是说，怪异模式下，width包含了border和padding

## box-sizing:context-box || border-box || inherit
context-box：采用标准模式 <br>
border-box：采用怪异模式

并不是称为怪异模式就应该被规避掉，在经常要使用width:100%;的情况下，相对而言，border-box会省去很多的麻烦。
这个麻烦主要是避免一开始element的with设置为100%，而后又加了padding和border，那么又要再回头计算width；
虽然可以用calc计算这种情况下的width，但是calc这个属性兼容性有限；<br>

另外，表单默认content-box，按钮submit默认border-box，button的默认值也为border-box。

