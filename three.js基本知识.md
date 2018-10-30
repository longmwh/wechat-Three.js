three.js 可以简化webgl创建三维场景的过程。
使用three.js的好处：

1.创建简单和复杂的三维几何图形

2.在三维场景下创建动画和移动物体

3.为物体添加纹理和材质

4.使用各种光源来装饰场景

5.通过三维模型软件加载物体

6.为三维场景添加高级后期处理效果

7.使用自定义着色器
8.创建点云（粒子系统）


场景：
var scene = new THREE.Scene();
作用：用于保存、跟踪所要渲染的物体和使用的光源。
属性：
1.fog
2.overrideMaterial 设置改属性，会将场景中所有物体的材质设置为改属性值
3.autoUpdate: bool类型 
4.background: 首先被渲染
方法：
toJSON：获取场景的data
copy
add:添加元素到场景中（从Object3D中继承过来的方法）

[scene源码](https://github.com/mrdoob/three.js/blob/master/src/scenes/Scene.js "Markdown")

---------------------------------------------------------------------------------------
Object3d:three.js 中大多数对象的基类，
构造函数：Object3D()无参数
属性：
1.castShadow：对象是否渲染阴影，默认为false
2.children：子节点数组
3.frustumCulled：bool类型  设置true后，当boject不在摄像机视野范围内，则不再渲染。如果为false，则即使object不在视野范围内也会每一帧都渲染
4.id:只读，object的唯一码
5.isObject3D:内部使用，用来判断是否为object3d
6.layers:
7.matrix:Matrix4  本地转换矩阵
8.matrixAutoUpdate:bool  设置为true后，每一帧都会计算  位置，旋转，quaternion，缩放
9.matrixWorld:对象的世界变换矩阵，如果对象没有父节点（直接添加在场景上面）则改矩阵和matrix矩阵相同
10.matrixWorldNeedsUpdate:bool类型  设置后将会计算该帧的matrixWorld值，然后重置为false，该值默认为false
11.modelViewMatrix:传递给shader用于计算对象的位置
12.name:object的name，允许相同
13.normalMatrix:Matrix3 传递个shader用于计算光线
14.parent:object3d
15.position:Vector3   local position
16.quaternion:Quaternion   local rotation
17.receiveShadow:bool  该材质是否接收（渲染）阴影，默认为false
18.renderOrder: Number   控制对象的呈现顺序
19.rotation: Eduler   local rotation
20.scale: Vector3   local scale
21.up: Vector3  -----------------------和camera 还没有理解
22.userData: object   用于存储object3d数据的对象，不应该包含function
23.uuid:不应该被修改
24.visible:bool  对象是否被渲染

方法：
1.onAfterRender：object3D渲染后立即调用，参数：renderer,scene,camera,geometry,material,group
2.onBeforeRender:object3d渲染前调用，参数：renderer,scene,camera,geometry,material,group

Static Properties 静态属性
1.DefaultUp :Vector3
2.DefaultMatrixAutoUpdate:Vector3

方法：
1.add(object:Object3D,...):null
添加一个object作为该object的子节点，会删除传入对象之前的父节点

2.applyMatrix(matrix:Matrix4):null
将矩阵变换应用于该object 并且更新该object的位置，旋转，缩放

3.applyQuaternion(quaternion:Quaternion):Object3D
旋转

4.clone(recursive:Boolean):Object3D
clone该对象,如果recursive为true还clone其子节点.默认recursive为true

5.copy(object：Object3D,recursive:Boolean):this


6.






