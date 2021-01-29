好生意移动端

# 打开壳子：

## 打开CC

点击文件 CCApp/ios/CCApp.xcodeproj

## 打开HSY

点击文件 saas-hsy-mobile-app/ios/HsyMobile.xcodeproj

/Users/ninemilli/.rncache

# 配置环境：

1. xcode 中修改工程info/NET_ENV (例：TEST)
2. package 中修改 hsy-mobile-client/index.ts 中的 host 变量
```
https://test-cloud.chanjet.com
```

# 安装依赖

工程目录下（hsy-mobile-client/CCApp）

```
lerna bootstrap
```

# 启动应用

1. xcode: Project -> Clean Build Floder
2. xcode: run
3. hsy-mobile-client/CCApp: npm run haul-ios/android

# 移动报表：

```
# 克隆工程
yao clone

# 进入工程目录
yao biz-common

# 创建特性分支后
lerna bootstrap

# 启动项目
npm run dev

# 自动生成报表文件
yao report
```

# 账号

```
# 原始 
15905280000 890125

# 待审核单据 
17778131921 wqw36641

# DEV测试 
13211111111 111111

15175757878 123456

# 门店列表 
11111111199 123456

# UE给的要货单账号 
19000001111 1qaz2wsx

# 夏凡给的测试账号 
15011366918 111111

# 演示账号 
15175757878 123456

# 毕赢测试账号 
15100000002 by654321

# 主账号(权限多) 
16720201212 123456

# 店长 
12320200101 286459
```

# RN工程中加SVG icon图标

1. 下载图标库 SVG格式的图标到本地
2. 把本地的图标文件改名xxx.svg,放入目录 saas-hsy-mobile-app/packages/assets/svg/xxx.svg
3. 打开文件 saas-hsy-mobile-app/packages/hsy-mobile-components/src/theme/AppIcons.ts
4. 代码里加入 xxx: 'xxx'
5. 在saas-hsy-mobile-app目录下执行 node scripts/generateSvgs 命令,大功告成可以使用了

