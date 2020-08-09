# 讲师：张长志

  区块链、大数据项目讲师, Java开发、10余年软件研发及企业培训经验，曾为多家大型企业提供企业内训。
擅长领域

python领域

Java领域: SSM、SpringBoot、SpringCloud等java体现；
大数据：Hadoop、HDFS、MapReduce、HBase、Kafka、Spark、CDH 5.3.x集群；
10余年软件研发及企业培训经验，丰富的企业应用软件开发经验、深厚的软件架构设计理论基础及实践能力。
为中石化，中国联通，中国移动等知名企业提供企业培训服务。
项目开发历程：基于大数据技术推荐系统 ，电商大数据分析与统计推断，H5跨平台APP，电信系统，go语言实现storm和zk类似框。



# 前端搭建

## 1.工具安装

1.<https://www.dcloud.io/>

![1573863276964](assets/1573863276964.png)

2.解压

3.登录

![1573864059368](assets/1573864059368.png)



![1573864176567](assets/1573864176567.png)



## 创建一个前端工程

![1573864288015](assets/1573864288015.png)

![1573865006212](assets/1573865006212.png)



# 前端页面

1.分析模块

![1573865441344](assets/1573865441344.png)

# 页面的实现

```
<!DOCTYPE html>
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style>
			#container{
				margin: 0 auto;
				text-align: center;
				width: 1000px;
				border: 2px solid gray;
			}
			
			.header{
				margin: 10px;
				border: 1px solid gray;
			}
			.header .titile{
				color: rgb(53,73,93);
				background: rgb(65,184,131);
			}
			
			.logo{
				position: relative;
				top: 12px;
			}
			.form-warp{
				margin: 10px;
				padding-bottom: 10px;
				border: 1px solid gray;
			
			}
			.sub_title{
				color: rgb(65,184,131);
				background: rgb(53,73,93);
				font-size: 30px;
			}
			
			.form-warp .content{
				line-height: 35px;
			}
			
			.table-warp{
				margin: 10px;
				padding-bottom: 10px;
				border: 1px solid gray;
			
			}
			.form-btn{
				padding: 12px;
			}
			
			
			
		</style>
	</head>
	<body>
		
		<div id="container">
			<div class="header">
				<img src="img/1.png" class="logo" height="80px" width="100px"/>
				<h1 class="titile">商品管理</h1>		
			</div>
			<div class="form-warp">
				<div class="sub_title">添加商品</div>
				<div class="content">
					商品编号：<input type="text" placeholder="请输入商品编号"><br/>
					商品名称：<input type="text" placeholder="请输入商品名称"><br/>
					商品价格：<input type="text" placeholder="请输入商品编号"><br/>
					商品数量：<input type="text" placeholder="请输入商品价格"><br/>
					商品类型：<select>
						<option value="" disabled="disabled">--请选择--</option>
						<option value="">电子产品</option>
						<option value="">食品</option>
					</select>
				</div>
				<div class="form-btn">
					<button>确认添加</button>
					<button>重置信息</button>
				</div>
			</div>
			<div class="table-warp"></div>
		</div>
		
	</body>

	<script>

	</script>
</html>
```



# 商品列表实现

```
<!DOCTYPE html>
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style>
			#container{
				margin: 0 auto;
				text-align: center;
				width: 1000px;
				border: 2px solid gray;
			}
			
			.header{
				margin: 10px;
				border: 1px solid gray;
			}
			.header .titile{
				color: rgb(53,73,93);
				background: rgb(65,184,131);
			}
			
			.logo{
				position: relative;
				top: 12px;
			}
			.form-warp{
				margin: 10px;
				padding-bottom: 10px;
				border: 1px solid gray;
			
			}
			.sub_title{
				color: rgb(65,184,131);
				background: rgb(53,73,93);
				font-size: 30px;
			}
			
			.form-warp .content{
				line-height: 35px;
			}
			
			.form-warp select{
				width: 154px;
				height: 24px;
			}
			.table-warp{
				margin: 10px;
				padding-bottom: 10px;
				border: 1px solid gray;
			
			}
			.form-btn{
				padding: 12px;
			}
			
			.table-warp th{
				width: 80px;
				color: #ffff;
				background: rgb(53,73,93);
			}
			
			
			
		</style>
	</head>
	<body>
		
		<div id="container">
			<div class="header">
				<img src="img/1.png" class="logo" height="80px" width="100px"/>
				<h1 class="titile">商品管理</h1>		
			</div>
			<div class="form-warp">
				<div class="sub_title">添加商品</div>
				<div class="content">
					商品编号：<input type="text" placeholder="请输入商品编号"><br/>
					商品名称：<input type="text" placeholder="请输入商品名称"><br/>
					商品价格：<input type="text" placeholder="请输入商品编号"><br/>
					商品数量：<input type="text" placeholder="请输入商品价格"><br/>
					商品类型：<select>
						<option value="" disabled="disabled">--请选择--</option>
						<option value="">电子产品</option>
						<option value="">食品</option>
					</select>
				</div>
				<div class="form-btn">
					<button>确认添加</button>
					<button>重置信息</button>
				</div>
			</div>
			<!--
            	作者：530979104@qq.com
            	时间：2019-11-16
            	描述：显示表格
            -->
			<div class="table-warp">
				<div class="sub_title">商品列表</div>
				1111
				<table border="1" align="center">
					<tr>
						<th>序号</th>
						<th>编号</th>
						<th>名称</th>
						<th>价格</th>
						<th>数量</th>
						<th>类型</th>
						<th>删除</th>
						<th>选择</th>
					</tr>
					<tr>
						<td>序号1</td>
						<td>编号001</td>
						<td>名称001</td>
						<td>价格001</td>
						<td>数量001</td>
						<td>类型01</td>
						<td><button>删除</button></td>
						<td><input type="checkbox"></td>
					</tr>
				</table>
				
				<div class="form-btn">
					<a>删除选择</a>
					<a>清空全部</a>
				</div>
			</div>
		</div>
		
	</body>
	
	<script>
		
		
	</script>
</html>
```



# 页面和vue的绑定

1.引入 vue.js

```
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
```

2.下载vue.js 保存到项目里面，做本地引入

3.比如vue实现

```html
商品类型：<select>
					<option value="" disabled="disabled">--请选择--</option>
					<option v-for="type in goodsType">{{type}}</option>
```


```js
<script>
	var vm = new Vue({
		el:"#container",
		data:{
			imgUrl:"./img/",
			imgName:'1.png',
			goodsType:['零食','电子商品','生活用品']
		}
	})
	
</script>
```


## 列表实现

```html
<tr v-for="(item,index) in goodsArray" :key="item.id">
						<td>{{index}}</td>
						<td>{{item.id}}</td>
						<td>{{item.name}}</td>
						<td>{{item.price}}</td>
						<td>{{item.num}}</td>
						<td>{{item.type}}</td>
						<td><button>删除</button></td>
						<td><input type="checkbox"></td>
					</tr>
```

```js
<script>
	var vm = new Vue({
		el:"#container",
		data:{
			imgUrl:"./img/",
			imgName:'1.png',
			goodsType:['零食','电子商品','生活用品'],
			goodsArray:[
			{id:'001',name:'海尔电商',price:3500,num:10,type:"电子商品"},
			{id:'002',name:'可口可乐',price:3.5,num:100,type:"零食"},
			{id:'003',name:'毛巾',price:10,num:20,type:"生活用品"},
			]
		}
	})
	
</script>
```


## vue 添加列表

```
<div class="content">
					商品编号：<input type="text" placeholder="请输入商品编号" v-model="goods.id"><br/>
					商品名称：<input type="text" placeholder="请输入商品名称" v-model="goods.name"><br/>
					商品价格：<input type="text" placeholder="请输入商品编号" v-model="goods.price"><br/>
					商品数量：<input type="text" placeholder="请输入商品价格" v-model="goods.num"><br/>
					商品类型：<select v-model="goods.type">
						<option value="" disabled="disabled">--请选择--</option>
						<option v-for="type in goodsType">{{type}}</option>
					</select>
				</div>
				<div class="form-btn">
					<button @click="addGoods">确认添加</button>
					<button>重置信息</button>
				</div>
```




```js
<script>
	var vm = new Vue({
		el:"#container",
		data:{
			imgUrl:"./img/",
			imgName:'1.png',
			goodsType:['零食','电子商品','生活用品'],
			goodsArray:[
			{id:'001',name:'海尔电商',price:3500,num:10,type:"电子商品"},
			{id:'002',name:'可口可乐',price:3.5,num:100,type:"零食"},
			{id:'003',name:'毛巾',price:10,num:20,type:"生活用品"},
			],
			goods:{
				id:'',
				name:'',
				price:'',
				num:'',
				type:''
			},
		},
		methods:{
			addGoods(){
				this.goodsArray.push(this.goods);
				this.goods = {};
				
			}
		}
	})
	
</script>
```


# vue 删除功能

```html
<!DOCTYPE html>
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style>
			#container{
				margin: 0 auto;
				text-align: center;
				width: 1000px;
				border: 2px solid gray;
			}
			
			.header{
				margin: 10px;
				border: 1px solid gray;
			}
			.header .titile{
				color: rgb(53,73,93);
				background: rgb(65,184,131);
			}
			
			.logo{
				position: relative;
				top: 12px;
			}
			.form-warp{
				margin: 10px;
				padding-bottom: 10px;
				border: 1px solid gray;
			
			}
			.sub_title{
				color: rgb(65,184,131);
				background: rgb(53,73,93);
				font-size: 30px;
			}
			
			.form-warp .content{
				line-height: 35px;
			}
			
			.form-warp select{
				width: 154px;
				height: 24px;
			}
			.table-warp{
				margin: 10px;
				padding-bottom: 10px;
				border: 1px solid gray;
			
			}
			.form-btn{
				padding: 12px;
			}
			
			.table-warp th{
				width: 80px;
				color: #ffff;
				background: rgb(53,73,93);
			}
			
			
			
		</style>
	</head>
	<body>
		
		<div id="container">
			<div class="header">
				<img :src='imgUrl+imgName' class="logo" height="80px" width="100px"/>
				<h1 class="titile">商品管理</h1>		
			</div>
			<div class="form-warp">
				<div class="sub_title">添加商品</div>
				<div class="content">
					商品编号：<input type="text" placeholder="请输入商品编号" v-model="goods.id"><br/>
					商品名称：<input type="text" placeholder="请输入商品名称" v-model="goods.name"><br/>
					商品价格：<input type="text" placeholder="请输入商品编号" v-model="goods.price"><br/>
					商品数量：<input type="text" placeholder="请输入商品价格" v-model="goods.num"><br/>
					商品类型：<select v-model="goods.type">
						<option value="" disabled="disabled">--请选择--</option>
						<option v-for="type in goodsType">{{type}}</option>
					</select>
				</div>
				<div class="form-btn">
					<button @click="addGoods">确认添加</button>
					<button>重置信息</button>
				</div>
			</div>
			<!--
            	作者：530979104@qq.com
            	时间：2019-11-16
            	描述：显示表格
            -->
			<div class="table-warp">
				<div class="sub_title">商品列表</div>
				1111
				<table border="1" align="center">
					<tr>
						<th>序号</th>
						<th>编号</th>
						<th>名称</th>
						<th>价格</th>
						<th>数量</th>
						<th>类型</th>
						<th>删除</th>
						<th>选择</th>
					</tr>
					<td :colspan="colNum" height="150px" v-show="goodsArray.length<=0">
						暂无商品
					</td>
					<tr v-for="(item,index) in goodsArray" :key="item.id">
						<td>{{index}}</td>
						<td>{{item.id}}</td>
						<td>{{item.name}}</td>
						<td>{{item.price}}</td>
						<td>{{item.num}}</td>
						<td>{{item.type}}</td>
						<td><button @click="delGoods(index)">删除</button></td>
						<td><input type="checkbox" :value="index" v-model="delArray"></td>
					</tr>
				</table>
				
				<div class="clear-btn">
					<a @click="delSelected" v-show="goodsArray.length>0">删除选择</a>
					<a @click="clearGoodsArray" v-show="goodsArray.length>0">清空全部</button>
				</div>
			</div>
		</div>
		
	</body>
	
	<script>
		var vm = new Vue({
			el:"#container",
			data:{
				imgUrl:"./img/",
				imgName:'1.png',
				goodsType:['零食','电子商品','生活用品'],
				goodsArray:[
				{id:'001',name:'海尔电商',price:3500,num:10,type:"电子商品"},
				{id:'002',name:'可口可乐',price:3.5,num:100,type:"零食"},
				{id:'003',name:'毛巾',price:10,num:20,type:"生活用品"},
				],
				goods:{
					id:'',
					name:'',
					price:'',
					num:'',
					type:''
				},
				delArray:[],//删除选中的索引
				colNum:8
			},
			methods:{
				addGoods(){
					this.goodsArray.push(this.goods);
					this.goods = {};
					
				},
				delGoods(index){
					this.goodsArray.splice(index,1)
				},
				 delSelected(){
                         this.delArray.sort((a,b)=>{
                             return a-b;
                         });
                         
                         console.log(this.delArray);
                         
                         for(var i=0;i<this.delArray.length;i++)
                         {
                             this.goodsArray.splice(this.goodsArray[i]-i,1);
                         }
                         this.delArray=[];
                },
                clearGoodsArray(){
                	this.goodsArray=[];
                }
				
			}
		})
		
	</script>
</html>
```

# Springboot

![1573874134572](assets/1573874134572.png)

![1573874146333](assets/1573874146333.png)



## springboot项目创建

![1573874268873](assets/1573874268873.png)

![1573874314010](assets/1573874314010.png)

![1573874334055](assets/1573874334055.png)

![1573874359690](assets/1573874359690.png)

![1573874399054](assets/1573874399054.png)

引入maven文件

![1573874448839](assets/1573874448839.png)

![1573874626330](assets/1573874626330.png)

## 修改pom文件配置

```xml
	<properties>
		<java.version>1.8</java.version>
		<project.buid.sourceEncoding>UTF-8</project.buid.sourceEncoding>
		<maven.compiler.source>1.8</maven.compiler.source>
		<maven.compiler.target>1.8</maven.compiler.target>
	</properties>
```

修改配置端口

```xml
server.port=8081
```

在controller写代码

```
package com.zhang.shop.controller;

import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

/**
 * @author zhchzh100
 * @create 2019-11-16  11:32
 */
@RestController
public class GoodsController {

    @RequestMapping("/test")
    public String test(){
        return "test";
    }
}

```



访问 ：<http://127.0.0.1:8081/test>

![1573875283462](assets/1573875283462.png)



# 加载thymeleaf页面



1.引入maven文件

```xml
<dependency>
   <groupId>org.springframework.boot</groupId>
   <artifactId>spring-boot-starter-thymeleaf</artifactId>
</dependency>
```

2.修改配置文件

```
spring.thymeleaf.prefix=classpath:/templates
spring.thymeleaf.suffix=.html
```

3.创建控制器

```java
@Controller
public class GoodsController {

    @RequestMapping("/test")
    @ResponseBody
    public String test(){
        return "test";
    }

    @RequestMapping("/index")
    public ModelAndView index(){
        ModelAndView modelAndView = new ModelAndView("/index.html");
        return modelAndView;
    }
}
```



# 链接数据库

![1573877066537](assets/1573877066537.png)



| 字段名称 | 字段类型     | 备注     |
| -------- | ------------ | -------- |
| id       | int          | 商品id   |
| name     | VARCHAR(20)  | 商品名称 |
| price    | DECIMAL(8,2) | 商品价格 |
| num      |              | 商品数量 |
| type     |              | 商品类型 |



```
CREATE TABLE goods(
				id INT UNSIGNED auto_increment NOT NULL comment '商品ID',
				name VARCHAR(20) NOT NULL comment '商品名称',
				price DECIMAL(8,2) NOT NULL comment '商品售价价格',
			    num INT NOT NULL DEFAULT 1 comment '商品数量',
				type VARCHAR(10) NOT NULL comment '商品类型',
				PRIMARY KEY pk_productid(id)
 )engine = innodb comment '商品信息表';

```

![1573877193296](assets/1573877193296.png)



![1573877232635](assets/1573877232635.png)



![1573877298570](assets/1573877298570.png)



## mybatis获取mysql里面数据

1.集成mybatis逆向工程。

修改pom文件

```
	<dependency>
			<groupId>mysql</groupId>
			<artifactId>mysql-connector-java</artifactId>
			<version>5.1.35</version>
		</dependency>
		<dependency>
			<groupId>org.mybatis.generator</groupId>
			<artifactId>mybatis-generator-core</artifactId>
			<version>1.3.2</version>
		</dependency>
		
		
		
	<build>
		<pluginManagement>
			<plugins>
				<plugin>
					<groupId>org.apache.maven.plugins</groupId>
					<artifactId>maven-compiler-plugin</artifactId>
					<configuration>
						<source>1.8</source>
						<target>1.8</target>
					</configuration>
					<version>3.3</version>
				</plugin>
				<plugin>
					<groupId>org.mybatis.generator</groupId>
					<artifactId>mybatis-generator-maven-plugin</artifactId>
					<version>1.3.2</version>
					<dependencies>
						<dependency>
							<groupId>mysql</groupId>
							<artifactId>mysql-connector-java</artifactId>
							<version>5.1.35</version>
						</dependency>
					</dependencies>
					<configuration>
						<!--配置文件的路径-->
						<configurationFile>src/main/resources/generatorConfig.xml</configurationFile>
						<overwrite>true</overwrite>
					</configuration>
				</plugin>
			</plugins>
		</pluginManagement>


		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>
		</plugins>
	</build>
```



2.创建generatorConfig.xml文件

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE generatorConfiguration
        PUBLIC "-//mybatis.org//DTD MyBatis Generator Configuration 1.0//EN"
        "http://mybatis.org/dtd/mybatis-generator-config_1_0.dtd">
<generatorConfiguration>
    <context id="test" targetRuntime="MyBatis3">
        <plugin type="org.mybatis.generator.plugins.EqualsHashCodePlugin"></plugin>
        <plugin type="org.mybatis.generator.plugins.SerializablePlugin"></plugin>
        <plugin type="org.mybatis.generator.plugins.ToStringPlugin"></plugin>
        <commentGenerator>
            <!-- 这个元素用来去除指定生成的注释中是否包含生成的日期 false:表示保护 -->
            <!-- 如果生成日期，会造成即使修改一个字段，整个实体类所有属性都会发生变化，不利于版本控制，所以设置为true -->
            <property name="suppressDate" value="true" />
            <!-- 是否去除自动生成的注释 true：是 ： false:否 -->
            <property name="suppressAllComments" value="true" />
        </commentGenerator>
        <!--数据库链接URL，用户名、密码 -->
        <jdbcConnection driverClass="com.mysql.jdbc.Driver"
                        connectionURL="jdbc:mysql://192.168.1.102:3306/shop" userId="root"
                        password="root">
        </jdbcConnection>
        <javaTypeResolver>
            <!-- This property is used to specify whether MyBatis Generator should
                force the use of java.math.BigDecimal for DECIMAL and NUMERIC fields, -->
            <property name="forceBigDecimals" value="false" />
        </javaTypeResolver>
        <!-- 生成模型的包名和位置 -->
        <javaModelGenerator targetPackage="com.zhang.shop.model"
                            targetProject="src/main/java">
            <property name="enableSubPackages" value="true" />
            <property name="trimStrings" value="true" />
        </javaModelGenerator>
        <!-- 生成映射文件的包名和位置 -->
        <sqlMapGenerator targetPackage="mapping"
                         targetProject="src/main/resources">
            <property name="enableSubPackages" value="true" />
        </sqlMapGenerator>
        <!-- 生成DAO的包名和位置 -->
        <javaClientGenerator type="XMLMAPPER"
                             targetPackage="com.zhang.shop.dao"
                             targetProject="src/main/java">
            <property name="enableSubPackages" value="true" />
        </javaClientGenerator>

        <!-- 要生成哪些表 -->
        <table tableName="`goods`" domainObjectName="Goods" enableCountByExample="false"
               enableUpdateByExample="false" enableDeleteByExample="false"
               enableSelectByExample="false" selectByExampleQueryId="false">
            <generatedKey column="id" sqlStatement="Mysql" identity="true"/>
        </table>

    </context>
</generatorConfiguration>
```

修改内容：

![1573878262513](assets/1573878262513.png)

![1573878281054](assets/1573878281054.png)



![1573878296270](assets/1573878296270.png)



![1573878353990](assets/1573878353990.png)

![1573878422729](assets/1573878422729.png)



```xml
mybatis-generator:generate
```



3. 操作配置操作的文件

   引入pom文件

   ```xml
   <dependency>
      <groupId>com.alibaba</groupId>
      <artifactId>druid</artifactId>
      <version>1.1.12</version>
   </dependency>
   
   <dependency>
   <groupId>org.mybatis.spring.boot</groupId>
   <artifactId>mybatis-spring-boot-starter</artifactId>
   <version>1.3.3</version>
   </dependency>
   ```

   

   2.修改配置文件

   ```xml
   #配置mybatis
   mybatis.mapper-locations=classpath:mapping/*.xml
   spring.datasource.name=shop
   spring.datasource.url=jdbc:mysql://192.168.1.102:3306/shop?serverTimezone=UTC&useUnicode=true&characterEncoding=UTF-8
   spring.datasource.username=root
   spring.datasource.password=root
   
   # 使用druid链接池
   spring.datasource.type=com.alibaba.druid.pool.DruidDataSource
   spring.datasource.driver-class-name=com.mysql.jdbc.Driver
   ```

   3.在启动类添加注解

   ```java
   @MapperScan("com.zhang.shop.dao")
   ```

   4.开发代码

   ```java
   package com.zhang.shop.service;
   
   import com.zhang.shop.model.Goods;
   
   /**
    * @author zhchzh100
    * @create 2019-11-16  12:36
    */
   public interface GoodsService {
   
       Goods getGoods(Integer id);
   }
   ```

   ```java
   package com.zhang.shop.service.impl;
   
   import com.zhang.shop.dao.GoodsMapper;
   import com.zhang.shop.model.Goods;
   import com.zhang.shop.service.GoodsService;
   import org.springframework.beans.factory.annotation.Autowired;
   import org.springframework.stereotype.Service;
   
   /**
    * @author zhchzh100
    * @create 2019-11-16  12:37
    */
   @Service
   public class GoodsServiceImpl implements GoodsService {
   
       @Autowired
       private GoodsMapper goodsMapper;
   
       @Override
       public Goods getGoods(Integer id) {
           return goodsMapper.selectByPrimaryKey(id);
       }
   }
   ```

   ```java
   package com.zhang.shop.controller;
   
   import com.zhang.shop.model.Goods;
   import com.zhang.shop.service.GoodsService;
   import org.springframework.beans.factory.annotation.Autowired;
   import org.springframework.stereotype.Controller;
   import org.springframework.web.bind.annotation.RequestMapping;
   import org.springframework.web.bind.annotation.ResponseBody;
   import org.springframework.web.bind.annotation.RestController;
   import org.springframework.web.servlet.ModelAndView;
   
   /**
    * @author zhchzh100
    * @create 2019-11-16  11:32
    */
   @Controller
   public class GoodsController {
   
       @Autowired
      private   GoodsService goodsService;
   
       @RequestMapping("/test")
       @ResponseBody
       public String test(){
           return "test";
       }
   
       @RequestMapping("/index")
       public ModelAndView index(){
           ModelAndView modelAndView = new ModelAndView("/index.html");
           return modelAndView;
       }
   
       @RequestMapping("/get")
       @ResponseBody
       public Goods getGoods(Integer id){
           return  goodsService.getGoods(id);
       }
   }
   ```

   访问<http://127.0.0.1:8081/get?id=1>

   ![1573879891869](assets/1573879891869.png)

   #  通用返回值

   ![1573886379279](assets/1573886379279.png)

   ```java
   package com.zhang.shop.comm;
   
   /**
    * @author zhchzh100
    * @create 2019-11-16  14:49
    * 错误处理
    */
   public class CommonError {
   
       //错误码
       private Integer errCode;
   
       //错误描述
       private String errMsg;
   
       public CommonError(Integer errCode,String errMsg){
           this.errCode = errCode;
           this.errMsg = errMsg;
       }
   
       public CommonError(EmBusinessError emBusinessError){
           this.errCode = emBusinessError.getErrCode();
           this.errMsg = emBusinessError.getErrMsg();
   
       }
   
   
       public Integer getErrCode() {
           return errCode;
       }
   
       public void setErrCode(Integer errCode) {
           this.errCode = errCode;
       }
   
       public String getErrMsg() {
           return errMsg;
       }
   
       public void setErrMsg(String errMsg) {
           this.errMsg = errMsg;
       }
   }
   ```

   ```java
   package com.zhang.shop.comm;
   
   /**
    * @author zhchzh100
    * @create 2019-11-16  14:39
    */
   public class CommonRes {
   
       //表明请求的处理结果 success fail
       private String status;
   
       //success Oject   fail 返回错误码
       private Object data;
   
       public static  CommonRes create(Object object){
              return create(object,"success");
       }
   
       //定义一个通用的返回值对象
       public static  CommonRes create(Object object,String status){
           CommonRes commonRes = new CommonRes();
           commonRes.setStatus(status);
           commonRes.setData(object);
           return  commonRes;
       }
   
   
       public String getStatus() {
           return status;
       }
   
       public void setStatus(String status) {
           this.status = status;
       }
   
       public Object getData() {
           return data;
       }
   
       public void setData(Object data) {
           this.data = data;
       }
   }
   ```

   ```java
   package com.zhang.shop.comm;
   
   /**
    * @author zhchzh100
    * @create 2019-11-16  14:53
    */
   public enum EmBusinessError {
       NO_OBJECT_FOUND(10000,"请求对象不存在"),
   
       ;
   
   
       private Integer errCode;
       private String errMsg;
       EmBusinessError(Integer errCode,String errMsg){
           this.errCode = errCode;
           this.errMsg = errMsg;
       }
   
       public Integer getErrCode() {
           return errCode;
       }
   
       public void setErrCode(Integer errCode) {
           this.errCode = errCode;
       }
   
       public String getErrMsg() {
           return errMsg;
       }
   
       public void setErrMsg(String errMsg) {
           this.errMsg = errMsg;
       }
   }
   ```



# 通用异常处理

```java
package com.zhang.shop.comm;

/**
 * @author zhchzh100
 * @create 2019-11-16  15:18
 */
public class BusinessException extends  Exception {
    private  CommonError commonError;

    public BusinessException(EmBusinessError emBusinessError){
        super();
        this.commonError = new CommonError(emBusinessError);
    }

    public CommonError getCommonError() {
        return commonError;
    }

    public void setCommonError(CommonError commonError) {
        this.commonError = commonError;
    }
}
```

2.引入maven

```xml
<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-aop</artifactId>
		</dependency>

```

3.添加注解

```
@EnableAspectJAutoProxy(proxyTargetClass = true)
```



4.统一的处理注解

```java
package com.zhang.shop.comm;

import org.springframework.web.bind.ServletRequestBindingException;
import org.springframework.web.bind.annotation.ControllerAdvice;
import org.springframework.web.bind.annotation.ExceptionHandler;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.ResponseBody;
import org.springframework.web.servlet.NoHandlerFoundException;

import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

/**
 * @author zhchzh100
 * @create 2019-11-16  15:22
 */
@ControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(Exception.class)
    @ResponseBody
    public CommonRes doError(HttpServletRequest request, HttpServletResponse response,Exception excetion){
        if (excetion instanceof  BusinessException){
            return  CommonRes.create(((BusinessException)excetion).getCommonError(),"fail");
        }else if(excetion instanceof NoHandlerFoundException){
            CommonError commonError = new CommonError(EmBusinessError.NO_HANDLER_FOUT);
            return CommonRes.create(commonError,"fail");
        }else if(excetion instanceof ServletRequestBindingException){
            CommonError commonError = new CommonError(EmBusinessError.BIND_EXCEPTION_FOUT);
            return CommonRes.create(commonError,"fail");
        }else {
            CommonError commonError = new CommonError(EmBusinessError.UNKNOEN_ERROR);
            return CommonRes.create(commonError,"fail");
        }

    }

}
```



6.放开static 路径

```xml
#404异常处理
#add-mappings = true  表示如果所有的controller 都没有命中，则使用默认处理资源
spring.resources.add-mappings=true
spring.mvc.throw-exception-if-no-handler-found=true

spring.mvc.static-path-pattern=/static/**
```

7. ```java
   public CommonRes getGoods(@RequestParam(name="id") Integer id) throws BusinessException {
   ```

   如果定义请求参数异常必须要加RequestParam 定义参数名字。

# vue 和springboot 的整合

1.拷贝html页面到我们springboot的static下面

2.引入vue.js 和 jquery.min.js

3.运行

## 查询所有的商品

1. 写xml sql语句

   ```xml
   <select id="findAll" resultMap="BaseResultMap"  >
     select
     <include refid="Base_Column_List" />
     from goods
   </select>
   ```

2. 在dao添加方法

   ```java
   List<Goods> findAll();
   ```

3. 在service里面添加方法

   ```java
   List<Goods> findAll();
   ```

   ```java
   @Override
   public List<Goods> findAll() {
       return goodsMapper.findAll();
   }
   ```

4. 控制器添加方法

   ```java
    @RequestMapping("/findAll")
   @ResponseBody
    public  CommonRes findAll() throws BusinessException {
        List<Goods> lists = goodsService.findAll();
        if (lists == null) {
            throw new BusinessException(EmBusinessError.NO_OBJECT_FOUND);
        }else {
            return  CommonRes.create(lists);
        }
    }
   ```

5. 在页面里面添加访问网络的代码

   ```xml
   show(){
       $.ajax({
         url:"/goods/findAll",
         contentType:"application/json;charset=utf-8",
         dataType:"json",
         success:function (data) {
             console.log(data)
            vm.goodsArray =data.data;
                       }
      })
   }
   ```

6. 第一次访问调用show方法

   ```xml
   created:function () {
      this.show()
            },
   ```



# 添加商品

1.控制器

```java
@RequestMapping(value = "/insertgoods",method = RequestMethod.POST)
@ResponseBody
 public CommonRes insertgoods(Goods goods) throws BusinessException{
     int id = goodsService.insert(goods);
     return  CommonRes.create(id);
 }
```



2.service

```java
int insert(Goods goods);
```



3.页面操作

```html
addGoods(){
    //this.goodsArry.push(this.goods);
    //this.goods={};
    _this = this

    $.ajax({
        url:"/goods/insertgoods",
        data: _this.goods,
        type:"post",
        success:function () {
            alert("添加成功");
            show();
        },error:function (rel) {
            alert(rel+"添加失败");
        }
    });
    show()
},
```



# 删除商品

```xml
<delete id="deleteBatch">
   DELETE FROM goods where id IN
   <foreach collection="array" item="id" open="(" separator="," close=")">
      #{id}
   </foreach>
</delete>
```

dao

```java
void deleteBatch(Long[] ids);
```



控制层

```java
@RequestMapping(value = "/delete",method = RequestMethod.POST)
@ResponseBody
public CommonRes delete(@RequestBody Long[] ids) throws BusinessException{
   // int id = goodsService.insert(goods);
    goodsService.deleteBatch(ids);
    return CommonRes.create("0");
}
```



maven文件

```xml
<dependency>
   <groupId>com.fasterxml.jackson.core</groupId>
   <artifactId>jackson-databind</artifactId>
   <version>2.8.8.1</version>
</dependency>
```



