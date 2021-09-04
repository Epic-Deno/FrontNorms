# Vue 前端风格指南

### 一、命名规范
* camelCase （小驼峰法命名 -- 首字母小写）
* PascalCase（大驼峰法命名 -- 首字母大写）
* kebab-case (短横线连线式)
* Snake (下划线连接 Pony_name)

#### 1.1 项目文件命名
##### 1.1.1 项目名
全部采用小写方式， 以短横线分隔。 例：<code>my-project-name</code>
##### 1.1.2 目录名称
参照项目命名规则， 有复数结构时，要采用复数命名法。 例： docs、 assets、
components、directives、mixins、utils、views。
```javascript
my-project-name/
|- BuildScript    // 流水线部署文件目录
|- docs           // 项目的细化文档目录（可选）
|- nginx          // 部署在容器上前端项目 nginx 代理文件目录
|- node_modules   // 下载的依赖包
|- public         // 静态页面目录
    |- index.html // 项目入口
|- src            // 源码目录
    |- api        // http 请求目录
    |- assets     // 静态资源目录，这里的资源会被wabpack构建
        |- icon   // icon 存放目录
        |- img    // 图片存放目录
        |- js     // 公共 js 文件目录
        |- scss   // 公共样式 scss 存放目录
            |- frame.scss   // 入口文件
            |- global.scss  // 公共样式
            |- reset.scss   // 重置样式
    |- components     // 组件
    |- plugins        // 插件
    |- router         // 路由
    |- routes         // 详细的路由拆分目录（可选）
        |- index.js
    |- store          // 全局状态管理
    |- utils          // 工具存放目录
        |- request.js // 公共请求工具
    |- views          // 页面存放目录
    |- App.vue        // 根组件
    |- main.js        // 入口文件
    |- tests          // 测试用例
    |- .browserslistrc// 浏览器兼容配置文件
    |- .editorconfig  // 编辑器配置文件
    |- .eslintignore  // eslint 忽略规则
    |- .eslintrc.js   // eslint 规则
    |- .gitignore     // git 忽略规则
    |- babel.config.js // babel 规则
    |- Dockerfile // Docker 部署文件
    |- jest.config.js
    |- package-lock.json
    |- package.json // 依赖
    |- README.md // 项目 README
    |- vue.config.js // webpack 配置
```
##### 1.1.3 图像文件名
全部采用小写方式， 优先选择单个单词命名， 多个单词一下划线分隔。
```javascript
banner_sina.gif
menu_aboutus.gif
menutitle_news.gif
logo_police.gif
logo_national.gif
pic_people.jpg
pic_TV.jpg

```
##### 1.1.4 HTML文件名
采用小写方式， 优先选择单个单词命名，多个单词名， 多个单词命名以下下划线分隔。
```javascript
|- error_report.html
|- success_report.html 
```

#### 1.1.5 CSS文件名
全部采用小写方式，优先选择单个单词命名，多个单词命名短横线分隔

```javascript
|- normalize.less
|- base.less
|- date-picker.scss
|- input-number.scss
```
##### 1.1.6 Javascript文件名
```javascript
|- index.js
|- plugin.js
|- util.js
|- date-util.js
|- account-model.js
|- collapse-transition.js   
```
#### 1.2 Vue组件命名

##### 1.2.1 单文件组件名称
文件拓展名为 .vue的 单文件组件 components。 单文件组件名称应该是中是单词大写开头（PascalCase）。
```javascript
components/
|- MyComponent.vue
``` 

### 重点
* 2.1.1 当行注释
```html
<!-- Comment Text -->
<div>...</div>
```
* 2.1.2 模块注释
```html
<!-- S Comment Text A --> 
<div class="mod_a">
  ...
</div>
<!-- E Comment Text A -->
 
<!-- S Comment Text B --> 
<div class="mod_b">
  ...
</div>
<!-- E Comment Text B -->
```
* 2.1.3 单行注释
```css
/* Comment Text */ 
.jdc {} 

/* Comment Text */ 
.jdc {}
```
* 2.1.4 模块注释
```css
/* Module A
---------------------------------------------------------------- */
.mod_a {}


/* Module B
---------------------------------------------------------------- */
.mod_b {}
```
* 2.1.5 javascript 单行注释
```javascript
// is current tab
const active = true

function getType () {  
  console.log('fetching type...')
  
  // set the default type to 'no type'
  const type = this.type || 'no type'
  return type
}

// 注释行上面是一个块的顶部时不需要空行
function getType () {  
  // set the default type to 'no type'
  const type = this.type || 'no type'   
  return type
}
```
* 2.1.6javascript 多行注释
```javascript
/**
 * make() returns a new element
 * based on the passed-in tag name
 */
function make (tag) {
  // ...

  return element
}
```

