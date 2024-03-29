IFE2016春季班ontoweb团队的代码仓库


规范草案：
总体原则◊

缩进◊
对于所有编程语言，我们要求缩进必须是软tab（用空格字符）。在你的文本编辑器里敲 Tab 应该等于 4个空格 。

**html**：
	* 属性使用双引号，属性名全小写，用**中**划线做分隔符
	* 不要在自动闭合标签结尾处使用斜线 `<br>` `<hr>` `<img>` `<input>` `<link>` `<meta>` `<area>` `<base>` `<col>` `<command>` `<embed>` `<keygen>` `<param>` `<source>` `<track>` `<wbr>`
	* 属性应该按照特定的顺序出现以保证易读性；
		* `class`
		* `id`
		* `name`
		* `data-*`
		* `src` `for` `type` `href` `value` `max-length` `max` `min` `pattern`
		* `placeholder` `title` `alt`
		* `aria-*` `role`
		* `required` `readonly` `disabled`  
		
		class是为高可复用组件设计的，所以应处在第一位；  
		id更加具体且应该尽量少使用，所以将它放在第二位。
		
	* boolean属性不需要声明取值
	* 
	

* **css/scss**:
编码总体原则◊

从外部文件加载CSS，尽可能减少文件数。加载标签必须放在文件的 HEAD 部分。
用 LINK 标签加载，永远不要用@import。

	* 每个html/组件对应一个scss/css
	* 类名使用小写字母，以**中**划线分隔
	* id采用驼峰式命名
	* scss中的变量、函数、混合、placeholder采用驼峰式命名
	* 最外层统一使用双引号
	* url的内容要用引号
	* 属性选择器中的属性值需要引号
	* 颜色16进制用小写字母
	* 颜色16进制尽量用简写
	* 尽量将媒体查询的规则靠近与他们相关的规则，不要将他们一起放到一个独立的样式文件中，或者丢在文档的最底部，这样做只会让大家以后更容易忘记他们
	* 去掉小数点前面的0
	* 属性值`0`后面不要加单位
	* 用 `border: 0;` 代替 `border: none;`
	* 属性不用添加厂商前缀, gulp编译scss时会自动添加

* **js**:
	* 每个文件对应一个js
	* 每个文件应wrap一层
	
		```
		$(function(){
			// code
		})
		```
	* 最外层统一使用单引号  
	* 标准变量采用驼峰式命名
	* jquery对象必须以`$`开头命名
	* `ID`在变量名中全大写
	* `URL`在变量名中全大写
	* `Android`在变量名中大写第一个字母
	* `iOS`在变量名中小写第一个，大写后两个字母
	* 常量全大写，用下划线连接
	* 构造函数，大写第一个字母
	* 一个函数作用域中所有的变量声明尽量提到函数首部，用一个var声明，不允许出现两个连续的var声明
	* 对象属性名不需要加引号
	* 下列关键字后必须有大括号（即使代码块的内容只有一行）：`if` `else` `for` `while` `do` `switch` `try` `catch` `finally` `with`
	* 用`===` `!==` 代替 `==` 	`!=`
	* for-in里一定要有`hasOwnProperty`的判断
	
留空◊

总的来说，使用留空应该遵循源远流长的英语阅读惯例。 例如，每个逗号和冒号（以及适用的分号）后面要空一格，但在括号内部的左侧和右侧都不要加空格。另外，大括号应该总是和他们前面的参数出现在同一行。	


* **注释**:
	* 难于理解的代码段
	* 可能存在错误的代码段
	* 浏览器特殊的hack代码
	* 业务逻辑强相关的代码
	* 各自代码的负责人
