TM4C1294NCPDT13, Tiva C

## 硬件资源
Cortex-M4 ARM core with internal 256KB SRAM, 1MB Flash
External 32 MB SDRAM
External 16MB Flash

## 开发步骤
### 步骤1，确认手头的硬件板
* 板子
* 电源
* 连接线

### 步骤2，确认电脑侧安装的软件


### 步骤3, 确认需要用到的模块模型
#### 建立一个driver

```
mkdir gen-gpio

cd gen-gpio

rap init driver

ls
README.md     driver.json   package.json  src/          test/

driver.json
{
    "models": [
        ""
    ],
    "inputs": {
        "": {
            "type": "",
            "args": {

            }
        }
    }
}

解释

package.json
{
    "name": "gen-gpio",
    "version": "0.1.0",
    "description": "a general gpio driver",
    "author": "yang jun",
    "main": "src/index.js"
}


```

### 步骤4, 生成项目
```
rap init -b ruff-1294-gw-v10
```

rap layout 

rap layout --visual


### 步骤5, 部署App
```
rap deploy --use-32-bit
```
程序将被编译成bin文件，下载到MCU中的程序分区上去。

这时候需要reset板子，让MCU运行新下载的App

观察窗口Terminal中的Log日志输出

```
'use strict';
$.ready(function (error) {
    if (error) {
        console.log('error', error);
        return;
    }
    setInterval(function () {
        console.log('Ruff MCU');
    }, 1000);

});
```
## 如何操作一个GPIO口
### 输入GPIO
建立一个驱动
gen-gpio


### 输出GPIO






