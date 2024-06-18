# 五子棋游戏开发流程

## 一、游戏菜单

### （1）、开始游戏

### （2）、游戏设置

### （3）、游戏说明

## 二、游戏面板

### （1）、棋盘

### （2）、玩家和电脑

### （3）、记录下子个数

### （4）、记录分数

### （5）、判定胜负

### （6）、头像

## 三、电脑AI算法

### （1）、五元组遍历

### （2）、计分表权重

​			五子棋盘为15 x 15 的大小，横竖斜四个方向共有572个五元组，给每个五元组一个评分（或权重），这个五元组为它的每个位置贡献的分数就是这个五元组自身的得分，对整个棋盘来说，每个位置的得分就是该位置所在的横竖斜四个方向的所有五元组的得分之和，

然后从所有空位置中选出得分最高的位置就是机器落子的位置。

## 四、输赢算法

以当前落子位置为中心，只要横、竖、正斜、反斜任一方向有五颗同色棋子连成一线则判定获胜。

## 五、游戏截图

![image](https://github.com/mao888/gobang/blob/main/img.assets/img-1.png)


![image](https://github.com/mao888/gobang/blob/main/img.assets/img-2.png)

## 六、命令
使用 lessc 命令行工具来编译 Less 文件
```shell
npm install -g less
```
编译 Less 文件
```shell
lessc css/game.less css/game.css
```
如果你想将编译后的 CSS 输出为单行，可以使用 --clean-css 插件

使用 clean-css 插件
```shell
npm install -g less-plugin-clean-css
```
编译
```shell
lessc css/game.less css/game.css --clean-css
```
