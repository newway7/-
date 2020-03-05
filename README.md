# Two-column-layout
#  两栏布局的总结

#### 两栏布局的主要点在于如何让两个div元素并列，以及让他们之间相互不重叠；

并列的几种方案：
inline-block，需要设置父元素字体大小，计算右侧的宽度，对齐方式；

双float；父容器清除浮动；计算右侧的宽度；

absolute，绝对定位，需要设置父元素的min-height，右侧元素的margin-left；

float+overflow；双bfc;两个元素相互不影响；不需要计算盒子宽度；只设置间距；清除浮动；利用块级元素宽度自动填充的特点；


float+margin-left方案：计算右侧盒子margin-left，清除浮动；

display：flex；这个没啥好说的
.wrapper-flex {
    display: flex;
    align-items: flex-start;
}

.wrapper-flex .left {
    flex: 0 0 auto;
}

.wrapper-flex .right {
    flex: 1 1 auto;
}

grid，这个兼容性不好；

.wrapper-grid {
    display: grid;
    grid-template-columns: 120px 1fr;
    align-items: start;
}
