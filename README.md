# iOS-Interview
> 面试知识点整理

- [UI视图相关](#UI视图相关)
  - [UIView跟CALayer](#UIView跟CALayer)
  - [事件传递与视图响应链](#事件传递与视图响应链)
  - [图像显示原理](#图像显示原理)
  - [UI卡顿掉帧原因](#UI卡顿掉帧原因)
  - [绘制原理一异步绘制](#绘制原理一异步绘制)
  - [离屏渲染](#离屏渲染)
- [内存管理](#内存管理)
  - [内存布局](#内存布局)
  - [内存管理方案](#内存管理方案)
  - [ARC与MRC](#ARC与MRC)
  - [弱引用](#弱引用)
  - [自动释放池](#自动释放池)
- [Objective-C语言特性](#Objective-C语言特性)
  - [分类](#分类)
  - [扩展](#扩展)
  - [代理](#代理)
  - [通知](#通知)
  - [KVO](#KVO)
  - [KVC](#KVC)
- [Block](#Block)
  - [Block介绍](#Block介绍)
  - [Block判空操作](#Block判空操作)
  - [截获变量](#截获变量)
  - [__block修饰符](#__block修饰符)
  - [Block内存管理](#Block内存管理)
  - [Block循环引用](#Block循环引用)
- [多线程](#多线程)
  - [进程和线程](#进程和线程)
  - [任务和队列](#任务和队列)
  - [GCD](#GCD)
  - [NSOperation](#NSOperation)
  - [NSThread](#NSThread)
  - [多线程与锁](#多线程与锁)
  - [线程间通信](#线程间通信)
- [Runtime](#Runtime)
  - [Runtime数据结构](#Runtime数据结构)
  - [对象一类对象一元类对象](#对象一类对象一元类对象)
  - [消息传递](#消息传递)
  - [消息转发](#消息转发)
  - [Method-Swizzling](#Method-Swizzling)
  - [动态添加方法](#动态添加方法)
  - [动态方法解析](#动态方法解析)
   
- [Runloop](#Runloop)
  - [概念](#概念)
  - [Runloop数据结构](#Runloop数据结构)
  - [Runloop与NSTimer](#Runloop与NSTimer)
  - [Runloop与多线程](#Runloop与多线程)

 - [Crash](#Crash)
 - [概念](#概念) 
  
- [网络](#网络)
  - [HTTP协议](#HTTP协议)
  - [HTTPS与网络安全](#HTTPS与网络安全)
  - [TCP和UDP传输层协议](#TCP和UDP传输层协议)
  - [DNS解析](#DNS解析)
  
  
- [设计模式](#设计模式)
  - [设计原则](#设计原则)
      - [单一职责原则](#单一职责原则)
      - [依赖倒置原则](#依赖倒置原则)
      - [开闭原则](#开闭原则)
      - [里氏替换原则](#里氏替换原则)
      - [接口隔离原则](#接口隔离原则)
      - [迪米特原则](#迪米特原则)
  - [设计模式](#设计模式)
      - [责任链模式](#责任链模式)
      - [桥接模式](#桥接模式)
      - [适配器模式](#适配器模式)
      - [单例模式](#单例模式)
      - [命令模式](#命令模式)
      
- [框架及架构](#框架及架构)
  - [图片缓存框架](#图片缓存框架)
  - [客户端架构](#客户端架构)
      

- [性能优化](#性能优化)
  - [UI](#UI)
  - [耗电优化](#耗电优化)
  - [APP启动优化](#APP启动优化)
  - [安装包瘦身](#安装包瘦身)
  - [崩溃优化](#崩溃优化)
  - [内存泄露](#内存泄露)
  
- [WKWebView的坑](#WKWebView的坑)
  - [WKWebView白屏](#WKWebView白屏)
  - [WKWebView的Cookie问题](#WKWebView的Cookie问题)
  - [WKWebView的loadRequest问题](#WKWebView的loadRequest问题)
  
- [AFNetWorking](#AFNetWorking)
  - [主要构成](#主要构成)
  - [相关面试问题](#相关面试问题)
  - [为什么要更换]
  
- [SDWebImage](#SDWebImage)
  - [主要构成](#主要构成)
  - [相关面试问题](#相关面试问题)  

- [算法](#算法)
  - [求和](#求和)
    - [俩数之和](#俩数之和)
    - [三数之和](#三数之和)
    - [四数之和](#四数之和)
  - [数组](#数组)
    - [二分查找](#二分查找)
    - [移除元素](#移除元素)
    - [数组平方](#数组平方) 
    - [长度最小子数组](#长度最小子数组) 
    - [螺旋矩阵](#螺旋矩阵)
  - [字符串](#字符串)
    - [翻转字符串1](#翻转字符串1)
    - [翻转字符串2](#翻转字符串2)
    - [替换空格](#替换空格)
    - [翻转单词](#翻转单词)
    - [左旋转字符串](#左旋转字符串)
    - [KMP](#KMP)
    - [重复子字符串](#重复子字符串)
 
  - [链表](#链表)
    - [移除链表元素](#移除链表元素)
    - [翻转链表1](#翻转链表1)
    - [翻转链表2](#翻转链表2)
    - [删除倒数N节点](#删除倒数N节点)
    - [链表相交](#链表相交)
    - [环入口](#环入口)
  - [二叉树](#二叉树)
    - [递归遍历](#递归遍历)
    - [迭代遍历](#迭代遍历)
    - [层序遍历1](#层序遍历1)
    - [层序遍历2](#层序遍历2)
    - [二叉树右视图](#二叉树右视图)
    - [二叉树层平均值](#二叉树层平均值)
    - [N叉树层次遍历](#N叉树层次遍历)
    - [每个数找最大值](#每个数找最大值)
    - [填充每个节点的下一个右侧节点指针1](#填充每个节点的下一个右侧节点指针1)
    - [填充每个节点的下一个右侧节点指针2](#填充每个节点的下一个右侧节点指针2)
    - [二叉树最大深度](#二叉树最大深度)
    - [二叉树最小深度](#二叉树最小深度)
    - [翻转二叉树](#翻转二叉树)
    - [对称二叉树](#对称二叉树)
    - [完全二叉树的节点个数](#完全二叉树的节点个数)
    - [平衡二叉树](#平衡二叉树)
    - [二叉树所有路径](#二叉树所有路径)
    - [左叶子之和](#左叶子之和)
    - [左下角](#左下角)
    - [路径总和1](#路径总和1)
    - [路径总和2](#路径总和2)
    - [构造二叉树](#构造二叉树)
    - [数组构造二叉树](#数组构造二叉树)
    - [合并二叉树](#合并二叉树)

-[Swift]

## UI视图相关

#### UIView跟CALayer
- 单一原则
- UIView为CALayer提供内容以及负责处理触摸事件,参与响应链
- CALayer负责显示内容的Content
#### 事件传递与视图响应链
```
- (UIView *)hitTest:(CGPoint)point withEvent:(UIEvent *)event;
- (BOOL)pointInside:(CGPoint)point withEvent:(UIEvent *)event;
```
###### 事件传递示例图

- 我们点击屏幕产生触摸事件，系统将这个事件加入到一个由UIApplication管理的事件队列中，UIApplication会从消息队列里取事件分发下去，首先传给UIWindow
- 在UIWindow中就会调用hitTest:withEvent:方法去返回一个最终响应的视图
- 在hitTest:withEvent:方法中就回去调用pointInside: withEvent:去判断当前点击的point是否在UIWindow范围内，如果是的话，就会去遍历它的子视图来查找最终响应的子视图
- 遍历的方式是使用倒序的方式来遍历子视图，也就是说最后添加的子视图会最先遍历，在每一个视图中都会去调用它的hitTest:withEvent:方法，可以理解为是一个递归调用
- 最终会返回一个响应视图，如果返回视图有值，那么这个视图就作为最终响应视图，结束整个事件传递；如果没有值，那么就会将UIWindow作为响应者
---
![avatar](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E4%BA%8B%E4%BB%B6%E4%BC%A0%E9%80%92.png)

---

###### `hitTest:withEvent:`系统实现示例图

- 首先会判断当前视图的hiden属性、是否可以交互以及透明度是否大于0.01，如果满足条件则进入下一步，否则返回nil
- 调用pointInside: withEvent:方法来判断这个点是否在当前视图范围内，如果满足条件则进入下一步，否则返回nil

- 然后以倒序的方式遍历它的子视图，在每个子视图中去调用hitTest:withEvent:方法，如果有一个子视图返回了一个最终的响应视图，那么就将这个视图返回给调用方；如果全部遍历完成都没有找到一个最终的响应视图，因为点击位置在当前视图范围内，就将当前视图作为最终响应视图返回

---
![avatar](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/hitTest.png)

---

###### 视图响应者链
- 与事件传递过程相反
- 如果hitTest:withEvent:找到了第一响应者initial view，但是该响应者没有处理该事件，那么事件会沿着响应者链向上传递：第一响应者 -> 父视图 -> 视图控制器，如果传递到最顶级视图还没处理事件，那么就传递给UIWindow去处理，若window对象也不处理那么就交给UIApplication处理，如果UIApplication对象还不处理，就丢弃该事件（但是并不会引起崩溃）

###### 给Button添加手势UIGes

> 给button添加手势后,不走button的方法
- UIButton--->UIContorl--->UIView--->UIResponder
- UIGestureRecognizer有个属性`cancelsTouchesInView`,默认值是`YES`,代表当手势识别成功后,会发送`touchsCancelled`消息给`view(此处是button)`来结束`view`的响应
- 解决一:`cancelsTouchesInView = NO`,那么手势跟view都响应
- 解决二:`gesture`代理方法加判断

  ```
  - (BOOL)gestureRecognizer:(UIGestureRecognizer *)gestureRecognizer shouldReceiveTouch:(UITouch *)touch{
    if ([touch.view isKindOfClass:[UIButton class]]) {
        return NO;
    }
    return YES;
  }
  ```

#### 图像显示原理
###### 图像显示原理
- CPU和GPU两个硬件是通过总线链接起来的
- 在CPU中输出的结果是位图，经由总线在合适的时机上传给GPU
- GPU拿到位图之后，会做相应位图的图层渲染，包括纹理的合成之后会把结果放到帧缓冲区（Frame Buffer）当中
- 由视频控制器根据VSync信号在指定时间之前去提取在帧缓存区当中的显示内容，最终显示到手机屏幕上

###### UIView显示原理
- 当创建一个UIView控件之后，显示部分是由 CALayer 来负责的
- CALayer当中有一个contents属性，就是我们最终要绘制到屏幕上的位图
- 比如说我们创建的是一个UILable，contents里面最终放置的结果就是关于hello word的文字位图
- 然后系统会在合适的时机回调一个drawRect：方法，在此基础上可以绘制一些自定义想要绘制的内容
- 绘制好的位图，最终会由Core Animation框架提交给GPU部分的OpenGL（ES）渲染管线进行最终的位图的渲染，包括纹理的合成，然后显示到屏幕上面


---
![avatar](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%9B%BE%E5%83%8F%E6%98%BE%E7%A4%BA%E5%8E%9F%E7%90%86.png)

---
#### UI卡顿掉帧原因

- 如果要保持界面滑动流畅那就需要保证60FPS,那么就需要在16.7ms的时间内,CPU和GPU协同完成产生一帧的数据
- 在这个时间内CPU和GPU没有来得及生产出一帧缓冲，那么在下一次`VSnc`信号之前, 那么这一帧会被丢弃，显示器就会保持不变，继续显示上一帧内容，这就将导致导致画面卡顿
---
![avatar](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%8D%A1%E9%A1%BF%E6%8E%89%E5%B8%A7.png)

---

###### 优化方案
- CPU
  - 对象创建、调整、销毁（可以放在子线程）
  - 预排版（布局计算，文本计算）
  - 预渲染（文本等异步绘制，图片编码等）
- GPU
  - 纹理渲染（避免离屏渲染、CPU异步绘制机制减轻GPU压力）
  - 视图混合（减轻层级复杂度）
#### 绘制原理一异步绘制

###### UIView绘制流程
- 当我们调用[UIView setNeedsDisplay]这个方法时，系统没有立即进行绘制工作，而是立刻调用CALayer的同名方法，并且会在当前layer上打上一个标记，然后会在当前runloop将要结束的时候调用[CALayer display]这个方法，然后进入真正绘制过程
- 在[CALayer display]这个方法的内部实现中会判断这个layer的delegate是否响应displayLayer:这个方法，
  - 不响应，进入到**系统绘制**流程中；
  - 响应，为我们提供**异步绘制**的入口

![avatar](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/UIView%E7%BB%98%E5%88%B6%E5%8E%9F%E7%90%86.png)

###### 系统绘制
- 在`CALayer`内部会先创建`backing store`(可以理解为`CGContext`)，一般在`drawRect`:方法中通过上下文堆栈当中取出栈顶的`context`,也就是上下文

- 然后这个`layer`会判断是否有代理
  - 如果没有代理，那么就会调用`[CALayer drawInCotext:]`；
  - 如果有代理，会调用代理的`drawLayer:inContext:`方法，然后做当前视图的绘制工作（这一步是发生在系统内部的），然后在一个合适的时机给与我们`[UIView drawRect:]`方法的回调
- 然后无论是哪个分支，最终都会由`CALayer`上传对应的`backing store`(位图)给`GPU`，然后就结束了系统默认的绘制流程

![CALayer%E7%BB%98%E5%88%B6.png](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/CALayer%E7%BB%98%E5%88%B6.png)
###### 异步绘制
- 异步绘制需要系统的`[layer.delegate displayLayer:]`,这个过程需要代理负责生成对应的`bitmap`,同时设置`bitmap`为`layer.contents`属性的值
- 假如在某一个时机调用了`[view setNeedsDisplay]`这个方法，系统会在当前`runloop`将要结束的时候调用`[CALyer display]`方法，然后如果我们这个layer的代理实现了`[view displayLayer]`这个方法
- 然后会通过子线程的切换，我们在子线程中去做一个位图的绘制，主线程可以去做一些其他的操作
- 在子线程中第一步先通过`CGBitmapContextCreate()`方法来创建一个位图的上下文，然后我们通过`CoreGraphic API`可以做当前UI控件的一些绘制工作，最后我们再通过`CGBitmapContextCreateImage()`这个函数来根据当前所绘制的上下文来生成一张`CGImage`图片

- 最后回到主线程来提交这个位图，设置`layer`的`contents`属性，这样就完成了一个UI控件的异步绘制过程
![avatar](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%BC%82%E6%AD%A5%E7%BB%98%E5%88%B6.png)
#### 离屏渲染

###### 含义
> 离屏渲染指的是GPU在当前屏幕缓冲区以外开辟了一个缓冲区进行渲染操作

###### 坏处
- 创建了新的缓冲区
- 上下文频繁切换

###### 原因
- 圆角(和maskToBounds一起使用)
- 图层蒙版(mask)
- 阴影(shadows)
- 光栅化(shouldRasterize)

## 内存管理
#### 内存布局

![内存布局](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%86%85%E5%AD%98%E7%A9%BA%E9%97%B4.png)
- 栈(stack) -- ↓
  - 方法调用
- 堆(heap) -- ↑
  - 通过alloc分配的对象
- 未初始化数据(.bss)
  - 未初始化的全局变量 未初始化静态变量
- 已初始化数据(.data)
  - 已初始化的全局变量
- 代码段(.text)
  - 程序代码

#### 内存管理方案

> 不同场景不同管理方案

- **Tagged Poingter** 
  - 64bit开始引入`Tagged Poingter `优化小对象的存储:如`NSNumber`,`NSDate`,`NSString`
  - 在没有使用Tagged Pointer之前， NSNumber等对象需要动态分配内存、维护引用计数等，NSNumber指针存储的是堆中NSNumber对象的地址值
  - 使用Tagged Pointer之后，NSNumber指针里面存储的数据变成了：Tag + Data，也就是将数据直接存储在了指针中
  - 当指针不够存储数据时，才会使用动态分配内存的方式来存储数据
  - objc_msgSend能识别Tagged Pointer，比如NSNumber的intValue方法，直接从指针提取数据，节省了以前的调用开销


- **NONPOINTER_ISA**

  ![NONPOINTER_ISA](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/NONPOINTER_ISA.png)
  - arm64架构下是一个64bit
    - 0 :indexed 0是纯`isa`指针
    - 1 :has_assoc 是否关联对象 
    - 2 :has_cxx_dtor 是否使用过c++
    - 3->15 + 16->31 + 32->35 共33位来表示内存地址
    - 36->41 magic
    - 42 :weakly_referenced 弱引用
    - 43 :deallocating 是否在进行dealloc操作
    - 44 :has_sidetable_rc 当前存储引用计数是否到达上限
    - 45-63 extra_rc 额外引用计数
- **散列表**

> 在64bit中，引用计数可以直接存储在优化过的isa指针中，也可能存储在SideTable类中
> 

  ![SideTables().png](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/SideTables().png)

  > 为什么不是一个`SideTable`,而是多个组成的`SideTables`?
  > 

  > 如果是一张大表的话,如果要操作某个对象的引用计数值进行修改,由于对象可能是在不同线程中创建的,所以进行操作时需要加锁操作才能保证数据安全,存在效率问题
  > 
  
  >  解决办法 

  > 分离锁计数方案,分拆成8个,假如对象A B分别在不同表的话,可以并发进行操作加锁处理
  > 

  > 怎么实现快速分流?通过对象的指针,如何快速定位到其属于哪张`SideTable`表?
  > 

  > `SideTables`本质是一张`Hash`表,里面有64张具体的`SideTable`,存储不同对象的引用计数表和弱引用表,通过对象的指针通过`hash`函数可以得到具体在`SideTables`中具体位置;`f(ptr) = (uintptr_t) % array.count`
  > 

  - `SideTables()`
    - `spinlock_t` 自旋锁
      - `spinlock_t` 是一种忙等的锁
      - 适用于轻量访问

    - `RefcountMap`引用计数表
      - `hash`表
      - `size_t`代表对象的引用计数值,需向右偏移俩位来计算
      ![RefcountMap.png](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/RefcountMap.png)
    - `weak_table_t`弱引用表
      - `hash`表
      ![%E5%BC%B1%E5%BC%95%E7%94%A8%E8%A1%A8.png](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%BC%B1%E5%BC%95%E7%94%A8%E8%A1%A8.png)

#### ARC与MRC

- MRC
  - **`alloc`**
    - 经过一系列的调用,最终调用了C函数的`calloc`
    - 此时并没有设置引用计数为1
  - **`retain`**
    - **`SideTable &table = SideTables()[this]`** //通过当前对象的指针,通过`hash`函数计算在`SideTables`找到对应的`sizeTable`
    - **`size_t &refcntStorage = table.refcnts[this]`**
    - **`refcntStorage += SIDE_TABLE_RC_ONE`**  // 此处加1,并不是实际的1,而是一个偏移量,实际是4
  - **`release`**
    - **`SideTable &table = SideTables()[this]`** //通过当前对象的指针,通过hash函数计算在SideTables找到对应的sizeTable
    - **`RefcountMap::iterator it = table.fefcnts.find(this)`**
    - **`refcntStorage -= SIDE_TABLE_RC_ONE`**
  - **`retainCount`**
    - **`SideTable &table = SideTables()[this]`**
    - **`sizt_t refcnt_result = 1`**
    - **`RefcountMap::iterator it = table.fefcnts.find(this)`**
    - **`refcnt_result += it->secont >> SIDE_TABLE_RC_SHIFT`**
  - **`dealloc`**

    ![dealloc.png](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/dealloc.png)
- ARC
  - `ARC`编译器在对应的位置为我们插入`retain`,`release`操作;
  - `ARC`是`LLVM`和`Runtime`协作的结果
  - 禁止手动调用`retain`,`release`,`retainCount`,`dealloc`
  - `weak`,`strong`

#### 弱引用

> `id __weak obj1 = obj;` -- > `objc_initWeak(&obj1,obj)`
> 
![%E6%B7%BB%E5%8A%A0weak%E5%8F%98%E9%87%8F.png](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E6%B7%BB%E5%8A%A0weak%E5%8F%98%E9%87%8F.png)
>  一个被声明为__weak对象指针,会经过如下方法 添加
- `objc_initWeak()`
  - 传入了弱引用变量的地址`&obj1`和被修饰的弱引用变量`obj`
- `storeWeak()`
- `weak_register_no_lock()`

> 问:系统是怎样把一个weak变量添加到他所对应的的弱引用表中的?

> 答:一个被声明为__weak的对象指针,经过编译器编译之后,会调用`objc_initWeak()`经过一系列函数调用栈,最终在`weak_register_no_lock()`中进行弱引用变量添加,添加的位置是通过一个hash算法进行位置查找,如果查找位置有当前对象的所对应的的弱引用数组,那么就将新弱引用变量加到数组里面,如果没有,就创建一个弱引用数组,将第0个设置为weak,其他位置置为nil


> 问:当一个weak释放时,怎么置为nil?

> 答:当一个对象被`dealloc`之后,在`dealloc`内部实现当中会调用`weak_clear_no_lock()`,在函数实现当中会根据当前对象的指针查找所对应的的弱引用表,把当前对象所对应的弱引用拿出来是一个数组,遍历置为nil
#### 自动释放池

- 是以栈为结点通过双向链表的形式组合而成的
- 是和线程一一对应的
> 问: `AutoreleasePool`实现原理

> 在当次runloop将要结束的时候调用`AutoreleasePoolPage::pop()`

> 问: `AutoreleasePool`嵌套使用

> 多次嵌套就是多次插入哨兵对象


> 问: 什么情况下使用

> 在for循环中alloc图片等数据消耗较大的场景手动插入autoreleasepool
> 

- `@autoreleasepool{}` 编译后转换为

  ```
   void *ctx = objc_autoreleasePoolPush();
   { 代码 };
   objc_autoreleasePoolPop(ctx);
  ```
  - `objc_autoreleasePoolPush()`
    - 内部会调用`c++`函数`AutoreleasePoolPage::push(void)`
  - `objc_autoreleasePoolPop(ctx)`
    - 内部会调用`c++`函数`AutoreleasePoolPage::pop(ctx)`
    - 一次pop相当于一次批量的pop操作
- `AutoreleasePoolPage`的数据结构

  ```
  class AutoreleasePoolPage{
    id *next;
    AutoreleasePoolPage *const parent;
    AutoreleasePoolPage *child;
    pthread_t const thread;
  }
  ```
  - `id *next` 用来作为游标指向栈顶添加新的`autoreleasepool`对象的下一个位置
  - `parent`和`child`双向链表
  - `thread` 和线程一一相关
  - 每个AutoreleasePoolPage对象占用4096字节内存，除了用来存放它内部的成员变量，剩下的空间用来存放autorelease对象的地址
  - 当当前的`AutoreleasePoolPage`页再加入一个`autoreleasepool`对象就要满时(next指针马上指向栈顶时),新建立一个下一页的`page`对象,与当前页链表链接完成后,新`page`页的`next`指针会被初始化在栈底,然后继续向栈顶添加对象
  - 每当进行`push`操作,runtime会向当前的`page`add一个哨兵对象nil,objc_autoreleasePoolPush的返回值正是这个哨兵对象的地址，被objc_autoreleasePoolPop(哨兵对象)作为入参:
  - 根据传入的哨兵对象地址找到哨兵对象所处的page
  - 在当前page中，将晚于哨兵对象插入的所有autorelease对象都发送一次- release消息，并向回移动next指针到正确位置

#### 循环引用

- 自循环引用
- 相互循环引用
- 多循环引用

- __weak
- __block
  - MRC下,不会增加引用计数,避免循环引用
  - ARC下,会被强引用,需要手动解环
- __unsafe_unretained
  - 修饰对象不会增加引用计数,避免循环引用
  - 会产生悬垂指针
- NSTimer的循环引用问题




## Objective-C语言特性

#### 分类
###### 分类做了什么事情
- 声明私有方法
- 分解体积庞大的类文件
- Framework私有方法公开化

###### 分类的特点
- 运行时决议 编译的时候宿主类没有分类的方法，运行时runtime才真实的添加到宿主类
- 可以为系统类添加分类 
 
###### 分类中都可以添加
- 实例方法
- 类方法
- 协议
- 属性 分类中定义的属性只生成set get方法 并没有实例变量
 
###### 分类的结构体
  ```
  struct category_t {
    const char *name;
    classref_t cls;
    WrappedPtr<method_list_t, method_list_t::Ptrauth> instanceMethods;
    WrappedPtr<method_list_t, method_list_t::Ptrauth> classMethods;
    // 协议方法
    struct protocol_list_t *protocols;
    // 对象属性
    struct property_list_t *instanceProperties;
    // Fields below this point are not always present on disk.
    // 类方法
    struct property_list_t *_classProperties;

    method_list_t *methodsForMeta(bool isMeta) const {
        if (isMeta) return classMethods;
        else return instanceMethods;
    }

    property_list_t *propertiesForMeta(bool isMeta, struct header_info *hi) const;
    
    protocol_list_t *protocolsForMeta(bool isMeta) const {
        if (isMeta) return nullptr;
        else return protocols;
    }
};
  
  ```
###### 分类的调用栈

![%E5%88%86%E7%B1%BB%E8%B0%83%E7%94%A8%E6%A0%88.png](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%88%86%E7%B1%BB%E8%B0%83%E7%94%A8%E6%A0%88.png)

- `remethodizeClass`
> **将传入的宿主类(假设为`Person`类)判断是否为元类对象(取决于添加的方法是实例方法还是类方法),然后取出宿主类中未完成整合的所有分类(假设有`Person+A`,`Person+B`,`Person+C`等),拼接到宿主类上**
> 
  ```
    static void remethodizeClass (Class cls){
        category_list *cats;
        bool isMeta;
        runtimeLock.assertWriting();
        // 判断当前类是否为元类对象,取决于添加的方法是实例方法还是类方法
        // 以实例方法添加逻辑为例,所以假设isMeta = NO;
        isMeta = cls->isMetaClass();
        // 获取cls中未完成整合的所有分类
        if((cats = unattachedCategoriesForClass(cls, false/*not realizing*/))){
            if(PrintConnecting){

            }
            // 将分类cats拼接到cls上
            attachCategories(cls, cats, true);
            free(cats);
        }
    }
  ```
- `attachCategories`   

> **传入的分类的数组`cats`是按照顺序编译的,假设为`Person+A`和`Person+B`;在这个方法中会根据`cats`数组总数,然后进行倒序遍历,最先访问最后编译的分类,先访问`Person+B`,将其方法列表协议列表等添加到新的二维数组中,当调用方法时,会先查找新的二维数组中的`Person+B`的对应的方法,这也就解释了分类方法覆盖的原因.  接下来会根据传入的宿主类的名字来获取宿主类的`rw`数据,此时将刚才的包含分类的二维数组拼接到宿主类中**
  ```
    static void attachCategories (Class cls, category_list *cats, bool flush_caches){
        // 非空判断
        if(!cats) return;
        // 打印相关 可忽略
        if(PrintReplacedMethods) printReplacements(cls, cats);
        // 以实例方法添加逻辑为例,所以假设isMeta = NO;
        bool isMeta = cls->isMetaClass();
        /*
         二维数组
         [[method_t,method_t],[method_t],[method_t,method_t,method_t],...]
         */
        method_list_t **mlists = (method_list_t*)malloc(cats->count *sizeof(*mlists));
        property_list_t **proplists = (property_list_t*)malloc(cats->count *sizeof(*proplists));
        protocol_list_t **protolists = (protocol_list_t*)malloc(cats->count *sizeof(*protolists));
        int mcount = 0;
        int propcount = 0;
        int protocount = 0;
        int i = cats->count; //宿主类分类的总数
        bool fromBundle = NO;
        while(i--){ // 倒叙遍历,最先访问最后编译的分类
            // 获取一个分类
            auto& entry = cats-list[i];
            // 获取该分类的方法列表
            method_list_t *mlist = entry.cat->methodsForMeta(isMeta);
            if(mlist){
                // 最后编译的分类最先添加的分类数组里面
                mlists[mcount++] = mlist;
                fromBoundle |= entry.hi->isBoundle();
            }
            // 属性列表同方法列表规则一样
            property_list_t *proplist = entry.cat->methodsForMeta(isMeta);
            if(proplist){
                proplists[propcount++] = proplist;
            }
            // 协议列表同方法列表规则一样
            protocol_list_t *protolist = entry.cat->protocols;
            if(protolist){
                protolists[propcount++] = protolist;
            }
        }
        // 获取当前宿主类当中的rw数据,其中包含宿主类的方法列表信息
        auto rw = cls->data();
        // 主要针对 分类中关于内存管理相关方法下 一些特殊处理 (自己实现set方法)
        prepareMethodLists(cls, mlists, mcount, NO, fromBundle)
        /*
         rw 代表类
         methods 代表类的方法列表
         attachLists 将含有mcount个元素的mlist拼接到rw的methods上
         */
        rw->methods.attachLists(mlists,mcount);
        free(mlists);
        if(flush_caches && mcount > 0) flushCaches(cls);
        rw->properties.attachLists(proplists,propcount);
        free(proplists);
        rw->protocols.attachLists(protolists,protocount);
        free(protolists);
    }
  ```
- `attachLists`  

> **根据传入的包含分类的二维数组个数(假设是A,B,C)和原来的个数(假设是X,Y),重新分配(增大)内存(5),然后将原来的元素进行内存移动,将原来的移动到尾部,将传入的二维数组拷贝到对应的位置,结果由原来的`[X,Y]`变为`[A,B,C,X,Y]`, 这就是分类会"覆盖"宿主类方法的原因**
  ```
  void attachLists (list *const *addedLists, unit32_t addedCount){
    if (addedCount == 0) return;
    if (hasArray()) {
        // 列表中原有元素总数  oldCount = 2
        unit32_t oldCount = array()->count;
        // 拼接之后的元素总数
        unit32_t newCount = oldCount + addedCount;
        // 根据新总数重新分配内存
        setArray((array_t *)realloc(array(),array_t::byteSize(newCount)));
        // 重新设置元素总数
        array()->count = newCount;
        /*
         内存移动
         [[],[],[],[原来的第一个元素],[原来的第二个元素]]
         */
        memmove(array()->lists + addedCount, array()->lists, oldCount * sizeof(array()->lists[0]));
        /*
         内存拷贝
         [
            A ----> [addedLists中的第一个元素],
            B ----> [addedLists中的第二个元素],
            C ----> [addedLists中的第三个元素],
            [原来的第一个元素],
            [原来的第二个元素]
         ]
         这就是分类会"覆盖"宿主类方法的原因
         宿主类的方法还存在m,由于消息发送机制,根据selecter选择器根据名字查找,一旦找到,就返回imp,分类位于数组前面,所以会覆盖
        */
        memcpy(array()->lists, addedLists, addedCount * sizeof(array()->lists[0]));
    }
  }
  ```
  
###### 结论
- 分类添加的方法会"覆盖"原类方法
- 同名分类方法谁能生效取决于编译顺序
- 名字相同的分类会引起编译报错 

#### 关联对象

###### 给分类添加`成员变量`

- 获取关联对象
  - **`id objc_getAssociatedObject(id object, const void *key)`**
- 设置关联对象 
  - **`void objc_setAssociatedObject(id object, const void *key,id value,objc_AssociationPolicy policy)`**
- 删除关联对象
  - **`void objc_removeAssociatedObjects(id object)`**

###### 位置
- 成员变量添加的位置并未添加到原宿主数组
- 关联对象由`AssociationsManager`管理在`AssociationHashMap`中
- 所有对象的关联内容都在一个相同的全局容器中
![%E5%85%B3%E8%81%94%E5%AF%B9%E8%B1%A1.png](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%85%B3%E8%81%94%E5%AF%B9%E8%B1%A1.png)

###### 源码分析

> 以设置关联对象方法为例 
> - 获取`AssociationsManager`管理的全局容器`AssociationHashMap`
> - 将传入的`value`和`policy`处理为`new_value`
> - 根据传入的要被关联的对象`object`,对其指针地址按位取反;作为全局容器`AssociationHashMap`中的某一对象的`object_key`
> - 根据这个`object_key`查找对应的`ObjectAssociationMap`结构的`map`,
>   - 找的到`map`,根据传入的`key`获取`ObjectAssociationMap`中的`ObjectAssociation`对象
>     - 如果有`ObjectAssociation`对象,将`new_value`覆盖值
>     - 如果没有`ObjectAssociation`对象,将传入的`value`和`policy`封装成一个`ObjectAssociation`对象,封住的对象作为新创建的`ObjectAssociationMap`对应`key(传入的)`的`value`
>   - 找不到`map`,创建一个`ObjectAssociationMap`,作为全局容器`AssociationHashMap`对应这个`object_key`的`ObjectAssociationMap_value`,然后将传入的`value`和`policy`封装成一个`ObjectAssociation`对象,封住的对象作为新创建的`ObjectAssociationMap`对应`key(传入的)`的`value`
> 
```
/// 关联对象的最终方法,参数是透传过来的
/// @param object 要被关联的对象 比如要给Person的分类Person+A关联,那么object就是Person+A
/// @param key  要关联的值的对应的key
/// @param value 要给Person+A关联的值
/// @param policy 内存管理策略 copy retain等
void _objc_set_associative_reference(id object, void *key, id value, uintptr_t policy){
    ObjcAssociation old_association(0, nil);
    // 根据策略值来对value进行加工
    id new_value = value ? acquireValue(value, policy) : nil;
    // 关联对象管理类 C++实现的一个类 主要管理的是AssociationHashMap
    AssociationsManager manager;
    // 获取manager维护的一个HashMap,是一个全局的容器
    AssociationHashMap &associations(manager.associations());
    // 对object对象指针地址按位取反来作为全局容器中的某一对象的唯一标识
    disguised_ptr_t disguised_object = DISGUISE(object);
    if (new_value) {
        // 根据对象的指针查找一个对应的ObjectAssociationMap结构的map
        AssociationHashMap::iterator i = associations.find(disguised_object)
        // 关联过
        if (i != associations.end()) {
            ObjectAssociationMap *refs = i->second;
            ObjectAssociationMap::iterator j = refs->find(key);
            if (j != refs->end()) {
                // 如果有值就替换
                old_association = j->second;
                j->seceond = ObjectAssociation(policy ,new_value);
            }else{
                // 没值就设置
                (*refs)[key] = ObjectAssociation(policy ,new_value);
            }
        }else{
            // 没找到 需要创建一个新的
            ObjectAssociationMap *refs = new ObjectAssociationMap;
            associations[disguised_object] = refs;
            (*refs)[key] = ObjectAssociation(policy ,new_value);
            // 设置有了关联对象的标识
            object->setHasAssociatedObjects();
        }
    }else{
        AssociationHashMap::iterator i = associations.find(disguised_object);
        if (i != associations.end()) {
            ObjectAssociationMap *refs = i->second;
            ObjectAssociationMap::iterator j = refs->find(key);
            if (j != refs->end()) {
                old_association = j->second;
                refs->erase(j);
            }
        }
    }
}
```
###### 生成的数据结构
```
// 全局容器
{    //A分类添加的实例变量
    "0x4927298472":{                ----key:被关联的对象A        value:ObjectAssociationMap
        "@selector(text)":{         ----key:被关联对象传入的key   value:ObjectAssociation   @selector(text)---->@property (retain) NSString *text;
            "value":"hellow",
            "policy":"retain"
        },
        "@selector(title)":{      @selector(title)---->@property (copy) NSString *title;
            "value":"a object",
            "policy":"copy"
        }
    },
    //B分类添加的实例变量
    "0x3428154292": {
        "@selector(backgroundColor)": {
            "value":"oxff55ff",
            "policy":"retain"
        }
    }
    
}
```
#### 扩展
###### 扩展用法
- 声明私有属性
- 声明私有方法
- 声明私有成员变量
###### 分类扩展区别
- 扩展特点:
  - 编译时决议,分类是运行时决议
  - 只有声明,没有实现,多数情况下寄生于宿主的.m中
  - 不能为系统类添加扩展

#### 代理
###### 含义
- 是一种软件设计模式,代理模式
- iOS当中以@protocol形式实现
- 传递方式一对一

###### 遇到的问题
- 一般声明为weak以规避循环引用

#### 通知
###### 含义
- 使用观察者模式来实现的用于跨层传递消息的机制
- 传递方式为一对多

###### 实现机制
- 创建一个类`NSNotificationCenter`,维护一个表`Notification_Map`,`key`为`notificationName`,`value`为`Observers_List`
- `Observers_List`里面应该有`Observer`及 接受 发送通知的相关方法
#### KVO
###### 什么是KVO
- KVO是Objective-C对观察者模式的又一实现
- 使用了isa混写(isa-swizzling)技术实现KVO
- KVC设置value能生效
- 通过成员变量直接赋值不生效,手动添加KVO才会生效

#### KVC
- Key-value coding缩写
- 破坏了面向对象的编程思想

#### 属性关键字

- 读写性
- 原子性
- 内存管理


## Runtime

#### Runtime数据结构

![avatar](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/runtime%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84.png)
###### **objc_object**

- `id` 类型
- `isa_t` 共用体
  - 指针型`isa` : `isa`64位的值代表`Class`地址
  - 非指针型`isa`:  `isa`64位的部分值代表`Class`地址
- 关于`isa`操作相关方法
  - 对象指向类对象: 实例------>Class
  - 类对象指向元类对象: Class------>MetaClass
- 弱引用相关
- 关联对象相关
- 内存管理

###### **objc_class**

- `Class`类型,继承于`objc_object`
- `Class` `superClass`
- `cache_t` `cache` 方法缓存
  - 特点:
    - 用于**快速**查找方法执行函数
    - 可**增量扩展**的**哈希表**结构
    - 是**局部性原理**的最佳应用
  - 结构
    - `bucket_t`
      - `key`---->`selector`
      - `IMP`---->无类型的函数指针
- `class_data_bits_t` `bits`
    - `class_data_bits_t`是对 `class_rw_t`的封装
    - `class_rw_t`代表了类相关的读写信息,是对`class_ro_t`的封装
      - `class_ro_t`
      - `protocols` 二维数组
      - `properties` 二维数组
      - `methods` 二维数组
    - `class_ro_t`类的只读信息
      - `name` 类名 `NSClassFromString(aClassName)`
      - `ivars` 成员变量 --- 一维数组
      - `properties` 属性 --- 一维数组
      - `protocols` 遵循的协议 --- 一维数组
      - `methodList` 方法 --- 一维数组

- `method_t` 
  - `SEL name` 函数名称
  - `const char *types`  函数返回值和参数
  - `IMP imp`  函数体

- `Type Encodings`
  - `const char *types`  返回值+参数1+参数2+....
  - `-(void)aMethod`-->`v@:`-->`void`+`id`+`SEL`

#### **对象一类对象一元类对象**
![avatar](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%AF%B9%E8%B1%A1.png)

#### **消息传递**

- `void objc_msgSend(id self, Sel op, ...)`
- `void objc_msgSendSuper(struct objc_super *super, Sel op, ...)`

![消息传递](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E6%B6%88%E6%81%AF%E4%BC%A0%E9%80%92%E6%B5%81%E7%A8%8B.png)

###### **缓存查找**

> 可以理解为: 给定值是SEL,目标值是对应的`bucket_t`中的`IMP`
- 使用的是哈希查找
- 根据给定的`SEL`通过一个函数来映射出对应的`bucket_t`在数组当中的位置
- `f(key)`就是`SEL`跟`mask`做`&`操作,而`mask`也是`cache_t`的一个成员变量
![缓存查找](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E7%BC%93%E5%AD%98%E6%9F%A5%E6%89%BE.png)

###### **当前类中查找**

- 对于`已排序好的`列表,采用`二分查找法`查找方法相应的执行函数
- 对于`未排序的`列表,采用`一般遍历法`查找方法相应的执行函数

###### **父类中查找**

- 如图

![父类查找](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E7%88%B6%E7%B1%BB%E6%9F%A5%E6%89%BE.png)

#### **消息转发**


![消息转发](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E6%B6%88%E6%81%AF%E8%BD%AC%E5%8F%91%E6%B5%81%E7%A8%8B.png)
- `+ (BOOL)resolveInstanceMethod:(SEL)sel`
  - 告诉系统要不要解决当前传入的方法的实现
- `- (id)forwardingTargetForSelector:(SEL)aSelector`
  - 告诉系统这次的方法调用应该由哪个对象来处理
- `- (NSMethodSignature *)methodSignatureForSelector:(SEL)aSelector`和`forwardInvocation`
  - 是否返回方法签名,进而处理

#### **Method-Swizzling**

![交换方法](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E6%96%B9%E6%B3%95%E4%BA%A4%E6%8D%A2.png)
#### **动态添加方法**

- 添加时机是在`resolveInstanceMethod`方法中添加
- 添加方法是 `class_addMethod(Class cls, SEL name, IMP imp,
    const char *types)`
- `performSelector: `

#### **动态方法解析**

- `@dynamic`
  - 动态运行时语言将函数决议推迟到运行时
  - 编译时语言在编译器进行函数决议


## Block

#### Block介绍
- Block是将`函数`及其`执行上下文`封装起来的`对象`

怎么样来理解这段话呢,我们通过源码来进行分析

- 创建一个`MCBlock`文件,在其`.m`中写如下代码

  ```
  - (void) method {
      int multiplier = 6;
      int(^Block)(int) = ^int(int num){
          return num *multiplier;
      };
      Block(2);
  }
  ```
- `clang -rewrite-objc MCBlock.m` 通过clang编译器编辑生成`MCBlock.cpp`文件

  ```
   // _I_MCBlock_method I代表是当前类`MCBlock`类的实例方法
   static void _I_MCBlock_method(MCBlock * self, SEL _cmd) {
      int multiplier = 6;
      int(*Block)(int) = ((int (*)      (int))&__MCBlock__method_block_impl_0((void *)__MCBlock__method_block_func_0, &__MCBlock__method_block_desc_0_DATA, multiplier));
      ((int (*)(__block_impl *, int))((__block_impl *)Block)->FuncPtr)((__block_impl *)Block, 2);
  }
    ``` 

- `__MCBlock__method_block_impl_0`

  ```
  struct __MCBlock__method_block_impl_0 {
    struct __block_impl impl;
    struct __MCBlock__method_block_desc_0* Desc;
    int multiplier;
    __MCBlock__method_block_impl_0(void *fp, struct __MCBlock__method_block_desc_0 *desc, int _multiplier, int flags=0) : multiplier(_multiplier) {
      impl.isa = &_NSConcreteStackBlock;
      impl.Flags = flags;
      impl.FuncPtr = fp;
      Desc = desc;
    }
  };
  ```
- `_block_impl`

    ```
    struct __block_impl {
      void *isa;
      int Flags;
      int Reserved;
      void *FuncPtr;
    };
    
    ``` 

- `__MCBlock__method_block_func_0`

    ```
    static int __MCBlock__method_block_func_0(struct __MCBlock__method_block_impl_0 *__cself, int num) {
      int multiplier = __cself->multiplier; // bound by copy
      return num *multiplier;
    }
    ```
    
##### Block判空操作
> `Block`执行时需判空,否则`Crash`
> 
- 定义一个`Block`时,底层会将其转为`_block_impl`的结构体指针,而其成员结构上面我们也可以看到;当`block()`调用时,底层为函数的地址调用`block->FuncPtr`,去访问`FuncPtr`地址,而由于这个地址是无效的,所以会抛出异常

> 异常的`EXC_BADACCESS`,地址`address`是多少呢?
> 
- `EXC_BADACCESS(code=1,address=0x10)`,是因为这个`_block_impl`数据结构为:
  - 占8个字节的`isa`指针
  - 占4个字节的`Flags`int
  - 占4个字节的`Reserved`int

偏移量刚好为16所对应的`block`调用`FuncPtr`

#### 截获变量
- 局部变量(基本数据类型) 
  - 截获其值
  
  ```
  - (void) method {
      int multiplier = 6;
      int(^Block)(int) = ^int(int num){
          return num *multiplier;
      };
      multiplier = 4;
      Block(2);
  }
  // 12
  ```
- 局部变量(对象类型)    
  - 连同其所有权修饰符一起截获
- 静态局部变量
  - 指针形式

  ```
  - (void) method {
      static int multiplier = 6;
      int(^Block)(int) = ^int(int num){
          return num *multiplier;
      };
      multiplier = 4;
      Block(2);
  }
  // 8
  ```
- 全局变量
  - 不截获
- 静态全局变量
  - 不截获

**源码分析**
```
// 全局变量
int global_var = 4;
// 静态全局变量
static int static_global_var = 5;

- (void)method{
    // 基本数据类型局部变量
    int var = 1;
    // 对象类型局部变量
    __unsafe_unretained id unsafe_obj = nil;
    __strong id strong_obj = nil;
    // 局部静态变量
    static int static_var = 3;
    
    void(^Block)(void) = ^{
        NSLog(@"局部变量<基本数据类型> var %d",var);
        NSLog(@"局部变量<__unsafe_unretained 对象类型> var %@",unsafe_obj);
        NSLog(@"局部变量<__strong 对象类型> var %@",strong_obj);
        NSLog(@"局部 静态变量 %d",static_var);
        NSLog(@"全局变量 %d",global_var);
        NSLog(@"静态全局变量 %d",static_global_var);
    };
    Block();
}
```
**clang**后
```
int global_var = 4;

static int static_global_var = 5;

struct __MCBlock__method_block_impl_0 {
  struct __block_impl impl;
  struct __MCBlock__method_block_desc_0* Desc;
  // 截获局部变量的值
  int var;
  // 连同所有权修饰符一起截获
  __unsafe_unretained id unsafe_obj;
  __strong id strong_obj;
  // 以指针的形式截获局部变量
  int *static_var;
  // 全局变量,全局静态变量不截获
  __MCBlock__method_block_impl_0(void *fp, struct __MCBlock__method_block_desc_0 *desc, int _var, __unsafe_unretained id _unsafe_obj, __strong id _strong_obj, int *_static_var, int flags=0) : var(_var), unsafe_obj(_unsafe_obj), strong_obj(_strong_obj), static_var(_static_var) {
    impl.isa = &_NSConcreteStackBlock;
    impl.Flags = flags;
    impl.FuncPtr = fp;
    Desc = desc;
  }
};
```
#### __block修饰符

###### 使用场景 
- 一般情况下,对被截获的变量进行`赋值`操作的时候需要加`__block`修饰符

  ```
  __block NSMutableArray *array = nil;
  void(^Block)(void) = ^{
    array = [NSMutableArray array]; // 赋值
  } ;
  Block();
  ```
- 使用情况下不需要

  ```
  NSMutableArray *array = [NSMutableArray array];
  void(^Block)(void) = ^{
    [array addObject:@123]; // 使用 
  } ;
  Block();
  ```
  
###### 做了什么

- 使用`__block`修饰符的变量变成了对象
  ```
  - (void) method {
      __block int multiplier = 6;
      int(^Block)(int) = ^int(int num){
          return num *multiplier;
      };
      multiplier = 4;
      Block(2);
  }
  // 8
  ```
  **`__block int multiplier` 变为了下面的结构体**
  ```
   Struct _Block_byref_multiplier_0{
      void *_isa;
      _Block_byref_multiplier_0 *_forwarding;
      int _flags;
      int size;
      int multiplier;
   }
  ```  
  **`multiplier = 4;`则转为如下代码**
  
  ```
  (multiplier.__forwarding ->multiplier) = 4;
  ```
  这一步操作,`multiplier`已经变成了对象,通过`multiplier`对象中同类型的`__forwarding`找到对象(由于这是栈上的block,此时__forwarding指针指向的是自己),进行赋值操作
  

#### Block内存管理
###### 种类
- **栈** `_NSConcreteStackBlock`
- **堆** `_NSConcreteMallocBlock`
- **全局** `_NSConcreteGlobalBlock`
###### `copy`操作
- **栈** 堆上生成block
- **堆** 增加引用计数
- **全局** 什么都不做

###### `__forwarding`指针作用

一个在栈上,被`__block`修饰的变量,经过`copy`操作,`__forwarding`指向了堆上的`__block`变量,而堆上的`__block`变量中的`__forwarding`指向自己

```
{
    __block int multiplier = 10;
    _blk = ^int(int num){
        return num * multiplier;
    };
    multiplier = 6;
    [self executeBlock];
}
```
```
  - (void)executeBlock{
      int result = _blk(4);
      NSLog(@"%d",result);
  }
  
  // 24;
```
- 栈上创建了局部变量`multiplier`,并且用`__block`修饰,此时`multiplier`变成了一个对象
- `_blk`变量作为当前对象的一个成员变量,当对其进行赋值操作的时候,会对其进行`copy`操作,此时堆上会生成一个`_blk`副本
- `multiplier = 6;`不是对`multiplier`变量进行赋值,而是通过`multiplier`对象`__forwarding`指针对其成员变量`multiplier`进行赋值
- 当第一段代码执行完后: 如果`_blk`没有进行`copy`操作,`multiplier = 6;`修改的就是栈上对应的`__block`修饰的变量
- 如果`_blk`进行`copy`操作,`multiplier = 6;`通过栈上的`multiplier`的`__farwarding`指针找到堆上的`__block`变量对应的副本进行修改
- 第二段代码调用堆上的`_blk`,入参是4,所以是24


#### Block循环引用

- 自循环

  ```
   {
      _array = [NSMutableArray arrayWithObjects:@"block", nil];
      _strBlk = ^NSString *(NSString *num){
          return [NSString stringWithFormat:@"hello %@",_array[0]];
      };
      _strBlk(@"hello");
  }
  ```
  - `_strBlk`作为当前对象的一个成员变量,一般copy修饰,所以`self`持有`_strBlk`
  - `_strBlk`表达式中使用了`_array`,由于`Block`截获变量时将其权限修饰符的特性,所以`_strBlk`中有一个`__strong`指针的`self`;
  - `__weak`解决: `__weak NSArray *weakArray = _array`
- 大环循环

  ```
  {
    __block MCBlock *blockSelf = self;
    _blk = ^int(int num){
        return num *blockSelf.var;
    };
    _blk(3);
  }
  ```
  - `MRC`下不会产生循环引用
  - `ARC`下会产生循环引用,引起内存泄露
    - 对象持有`_blk`
    - `blk`持有`__block`变量
    - `__block`变量持有原对象(__farwarding指针指向自己)
    - 解决办法如下,但是有一个弊端,就是如果不执行这段代码的话,闭环永远存在
    ```
    {
      __block MCBlock *blockSelf = self;
      _blk = ^int(int num){
          int result = num *blockSelf.var;
          blockSelf = nil;
          return result;
      };
      _blk(3);
    }
    ```

## 多线程

#### 进程和线程

###### 进程
- 进程是一个具有一定独立功能的程序关于某次数据集合的一次运行活动，它是操作系统分配资源的基本单元。
- 进程是指在系统中正在运行的一个应用程序，就是一段程序的执行过程，我们可以理解为手机上的一个app。
- 每个进程之间是独立的，每个进程均运行在其专用且受保护的内存空间内，拥有独立运行所需的全部资源。

###### 线程
- 程序执行流的最小单元，线程是进程中的一个实体。
- 一个进程要想执行任务，必须至少有一条线程。应用程序启动的时候，系统会默认开启一条线程，也就是主线程。

###### 关系
- 线程是进程的执行单元，进程的所有任务都在线程中执行。
- 线程是CPU分配资源和调度的最小单位。
- 一个程序可以对应多个进程(多进程)，一个进程中可有多个线程，但至少要有一条线程。
- 同一个进程内的线程共享进程资源。


###### 坑
> 一个进程中可以开启另一个进程吗？
> 

- WKWebView

#### 任务和队列
###### 任务
> 就是执行操作的意思，也就是在线程中执行的那段代码；在GCD中是放在block中的；执行任务有两种方式：同步执行（sync）和异步执行（async）

- **同步(Sync)：** 同步添加任务到指定的队列中，在添加的任务执行结束之前，会一直等待，直到队列里面的任务完成之后再继续执行，即会阻塞线程。只能在当前线程中执行任务(是当前线程，不一定是主线程)，不具备开启新线程的能力。
- **异步(Async)：** 线程会立即返回，无需等待就会继续执行下面的任务，不阻塞当前线程。可以在新的线程中执行任务，具备开启新线程的能力(并不一定开启新线程)。如果不是添加到主队列上，异步会在子线程中执行任务

###### 队列
> 队列（DispatchQueue）：这里的队列指执行任务的等待队列，即用来存放任务的队列。队列是一种特殊的线性表，采用FIFO（先进先出）的原则，即新任务总是被插入到队列的末尾，而读取任务的时候总是从队列的头部开始读取。每读取一个任务，则从队列中释放一个任务。

- **串行队列（SerialDispatchQueue）：** 同一时间内，队列中只能执行一个任务，只有当前的任务执行完成之后，才能执行下一个任务。（只开启一个线程，一个任务执行完毕后，再执行下一个任务）。主队列是主线程上的一个串行队列，是系统自动为我们创建的。
- **并发队列（ConcurrentDispatchQueue）：** 同时允许多个任务并发执行（可以开启多个线程，并且同时执行任务）。并发队列的并发功能只有在异步（dispatch_async）函数下才有效。
###### 组合
- 组合1 同步分派任务到串行队列
  > `dispatch_sync(serial_queue,^{//任务})`
  > 
    ```
    // 头条面试题  死锁
    - (void)viewDidLoad{
        dispatch_sync(dispatch_get_main_queue(),^{
        [self doSomething];
        }); 
    }
    // 原因:队列引起的循环等待
    ```
     ```
    // 改为异步
    - (void)viewDidLoad{
        dispatch_async(dispatch_get_main_queue(),^{
        [self doSomething];
        }); 
    }
    // 正常运行
    // 说明:主队列不管是以同步方式添加任务还是异步方式添加任务,都是在主线程来执行
    ```
    ```
    // 改为自定义串行队列
    - (void)viewDidLoad{
        dispatch_sync(serialQueue,^{
        [self doSomething];
        }); 
    }
    // 正常运行
    ```
    ```
    /// 在主线程中执行这句代码
    dispatch_sync(dispatch_get_main_queue(), ^{
        NSLog(@"这里死锁了");
    });


    /// 在哪里执行都可以
    dispatch_queue_t theSerialQueue = dispatch_queue_create("我是个串行队列", DISPATCH_QUEUE_SERIAL);
    dispatch_async(theSerialQueue, ^{ /// 正在执行任务，同步异步无所谓
        NSLog(@"第一层");

        /// 同一个串行队列
        dispatch_sync(theSerialQueue, ^{
            NSLog(@"第二层");

        });
    });
    ```
- 组合2 异步分派任务到串行队列
  > `dispatch_async(serial_queue,^{//任务})`

    ```
    - (void)viewDidLoad{
        dispatch_async(dispatch_get_main_queue(),^{
          [self doSomething];// 刷新UI
        }); 
    }
    ```
- 组合3 同步分派任务到并发队列
  > `dispatch_sync(concurrent_queue,^{//任务})`
  
    ```
    // 美团面试
    - (void)viewDidLoad{
        NSLog(@"1");
        dispatch_sync(global_queue,^{
          NSLog(@"2");
            dispatch_sync(global_queue,^{
              NSLog(@"3");
          }); 
          NSLog(@"4");
        }); 
        NSLog(@"5");
    }
    // 12345
    ```
- 组合4 异步分派任务到并发队列
  > `dispatch_async(concurrent_queue,^{//任务})`

    ```
    // 腾讯
     - (void)viewDidLoad{
        dispatch_async(global_queue,^{
          NSLog(@"1");
          [self performSelector:@selector(printLog) withObject:nil afterDelay:0]; 
          NSLog(@"3");
        }); 
    }
    -(void)printLog{NSLog(@"2");}
    // 13
    // 异步方式分派到global_queue队列,子线程执行没有开启runloop
    ```
    
#### GCD

###### dispatch_once
> 我们在创建单例、或者有整个程序运行过程中只执行一次的代码时，我们就用到了 GCD 的 dispatch_once 方法。使用 dispatch_once 方法能保证某段代码在程序运行过程中只被执行 1 次，并且即使在多线程的环境下，dispatch_once 也可以保证线程安全。
> 
```
/**
 * 一次性代码（只执行一次）dispatch_once
 */
- (void)once {
    static dispatch_once_t onceToken;
    dispatch_once(&onceToken, ^{
        // 只执行 1 次的代码（这里面默认是线程安全的）
    });
}

```

###### dispatch_barrier_async() 
> 用来实现多读单写

```
- (id)readDataForKey:(NSString *)key{
    __block id result;
    dispatch_sync(_concurrentQueue, ^{
        result = [self valueForKey:key];
    });
    return result;;
}

- (void)writeData:(id)data forKey:(NSString *)key{
    dispatch_barrier_async(_concurrentQueue, ^{
        [self setValue:data forKey:key];
    });
}
```

###### dispatch_semaphore
> GCD 中的信号量是指 Dispatch Semaphore，是持有计数的信号。
- dispatch_semaphore_create：创建一个 Semaphore 并初始化信号的总量
  ```
  struct semaphore{
    int value;
    List<thread>;
  }
  ```
- dispatch_semaphore_signal：发送一个信号，让信号总量加 1
  ```
  {
    S.value = S.value + 1;
    if S.value <= 0 then wakeup(S.list);唤醒是一个被动行为
  }
  ``` 
- dispatch_semaphore_wait：可以使总信号量减 1，信号总量小于 0 时就会一直等待（阻塞所在线程），否则就可以正常执行。
  ```
  {
    S.value = S.value - 1;
    if S.value < 0 then Block(S.list);阻塞是一个主动行为
  }
  ``` 
**应用**
- 保证线程同步，异步执行任务转换为同步执行任务
  - AFN
  ```
  - (NSArray *)tasksForKeyPath:(NSString *)keyPath {
    __block NSArray *tasks = nil;
    dispatch_semaphore_t semaphore = dispatch_semaphore_create(0);
    [self.session getTasksWithCompletionHandler:^(NSArray *dataTasks, NSArray *uploadTasks, NSArray *downloadTasks) {
        if ([keyPath isEqualToString:NSStringFromSelector(@selector(dataTasks))]) {
            tasks = dataTasks;
        } else if ([keyPath isEqualToString:NSStringFromSelector(@selector(uploadTasks))]) {
            tasks = uploadTasks;
        } else if ([keyPath isEqualToString:NSStringFromSelector(@selector(downloadTasks))]) {
            tasks = downloadTasks;
        } else if ([keyPath isEqualToString:NSStringFromSelector(@selector(tasks))]) {
            tasks = [@[dataTasks, uploadTasks, downloadTasks] valueForKeyPath:@"@unionOfArrays.self"];
        }

        dispatch_semaphore_signal(semaphore);
    }];

    dispatch_semaphore_wait(semaphore, DISPATCH_TIME_FOREVER);

    return tasks;
  }
  ```
  - 举例
  ```
  // semaphore 线程同步
  - (void)semaphoreSync {

      NSLog(@"currentThread---%@",[NSThread currentThread]);  // 打印当前线程
      NSLog(@"semaphore---begin");

      dispatch_queue_t queue = dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0);
      dispatch_semaphore_t semaphore = dispatch_semaphore_create(0);

      __block int number = 0;
      dispatch_async(queue, ^{
          // 追加任务 1
          [NSThread sleepForTimeInterval:2];              // 模拟耗时操作
          NSLog(@"1---%@",[NSThread currentThread]);      // 打印当前线程

          number = 100;

          dispatch_semaphore_signal(semaphore);
      });

      dispatch_semaphore_wait(semaphore, DISPATCH_TIME_FOREVER);
      NSLog(@"semaphore---end,number = %zd",number);
  }
  
    // 打印
    <NSThread: >{number = 1, name = main}
    semaphore---begin
    1---<NSThread: >{number = 7, name = (null)}
    semaphore---end
    number = 100
  ```
- 保证线程安全,为线程加锁


###### dispatch_group_t
> 异步执行若干耗时任务后再执行其他任务
> 

- **说明:**
  - 调用队列组的 dispatch_group_async 先把任务放到队列中，然后将队列放入队列组中。或者使用队列组的 dispatch_group_enter、dispatch_group_leave 组合来实现 dispatch_group_async。
  - 调用队列组的 dispatch_group_notify 回到指定线程执行任务。或者使用 dispatch_group_wait 回到当前线程继续向下执行（会阻塞当前线程）。

- **举例:**
  - **dispatch_group_notify**
  ```
  // 队列组 dispatch_group_notify
  - (void)groupNotify {
      NSLog(@"currentThread---%@",[NSThread currentThread]);  // 打印当前线程
      NSLog(@"group---begin");

      dispatch_group_t group =  dispatch_group_create();

      dispatch_group_async(group, dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{
          // 追加任务 1
          [NSThread sleepForTimeInterval:2];              // 模拟耗时操作
          NSLog(@"1---%@",[NSThread currentThread]);      // 打印当前线程
      });

      dispatch_group_async(group, dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{
          // 追加任务 2
          [NSThread sleepForTimeInterval:2];              // 模拟耗时操作
          NSLog(@"2---%@",[NSThread currentThread]);      // 打印当前线程
      });

      dispatch_group_notify(group, dispatch_get_main_queue(), ^{
          // 等前面的异步任务 1、任务 2 都执行完毕后，回到主线程执行下边任务
          [NSThread sleepForTimeInterval:2];              // 模拟耗时操作
          NSLog(@"3---%@",[NSThread currentThread]);      // 打印当前线程

          NSLog(@"group---end");
      });
  }
  // 打印:  
    <NSThread:>{number = 1, name = main}
    group---begin
    2---<NSThread>{number = 4, name = (null)}
    1---<NSThread:>{number = 5, name = (null)}
    3---<NSThread:>{number = 1, name = main}
    group---end

  ```
  - **dispatch_group_wait**
  ```
  - (void)groupWait {
    NSLog(@"currentThread---%@",[NSThread currentThread]);  // 打印当前线程
    NSLog(@"group---begin");
    
    dispatch_group_t group =  dispatch_group_create();
    
    dispatch_group_async(group, dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{
        // 追加任务 1
        [NSThread sleepForTimeInterval:2];              // 模拟耗时操作
        NSLog(@"1---%@",[NSThread currentThread]);      // 打印当前线程
    });
    
    dispatch_group_async(group, dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{
        // 追加任务 2
        [NSThread sleepForTimeInterval:2];              // 模拟耗时操作
        NSLog(@"2---%@",[NSThread currentThread]);      // 打印当前线程
    });
    
    // 等待上面的任务全部完成后，会往下继续执行（会阻塞当前线程）
    dispatch_group_wait(group, DISPATCH_TIME_FOREVER);
  }    
    // 打印
    NSLog(@"group---end");
    <NSThread: >{number = 1, name = main}
    group---begin
    1---<NSThread: >{number = 5, name = (null)}
    2---<NSThread: >{number = 4, name = (null)}
    group---end
  ```
  - **dispatch_group_enter**,**dispatch_group_leave**
  ```
  - (void)groupEnterAndLeave {
    NSLog(@"currentThread---%@",[NSThread currentThread]);  // 打印当前线程
    NSLog(@"group---begin");
    
    dispatch_group_t group = dispatch_group_create();
    dispatch_queue_t queue = dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0);
    dispatch_group_enter(group);
    dispatch_async(queue, ^{
        // 追加任务 1
        [NSThread sleepForTimeInterval:2];              // 模拟耗时操作
        NSLog(@"1---%@",[NSThread currentThread]);      // 打印当前线程

        dispatch_group_leave(group);
    });
    
    dispatch_group_enter(group);
    dispatch_async(queue, ^{
        // 追加任务 2
        [NSThread sleepForTimeInterval:2];              // 模拟耗时操作
        NSLog(@"2---%@",[NSThread currentThread]);      // 打印当前线程
        
        dispatch_group_leave(group);
    });
    
    dispatch_group_notify(group, dispatch_get_main_queue(), ^{
        // 等前面的异步操作都执行完毕后，回到主线程.
        [NSThread sleepForTimeInterval:2];              // 模拟耗时操作
        NSLog(@"3---%@",[NSThread currentThread]);      // 打印当前线程
    
        NSLog(@"group---end");
    });
  }
  
    // 打印:  
    <NSThread:>{number = 1, name = main}
    group---begin
    2---<NSThread>{number = 4, name = (null)}
    1---<NSThread:>{number = 5, name = (null)}
    3---<NSThread:>{number = 1, name = main}
    group---end
  ```
#### NSOperation
- 优点
  - 添加任务依赖
  - 任务执行状态的控制
    - isReady
    - isExecuting
    - isFinished
    - isCancelled
    - 重写了`main`方法，底层控制变更任务执行完成的状态及任务退出状态
    - 重写了`start`方法，自行控制任务状态
  - 最大并发量

- 面试题 
  - 系统是怎么样移除一个isFinished = YES的NSOperation？通过KVO
#### NSThread
###### 启动流程
- start()
- 创建pthread
- main()
- [target performSelector:selector]
- exit()

###### 使用方法
- 初始化方法
  ```
   // 初始化方法
    NSThread *thread = [[NSThread alloc] initWithTarget:self selector:@selector(testThread: ) object:@"参数"];
    // start启动
    [thread start];
    // 可以为开辟的子线程起名字
    thread.name = @"NSThread线程";
    // 调整thread权限,0-1,越大被执行概率越高,由于是概率无法精确控制顺序
    thread.threadPriority = 1;
    // 取消启动的线程
    [thread cancel];
  ```
- 构造器方法
  ```
    // 构造器方式开辟子线程
    [NSThread detachNewThreadSelector:@selector(testThread: ) toTarget:self withObject:@"构造器方法"];
  ```
  
- `performSelector...`  
  - 只要是NSObject的子类或者对象都可以通过调用方法进入子线程和主线程，其实这些方法所开辟的子线程也是NSThread的另一种体现方式。
  - 在编译阶段并不会去检查方法是否有效存在，如果不存在只会给出警告
  -  带`afterDelay`的需要跟runloop相关
  ```
  // 在当前线程 延迟1秒执行 响应OC语言动态性 延迟到运行时才绑定方法
    [self performSelector:@selector(aaa) withObject:nil afterDelay:1.0];
    // 回到主线程 waitUntilDone是否将回调方法执行完再执行后面的代码
    [self performSelectorOnMainThread:@selector(aaa) withObject:nil waitUntilDone:YES];
    // 开辟子线程
    [self performSelectorInBackground:@selector(aaa) withObject:nil];
    // 在指定线程执行
    [self performSelector:@selector(aaa) onThread:[NSThread currentThread] withObject:nil waitUntilDone:YES];
  ```
###### 常驻线程
- 见runloop


#### 多线程与锁

##### 互斥锁
- 防止俩条线程同时对同一公共资源进行读写机制
- 获取锁失败时,线程会进入睡眠,等待锁释放时被唤醒
- 分为递归锁和非递归锁
  - 递归锁: 可重入锁 同一个线程在锁释放之前可以再次获取锁
  - 非递归: 不可重入,必须等锁释放后才能再次获取锁

##### 自旋锁
- 线程反复检查锁变量是否可用,由于线程在这一过程中一直保持执行,所以是一种忙等的锁
- 线程一旦获取自旋锁就会一直保持该锁,直到显式释放自旋锁
- 避免了进程的上下文调度开销,适用于阻塞很短时间线程的场合
###### atomic
- set get方法会有atomic判断 spinlock_t保证堆属性的读写安全
  ```
    void objc_setProperty_atomic(id self, SEL _cmd, id newValue, ptrdiff_t offset)
  {
      reallySetProperty(self, _cmd, newValue, offset, true, false, false);
  }
  static inline void reallySetProperty(id self, SEL _cmd, id newValue, ptrdiff_t offset, bool atomic, bool copy, bool mutableCopy)
  {
      // ...

      if (!atomic) {
          // 不是 atomic 修饰
          oldValue = *slot;
          *slot = newValue;
      } else {
          // 如果是 atomic 修饰，加一把同步锁，保证 setter 的安全
          spinlock_t& slotlock = PropertyLocks[slot];
          slotlock.lock();
          oldValue = *slot;
          *slot = newValue;        
          slotlock.unlock();
      }
  }

  id objc_getProperty(id self, SEL _cmd, ptrdiff_t offset, BOOL atomic) {
      // ...

      // 非原子属性，直接返回值
      if (!atomic) return *slot;
      // 原子属性，加同步锁，保证 getter 的安全
      spinlock_t& slotlock = PropertyLocks[slot];
      slotlock.lock();
      id value = objc_retain(*slot);
      slotlock.unlock();
  }

  ```

###### @synchronized
- 创建单例对象使用，保证多线程环境下创建的对象是唯一的
###### atomic
- 属性关键字 对被修饰的对象进行原子操作(不负责使用)
  - @property(atomic)NSMutableArray *arr;
  - self.array = [NSMutableArray array];  可以
  - [self.array addObject:obj]  不可以
###### OSSpinLock 
- 自旋锁
- 循环等待访问，不释放当前资源
- 用于轻量级数据访问，例如简单的int值的+1/-1操作，系统源码层面引用计数简单的+1/-1操作
- 造成任务优先级反转
###### NSRecursiveLock
- 互斥锁
- 当上一个线程的任务没有执行完毕的时候（被锁住），那么下一个线程会进入睡眠状态等待任务执行完毕，当上一个线程的任务执行完毕，下一个线程会自动唤醒然后执行任务。
###### NSLock
- 面试题(蚂蚁金服)
  ```
  - (void)methodA{
      [lock lock];
      [self methodB];
      [lock unlock];
  }

  - (void)methodB{
      [lock lock];
      // 操作逻辑
      [lock unlock];
  }
  
  // 死锁
  // 某一线程调取lock方法获取到这个锁,然后又对同一把锁再次调用`lock`方法,已经获取到锁,再次去获取锁,造成死锁
  // 使用递归锁
  ```

#### 线程间通信

###### 直接消息传递
通过 performSelector 的一系列方法，可以实现由某一线程指定在另外的线程上执行任务。因为任务的执行上下文是目标线程，这种方式发送的消息将会自动的被序列化。
###### 全局变量、共享内存块和对象
在两个线程之间传递信息的另一种简单方法是使用全局变量，共享对象或共享内存块。尽管共享变量既快速又简单，但是它们比直接消息传递更脆弱。必须使用锁或其他同步机制仔细保护共享变量，以确保代码的正确性。 否则可能会导致竞争状况，数据损坏或崩溃。
###### 条件执行
条件是一种同步工具，可用于控制线程何时执行代码的特定部分。您可以将条件视为关守，让线程仅在满足指定条件时运行。
###### Runloop sources
一个自定义的 Runloop source 配置可以让一个线程上收到特定的应用程序消息。由于 Runloop source 是事件驱动的，因此在无事可做时，线程会自动进入睡眠状态，从而提高了线程的效率。
###### Ports and sockets
基于端口的通信是在两个线程之间进行通信的一种更为复杂的方法，但它也是一种非常可靠的技术。更重要的是，端口和套接字可用于与外部实体（例如其他进程和服务）进行通信。为了提高效率，使用 Runloop source 来实现端口，因此当端口上没有数据等待时，线程将进入睡眠状态。
###### 消息队列
传统的多处理服务定义了先进先出（FIFO）队列抽象，用于管理传入和传出数据。尽管消息队列既简单又方便，但是它们不如其他一些通信技术高效。
###### Cocoa 分布式对象
分布式对象是一种 Cocoa 技术，可提供基于端口的通信的高级实现。尽管可以将这种技术用于线程间通信，但是强烈建议不要这样做，因为它会产生大量开销。分布式对象更适合与其他进程进行通信，尽管在这些进程之间进行事务的开销也很高
 
## Runloop

#### 概念
> Runloop是通过内部维护的`事件循环`来对`事件/消息进行管理`的一个对象
> 
- 没有消息需要处理时，休眠以避免资源占用 source1
  - 用户态 --> 内核态

- 有消息需要处理时，立刻被唤醒 source0
  - 内核态 --> 用户态

#### Runloop数据结构
> NSRunloop是对CFRunloop的封装，提供了面向对象的API
> 
![Runloop.png](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/Runloop%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84.png)
##### CFRunloop

```
struct __CFRunLoop {
    CFRuntimeBase _base;
    pthread_mutex_t _lock;
    __CFPort _wakeUpPort;
    Boolean _unused;
    volatile _per_run_data *_perRunData;          
    pthread_t _pthread;
    uint32_t _winthread;
    CFMutableSetRef _commonModes;
    CFMutableSetRef _commonModeItems;
    CFRunLoopModeRef _currentMode;
    CFMutableSetRef _modes;
    struct _block_item *_blocks_head;
    struct _block_item *_blocks_tail;
    CFTypeRef _counterpart;
};
```
- **pthread:** 代表线程，runloop跟线程是一一对应关系
- **currentMode:** CFRunLoopMode数据结构
- **modes**: 一个包含CFRunLoopMode类型的集合   (NSMutableSet<CFRunLoopMode *>)
- **commonModes:** 一个包含NSString类型的集合    (NSMutableSet<NSString *>)
- **commonModeItems:** 包含多个元素的集合 (NSMutableSet<observer,timer,source *>)
##### CFRunloopMode

```
struct __CFRunLoopMode {
    CFRuntimeBase _base;
    pthread_mutex_t _lock;
    CFStringRef _name;
    Boolean _stopped;
    char _padding[3];
    CFMutableSetRef _sources0;
    CFMutableSetRef _sources1;
    CFMutableArrayRef _observers;
    CFMutableArrayRef _timers;
    CFMutableDictionaryRef _portToV1SourceMap;
    __CFPortSet _portSet;
    CFIndex _observerMask;
};

```
- **name:** 模式的名称
  - 如NSDefaultRunLoopMode，通过这样一个名称来切换对应的模式；
  - commonModes里面都是名称字符串，通过这些名称来支持多种模式(NSDefaultRunloopMode)
- **sources0:** 集合类型的数据结构(NSMutableSet)
- **sources1:** 集合类型的数据结构(NSMutableSet)
- **observers:** 数组类型的数据结构(NSMutableArray)
- **timers:** 数组类型的数据结构(NSMutableArray)
##### Source/Timer/Observer
###### CFRunLoopSource
- source0
  - 需要手动唤醒线程
- source1
  - 具备唤醒线程能力

###### CFRunLoopTimer
- 基于事件的定时器
- 和NSTimer是`toll-free bridged`

###### CFRunLoopObserver
> 观测时间点
- kCFRunLoopEntry (runloop启动)
- kCFRunLoopBeforeTimers (将要对timer进行观察处理)
- kCFRunLoopBeforeSources (将要对sources进行观察处理)
- kCFRunLoopBeforeWaiting (将要进入休眠 用户态-->内核态)
- kCFRunLoopAfterWaiting (内核态-->用户态)
- kCFRunLoopeExit (runloop退出)
##### CommonMode特殊性
- CommonMode不是实际存在的一种Mode
- 是同步Source/Timer/Observer到多个Mode中的一种技术方案
##### 事件循环的实现机制
###### void CFRunLoopRun()

![runloop事件循环](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/Runloop%E4%BA%8B%E4%BB%B6%E5%BE%AA%E7%8E%AF%E6%9C%BA%E5%88%B6.png)
- 1.即将进入Runloop，发通知
- 2.将要处理Timer/Source0事件，发通知
- 3.处理source0事件
- 4.如果有source1事件处理，goto语句跳转8
- 5.没事件处理，线程将要休眠，发通知
- 6.休眠，等待唤醒
  - Source1唤醒
  - Timer事件唤醒
  - 外部手动唤醒
- 7.线程刚被唤醒，发通知
- 8.处理唤醒时收到的消息，处理完后回到2
- 9.即将推出RunLoop，发通知


##### Runloop的核心

![runloop核心](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/runloop%E7%9A%84%E6%A0%B8%E5%BF%83.png)
- `main()`函数经过一系列调用会调用为系统的`mach_msg()`函数，这样就发生了系统调用
- 经过系统调，当前线程就把控制权交给了内核态，`mach_msg()`函数在一定条件下会返回给调用方，这个触发返回的逻辑就是唤醒线程的逻辑(source1、手动唤醒等)
#### Runloop与NSTimer
###### 如何将Timer同步到多个Mode中

- void CFRunLoopAddTimer(runLoop,timer,commonMode) ==> void CFRunLoopAddTimer(CFRunLoopRef rl, CFRunLoopTimerRef rlt, CFStringRef modeName)
  - 通过modeName判断，如果当前是commonMode `(modeName = kCFRunLoopCommonModes)`
  - 取出传入runloop(rl)的commonModes这个集合 `CFSetRef set = rl->_commonModes`
  - 同时判断传入runloop(rl)对应的_commonModeItems是否为空，为空时创建
  - 然后把timer(rlt)添加到commonModeItems集合中 `CFSetAddValue(rl->_commonModeItems, rlt)`
  - 然后把runloop跟timer封装成一个context `CFTypedef context[2] = {rl, rlt}`
  - 然后对集合set中每一个元素调用 `CFSetApplyFunction(set, (__CFRunLoopAddItemToCommonModes), (void *)context)`

- void __CFRunLoopAddItemToCommonModes(const void *value, void *ctx) 
  - 取当前mode名称(value) `CFStringRef modeName = (CFStringRef)value`
  - 取当前上下文中的runloop和item
  - 根据item类型判断来决定调用 addSource addObserver还是addTimer
  - 此时调用addTimer回到上面的方法`CFRunLoopAddTimer(rl, (CFRunloopTimerRef)item, modeName)`，此时的入参modeName已经从commonMode变成了被打上了commonMode标记的一个具体的实际的mode
  - 在CFRunLoopAddTimer中，才会真正的把timer添加到对应的runloop mode下的timers数组中，这样就实现了多个timer同步到多个mode下

#### Runloop与多线程
###### 关系
- 一一对应
- 自己创建的线程没有RunLoop
###### 怎么实现一个常驻线程
- 为当前线程开启一个RunLoop
- 向该RunLoop中添加一个Port/Source等维护RunLoop的事件循环
- 启动该RunLoop



## 网络

#### HTTP协议
> 超文本传输协议
> 
##### 请求/响应报文

###### 请求报文
![请求报文](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E8%AF%B7%E6%B1%82%E6%8A%A5%E6%96%87.png)
- 请求行
  - 方法: `GET` `POST`等
  - URL:请求地址
  - 协议版本:HTTP1.1
- 请求头
  - 头部字段以`key:value`形式组合在一起,多个首部字段构成首部字段区域
- 实体主体
  - 一般`GET`请求没有实体主体,`POST`请求有请求主体

###### 响应报文

![响应报文](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%93%8D%E5%BA%94%E6%8A%A5%E6%96%87.png)
- 响应行
  - 版本
  - 状态码:`100` `200` `303` `404` `500`
  - 短语:状态码的描述
- 请求头
  - 头部字段以`key:value`形式组合在一起,多个首部字段构成首部字段区域
- 实体主体

###### 请求方式

- GET
- POST
- HEAD
- PUT
- DELETE
- OPTIONS


###### GET POST区别
**一般的回答是:**
- `GET`请求参数是以`?`拼接到`URL`后面的,而`POST`请求的参数一般是放在`Body`里面的
- `GET`的参数长度限制是`2048`个字符,而`POST`请求一般没有限制
- `GET`请求不太安全,`POST`请求是比较安全的

**但从语义的角度来比较的话,应该是这样的:**
  - GET: 获取资源 `安全的` `幂等的` `可缓存的`
  - POST: 处理资源 `不安全的` `不幂等的` `不可缓存的`


**语义对应的解释:**
- 安全性:
  - 不应该引起`server`端任何状态变化;如`GET`请求多次去`Server`端获取数据,不会引起`Server`端的状态变化
  - 安全请求包括: `GET`,`HEAD`,`OPTIONS`

- 幂等性:
  - 同一个请求方法执行多次跟执行一次的效果完全相同;如`GET`请求多次去`Server`端获取数据,执行的效果是完全相同的;此处并不是指的是获取的数据完全相同(如多次`GET`请求中间有`POST`数据有可能发生改变),指的是`GET`请求这个方法 `执行的效果`
  - 幂等性请求包括: `GET`,`PUT`,`DELETE`
- 可缓存性:
  - 请求是否可以缓存;当我们在发起一个`HTTP`请求的过程中,传递的链路我们是不确定的,虽然说在一条`TCP`链接上,但是网络路径在接触或者通过网关包括一些代理到底`Server`端,在这上面会涉及到方方面面内容,往往对于一些代理服务器会有缓存,而这种缓存性是官方的一种规范,可以遵守也可以不遵守,大多数情况下会遵守,所以在`GET`请求会有相对应的缓存
  - 可缓存的请求有`GET`,`HEAD`
##### 链接建立流程

![HTTP建立流程](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/HTTP%E9%93%BE%E6%8E%A5%E5%BB%BA%E7%AB%8B%E6%B5%81%E7%A8%8B.png)
###### 三次握手
- 为什么是3次握手?(超时)
  - Client第一次发送syn1,超时了,Server没收到
  - Client启动超时重发策略,发送了syn2,Server收到以后,建立链接;
  - 此时第一次发送syn1的也收到,Server以为要再次建立链接
###### 四次挥手
- Client-->FIN-->Server
- Server-->ACK-->Client(半关闭状态)
- Server-->FIN+ACK-->Client
- Client-->ACK-->Server

##### HTTP特点
###### 无连接

- 含义: HTTP链接有建立链接和释放链接的一个过程
- 补偿: HTTP的持久链接
![持久链接](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E6%8C%81%E4%B9%85%E9%93%BE%E6%8E%A5.png)
  - 涉及到的请求头部字段
    - Connection: keep-alive (客户端期许持久链接)
    - time:20 (持久链接持续时间)
    - max:10 (当前链接最大的http请求和响应对)
  - HTTP的持久链接好处
    - 提升网络请求效率,减少`TCP`连接建立的数量 
  - 怎么判断一个请求是否结束
    > 在一个tcp连接里面发送了多次http请求,怎么区分前一个请求结束了,后一个请求开始
    > 
    - Content-length: 1024 (请求报文跟响应报文都有头部字段,根据服务端响应的数据大小,客户端根据接收数据字节数是否到达1024)
    - chunked: 通过post请求时,server端返回给客户端的数据是需要通过多次响应来返回给客户端这些数据,可以根据http响应报文中头部字段chunked来判断http请求是否结束;当有多个块儿通过http的TCP链接传输给客户端时,每个报文都会带有chunked字段,最后一个是空的chunked


###### 无状态
- 含义:server端对事务处理没有记忆能力
- 补偿: Cookie / Session


#### HTTPS与网络安全

###### HTTPS跟HTTP有什么样的区别

> HTTPS = HTTP + SSL/TLS
> 

###### HTTPS连接建立流程

![HTTPS链接流程](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/HTTPS%E9%93%BE%E6%8E%A5%E6%B5%81%E7%A8%8B.png)
- Client向Server发送TLS版本,支持的算法及一个随机数C
- Server向Client发送商定的加密算法,随机数S,server证书
- Client证书验证(验证公钥)
- Client组装会话秘钥(随机数C+随机数S+客户端产生的预主秘钥)
- Client通过Server的公钥对预主秘钥进行加密传输
- Server通过私钥解密得到预主秘钥
- 组装会话秘钥(随机数C+随机数S+解密得到预主秘钥)
- Client发送加密握手消息
- Server返回加密的握手消息

###### HTTPS连接使用了哪些加密手段?为什么?
- 连接建立过程中使用非对称加密,耗时但是安全
- 后续通信过程使用对称加密
#### TCP和UDP传输层协议

##### TCP 传输控制协议
###### 特点
- 面向连接 (三次握手,四次挥手)
- 可靠传输
  - 特点
    - 无差错
    - 不丢失
    - 不重复
    - 按序到达 (滑动窗口协议)
  - 实现:停止等待协议
    - 无差错情况
    - 超时重传
    - 确认丢失
    - 确认迟到
  ![可靠传输](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%8F%AF%E9%9D%A0%E4%BC%A0%E8%BE%93.png)

- 面向字节流
  - 不管发送方提交给TCP的缓冲是多大的数据,对TCP本身来说它会根据一个实际的情况来进行划分一次性传递的字节数

  ![面向字节流](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E9%9D%A2%E5%90%91%E5%AD%97%E8%8A%82%E6%B5%81.png)
- 流量控制 
  - 滑动窗口协议
    > 发送方的窗口由接收方确定，目的在于控制发送速度，以免接受方缓存不够大，而导致溢出。假如接收方告诉发送方，建议滑动窗口为6，（否则太大一次发送太大，我接收缓冲区太小，处理不过来），然后发送方可以一次发送6个数据帧，假设已经发送了4,5,6，但是没收到关联的ACK，7,8,9则等待发送，如果此时发送端收到4号ACK，则窗口向右收缩，此时窗口就“滑动”了
    
  - 后退n针协议 
    > 发送方一次发送比如说10个帧，前两个针都返回了对应的ACK，数据帧2出现了错误，这时发送方被迫重新发送2-8这七个帧，这就是回退n帧协议。但是如果接收方已经接收到了3-8帧，只是丢失了2帧，全部重传太浪费网络条件了，所以有时候会选择重传丢失的的帧。这就是选择重传协议。

  ![滑动窗口](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E6%BB%91%E5%8A%A8%E7%AA%97%E5%8F%A3.png)
- 拥塞控制
  > 拥塞控制就是防止过多的数据注入到网络中，这样使得网络中的路由器或者链路不至于过载。
  - 慢开始 拥塞避免
    > 慢开始是指发送方先设置cwnd=1，一次发送一个报文段，随后每经过一个传输轮次，拥塞串口cwnd就加倍，其实增长并不慢，以指数形式增长。还要设定一个慢开始门限，当cwnd>门限值，改用拥塞避免算法。拥塞避免算法使cwnd按线性规律缓慢增长。当网络发生延时，门限值减半，拥塞窗口执行慢开始算法。
  - 快恢复 快重传
    >  当接收方收到失序的报文段，按照快重传，需要尽快发送对未收到的报文段的重复确认。快恢复是指当拥塞串口达到门限值，不直接开启慢启动算法，而是快恢复，快恢复就是收到三个重复的确认（可看作是网络已经拥塞了），此时并不执行慢开始算法，而是执行快恢复，就是新的门限值是原来的一半，直接进入拥塞避免阶段。
    
    
  ![慢开始](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E6%85%A2%E5%BC%80%E5%A7%8B.png)

###### 功能
- 复用 分用(多端口复用)
- 差错检测


##### UDP 用户数据包协议 
###### 特点
- 无连接
- 尽最大努力交付
  - 不保证可靠传输
- 面向报文 既不合并也不拆分
  
  ![面向报文](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E9%9D%A2%E5%90%91%E6%8A%A5%E6%96%87.png)

###### 功能

- 复用 分用(多端口复用)

  ![复用](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%A4%8D%E7%94%A8%20%E5%88%86%E7%94%A8.png)
- 差错检测

  ![差错检测](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%B7%AE%E9%94%99%E6%A3%80%E6%B5%8B.png)
#### DNS解析
> 域名到IP地址的映射,DNS解析请求采用UDP数据报,且明文,端口号53
> 
- 递归查询
   > 我去给你问一下
- 迭代查询
  > 我告诉你谁可能知道
  > 
- DNS劫持问题
  - httpDNS
    - IP直连 `http://119.29.29.29?dn=www.xxx.com&ip=172.12.134.108`
    - 由原来的使用DNS协议向DNS服务器的53端口进行请求转换为使用HTTP协议向DNS服务器的80端口进行请求
  - 长连接
   ![长连接](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E9%95%BF%E8%BF%9E%E6%8E%A5.png)
- DNS解析转发
  - 例如移动网络下向移动DNS解析
  - 移动DNS解析为了节省资源转给电信DNS
  - 电信DNS通过权威DNS解析对应电信对应的服务器返回
  - 这样的话相当于移动网络访问电信服务器,跨网访问,请求缓慢
#### Session/Cookies
> HTTP协议无状态特点的补偿
> 
##### Session
> Session主要用来记录用户的状态,区分用户;状态保存在服务器端
> 

##### Cookies
> Cookie主要用来记录用户的状态,区分用户;状态保存在客户端
> 客户端发送的cookie是在http请求报文的Cookie首部字段中
> 服务器设置http响应报文的Set-Cookie首部字段
> 
###### 怎么修改cookie?
- 新cookie覆盖旧cookie
- 覆盖规则:name,path,domain需要跟原cookie一致
###### 怎么删除cookie?
- 新cookie覆盖旧cookie
- 覆盖规则:name,path,domain需要跟原cookie一致
- 设置cookie的expries = 过去的某一时间点(cookie失效),或设置maxAge = 0

###### 怎么保证cookie安全?
- 对cookie进行加密处理
- 只在https上携带cookie
- 设置cookie为httpOnly,防止跨站脚本攻击



## 设计模式
#### 设计原则
##### 单一职责原则
> 一个类只负责一件事儿
- CALayer 和 UIView
##### 依赖倒置原则
> 抽象不应该依赖具体实现,具体实现可以依赖于抽象
> 
- 数据的增删改查依赖定义抽象的接口
- 接口数据具体实现是数据库还是plist,文件等等不关心
##### 开闭原则
> 对修改关闭,对扩展开放
> 
- 设计类的时候考虑后续迭代扩展的需求,成员变量定义尽量谨慎,避免反复修改
- 子类继承
##### 里氏替换原则
> 父类可以被子类无缝替换,且原有功能不受任何影响
> 
- KVO机制
##### 接口隔离原则
> 使用多个专门的协议 而不是一个庞大臃肿的协议
> 协议中的方法应该尽量少
- UITableView
##### 迪米特原则
> 一个对象应当对其他对象有尽可能少的了解
> 高内聚 低耦合
#### 设计模式
##### 责任链模式 
###### 场景
![%E8%B4%A3%E4%BB%BB%E9%93%BE%E6%A8%A1%E5%BC%8F.png](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E8%B4%A3%E4%BB%BB%E9%93%BE%E6%A8%A1%E5%BC%8F.png)
###### 类构成
![%E8%B4%A3%E4%BB%BB%E9%93%BE%E6%A8%A1%E5%BC%8F%E7%B1%BB%E6%9E%84%E6%88%90.png](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E8%B4%A3%E4%BB%BB%E9%93%BE%E6%A8%A1%E5%BC%8F%E7%B1%BB%E6%9E%84%E6%88%90.png)
```
#import <Foundation/Foundation.h>

@class BusinessObject;
typedef void(^CompletionBlock)(BOOL handled);
typedef void(^ResultBlock)(BusinessObject *handler, BOOL handled);

@interface BusinessObject : NSObject

// 下一个响应者(响应链构成的关键)
@property (nonatomic, strong) BusinessObject *nextBusiness;
// 响应者的处理方法
- (void)handle:(ResultBlock)result;

// 各个业务在该方法当中做实际业务处理
- (void)handleBusiness:(CompletionBlock)completion;
@end

```
```
#import "BusinessObject.h"

@implementation BusinessObject

// 责任链入口方法
- (void)handle:(ResultBlock)result
{
    CompletionBlock completion = ^(BOOL handled){
        // 当前业务处理掉了，上抛结果
        if (handled) {
            result(self, handled);
        }
        else{
            // 沿着责任链，指派给下一个业务处理
            if (self.nextBusiness) {
                [self.nextBusiness handle:result];
            }
            else{
                // 没有业务处理, 上抛
                result(nil, NO);
            }
        }
    };
    
    // 当前业务进行处理
    [self handleBusiness:completion];
}

- (void)handleBusiness:(CompletionBlock)completion
{
    /*
     业务逻辑处理
     如网络请求、本地照片查询等
     */
}
```
- 这样做就可以根据产品经理的需求,来调整业务之间的指向,来动态调整业务的顺序
- 进一步的调整为服务端动态下发,本地对任务定义任务号及一一对应的类名,作为`key value`形式的通过后端下发,本地根据`Class`的反射来解析出具体的类,根据数组的顺序调整责任链的下一个响应者来动态调整
###### 示例
**[Responder](https://github.com/tutu279737146/DesignPatten/tree/master/Responder)**

##### 桥接模式
###### 场景--业务解耦问题
![avatar](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E4%B8%9A%E5%8A%A1%E8%A7%A3%E8%80%A6.png)
###### 类构成
![avatar](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E6%A1%A5%E6%8E%A5%E6%A8%A1%E5%BC%8F%E7%B1%BB%E6%9E%84%E6%88%90.png)
###### 示例
**[Bridge](https://github.com/tutu279737146/DesignPatten/tree/master/Bridge)**
##### 适配器模式
###### 场景--一个现有类需要适应变化的问题
> 错误: 对原有类增加实力变量或者方法;

###### 类构成
![avatar](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E9%80%82%E9%85%8D%E5%99%A8%E6%A8%A1%E5%BC%8F%E7%B1%BB%E6%9E%84%E6%88%90.png)
###### 示例
**[Adapter](https://github.com/tutu279737146/DesignPatten/tree/master/Adapter)**

##### 单例模式

###### 示例
```
+ (id)sharedInstance
{
    // 静态局部变量
    static Mooc *instance = nil;
    // 通过dispatch_once方式 确保instance在多线程环境下只被创建一次
    static dispatch_once_t onceToken;
    dispatch_once(&onceToken, ^{
        // 创建实例
        instance = [[super allocWithZone:NULL] init];
    });
    return instance;
}

// 重写方法【必不可少】
+ (id)allocWithZone:(struct _NSZone *)zone{
    return [self sharedInstance];
}

// 重写方法【必不可少】
- (id)copyWithZone:(nullable NSZone *)zone{
    return self;
}
```
##### 命令模式

###### 场景
> 行为参数化
> 降低代码重合度
###### 示例
**[Command](https://github.com/tutu279737146/DesignPatten/tree/master/Command)**


## 框架及架构
#### 图片缓存框架
> 如何设计一个图片缓存框架?
> 
##### 框架构成

![图片缓存](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%9B%BE%E7%89%87%E7%BC%93%E5%AD%98%E6%A1%86%E6%9E%B6%E7%9A%84%E7%BB%93%E6%9E%84.png)
##### Manager
> 负责调度各个模块
> 
- 读写
  - 以图片URL单向hash值作为key,多级缓存提高查找效率
  - 内存
  - 磁盘
  - 网络
##### 内存模块
###### size
- 数据结构--队列
- 小于10kb 50张
- 小于100kb 20张
- 大于100kb 10张
###### 淘汰策略
- 以队列先进先出方式进行淘汰
- LRU
  - 定时检查(落地难)
  - 提高检查触发频率(图片读写时,前后台切换时)

##### 磁盘模块

###### 存储方式
###### size
###### 淘汰策略

##### 网络模块

###### 最大并发量

###### 超时重试
###### 请求的优先级

##### CodeManager
###### 压缩
###### 解码
- 方式

> 应用策略模式对不同图片格式进行解码
- 时机

> 磁盘读取后  网络请求返回后
> 
#### 客户端架构

![客户端架构](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/%E5%AE%A2%E6%88%B7%E7%AB%AF%E6%95%B4%E4%BD%93%E6%9E%B6%E6%9E%84.png)
- 独立App的通用层(时长统计,崩溃统计,网络第三方库)
  - 放于任何App中都能起到支撑作用
- 通用业务层 (当前业务相关比如imageView的封装)
- 中间层 (解耦)
- 业务A 业务B 业务C 业务D ....

##### 解耦
- openURL
- 依赖注入
  - 中间层,业务C将自己注入到中间层,业务A去中间层获取所依赖的方法等等
  - 注册protocol
  
## 性能优化

#### UI

###### CPU

- 尽量用轻量级的对象，比如用不到事件处理的地方，可以考虑使用CALayer取代UIView

- 不要频繁地调用UIView的相关属性，比如frame、bounds、transform等属性，尽量减少不必要的修改

- 尽量提前计算好布局，在有需要时一次性调整对应的属性，不要多次修改属性

- Autolayout会比直接设置frame消耗更多的CPU资源

- 图片的size最好刚好跟UIImageView的size保持一致

- 控制一下线程的最大并发数量

- 尽量把耗时的操作放到子线程
- 文本处理（尺寸计算、绘制）
- 图片处理（解码、绘制）

###### GPU

- 尽量避免短时间内大量图片的显示，尽可能将多张图片合成一张进行显示

- GPU能处理的最大纹理尺寸是4096x4096，一旦超过这个尺寸，就会占用CPU资源进行处理，所以纹理尽量不要超过这个尺寸

- 尽量减少视图数量和层次

- 减少透明的视图（alpha<1），不透明的就设置opaque为YES

- 尽量避免出现离屏渲染
  - 在OpenGL中，GPU有2种渲染方式
  - On-Screen Rendering：当前屏幕渲染，在当前用于显示的屏幕缓冲区进行渲染操作
  - Off-Screen Rendering：离屏渲染，在当前屏幕缓冲区以外新开辟一个缓冲区进行渲染操作

  - 离屏渲染消耗性能的原因
  - 需要创建新的缓冲区
  - 离屏渲染的整个过程，需要多次切换上下文环境，先是从当前屏幕（On-Screen）切换到离屏（Off-Screen）；等到离屏渲染结束以后，将离屏缓冲区的渲染结果显示到屏幕上，又需要将上下文环境从离屏切换到当前屏幕

  - 哪些操作会触发离屏渲染？
  - 光栅化:layer.shouldRasterize = YES

  - 遮罩:layer.mask

  - 圆角:同时设置layer.masksToBounds = YES、layer.cornerRadius大于0
  - 考虑通过CoreGraphics绘制裁剪圆角，或者叫美工提供圆角图片

  - 阴影:layer.shadowXXX
  - 如果设置了layer.shadowPath就不会产生离屏渲染

###### 卡顿
- 平时所说的“卡顿”主要是因为在主线程执行了比较耗时的操作

- 可以添加Observer到主线程RunLoop中，通过监听RunLoop状态切换的耗时，以达到监控卡顿的目的

#### 耗电优化

###### 主要来源
- CPU处理，Processing

- 网络，Networking

- 定位，Location

- 图像，Graphics

###### 优化方案

- 尽可能降低CPU、GPU功耗

- 少用定时器

- 优化I/O操作
  - 尽量不要频繁写入小数据，最好批量一次性写入
  - 读写大量重要数据时，考虑用dispatch_io，其提供了基于GCD的异步操作文件I/O的API。用dispatch_io系统会优化磁盘访问
  - 数据量比较大的，建议使用数据库（比如SQLite、CoreData）

- 网络优化
  - 减少、压缩网络数据
  - 如果多次请求的结果是相同的，尽量使用缓存
  - 使用断点续传，否则网络不稳定时可能多次传输相同的内容
  - 网络不可用时，不要尝试执行网络请求
  - 让用户可以取消长时间运行或者速度很慢的网络操作，设置合适的超时时间
  - 批量传输，比如，下载视频流时，不要传输很小的数据包，直接下载整个文件或者一大块一大块地下载。如果下载广告，一次性多下载一些，然后再慢慢展示。如果下载电子邮件，一次下载多封，不要一封一封地下载

- 定位优化
  - 如果只是需要快速确定用户位置，最好用CLLocationManager的requestLocation方法。定位完成后，会自动让定位硬件断电
  - 如果不是导航应用，尽量不要实时更新位置，定位完毕就关掉定位服务
  - 尽量降低定位精度，比如尽量不要使用精度最高的kCLLocationAccuracyBest
  - 需要后台定位时，尽量设置pausesLocationUpdatesAutomatically为YES，如果用户不太可能移动的时候系统会自动暂停位置更新
  - 尽量不要使用startMonitoringSignificantLocationChanges，优先考虑startMonitoringForRegion:

- 硬件检测优化
  - 用户移动、摇晃、倾斜设备时，会产生动作(motion)事件，这些事件由加速度计、陀螺仪、磁力计等硬件检测。在不需要检测的场合，应该及时关闭这些硬件

#### APP启动优化

###### APP启动方式

- 冷启动（Cold Launch）：从零开始启动APP
- 热启动（Warm Launch）：APP已经在内存中，在后台存活着，再次点击图标启动APP

> APP启动时间的优化，主要是针对冷启动进行优化
> 
![main](https://raw.githubusercontent.com/tutu279737146/BlogImages/master/Images/main%E5%87%BD%E6%95%B0%E5%90%AF%E5%8A%A8.png)
###### APP启动时间查看
- 通过添加环境变量可以打印出APP的启动时间分析（Edit scheme -> Run -> Arguments）DYLD_PRINT_STATISTICS设置为1
- 如果需要更详细的信息，那就将DYLD_PRINT_STATISTICS_DETAILS设置为1

#### 安装包瘦身

> 安装包（IPA）主要由可执行文件、资源组成

- 资源（图片、音频、视频等）
  - 采取无损压缩
  - 去除没有用到的资源： https://github.com/tinymind/LSUnusedResources

- 可执行文件瘦身
  - 编译器优化
    - Strip Linked Product、Make Strings Read-Only、Symbols Hidden by Default设置为YES
    - 去掉异常支持，Enable C++ Exceptions、Enable Objective-C Exceptions设置为NO， Other C Flags添加-fno-exceptions

- 利用AppCode（https://www.jetbrains.com/objc/）检测未使用的代码：菜单栏 -> Code -> Inspect Code

- 编写LLVM插件检测出重复代码、未被调用的代码 

#### 崩溃优化
- 数组越界,字典插nil
- KVC私有属性
- 多次移除同一 KVO 会 crash
- 通知9.0之前移除问题

### 内存泄露
- 在 dealloc 中打印日志
- 通过 Memory Graph 查找


## WKWebView的坑


#### WKWebView白屏

#### WKWebView白屏原因

- WKWebView是App内部的多进程组件
- UIWebView内存过大,App会crash
- WKWebView内存过大,WebContent Process会crash,出现白屏

#### WKWebView白屏解决办法

###### WKNavigationDelegate

` - (void)webViewWebContentProcessDidTerminate:(WKWebView *)webView API_AVAILABLE(macosx(10.11), ios(9.0));
`
- 当 WKWebView 总体内存占用过大，页面即将白屏的时候，系统会调用上面的回调函数，我们在该函数里执行[webView reload](这个时候 webView.URL 取值尚不为 nil）解决白屏问题。在一些高内存消耗的页面可能会频繁刷新当前页面，H5侧也要做相应的适配操作。

###### 检测webView.title是否为空

- 可以在 viewWillAppear 的时候检测 webView.title 是否为空来 reload 页面。


#### WKWebView的Cookie问题

> WKWebView Cookie 问题在于 WKWebView 发起的请求不会自动带上存储于 NSHTTPCookieStorage 容器中的 Cookie。
> 

WKWebView loadRequest 前，在 request header 中设置 Cookie, 解决首个请求 Cookie 带不上的问题；

```
  WKWebView * webView = [WKWebView new]; 
  NSMutableURLRequest * request = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:@"手机统一登录"]]; 
  [request addValue:@"skey=skeyValue" forHTTPHeaderField:@"Cookie"]; 
  [webView loadRequest:request];
```

通过 document.cookie 设置 Cookie 解决后续页面(同域)Ajax、iframe 请求的 Cookie 问题；
注意：document.cookie()无法跨域设置 cookie

```
  WKUserContentController* userContentController = [WKUserContentController new]; 
  WKUserScript * cookieScript = [[WKUserScript alloc] initWithSource: @"document.cookie = 'skey=skeyValue';" injectionTime:WKUserScriptInjectionTimeAtDocumentStart forMainFrameOnly:NO]; 
  [userContentController addUserScript:cookieScript];
```

#### WKWebView的loadRequest问题
在 WKWebView 上通过 loadRequest 发起的 post 请求 body 数据会丢失：

```
 //同样是由于进程间通信性能问题，HTTPBody字段被丢弃
 [request setHTTPMethod:@"POST"];
 [request setHTTPBody:[@"bodyData" dataUsingEncoding:NSUTF8StringEncoding]];
 [wkwebview loadRequest: request];
```

> 假如想通过-[WKWebView loadRequest:]加载 post 请求 request1: http://h5.qzone.qq.com/mqzone/index,可以通过以下步骤实现：

- 替换请求 scheme，生成新的 post 请求 request2: post://http://h5.qzone.qq.com/mqzone/index, 同时将 request1 的 body 字段复制到 request2 的 header 中（WebKit 不会丢弃 header 字段）;
- 通过-[WKWebView loadRequest:]加载新的 post 请求 request2;
- 通过 +[WKBrowsingContextController registerSchemeForCustomProtocol:]注册 scheme: post://;
- 注册 NSURLProtocol 拦截请求post://http://h5.qzone.qq.com/mqzone/index ,替换请求 scheme, 生成新的请求 request3: http://h5.qzone.qq.com/mqzone/index，将 request2 header的body 字段复制到 request3 的 body 中，并使用 NSURLConnection 加载 request3，最后通过 NSURLProtocolClient 将加载结果返回 WKWebView;

## AFNetWorking


> `AFNetworking`是基于[Foundation URL Loading System](https://links.jianshu.com/go?to=https%3A%2F%2Fdeveloper.apple.com%2Fdocumentation%2Ffoundation%2Furl_loading_system)设计，是对`NSURLSession`的高度集中封装，使其简单易用。
> 

#### 主要构成
|            核心类            |                           负责模块                           |
| :--------------------------: | :----------------------------------------------------------: |
|     AFURLSessionManager      | `AFNetworking`的核心，用于管理`NSURLSession`，生成`NSURLSessionTask`以及处理`NSURLSessionDelegate`等代理回调。 |
|     AFHTTPSessionManager     | `AFHTTPSessionManager`继承自`AFURLSessionManager`，专门用于`HTTP`连接。 |
| AFNetworkReachabilityManager |                         网络连接检测                         |
|       AFSecurityPolicy       |                    处理`HTTPS`证书信任等                     |
|  AFURLRequestSerialization   |               序列化客户端的请求`NSURLRequest`               |
|  AFURLResponseSerialization  |              序列化服务端的响应`NSURLResponse`               |

#### 相关面试问题

##### AFN2.0和AFN3.0的区别
|            2.0            |                           3.0                           |
| :---: | :--: |
|     AFURLConnectionOperation      | AFURLSessionManager |
|     AFHTTPRequestOperation      | AFHTTPSessionManager |
|     AFHTTPRequestOperationManager      | AFNetworkReachabilityManager |

- 三个主要类的更换对应着请求方法也进行更换
- AFN2.0常驻线程,AFN3.0不需要
- `operationQueue`作用不同

#### 为什么要更换
- NSURLSession提升了网络连接速度，采用了 HTTP2.0，HTTP2.0 多路复用、新的二进制格式、header压缩
- Session采用了共享，而非每次都新建


##### AFN2.0 为何使用常驻线程?
- AFN2.0里面把多个网络请求的发起和解析都放在了一个子线程里执行
- 子线程默认不会开启`runloop`,执行完任务后就退出了。基于connection的网络请求是异步的，导致获取到数据时线程就退出了，网络回调的代理方法无法执行。
- 所以AFN2.0 通过一个单例，用NSThread创建了一个线程，并且为这个线程添加了一个runloop，并且加了一个NSMachPort，来防止runloop直接退出。 
- 这条线程就是AFN用来发起网络请求，并且接受网络请求回调的线程，仅仅就这一条线程。


```
//首先用NSThread创建了一个线程，并且这个线程是个单例。
+ (NSThread *)networkRequestThread {
    static NSThread *_networkRequestThread = nil;
    static dispatch_once_t oncePredicate;
    dispatch_once(&oncePredicate, ^{
        _networkRequestThread = [[NSThread alloc] initWithTarget:self selector:@selector(networkRequestThreadEntryPoint:) object:nil];
        [_networkRequestThread start];
    });

    return _networkRequestThread;
}

//新建的子线程默认是没有添加Runloop的，因此给这个线程添加了一个runloop，并且加了一个NSMachPort，来防止这个新建的线程由于没有活动直接退出。
+ (void)networkRequestThreadEntryPoint:(id)__unused object {
    @autoreleasepool {
        [[NSThread currentThread] setName:@"AFNetworking"];

        NSRunLoop *runLoop = [NSRunLoop currentRunLoop];
        [runLoop addPort:[NSMachPort port] forMode:NSDefaultRunLoopMode];
        [runLoop run];
    }
}
```
##### 那有人会问：那网络请求岂不是变成了单线程？
 - 一个请求对应一个AFHTTPRequestOperation实例对象（以下简称operation），
 - 每一个operation在初始化完成后都会被添加到一个NSOperationQueue中- 由这个NSOperationQueue来控制并发，系统会根据当前可用的核心数以及负载情况动态地调整最大的并发 operation 数量，我们也可以通过setMaxConcurrentoperationCount:方法来设置最大并发数。
 - 并发数并不等于所开辟的线程数。具体开辟几条线程由系统决定。
 - 也就是说此处执行operation是并发的、多线程的。

##### AFN3.0 为何不需要常驻线程?

> NSURLSession发起的请求，不再需要在当前线程进行代理方法的回调！可以指定回调的delegateQueue，这样我们就不用为了等待代理回调方法而苦苦保活线程了。
>


##### AFN2.0 `operationQueue`
> AF2.0的operationQueue是用来添加operation并进行并发请求的，不要设置为1。
##### AFN3.0 `operationQueue`
> AF3.0的operationQueue是用来接收NSURLSessionDelegate回调的，鉴于一些多线程数据访问的安全性考虑，设置了maxConcurrentOperationCount = 1来达到串行回调的效果。
```
self.operationQueue = [[NSOperationQueue alloc] init];
self.operationQueue.maxConcurrentOperationCount = 1;
self.session = [NSURLSession sessionWithConfiguration:self.sessionConfiguration delegate:self delegateQueue:self.operationQueue];
```
- 串行回调原因:
> 为了保证多线程环境下的数据安全,对self.mutableTaskDelegatesKeyedByTaskIdentifier 的访问进行了加锁处理，就算maxConcurrentOperationCount不设为1，当某个请求正在回调时，下一个请求还是得等待一直到上个请求获取完所要的资源后解锁，所以这边并发回调也是没有意义的。相反多task回调导致的多线程并发，还会导致性能的浪费。

```
- (AFURLSessionManagerTaskDelegate *)delegateForTask:(NSURLSessionTask *)task {
     NSParameterAssert(task);
     AFURLSessionManagerTaskDelegate *delegate = nil;
     [self.lock lock];
     //给所要访问的资源加锁，防止造成数据混乱
     delegate = self.mutableTaskDelegatesKeyedByTaskIdentifier[@(task.taskIdentifier)];
     [self.lock unlock];
     return delegate;
}
```


##### AFN3.0 弃用了NSURLConnection

- NSURLSession提升了网络连接速度

  > 我们知道iOS9以后，NSURLSession开始正式支持HTTP/2，也就意味着你的网络连接速度可以提升不少。更人性化更优秀的API设计，HTTP/2的支持，成为了开发者摒弃NSURLConnection的理由。
- Session采用了共享，而非每次都新建

  > 事实上在HTTP/0.9,HTTP/1.0协议的时代，每次HTTP的请求，都需要先经过TCP的连接，而后才能开始HTTP的请求。那么，为了让我们的请求更快，避免每次都产生一个TCP三次握手，成了一个优化的选项。于是在HTTP/1.1中共享的Session将会复用TCP的连接，这样就避免了每次操作都开启一个TCP三次握手的时间浪费，即加速了网络请求时间。
  
##### AFN进行数据请求会开辟多条线程吗？

```
self.operationQueue = [[NSOperationQueue alloc] init];
self.operationQueue.maxConcurrentOperationCount = 1;
self.session = [NSURLSession sessionWithConfiguration:self.sessionConfiguration delegate:self delegateQueue:self.operationQueue];
```
> 这里在operation队列中设置了最大并发数是1，让所有网络请求和等待网络响应都在同一条线程，而不是为每一条网络请求都新建一个线程，这样会节约很多资源。
> 
##### 使用AFN之后需要在回调后如果操作UI，需要回到主线程进行操作吗?

> 不需要，AFN内部已经进行了处理
```
dispatch_group_async(manager.completionGroup ?: url_session_manager_completion_group(), manager.completionQueue ?: dispatch_get_main_queue(), ^{
     if (self.completionHandler) {
         self.completionHandler(task.response, responseObject, error);
     }
     dispatch_async(dispatch_get_main_queue(), ^{
         [[NSNotificationCenter defaultCenter] postNotificationName:AFNetworkingTaskDidCompleteNotification object:task userInfo:userInfo];
     });
 });
 
```
## SDWebImage

#### 主要介绍

图片内存层面的相当是个缓存器，以`Key-Value`的形式存储图片。当内存不够的时候会清除所有缓存图片。用搜索文件系统的方式做管理，文件替换方式是以时间为单位，剔除时间大于一周的图片文件。当`SDWebImageManager`向`SDImageCache`要资源时，先搜索内存层面的数据，如果有直接返回，没有的话去访问磁盘，将图片从磁盘读取出来，然后做`Decoder`，将图片对象放到内存层面做备份，再返回调用层。

#### 主要构成
|            核心类            |                           负责模块                           |
| :--------------------------: | :----------------------------------------------------------: |
| SDWebImageManager  | 负责做任务或者分配任务的，所有的任务操作都会围绕着他去做操作。（调度各个类） |
| SDImageCache | 下载  |
| SDWebImageDownloader  | 缓存, 包括内存缓存和磁盘缓存  |
| SDWebImageCodersManager  | 图片解码 |

`SDWebImageManager`会结合`SDImageCache`和`SDWebImageDownloader`两个类，完成图片加载


##### 调度模块（SDWebImageManager）
> `SDWebImageManager` 负责调度其他核心类配合工作；也是与 SD 的调用者交互的一个类；`SDWebImageManager`将图片下载和图片缓存组合起来了。

- 例如`UIImageView+WebCache`中的 `- (nullable NSURL *)sd_setImageWithURL`方法
会直接来到 `SDWebImageManager` 的这个方法 :

  ```
  SDWebImageManager *manager = [SDWebImageManager sharedManager];
  [manager loadImageWithURL:urlString
                    options:0
                   progress:^(
                              NSInteger receivedSize,
                              NSInteger expectedSize,
                              NSURL * _Nullable targetURL)
  {

  } completed:^(UIImage * _Nullable image,
                NSData * _Nullable data,
                NSError * _Nullable error,
                SDImageCacheType cacheType,
                BOOL finished,
                NSURL * _Nullable imageURL) {

  }];
  ```
##### 缓存模块（SDImageCache）
> `SDWebImage` 的缓存包括内存缓存和磁盘缓存内存缓存和磁盘存储都交给 `SDImageCache` 这个类。

```
/** 用于管理内存缓存  */
@property (strong, nonatomic, nonnull) SDMemoryCache *memCache;

/** 磁盘路径， Library/Caches + 默认命名空间 @"default" */
@property (strong, nonatomic, nonnull) NSString *diskCachePath;

/** 磁盘缓存路径数组 */
@property (strong, nonatomic, nullable) NSMutableArray<NSString *> *customPaths;

/** 执行任务用的串行队列 */
@property (strong, nonatomic, nullable) dispatch_queue_t ioQueue;

/** 文件管理 */
@property (strong, nonatomic, nonnull) NSFileManager *fileManager;
```
##### 下载模块（SDWebImageDownloader和SDWebImageDownloaderOperation）

- `SDWebImageDownloader`
    - 下载模块由 `SDWebImageDownloader` 管理的，是以单例存在的；
    - 作用是创建 `NSURLSession`, 处理所有下载任务的回调并分发给对应的 `SDWebImageDownloaderOperation`
    - 对图片下载管理进行一些全局的配置,包含最大并行数、超时时间、operation之间的下载顺序、Https等属性进行配置、定义SDWebImageDownloaderOptions的枚举属性等
        - 设置最大并发数（6），下载时间默认时间（15秒），是否压缩图片和operation之间的下载顺序等
        - 设置operation的请求头信息，负责生成每个图片的下载单位 SDWebImageDownloaderOperation 以及取消operation 等
        - 设置下载的策略SDWebImageDownloaderOptions。

- `SDWebImageDownloaderOperation`
  - `SDWebImageDownloaderOperation` 继承自 `NSOperation`, 是具体的图片下载单位；
  - 重写了 `NSOperation` 的 `start` 方法。
    - 当任务添加到 NSOperationQueue 后会执行该方法，启动下载任务。
    - start 方法执行后, 下载任务开启；但是下载回调由 SDWebImageDownloader 接收, 然后分发给对应的 SDWebImageDownloaderOperation。
    - 图片下载结束并解码后回调；下载任务就完成了。
  - 使用 SDWebImageDownloader 的 NSURLSession 创建NSURLSessionTask 发起图片下载；支持下载取消和后台下载，在下载中及时汇报下载进度; 在下载成功后，对图片进行解码，缩放和压缩等操作。


##### 解码模块（SDWebImageCodersManager）

- **图片为什么要解码**
  - `JPEG` 和 `PNG` 图片都是一种压缩的位图格式；
  - `PNG` 图片是无损压缩，并且支持 `alpha` 通道
  - `JPEG` 图片则是有损压缩，可以指定 0-100% 的压缩比
  - 因此，在将磁盘中的图片渲染到屏幕之前必须先要得到图片的原始像素数据才能执行后续的绘制操作

- **图片解码的好处**
  - 使用`UIImage` 或 `CGImageSource` 的那几个方法创建图片时图片数据并不会立刻解码；
  - 当图片设置到 `UIImageView` 或者 `CALayer.contents `中去并且 `CALayer` 被提交到 `GPU` 前`CGImage` 中的数据才会得到解码；但是这一步是发生在主线程的，这样就会产生性能问题。
  - 解决方案是在子线程提前对图片进行强制解码；而强制解码的原理就是对图片进行重新绘制，得到一张新的解码后的位图
将把图片解码这个默认在主线程执行,耗损CPU的行为,放在了后台线程
  - 只需要在使用的时候,直接`setImage`,不会有太大的`CPU`消耗，这只是对图片优化的其中一种方式。在图片从下载到显示的过程中有很多个步骤可以优化:[IOS异步图片加载与常用的优化](https://link.jianshu.com/?t=https://segmentfault.com/a/1190000002776279)


#### 相关面试问题

##### `SDWebImage`如何保证`UI`操作放在主线程中执行？

> 通过判断是否在**主线程执行改为判断是否由主队列上调度**。

- 由于主队列是一个串行队列，无论任务是异步同步都不会开辟新线程，所以当前队列是主队列等价于当前在主线程上执行。
- 可以这样说，**在主队列调度的任务肯定在主线程执行，而在主线程执行的任务不一定是由主队列调度的。**
 

##### `SDWebImage`的最大并发数和超时时长?

> `_downloadQueue.maxConcurrentOperationCount = 6;` //最大并发数 6
> `_downloadTimeout = 15.0;` //超时时长 15秒

##### `SDWebImage`的`Memory`缓存和`Disk`缓存是用什么实现的？

- `Memory`缓存使用`SDMemoryCache`
  - `SDMemoryCache`类继承自`NSCache (NSMapTable)`
  - `SDWebImage`还专门实现了一个叫做 `AutoPurgeCache` 的类 继承自 `NSCache` ，相比于普通的 `NSCache`，它提供了一个在内存紧张时候释放缓存的能力。
  - 自动删除机制：当系统内存紧张时，`NSCache` 会自动删除一些缓存对象
  - 线程安全：从不同线程中对同一个 `NSCache` 对象进行增删改查时，不需要加锁，不同于 `NSMutableDictionary`、`NSCache`存储对象时不会对 `key` 进行 `copy` 操作。
  - `SDImageCache` 的磁盘缓存是通过异步操作 
 
- `Disk`缓存使用`NSFileManager` 
  - `NSFileManager` 存储缓存文件到沙盒来实现的。

##### 读取Memory和Disk的时候如何保证线程安全？

- 读取`Memory`
    -  `NScache`是线程安全的，在多线程操作中，不需要对`Cache`加锁。
    - 读取缓存的时候是在主线程进行。由于使用`NSCache`进行存储、所以不需要担心单个`value`对象的线程安全。

- 读取`Disk`
    > 创建了一个名为 **IO的串行队列**，所有`Disk`操作都在此队列中，逐个执行！！
  - 判断当前是否是`IOQueue` (原理：`SDWebImage` 如何保证`UI`操作放在主线程中执行？)
  - 在主要存储函数中，**dispatch_async(self.ioQueue, ^{})**
  - 真正的磁盘缓存是在另一个IO专属线程中的一个串行队列下进行的。
  - 如果你搜索self.ioQueue还能发现、不只是读取磁盘内容。
  - 包括删除、写入等所有磁盘内容都是在这个IO线程进行、以保证线程安全。
  - 但计算大小、获取文件总数等操作。则是在主线程进行。（**看下面代码**）
   - 我们可以看见，不会创建新线程并且一切操作会顺序执行。你可能会疑惑：为什么同样都是在主线程执行，这样没有死锁。其实这个和线程没有关系，和队列有关系，只要不放在主队列就不会阻塞主队列上的操作(各种系统的UI方法)，这个操作只是选择了合适的时机在主线程上跑了一下而已。

##### SDWebImage 缓存图片的名称如何避免重名?

> 对『绝对路径』进行MD5
  - 如果单纯使用文件名保存，重名的几率很高！
  - 使用 `MD5` 的散列函数，对完整的 `URL` 进行 `md5`，结果是一个 32 个字符长度的字符串！

##### `SDWebImage Disk`缓存时长？
> 时长：默认为一周

##### `SDWebImage Disk`清理操作时间点？

> 分别在『应用被杀死时』和 『应用进入后台时』进行清理操作

```
[[NSNotificationCenter defaultCenter] addObserver:self selector:@selector(deleteOldFiles) name:UIApplicationWillTerminateNotification object:nil];
[[NSNotificationCenter defaultCenter] addObserver:self selector:@selector(backgroundDeleteOldFiles) name:UIApplicationDidEnterBackgroundNotification object:nil];
//清理磁盘的方法
- (void)deleteOldFilesWithCompletionBlock:(nullable SDWebImageNoParamsBlock)completionBlock;
```

- 当应用进入后台时，会涉及到『**Long-Running Task**』(向 iOS 借点时间)
- 正常程序在进入后台后、虽然可以继续执行任务。但是在时间很短内就会被挂起待机。
- Long-Running可以让系统为app再多分配一些时间来处理一些耗时任务。

 ```
- (void)backgroundDeleteOldFiles {
    Class UIApplicationClass = NSClassFromString(@"UIApplication");
    if(!UIApplicationClass || ![UIApplicationClass respondsToSelector:@selector(sharedApplication)]) {
        return;
    }
    UIApplication *application = [UIApplication performSelector:@selector(sharedApplication)];
    // 后台任务标识--注册一个后台任务
    __block UIBackgroundTaskIdentifier bgTask = [application beginBackgroundTaskWithExpirationHandler:^{
        [application endBackgroundTask:bgTask];
        bgTask = UIBackgroundTaskInvalid;
    }];
    [self deleteOldFilesWithCompletionBlock:^{
        //结束后台任务
        [application endBackgroundTask:bgTask];
        bgTask = UIBackgroundTaskInvalid;
    }];
}
```

##### `SDWebImage Disk`缓存清理规则?

> 清理缓存的规则分两步进行: 第一步先清除掉过期的缓存文件。 如果清除掉过期的缓存之后，空间还不够。 那么就继续按文件时间从早到晚排序，先清除最早的缓存文件，直到剩余空间达到要求。
- `SDWebImage` 通过两个属性来控制哪些缓存过期及剩余空间

```objective-c
@interface SDImageCacheConfig : NSObject

 /**
* The maximum length of time to keep an image in the cache, in seconds
*/
@property (assign, nonatomic) NSInteger maxCacheAge;

/**
 * The maximum size of the cache, in bytes.
 */
@property (assign, nonatomic) NSUInteger maxCacheSize;
```

##### `maxCacheAge` 和 `maxCacheSize` 有默认值吗？
- `maxCacheAge` 在上述已经说过了，是有默认值的 **1week**，单位秒。
- `maxCacheSize` 翻了一遍 SDWebImage 的代码，并没有对 maxCacheSize 设置默认值。 这就意味着 SDWebImage 在默认情况下不会对缓存空间设限制。可以这样设置：


```objective-c
[SDImageCache sharedImageCache].maxCacheSize = 1024 * 1024 * 50;    // 50M
//maxCacheSize 是以字节来表示的，我们上面的计算代表 50M 的最大缓存空间。 把这行代码写在你的 APP 启动的时候，这样 SDWebImage 在清理缓存的时候，就会清理多余的缓存文件了。
```


###### SDWebImage 的Memory警告是如何处理的！

> 利用通知中心观察
UIApplicationDidReceiveMemoryWarningNotification 接收到内存警告的通知执行 clearMemory 方法，清理内存缓存！
```objective-c
[[NSNotificationCenter defaultCenter] addObserver:self selector:@selector(clearMemory) name:UIApplicationDidReceiveMemoryWarningNotification object:nil];
```

##### `SDWebImage Disk`目录位于哪里？

> 缓存在沙盒目录下 `Library/Caches`
> 默认情况下，二级目录为 `~/Library/Caches/default/com.hackemist.SDWebImageCache.default`也可自定义文件名
```
- (instancetype)init {
    return [self initWithNamespace:@"default"];
}
- (instancetype)initWithNamespace:(nonnull NSString *)ns {
    NSString *path = [self makeDiskCachePath:ns];
    return [self initWithNamespace:ns diskCacheDirectory:path];
}
- (instancetype)initWithNamespace:(nonnull NSString *)ns diskCacheDirectory:(nonnull NSString *)directory {
    if ((self = [super init])) {
        NSString *fullNamespace = [@"com.hackemist.SDWebImageCache." stringByAppendingString:ns];
    }
}
```

##### `SDWebImage`是如何做到Url不变的情况下，更新图片内容的?

> 方法一：`在AppDelegate didFinishLaunching`的地方追加如下代码：
```
-(void)dealHeader{
    SDWebImageDownloader *imgDownloader = SDWebImageManager.sharedManager.imageDownloader;
    imgDownloader.headersFilter = ^NSDictionary *(NSURL *url, NSDictionary *headers) {
        NSFileManager *fm = [[NSFileManager alloc] init];
        NSString *imgKey = [SDWebImageManager.sharedManager cacheKeyForURL:url];
        NSString *imgPath = [SDWebImageManager.sharedManager.imageCache defaultCachePathForKey:imgKey];
        NSDictionary *fileAttr = [fm attributesOfItemAtPath:imgPath error:nil];
        NSMutableDictionary *mutableHeaders = [headers mutableCopy];
        NSDate *lastModifiedDate = nil;
        if (fileAttr.count > 0) {
            if (fileAttr.count > 0) {
                lastModifiedDate = (NSDate *)fileAttr[NSFileModificationDate];
            }
        }
        NSDateFormatter *formatter = [[NSDateFormatter alloc] init];
        formatter.timeZone = [NSTimeZone timeZoneWithAbbreviation:@"GMT"];
        formatter.locale = [[NSLocale alloc] initWithLocaleIdentifier:@"en_US"];
        formatter.dateFormat = @"EEE, dd MMM yyyy HH:mm:ss z";
        NSString *lastModifiedStr = [formatter stringFromDate:lastModifiedDate];
        lastModifiedStr = lastModifiedStr.length > 0 ? lastModifiedStr : @"";
        [mutableHeaders setValue:lastModifiedStr forKey:@"If-Modified-Since"];
        return mutableHeaders;
    };
}

```
>   然后，加载图片的地方以前怎么写还是怎么写，但别忘了Option是SDWebImageRefreshCached


```
NSURL *imgURL = [NSURL URLWithString:@"http://handy-img-storage.b0.upaiyun.com/3.jpg"];
[[self imageView] sd_setImageWithURL:imgURL placeholderImage:nil options:SDWebImageRefreshCached];
```

> - 方法二：在SDWebImageManager.m大约167行的


```
if (cachedImage && options & SDWebImageRefreshCached) {
    downloaderOptions &= ~SDWebImageDownloaderProgressiveDownload;
    downloaderOptions |= SDWebImageDownloaderIgnoreCachedResponse;
}
```
中间加上：
```
downloaderOptions &= ~SDWebImageDownloaderUseNSURLCache;
```
变成：
```
if (cachedImage && options & SDWebImageRefreshCached) {
    downloaderOptions &= ~SDWebImageDownloaderProgressiveDownload;
    downloaderOptions &= ~SDWebImageDownloaderUseNSURLCache;
    downloaderOptions |= SDWebImageDownloaderIgnoreCachedResponse;
}
```



##### `SDWebImage`加载图片的流程

- 入口`sd_setImageWithURL:placeholderImage:`会先把 `placeholderImage`显示，然后 `SDWebImageManager` 根据 `URL` 开始处理图片。(UIImageView+WebCache)
  - 由于分类中不能添加成员变量，所以runtime关联了sd_imageURL图片的url、sd_imageProgress下载进度
  -sd_cancelCurrentImageLoad方法取消当前下载
  - sd_imageIndicator设置当前加载动画，
  - sd_internalSetImageWithURL:内部通过SDWebImageManager调用加载图片过程并返回调用进度(UIImageView+WebCache)

- 进入 `SDWebImageManager`的 `loadImageWithURL: options: progress: completed:`，交给 `SDImageCache` 从缓存查找图片是否已经存在`queryCacheOperationForKey: options: done`；

  - 先从内存中取（imageFromMemoryCacheForKey:），如果在内存中取，就在当前线程中直接回调doneBlock；
  - 如果内存中没有，就开子线程从磁盘中取（diskImageDataBySearchingAllPathsForKey:），如果取到图片（ 从硬盘得到的是图片压缩的二进制数据，使用前需要先解码（decompressedImageWithImage:  data: options:），并同步保存到内存缓存中（ [**self**.memCache setObject:diskImage forKey:key cost:cost];）），就回调doneBlock

- 如果磁盘都没有找到图片，则通过`SDImageDownloader(异步下载器)`的`downloadImageWithURL: options: progress: completed:`进行图片下载。
  -  图片的下载过程是在`SDWebImageDownloader.m`中进行的，实质是通过`SDWebImageDownloaderOperation`(继承自`NSOperation`)对象，把该对象加入到`downloadQueue`里，然后在`start`方法里通过`NSURLSession`来下载图片。
  - `NSOperation`有两个方法：`main`和`start`，如果想使用同步，那么最简单方法的就是把逻辑写在`main()`中，使用异步，需要把逻辑写到`start()`中，然后加入到队列之中
    
    - 首先根据下载 URL 去取下载任务；如果下载任务不存在或者已完成, 就创建新的下载任务；
    - 创建一个 operation （createDownloaderOperationWithUrl）：网络请求的配置
    - 创建下载任务 SDWebImageDownloaderOperation 的时候, 传入了 self.session 也就是 NSURLSession；(self.session 的创建是在 SDWebImageDownloader 单例初始化的时候创建的)
    - SDWebImageDownloaderOperation 拿到这个 NSURLSession 创建 NSURLSessionTask 进行图片请求；
    - 也就是说 NSURLSession 的代理的是 SDWebImageDownloader；所以所有图片下载任务的代理回调都由 SDWebImageDownloader 来处理；SDWebImageDownloader 再把每个下载任务的回调分发给对应的 SDWebImageDownloaderOperation。
    - 把下载任务加入任务队列后执行下载任务；SDWebImageDownloadToken 用于取消任务。



- 图片下载完成后并解码后回调；下载任务就完成了，下载任务完成后，先存储到内存缓存
  再存储到磁盘中（缓存路径：用图片的下载链接生成 MD5 串, 作为图片缓存的路径）。
  
  
  

## 算法
#### 求和
###### 俩数之和

  ```
  class Solution:
      def twoSum(self, nums: List[int], target: int) -> List[int]:
          hashmap={}
          for ind,num in enumerate(nums):
              hashmap[num] = ind
          for i,num in enumerate(nums):
              j = hashmap.get(target - num)
              if j is not None and i!=j:
                  return [i,j]
  ```

###### 三数之和

  ```
  class Solution:
      def threeSum(self, nums):
          ans = []
          n = len(nums)
          nums.sort()
          for i in range(n):
              left = i + 1
              right = n - 1
              if nums[i] > 0:
                  break
              if i >= 1 and nums[i] == nums[i - 1]:
                  continue
              while left < right:
                  total = nums[i] + nums[left] + nums[right]
                  if total > 0:
                      right -= 1
                  elif total < 0:
                      left += 1
                  else:
                      ans.append([nums[i], nums[left], nums[right]])
                      while left != right and nums[left] == nums[left + 1]: left += 1
                      while left != right and nums[right] == nums[right - 1]: right -= 1
                      left += 1
                      right -= 1
          return ans
  ```

###### 四树之和

      ```python
        # 双指针法
      class Solution:
          def fourSum(self, nums: List[int], target: int) -> List[List[int]]:

              nums.sort()
              n = len(nums)
              res = []
              for i in range(n):
                  if i > 0 and nums[i] == nums[i - 1]: continue
                  for k in range(i+1, n):
                      if k > i + 1 and nums[k] == nums[k-1]: continue
                      p = k + 1
                      q = n - 1

                      while p < q:
                          if nums[i] + nums[k] + nums[p] + nums[q] > target: q -= 1
                          elif nums[i] + nums[k] + nums[p] + nums[q] < target: p += 1
                          else:
                              res.append([nums[i], nums[k], nums[p], nums[q]])
                              while p < q and nums[p] == nums[p + 1]: p += 1
                              while p < q and nums[q] == nums[q - 1]: q -= 1
                              p += 1
                              q -= 1
              return res

      # 哈希表法
      class Solution(object):
          def fourSum(self, nums, target):
              """
              :type nums: List[int]
              :type target: int
              :rtype: List[List[int]]
              """
              # use a dict to store value:showtimes
              hashmap = dict()
              for n in nums:
                  if n in hashmap:
                      hashmap[n] += 1
                  else: 
                      hashmap[n] = 1

              # good thing about using python is you can use set to drop duplicates.
              ans = set()
              for i in range(len(nums)):
                  for j in range(i + 1, len(nums)):
                      for k in range(j + 1, len(nums)):
                          val = target - (nums[i] + nums[j] + nums[k])
                          if val in hashmap:
                              # make sure no duplicates.
                              count = (nums[i] == val) + (nums[j] == val) + (nums[k] == val)
                              if hashmap[val] > count:
                                  ans.add(tuple(sorted([nums[i], nums[j], nums[k], val])))
                          else:
                              continue
              return ans
      ```


#### 数组
###### 二分查找

      ```python
      class Solution:
          def search(self, nums: List[int], target: int) -> int:
              left, right = 0, len(nums) - 1

              while left <= right:
                  middle = (left + right) // 2

                  if nums[middle] < target:
                      left = middle + 1
                  elif nums[middle] > target:
                      right = middle - 1
                  else:
                      return middle
              return -1
      ```

###### 移除元素

      ```python
      class Solution:
          """双指针法
          时间复杂度：O(n)
          空间复杂度：O(1)
          """

          @classmethod
          def removeElement(cls, nums: List[int], val: int) -> int:
              fast = slow = 0

              while fast < len(nums):

                  if nums[fast] != val:
                      nums[slow] = nums[fast]
                      slow += 1

                  # 当 fast 指针遇到要删除的元素时停止赋值
                  # slow 指针停止移动, fast 指针继续前进
                  fast += 1

              return slow
      ```

###### 数组平方

      ```python
      class Solution:
          """双指针法
          时间复杂度：O(n)
          """
          def sortedSquares(self, nums: List[int]) -> List[int]:
              n = len(nums)
              i,j,k = 0,n - 1,n - 1
              ans = [-1] * n
              while i <= j:
                  lm = nums[i] ** 2
                  rm = nums[j] ** 2
                  if lm > rm:
                      ans[k] = lm
                      i += 1
                  else:
                      ans[k] = rm
                      j -= 1
                  k -= 1
              return ans
      ```

###### 长度最小子数组

      ```python
      class Solution:
          """滑动窗口
          时间复杂度：O(n)
          """
          def minSubArrayLen(self, s: int, nums: List[int]) -> int:
              # 定义一个无限大的数
              res = float("inf")
              Sum = 0
              index = 0
              for i in range(len(nums)):
                  Sum += nums[i]
                  while Sum >= s:
                      res = min(res, i-index+1)
                      Sum -= nums[index]
                      index += 1
              return 0 if res==float("inf") else res
      ```

###### 螺旋矩阵

      ```python
      class Solution:

          def generateMatrix(self, n: int) -> List[List[int]]:
              # 初始化要填充的正方形
              matrix = [[0] * n for _ in range(n)]

              left, right, up, down = 0, n - 1, 0, n - 1
              number = 1  # 要填充的数字

              while left < right and up < down:

                  # 从左到右填充上边
                  for x in range(left, right):
                      matrix[up][x] = number
                      number += 1

                  # 从上到下填充右边
                  for y in range(up, down):
                      matrix[y][right] = number
                      number += 1

                  # 从右到左填充下边
                  for x in range(right, left, -1):
                      matrix[down][x] = number
                      number += 1

                  # 从下到上填充左边
                  for y in range(down, up, -1):
                      matrix[y][left] = number
                      number += 1

                  # 缩小要填充的范围
                  left += 1
                  right -= 1
                  up += 1
                  down -= 1

              # 如果阶数为奇数，额外填充一次中心
              if n % 2:
                  matrix[n // 2][n // 2] = number

              return matrix
      ```

#### 字符串
###### 翻转字符串1

      ```python
      class Solution:
          def reverseString(self, s: List[str]) -> None:
              """
              Do not return anything, modify s in-place instead.
              """
              left, right = 0, len(s) - 1

              # 该方法已经不需要判断奇偶数，经测试后时间空间复杂度比用 for i in range(right//2)更低
              # 推荐该写法，更加通俗易懂
              while left < right:
                  s[left], s[right] = s[right], s[left]
                  left += 1
                  right -= 1
      ```

###### 翻转字符串2

      ```python
      class Solution:
          def reverseStr(self, s: str, k: int) -> str:
              """
              1. 使用range(start, end, step)来确定需要调换的初始位置
              2. 对于字符串s = 'abc'，如果使用s[0:999] ===> 'abc'。字符串末尾如果超过最大长度，则会返回至字符串最后一个值，这个特性可以避免一些边界条件的处理。
              3. 用切片整体替换，而不是一个个替换.
              """
              def reverse_substring(text):
                  left, right = 0, len(text) - 1
                  while left < right:
                      text[left], text[right] = text[right], text[left]
                      left += 1
                      right -= 1
                  return text

              res = list(s)

              for cur in range(0, len(s), 2 * k):
                  res[cur: cur + k] = reverse_substring(res[cur: cur + k])

              return ''.join(res)
      ```

###### 替换空格

      ```python
      # 时间 O(n) 空间O(1)

      class Solution:
          def replaceSpace(self, s: str) -> str:
              counter = s.count(' ')

              res = list(s)
              # 每碰到一个空格就多拓展两个格子，1 + 2 = 3个位置存’%20‘
              res.extend([' '] * counter * 2)

              # 原始字符串的末尾，拓展后的末尾
              left, right = len(s) - 1, len(res) - 1

              while left >= 0:
                  if res[left] != ' ':
                      res[right] = res[left]
                      right -= 1
                  else:
                      # [right - 2, right), 左闭右开
                      res[right - 2: right + 1] = '%20'
                      right -= 3
                  left -= 1
              return ''.join(res)
      ```

###### 翻转单词

      ```python
      class Solution:
        #1.去除多余的空格
              def trim_spaces(self,s):     
                  n=len(s)
                  left=0
                  right=n-1

                  while left<=right and s[left]==' ':       #去除开头的空格
                      left+=1
                  while left<=right and s[right]==' ':        #去除结尾的空格
                      right=right-1
                  tmp=[]
                  while left<=right:                                    #去除单词中间多余的空格
                      if s[left]!=' ':
                          tmp.append(s[left])
                      elif tmp[-1]!=' ':                                  #当前位置是空格，但是相邻的上一个位置不是空格，则该空格是合理的
                          tmp.append(s[left])
                      left+=1
                  return tmp
      #2.翻转字符数组
              def reverse_string(self,nums,left,right):
                  while left<right:
                      nums[left], nums[right]=nums[right],nums[left]
                      left+=1
                      right-=1
                  return None
      #3.翻转每个单词
              def reverse_each_word(self, nums):
                  start=0
                  end=0
                  n=len(nums)
                  while start<n:
                      while end<n and nums[end]!=' ':
                          end+=1
                      self.reverse_string(nums,start,end-1)
                      start=end+1
                      end+=1
                  return None

      #4.翻转字符串里的单词
              def reverseWords(self, s): #测试用例："the sky is blue"
                  l = self.trim_spaces(s)                     #输出：['t', 'h', 'e', ' ', 's', 'k', 'y', ' ', 'i', 's', ' ', 'b', 'l', 'u', 'e'
                  self.reverse_string( l,  0, len(l) - 1)   #输出：['e', 'u', 'l', 'b', ' ', 's', 'i', ' ', 'y', 'k', 's', ' ', 'e', 'h', 't']
                  self.reverse_each_word(l)               #输出：['b', 'l', 'u', 'e', ' ', 'i', 's', ' ', 's', 'k', 'y', ' ', 't', 'h', 'e']
                  return ''.join(l)                                 #输出：blue is sky the
      ```

###### 左旋转字符串

      ```python
      # 方法一：可以使用切片方法
      class Solution:
          def reverseLeftWords(self, s: str, n: int) -> str:
              return s[n:] + s[0:n]
      # 方法二：也可以使用上文描述的方法，有些面试中不允许使用切片，那就使用上文作者提到的方法
      class Solution:
          def reverseLeftWords(self, s: str, n: int) -> str:
              s = list(s)
              s[0:n] = list(reversed(s[0:n]))
              s[n:] = list(reversed(s[n:]))
              s.reverse()

              return "".join(s)
      # 方法三：如果连reversed也不让使用，那么自己手写一个
      class Solution:
          def reverseLeftWords(self, s: str, n: int) -> str:
              def reverse_sub(lst, left, right):
                  while left < right:
                      lst[left], lst[right] = lst[right], lst[left]
                      left += 1
                      right -= 1

              res = list(s)
              end = len(res) - 1
              reverse_sub(res, 0, n - 1)
              reverse_sub(res, n, end)
              reverse_sub(res, 0, end)
              return ''.join(res)

      # 同方法二
      # 时间复杂度：O(n)
      # 空间复杂度：O(n)，python的string为不可变，需要开辟同样大小的list空间来修改

      #方法四：考虑不能用切片的情况下，利用模+下标实现
      class Solution:
          def reverseLeftWords(self, s: str, n: int) -> str:
              new_s = ''
              for i in range(len(s)):
                  j = (i+n)%len(s)
                  new_s = new_s + s[j]
              return new_s
      ```

###### KMP

      ```python
      #时间 O(n+m)
      // 方法一
      class Solution:
          def strStr(self, haystack: str, needle: str) -> int:
              a=len(needle)
              b=len(haystack)
              if a==0:
                  return 0
              next=self.getnext(a,needle)
              p=-1
              for j in range(b):
                  while p>=0 and needle[p+1]!=haystack[j]:
                      p=next[p]
                  if needle[p+1]==haystack[j]:
                      p+=1
                  if p==a-1:
                      return j-a+1
              return -1

          def getnext(self,a,needle):
              next=['' for i in range(a)]
              k=-1
              next[0]=k
              for i in range(1,len(needle)):
                  while (k>-1 and needle[k+1]!=needle[i]):
                      k=next[k]
                  if needle[k+1]==needle[i]:
                      k+=1
                  next[i]=k
              return next
      // 方法二
      class Solution:
          def strStr(self, haystack: str, needle: str) -> int:
              a=len(needle)
              b=len(haystack)
              if a==0:
                  return 0
              i=j=0
              next=self.getnext(a,needle)
              while(i<b and j<a):
                  if j==-1 or needle[j]==haystack[i]:
                      i+=1
                      j+=1
                  else:
                      j=next[j]
              if j==a:
                  return i-j
              else:
                  return -1

          def getnext(self,a,needle):
              next=['' for i in range(a)]
              j,k=0,-1
              next[0]=k
              while(j<a-1):
                  if k==-1 or needle[k]==needle[j]:
                      k+=1
                      j+=1
                      next[j]=k
                  else:
                      k=next[k]
              return next
      ```

###### 重复子字符串

      ```python
      class Solution:
          def repeatedSubstringPattern(self, s: str) -> bool:  
              if len(s) == 0:
                  return False
              nxt = [0] * len(s)
              self.getNext(nxt, s)
              if nxt[-1] != -1 and len(s) % (len(s) - (nxt[-1] + 1)) == 0:
                  return True
              return False

          def getNext(self, nxt, s):
              nxt[0] = -1
              j = -1
              for i in range(1, len(s)):
                  while j >= 0 and s[i] != s[j+1]:
                      j = nxt[j]
                  if s[i] == s[j+1]:
                      j += 1
                  nxt[i] = j
              return nxt

      class Solution:
          def repeatedSubstringPattern(self, s: str) -> bool:  
              if len(s) == 0:
                  return False
              nxt = [0] * len(s)
              self.getNext(nxt, s)
              if nxt[-1] != 0 and len(s) % (len(s) - nxt[-1]) == 0:
                  return True
              return False

          def getNext(self, nxt, s):
              nxt[0] = 0
              j = 0
              for i in range(1, len(s)):
                  while j > 0 and s[i] != s[j]:
                      j = nxt[j - 1]
                  if s[i] == s[j]:
                      j += 1
                  nxt[i] = j
              return nxt
      ```

#### 链表
###### 移除链表元素

      ```python
      # Definition for singly-linked list.
      # class ListNode:
      #     def __init__(self, val=0, next=None):
      #         self.val = val
      #         self.next = next

      #头插法 t0(n),s0(1)
      class Solution:
          def removeElements(self, head: ListNode, val: int) -> ListNode:
              dummy_head = ListNode(next=head) #添加一个虚拟节点
              cur = dummy_head
              while(cur.next!=None):
                  if(cur.next.val == val):
                      cur.next = cur.next.next #删除cur.next节点
                  else:
                      cur = cur.next
              return dummy_head.next
      ```

###### 翻转链表1

      ```python
      #双指针 迭代
      # Definition for singly-linked list.
      # class ListNode:
      #     def __init__(self, val=0, next=None):
      #         self.val = val
      #         self.next = next
      class Solution:
          def reverseList(self, head: ListNode) -> ListNode:
              cur = head   
              pre = None
              while(cur!=None):
                  temp = cur.next # 保存一下 cur的下一个节点，因为接下来要改变cur->next
                  cur.next = pre #反转
                  #更新pre、cur指针
                  pre = cur
                  cur = temp
              return pre

      # 递归
      # Definition for singly-linked list.
      # class ListNode:
      #     def __init__(self, val=0, next=None):
      #         self.val = val
      #         self.next = next
      class Solution:
          def reverseList(self, head: ListNode) -> ListNode:

              def reverse(pre,cur):
                  if not cur:
                      return pre

                  tmp = cur.next
                  cur.next = pre

                  return reverse(cur,tmp)

              return reverse(None,head)
      ```

###### 翻转链表2

      ```python
      # Definition for singly-linked list.
      # class ListNode:
      #     def __init__(self, val=0, next=None):
      #         self.val = val
      #         self.next = next

      # 时间 O(n) 空间O(1)
      class Solution:
          def swapPairs(self, head: ListNode) -> ListNode:
              res = ListNode(next=head)
              pre = res

              # 必须有pre的下一个和下下个才能交换，否则说明已经交换结束了
              while pre.next and pre.next.next:
                  cur = pre.next
                  post = pre.next.next

                  # pre，cur，post对应最左，中间的，最右边的节点
                  cur.next = post.next
                  post.next = cur
                  pre.next = post

                  pre = pre.next.next
              return res.next
      ```

###### 删除倒数N节点

      ```python
      # Definition for singly-linked list.
      # class ListNode:
      #     def __init__(self, val=0, next=None):
      #         self.val = val
      #         self.next = next
      class Solution:
          def removeNthFromEnd(self, head: ListNode, n: int) -> ListNode:
              head_dummy = ListNode()
              head_dummy.next = head

              slow, fast = head_dummy, head_dummy
              while(n!=0): #fast先往前走n步
                  fast = fast.next
                  n -= 1
              while(fast.next!=None):
                  slow = slow.next
                  fast = fast.next
              #fast 走到结尾后，slow的下一个节点为倒数第N个节点
              slow.next = slow.next.next #删除
              return head_dummy.next
      ```

###### 链表相交

      ```python
      # Definition for singly-linked list.
      # class ListNode:
      #     def __init__(self, x):
      #         self.val = x
      #         self.next = None

      class Solution:
          def getIntersectionNode(self, headA: ListNode, headB: ListNode) -> ListNode:
              """
              根据快慢法则，走的快的一定会追上走得慢的。
              在这道题里，有的链表短，他走完了就去走另一条链表，我们可以理解为走的快的指针。

              那么，只要其中一个链表走完了，就去走另一条链表的路。如果有交点，他们最终一定会在同一个
              位置相遇
              """
              cur_a, cur_b = headA, headB     # 用两个指针代替a和b


              while cur_a != cur_b:
                  cur_a = cur_a.next if cur_a else headB      # 如果a走完了，那么就切换到b走
                  cur_b = cur_b.next if cur_b else headA      # 同理，b走完了就切换到a

              return cur_a
      ```

###### 环入口

      ```python
      class Solution:
          def detectCycle(self, head: ListNode) -> ListNode:
              slow, fast = head, head
              while fast and fast.next:
                  slow = slow.next
                  fast = fast.next.next
                  # 如果相遇
                  if slow == fast:
                      p = head
                      q = slow
                      while p!=q:
                          p = p.next
                          q = q.next
                      #你也可以return q
                      return p

              return None
      ```

#### 二叉树
###### 递归遍历

      ```python
      # 前序遍历-递归-LC144_二叉树的前序遍历
      class Solution:
          def preorderTraversal(self, root: TreeNode) -> List[int]:
              # 保存结果
              result = []

              def traversal(root: TreeNode):
                  if root == None:
                      return
                  result.append(root.val) # 前序
                  traversal(root.left)    # 左
                  traversal(root.right)   # 右

              traversal(root)
              return result

      # 中序遍历-递归-LC94_二叉树的中序遍历
      class Solution:
          def inorderTraversal(self, root: TreeNode) -> List[int]:
              result = []

              def traversal(root: TreeNode):
                  if root == None:
                      return
                  traversal(root.left)    # 左
                  result.append(root.val) # 中序
                  traversal(root.right)   # 右

              traversal(root)
              return result

      # 后序遍历-递归-LC145_二叉树的后序遍历
      class Solution:
          def postorderTraversal(self, root: TreeNode) -> List[int]:
              result = []

              def traversal(root: TreeNode):
                  if root == None:
                      return
                  traversal(root.left)    # 左
                  traversal(root.right)   # 右
                  result.append(root.val) # 后序

              traversal(root)
              return result
      ```

###### 迭代遍历

      ```python
      # 前序遍历-迭代-LC144_二叉树的前序遍历
      class Solution:
          def preorderTraversal(self, root: TreeNode) -> List[int]:
              # 根结点为空则返回空列表
              if not root:
                  return []
              stack = [root]
              result = []
              while stack:
                  node = stack.pop()
                  # 中结点先处理
                  result.append(node.val)
                  # 右孩子先入栈
                  if node.right:
                      stack.append(node.right)
                  # 左孩子后入栈
                  if node.left:
                      stack.append(node.left)
              return result

      # 中序遍历-迭代-LC94_二叉树的中序遍历
      class Solution:
          def inorderTraversal(self, root: TreeNode) -> List[int]:
              if not root:
                  return []
              stack = []  # 不能提前将root结点加入stack中
              result = []
              cur = root
              while cur or stack:
                  # 先迭代访问最底层的左子树结点
                  if cur:     
                      stack.append(cur)
                      cur = cur.left		
                  # 到达最左结点后处理栈顶结点    
                  else:		
                      cur = stack.pop()
                      result.append(cur.val)
                      # 取栈顶元素右结点
                      cur = cur.right	
              return result

      # 后序遍历-迭代-LC145_二叉树的后序遍历
      class Solution:
          def postorderTraversal(self, root: TreeNode) -> List[int]:
              if not root:
                  return []
              stack = [root]
              result = []
              while stack:
                  node = stack.pop()
                  # 中结点先处理
                  result.append(node.val)
                  # 左孩子先入栈
                  if node.left:
                      stack.append(node.left)
                  # 右孩子后入栈
                  if node.right:
                      stack.append(node.right)
              # 将最终的数组翻转
              return result[::-1]
      ```

###### 层序遍历1

      ```python
      class Solution:
          def levelOrder(self, root: TreeNode) -> List[List[int]]:
              if not root:
                  return []

              queue = [root]
              out_list = []

              while queue:
                  length = len(queue)  
                  in_list = []
                  for _ in range(length):
                      curnode = queue.pop(0)  # （默认移除列表最后一个元素）这里需要移除队列最头上的那个
                      in_list.append(curnode.val)
                      if curnode.left: queue.append(curnode.left)
                      if curnode.right: queue.append(curnode.right)
                  out_list.append(in_list)

              return out_list
      ```

###### 层序遍历2

      ```python
      class Solution:
          def levelOrderBottom(self, root: TreeNode) -> List[List[int]]:
              if not root:
                  return []
              quene = [root]
              out_list = []

              while quene:
                  in_list = []
                  for _ in range(len(quene)):
                      node = quene.pop(0)
                      in_list.append(node.val)
                      if node.left:
                          quene.append(node.left)
                      if node.right:
                          quene.append(node.right)

                  out_list.append(in_list)

              out_list.reverse()
              return out_list

      # 执行用时：36 ms, 在所有 Python3 提交中击败了92.00%的用户
      # 内存消耗：15.2 MB, 在所有 Python3 提交中击败了63.76%的用户
      ```

###### 二叉树右视图

      ```python
      class Solution:
          def rightSideView(self, root: TreeNode) -> List[int]:
              if not root:
                  return []

              # deque来自collections模块，不在力扣平台时，需要手动写入
              # 'from collections import deque' 导入
              # deque相比list的好处是，list的pop(0)是O(n)复杂度，deque的popleft()是O(1)复杂度

              quene = deque([root])
              out_list = []

              while quene:
                  # 每次都取最后一个node就可以了
                  node = quene[-1]
                  out_list.append(node.val)

                  # 执行这个遍历的目的是获取下一层所有的node
                  for _ in range(len(quene)):
                      node = quene.popleft()
                      if node.left:
                          quene.append(node.left)
                      if node.right:
                          quene.append(node.right)

              return out_list

      # 执行用时：36 ms, 在所有 Python3 提交中击败了89.47%的用户
      # 内存消耗：14.6 MB, 在所有 Python3 提交中击败了96.65%的用户
      ```

###### 二叉树层平均值

      ```python
      class Solution:
          def averageOfLevels(self, root: TreeNode) -> List[float]:
              if not root:
                  return []

              quene = deque([root])
              out_list = []

              while quene:
                  in_list = []

                  for _ in range(len(quene)):
                      node = quene.popleft()
                      in_list.append(node.val)
                      if node.left:
                          quene.append(node.left)
                      if node.right:
                          quene.append(node.right)

                  out_list.append(in_list)

              out_list = map(lambda x: sum(x) / len(x), out_list)

              return out_list

      # 执行用时：56 ms, 在所有 Python3 提交中击败了81.48%的用户
      # 内存消耗：17 MB, 在所有 Python3 提交中击败了89.68%的用户
      ```

###### N叉树层序遍历

      ```python
      class Solution:
          def levelOrder(self, root: 'Node') -> List[List[int]]:
              if not root:
                  return []

              quene = deque([root])
              out_list = []

              while quene:
                  in_list = []

                  for _ in range(len(quene)):
                      node = quene.popleft()
                      in_list.append(node.val)
                      if node.children:
                          # 这个地方要用extend而不是append，我们看下面的例子：
                          # In [18]: alist=[]
                          # In [19]: alist.append([1,2,3])
                          # In [20]: alist
                          # Out[20]: [[1, 2, 3]]
                          # In [21]: alist.extend([4,5,6])
                          # In [22]: alist
                          # Out[22]: [[1, 2, 3], 4, 5, 6]
                          # 可以看到extend对要添加的list进行了一个解包操作
                          # print(root.children)，可以得到children是一个包含
                          # 孩子节点地址的list，我们使用for遍历quene的时候，
                          # 希望quene是一个单层list，所以要用extend
                          # 使用extend的情况，如果print(quene),结果是
                          # deque([<__main__.Node object at 0x7f60763ae0a0>])
                 # deque([<__main__.Node object at 0x7f607636e6d0>, <__main__.Node object at 0x7f607636e130>, <__main__.Node object at 0x7f607636e310>])
                # deque([<__main__.Node object at 0x7f607636e880>, <__main__.Node object at 0x7f607636ef10>])
                # 可以看到是单层list
                          # 如果使用append，print(quene)的结果是
                          # deque([<__main__.Node object at 0x7f18907530a0>])
                # deque([[<__main__.Node object at 0x7f18907136d0>, <__main__.Node object at 0x7f1890713130>, <__main__.Node object at 0x7f1890713310>]])
                # 可以看到是两层list，这样for的遍历就会报错

                          quene.extend(node.children)

                  out_list.append(in_list)

              return out_list

      # 执行用时：60 ms, 在所有 Python3 提交中击败了76.99%的用户
      # 内存消耗：16.5 MB, 在所有 Python3 提交中击败了89.19%的用户
      ```

###### 每个树找最大值

      ```python
      class Solution:
          def largestValues(self, root: TreeNode) -> List[int]:
              if root is None:
                  return []
              queue = [root]
              out_list = []
              while queue:
                  length = len(queue)
                  in_list = []
                  for _ in range(length):
                      curnode = queue.pop(0)
                      in_list.append(curnode.val)
                      if curnode.left: queue.append(curnode.left)
                      if curnode.right: queue.append(curnode.right)
                  out_list.append(max(in_list))
              return out_list
      ```

###### 填充每个节点的下一个右侧节点指针1

      ```python
      # 层序遍历解法
      class Solution:
          def connect(self, root: 'Node') -> 'Node':
              if not root:
                  return None
              queue = [root]
              while queue:
                  n = len(queue)
                  for i in range(n):
                      node = queue.pop(0)
                      if node.left:
                          queue.append(node.left)
                      if node.right:
                          queue.append(node.right)
                      if i == n - 1:
                          break
                      node.next = queue[0]
              return root

      # 链表解法
      class Solution:
          def connect(self, root: 'Node') -> 'Node':
              first = root
              while first:
                  cur = first
                  while cur:  # 遍历每一层的节点
                      if cur.left: cur.left.next = cur.right  # 找左节点的next
                      if cur.right and cur.next: cur.right.next = cur.next.left  # 找右节点的next
                      cur = cur.next # cur同层移动到下一节点
                  first = first.left  # 从本层扩展到下一层
              return root
      ```

###### 填充每个节点的下一个右侧节点指针2

      ```python
      # 层序遍历解法
      class Solution:
          def connect(self, root: 'Node') -> 'Node':
              if not root:
                  return None
              queue = [root]
              while queue:  # 遍历每一层
                  length = len(queue)
                  tail = None # 每一层维护一个尾节点
                  for i in range(length): # 遍历当前层
                      curnode = queue.pop(0)
                      if tail:
                          tail.next = curnode # 让尾节点指向当前节点
                      tail = curnode # 让当前节点成为尾节点
                      if curnode.left : queue.append(curnode.left)
                      if curnode.right: queue.append(curnode.right)
              return root

      # 链表解法
      class Solution:
          def connect(self, root: 'Node') -> 'Node':
              if not root:
                  return None
              first = root
              while first:  # 遍历每一层
                  dummyHead = Node(None)  # 为下一行创建一个虚拟头节点，相当于下一行所有节点链表的头结点(每一层都会创建)；
                  tail = dummyHead  # 为下一行维护一个尾节点指针（初始化是虚拟节点）
                  cur = first
                  while cur:  # 遍历当前层的节点
                      if cur.left:  # 链接下一行的节点
                          tail.next = cur.left
                          tail = tail.next
                      if cur.right:
                          tail.next = cur.right
                          tail = tail.next
                      cur = cur.next  # cur同层移动到下一节点
                  first = dummyHead.next  # 此处为换行操作，更新到下一行
              return root
      ```

###### 二叉树最大深度

      ```python
      class Solution:
          def maxDepth(self, root: TreeNode) -> int:
              if root == None:
                  return 0

              queue_ = [root]
              result = []
              while queue_:
                  length = len(queue_)
                  sub = []
                  for i in range(length):
                      cur = queue_.pop(0)
                      sub.append(cur.val)
                      #子节点入队列
                      if cur.left: queue_.append(cur.left)
                      if cur.right: queue_.append(cur.right)
                  result.append(sub)


              return len(result)
      ```

###### 二叉树最小深度

      ```python
      # Definition for a binary tree node.
      # class TreeNode:
      #     def __init__(self, val=0, left=None, right=None):
      #         self.val = val
      #         self.left = left
      #         self.right = right
      class Solution:
          def minDepth(self, root: TreeNode) -> int:
              if root == None:
                  return 0

              #根节点的深度为1
              queue_ = [(root,1)]
              while queue_:
                  cur, depth = queue_.pop(0)

                  if cur.left == None and cur.right == None:
                      return depth
                  #先左子节点，由于左子节点没有孩子，则就是这一层了
                  if cur.left:
                      queue_.append((cur.left,depth + 1))
                  if cur.right:
                      queue_.append((cur.right,depth + 1))

              return 0
      ```

###### 翻转二叉树

      ```python
      # 递归前序
      class Solution:
          def invertTree(self, root: TreeNode) -> TreeNode:
              if not root:
                  return None
              root.left, root.right = root.right, root.left #中
              self.invertTree(root.left) #左
              self.invertTree(root.right) #右
              return root

      # 迭代 深度优先
      class Solution:
          def invertTree(self, root: TreeNode) -> TreeNode:
              if not root:
                  return root
              st = []
              st.append(root)
              while st:
                  node = st.pop()
                  node.left, node.right = node.right, node.left #中
                  if node.right:
                      st.append(node.right) #右
                  if node.left:
                      st.append(node.left) #左
              return root

      # 迭代广度优先
      import collections
      class Solution:
          def invertTree(self, root: TreeNode) -> TreeNode:
              queue = collections.deque() #使用deque()
              if root:
                  queue.append(root)
              while queue:
                  size = len(queue)
                  for i in range(size):
                      node = queue.popleft()
                      node.left, node.right = node.right, node.left #节点处理
                      if node.left:
                          queue.append(node.left)
                      if node.right:
                          queue.append(node.right)
              return root
      ```

###### 对称二叉树

      ```python
      # 递归
      class Solution:
          def isSymmetric(self, root: TreeNode) -> bool:
              if not root:
                  return True
              return self.compare(root.left, root.right)

          def compare(self, left, right):
              #首先排除空节点的情况
              if left == None and right != None: return False
              elif left != None and right == None: return False
              elif left == None and right == None: return True
              #排除了空节点，再排除数值不相同的情况
              elif left.val != right.val: return False

              #此时就是：左右节点都不为空，且数值相同的情况
              #此时才做递归，做下一层的判断
              outside = self.compare(left.left, right.right) #左子树：左、 右子树：右
              inside = self.compare(left.right, right.left) #左子树：右、 右子树：左
              isSame = outside and inside #左子树：中、 右子树：中 （逻辑处理）
              return isSame

      # 迭代 使用队列
      import collections
      class Solution:
          def isSymmetric(self, root: TreeNode) -> bool:
              if not root:
                  return True
              queue = collections.deque()
              queue.append(root.left) #将左子树头结点加入队列
              queue.append(root.right) #将右子树头结点加入队列
              while queue: #接下来就要判断这这两个树是否相互翻转
                  leftNode = queue.popleft()
                  rightNode = queue.popleft()
                  if not leftNode and not rightNode: #左节点为空、右节点为空，此时说明是对称的
                      continue

                  #左右一个节点不为空，或者都不为空但数值不相同，返回false
                  if not leftNode or not rightNode or leftNode.val != rightNode.val:
                      return False
                  queue.append(leftNode.left) #加入左节点左孩子
                  queue.append(rightNode.right) #加入右节点右孩子
                  queue.append(leftNode.right) #加入左节点右孩子
                  queue.append(rightNode.left) #加入右节点左孩子
              return True

      # 迭代使用栈
      class Solution:
          def isSymmetric(self, root: TreeNode) -> bool:
              if not root:
                  return True
              st = [] #这里改成了栈
              st.append(root.left)
              st.append(root.right)
              while st:
                  leftNode = st.pop()
                  rightNode = st.pop()
                  if not leftNode and not rightNode:
                      continue
                  if not leftNode or not rightNode or leftNode.val != rightNode.val:
                      return False
                  st.append(leftNode.left)
                  st.append(rightNode.right)
                  st.append(leftNode.right)
                  st.append(rightNode.left)
              return True
      ```

###### 完全二叉树的节点个数

  ```python
  # 递归
  class Solution:
      def countNodes(self, root: TreeNode) -> int:
          return self.getNodesNum(root)

      def getNodesNum(self, cur):
          if not cur:
              return 0
          leftNum = self.getNodesNum(cur.left) #左
          rightNum = self.getNodesNum(cur.right) #右
          treeNum = leftNum + rightNum + 1 #中
          return treeNum
  # 迭代
  import collections
  class Solution:
      def countNodes(self, root: TreeNode) -> int:
          queue = collections.deque()
          if root:
              queue.append(root)
          result = 0
          while queue:
              size = len(queue)
              for i in range(size):
                  node = queue.popleft()
                  result += 1 #记录节点数量
                  if node.left:
                      queue.append(node.left)
                  if node.right:
                      queue.append(node.right)
          return result
  ```

###### 平衡二叉树

  ```python
  # 递归
  class Solution:
      def isBalanced(self, root: TreeNode) -> bool:
          return True if self.getDepth(root) != -1 else False

      #返回以该节点为根节点的二叉树的高度，如果不是二叉搜索树了则返回-1
      def getDepth(self, node):
          if not node:
              return 0
          leftDepth = self.getDepth(node.left)
          if leftDepth == -1: return -1 #说明左子树已经不是二叉平衡树
          rightDepth = self.getDepth(node.right)
          if rightDepth == -1: return -1 #说明右子树已经不是二叉平衡树
          return -1 if abs(leftDepth - rightDepth)>1 else 1 + max(leftDepth, rightDepth)

  # 迭代
  class Solution:
      def isBalanced(self, root: TreeNode) -> bool:
          st = []
          if not root:
              return True
          st.append(root)
          while st:
              node = st.pop() #中
              if abs(self.getDepth(node.left) - self.getDepth(node.right)) > 1:
                  return False
              if node.right:
                  st.append(node.right) #右（空节点不入栈）
              if node.left:
                  st.append(node.left) #左（空节点不入栈）
          return True

      def getDepth(self, cur):
          st = []
          if cur:
              st.append(cur)
          depth = 0
          result = 0
          while st:
              node = st.pop()
              if node:
                  st.append(node) #中
                  st.append(None)
                  depth += 1
                  if node.right: st.append(node.right) #右
                  if node.left: st.append(node.left) #左
              else:
                  node = st.pop()
                  depth -= 1
              result = max(result, depth)
          return result
  ```

###### 二叉树所有路径

  ```python
  class Solution:
      def binaryTreePaths(self, root: TreeNode) -> List[str]:
          path=[]
          res=[]
          def backtrace(root, path):
              if not root:return 
              path.append(root.val)
              if (not root.left)and (not root.right):
                 res.append(path[:])
              ways=[]
              if root.left:ways.append(root.left)
              if root.right:ways.append(root.right)
              for way in ways:
                  backtrace(way,path)
                  path.pop()
          backtrace(root,path)
          return ["->".join(list(map(str,i))) for i in res]
  ```

###### 左叶子之和

  ```python
  # 递归
  class Solution:
      def sumOfLeftLeaves(self, root: TreeNode) -> int:
          if not root: 
              return 0

          left_left_leaves_sum = self.sumOfLeftLeaves(root.left)  # 左
          right_left_leaves_sum = self.sumOfLeftLeaves(root.right) # 右

          cur_left_leaf_val = 0
          if root.left and not root.left.left and not root.left.right: 
              cur_left_leaf_val = root.left.val  # 中

          return cur_left_leaf_val + left_left_leaves_sum + right_left_leaves_sum

  # 迭代
  class Solution:
      def sumOfLeftLeaves(self, root: TreeNode) -> int:
          """
          Idea: Each time check current node's left node. 
                If current node don't have one, skip it. 
          """
          stack = []
          if root: 
              stack.append(root)
          res = 0

          while stack: 
              # 每次都把当前节点的左节点加进去. 
              cur_node = stack.pop()
              if cur_node.left and not cur_node.left.left and not cur_node.left.right: 
                  res += cur_node.left.val

              if cur_node.left: 
                  stack.append(cur_node.left)
              if cur_node.right: 
                  stack.append(cur_node.right)

          return res
  ```

###### 左下角

  ```python
  # 递归
  class Solution:
      def findBottomLeftValue(self, root: TreeNode) -> int:
          max_depth = -float("INF")
          leftmost_val = 0

          def __traverse(root, cur_depth): 
              nonlocal max_depth, leftmost_val
              if not root.left and not root.right: 
                  if cur_depth > max_depth: 
                      max_depth = cur_depth
                      leftmost_val = root.val  
              if root.left: 
                  cur_depth += 1
                  __traverse(root.left, cur_depth)
                  cur_depth -= 1
              if root.right: 
                  cur_depth += 1
                  __traverse(root.right, cur_depth)
                  cur_depth -= 1

          __traverse(root, 0)
          return leftmost_val
  # 迭代
  class Solution:
      def findBottomLeftValue(self, root: TreeNode) -> int:
          queue = deque()
          if root: 
              queue.append(root)
          result = 0
          while queue: 
              q_len = len(queue)
              for i in range(q_len): 
                  if i == 0: 
                      result = queue[i].val 
                  cur = queue.popleft()
                  if cur.left: 
                      queue.append(cur.left)
                  if cur.right: 
                      queue.append(cur.right)
          return result
  ```
###### 路径总和1

  ```python
  # 递归
  class solution:
      def haspathsum(self, root: treenode, targetsum: int) -> bool:
          def isornot(root, targetsum) -> bool:
              if (not root.left) and (not root.right) and targetsum == 0:
                  return true  # 遇到叶子节点，并且计数为0
              if (not root.left) and (not root.right):
                  return false  # 遇到叶子节点，计数不为0
              if root.left:
                  targetsum -= root.left.val  # 左节点
                  if isornot(root.left, targetsum): return true  # 递归，处理左节点
                  targetsum += root.left.val  # 回溯
              if root.right:
                  targetsum -= root.right.val  # 右节点
                  if isornot(root.right, targetsum): return true  # 递归，处理右节点
                  targetsum += root.right.val  # 回溯
              return false

          if root == none:
              return false  # 别忘记处理空treenode
          else:
              return isornot(root, targetsum - root.val)
  # 迭代
  class solution:
      def haspathsum(self, root: treenode, targetsum: int) -> bool:
          if not root: 
              return false

          stack = []  # [(当前节点，路径数值), ...]
          stack.append((root, root.val))

          while stack: 
              cur_node, path_sum = stack.pop()

              if not cur_node.left and not cur_node.right and path_sum == targetsum: 
                  return true

              if cur_node.right: 
                  stack.append((cur_node.right, path_sum + cur_node.right.val))    

              if cur_node.left: 
                  stack.append((cur_node.left, path_sum + cur_node.left.val))

          return false
  ```

###### 路径总和2

  ```python
  # 递归
  class solution:
      def pathsum(self, root: treenode, targetsum: int) -> list[list[int]]:

          def traversal(cur_node, remain): 
              if not cur_node.left and not cur_node.right and remain == 0: 
                  result.append(path[:])
                  return

              if not cur_node.left and not cur_node.right: return 

              if cur_node.left: 
                  path.append(cur_node.left.val)
                  remain -= cur_node.left.val
                  traversal(cur_node.left, remain)
                  path.pop()
                  remain += cur_node.left.val

              if cur_node.right: 
                  path.append(cur_node.right.val)
                  remain -= cur_node.right.val
                  traversal(cur_node.right, remain)
                  path.pop()
                  remain += cur_node.right.val

          result, path = [], []
          if not root: 
              return []
          path.append(root.val)
          traversal(root, targetsum - root.val)
          return result
  ```

###### 构造二叉树

  ```python
  # 前序+中序
  class Solution:
      def buildTree(self, preorder: List[int], inorder: List[int]) -> TreeNode:
          # 第一步: 特殊情况讨论: 树为空. 或者说是递归终止条件
          if not preorder: 
              return None

          # 第二步: 前序遍历的第一个就是当前的中间节点. 
          root_val = preorder[0]
          root = TreeNode(root_val)

          # 第三步: 找切割点. 
          separator_idx = inorder.index(root_val)

          # 第四步: 切割inorder数组. 得到inorder数组的左,右半边. 
          inorder_left = inorder[:separator_idx]
          inorder_right = inorder[separator_idx + 1:]

          # 第五步: 切割preorder数组. 得到preorder数组的左,右半边.
          # ⭐️ 重点1: 中序数组大小一定跟前序数组大小是相同的. 
          preorder_left = preorder[1:1 + len(inorder_left)]
          preorder_right = preorder[1 + len(inorder_left):]

          # 第六步: 递归
          root.left = self.buildTree(preorder_left, inorder_left)
          root.right = self.buildTree(preorder_right, inorder_right)

          return root

  # 中序+后序
  class Solution:
      def buildTree(self, inorder: List[int], postorder: List[int]) -> TreeNode:
          # 第一步: 特殊情况讨论: 树为空. (递归终止条件)
          if not postorder: 
              return None

          # 第二步: 后序遍历的最后一个就是当前的中间节点. 
          root_val = postorder[-1]
          root = TreeNode(root_val)

          # 第三步: 找切割点. 
          separator_idx = inorder.index(root_val)

          # 第四步: 切割inorder数组. 得到inorder数组的左,右半边. 
          inorder_left = inorder[:separator_idx]
          inorder_right = inorder[separator_idx + 1:]

          # 第五步: 切割postorder数组. 得到postorder数组的左,右半边.
          # ⭐️ 重点1: 中序数组大小一定跟后序数组大小是相同的. 
          postorder_left = postorder[:len(inorder_left)]
          postorder_right = postorder[len(inorder_left): len(postorder) - 1]

          # 第六步: 递归
          root.left = self.buildTree(inorder_left, postorder_left)
          root.right = self.buildTree(inorder_right, postorder_right)

          return root
  ```

###### 数组构造最大二叉树

  ```python
  //递归法
  class Solution:
      def constructMaximumBinaryTree(self, nums: List[int]) -> TreeNode:
          if not nums: return None   //终止条件
          root = TreeNode(max(nums))   //新建节点
          p = nums.index(root.val)   //找到最大值位置
          if p > 0: //保证有左子树
              root.left = self.constructMaximumBinaryTree(nums[:p])   //递归
          if p < len(nums): //保证有右子树
              root.right = self.constructMaximumBinaryTree(nums[p+1:])  //递归
          return root
  ```

###### 合并二叉树

  ```python
  # 递归 前序遍历
  # Definition for a binary tree node.
  # class TreeNode:
  #     def __init__(self, val=0, left=None, right=None):
  #         self.val = val
  #         self.left = left
  #         self.right = right
  class Solution:
      def mergeTrees(self, root1: TreeNode, root2: TreeNode) -> TreeNode:
          # 递归终止条件: 
          #  但凡有一个节点为空, 就立刻返回另外一个. 如果另外一个也为None就直接返回None. 
          if not root1: 
              return root2
          if not root2: 
              return root1
          # 上面的递归终止条件保证了代码执行到这里root1, root2都非空. 
          root1.val += root2.val # 中
          root1.left = self.mergeTrees(root1.left, root2.left) #左
          root1.right = self.mergeTrees(root1.right, root2.right) # 右

          return root1 # ⚠️ 注意: 本题我们重复使用了题目给出的节点而不是创建新节点. 节省时间, 空间.

  # 迭代
  class Solution:
      def mergeTrees(self, root1: TreeNode, root2: TreeNode) -> TreeNode:
          if not root1: 
              return root2
          if not root2: 
              return root1

          queue = deque()
          queue.append(root1)
          queue.append(root2)

          while queue: 
              node1 = queue.popleft()
              node2 = queue.popleft()
              # 更新queue
              # 只有两个节点都有左节点时, 再往queue里面放.
              if node1.left and node2.left: 
                  queue.append(node1.left)
                  queue.append(node2.left)
              # 只有两个节点都有右节点时, 再往queue里面放.
              if node1.right and node2.right: 
                  queue.append(node1.right)
                  queue.append(node2.right)

              # 更新当前节点. 同时改变当前节点的左右孩子. 
              node1.val += node2.val
              if not node1.left and node2.left: 
                  node1.left = node2.left
              if not node1.right and node2.right: 
                  node1.right = node2.right

          return root1
  ```


##Swift
### 修饰符
Swift 的内存管理机制与 Objective-C一样为 ARC（Automatic Reference Counting）。它的基本原理是，一个对象在没有任何强引用指向它时，其占用的内存会被回收。反之，只要有任何一个强引用指向该对象，它就会一直存在于内存中。
strong 代表着强引用，是默认属性。当一个对象被声明为 strong 时，就表示父层级对该对象有一个强引用的指向。此时该对象的引用计数会增加1。
weak 代表着弱引用。当对象被声明为 weak 时，父层级对此对象没有指向，该对象的引用计数不会增加1。它在对象释放后弱引用也随即消失。继续访问该对象，程序会得到 nil，不亏崩溃
unowned 与弱引用本质上一样。不同的是，unowned 无主引用 实例销毁后仍然存储着实例的内存地址(类似于OC中的unsafe_unretained), 试图在实例销毁后访问无主引用，会产生运行时错误(野指针)
weak unowned 只能用在 类实例上面
weak、unowned 都能解决 循环引用，unowned 要比 weak 性能 稍高




