# UPC_Food
> The WeChat Mini Program Reference Code of UPC_Food.

### 一、功能简介

“UPC_Food”是一款致力于解决用户吃饭难、选择难的微信小程序。程序可以按照用户的口味和喜好包括位置价格等等来筛选推荐用户可能会喜欢的食物，基于微信平台，方便使用。

### 二、详细设计

#### 1. 前端设计

- 启动页

![](https://v-picgo-1252406892.cos.ap-chengdu.myqcloud.com/start.png)

- 主页

![](https://v-picgo-1252406892.cos.ap-chengdu.myqcloud.com/main.png)

- 口味

![](https://v-picgo-1252406892.cos.ap-chengdu.myqcloud.com/taste.png)

- 距离

![](https://v-picgo-1252406892.cos.ap-chengdu.myqcloud.com/distance.png)

- 价格

![](https://v-picgo-1252406892.cos.ap-chengdu.myqcloud.com/price.png)

- 结果

![](https://v-picgo-1252406892.cos.ap-chengdu.myqcloud.com/result.png)

- 结束

![](https://v-picgo-1252406892.cos.ap-chengdu.myqcloud.com/final.png)

#### 2. 后端设计

后端采用微信官方的腾讯云作为服务器，数据库采用phpMyAdmin下的MySQL实现，新建一个名字为upcclm的数据库，在其中新建一张名为 food 的表格，表格内容如下：

``` 
foodID：字符串类型，长度6，表格的主码，用来唯一标识某一款食物。
foodName：字符串类型，长度20，用来登记食物的名称。
foodTastela：整数型，长度1，用来标识食物口味中“辣”属性的值。
foodTastetian：整数型，长度1，用来标识食物口味中“甜”属性的值。
foodTastesuan：整数型，长度1，用来标识食物口味中“酸”属性的值。
foodTastexian：整数型，长度1，用来标识食物口味中“咸”属性的值。
foodPosition：字符串类型，长度20，用来登记餐厅名字，以后考虑具体到某一层某一个窗口。
positionID：整数型，长度1，用来标识餐厅的代码，1：玉兰苑 2：荟萃3：唐岛湾。
foodPrice：浮点型，用来存储食物的价格，可以包括小数。
foodRate：整数型，长度1，用于显示食物的评价星级，从1-5。                         
foodPicurl：字符串类型，长度255，用于存储食物图片对应的地址。
```

![](https://v-picgo-1252406892.cos.ap-chengdu.myqcloud.com/20190214213324.png)