**ER-GIKT-Flask-Vue** 

基于GIKT深度知识追踪模型的习题推荐系统（毕业设计）

### 目录结构

- Flask-BackEnd `flask后端`
  * app `后端主体文件`
    * alg `深度学习模块`
      * data  `数据集`
      * data_process.py `数据预处理`
      * gikt.py `GIKT模型`
      * pebg.py `PEBG模型`
        * params.py `一些参数`
      * train.py `模型训练`
      * utils.py `工具函数`
    * view `flask蓝图`
    * \__init__.py `初始化`
    * create_data `创建初始数据`
    * entity `实体类`
    * setup `启动`
  * migrate `数据库迁移文件`

* Vue-FrontEnd `vue前端`
  * public `共用文件`
  * src `源代码`
    * api `全局请求设置`
    * assets `静态组件`
    * components `自定义vue组件`
    * layout `页面布局`
    * router `路由`
    * store `信息储存`
    * views `页面`
    * App.vue `开始文件`
    * main.js `js包引入`
  * 其他的是一些配置

### 项目存在的一些问题

#### 算法

- PEBG模型未按论文实现，实际上忽略了pnn网络（实现中出现了问题，故将其忽略）
- GIKT模型训练时计算的是训练的acc和auc，非测试的acc和auc

#### 前端

- 前端使用的是vue2+vue-cli，下一届的学弟学妹最好可以用vue3+vite重构一遍

- 重复组件较多，Table，Chart等图都直接写在页面中

#### 后端

- 包引用（尤其是对算法包的引用）存在问题，使用了粗暴的解决方式 sys.path.append() 且无法使用相对路径导入
- flask数据库迁移会报错，只能自己手动修改

  
