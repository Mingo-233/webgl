## 理解为一个状态机，bindBuffer
请谨记：程序中如果有多个 buffer 的时候，在切换 buffer 进行操作时，一定要通过调用 gl.bindBuffer 将要操作的 buffer 绑定到 gl.ARRAY_BUFFER 上，这样才能正确地操作 buffer 。您可以将 bindBuffer 理解为一个状态机，bindBuffer 之后的对 buffer 的一些操作，都是基于最近一次绑定的 buffer 来进行的。
## 顶点顺序为逆时针时代表正面
请谨记，组成三角形的顶点要按照一定的顺序绘制。默认情况下，WebGL 会认为顶点顺序为逆时针时代表正面，反之则是背面，区分正面、背面的目的在于，如果开启了背面剔除功能的话，背面是不会被绘制的。当我们绘制 3D 形体的时候.