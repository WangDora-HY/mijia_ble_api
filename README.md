# mijia BLE Low level API
## master分支
master分支为工作分支，由米家开发人员维护，抽象mijia BLE 底层通用 API 。mible_api.c 中函数为弱定义实现。api的具体说明详见https://miecosystem.github.io/mijia_ble_api/

## 芯片厂分支
此分支为telink平台适配实现，SDK版本2.3。

各芯片厂提供兼容层适配：

保持原有主分支文件不变，增加各自平台上的适配文件，以芯片型号命名 xxxx_api.c， 如 chipsea_api.c 是Chipsea CST92F30平台对 mible_api.c 内函数的实现。 此文件中还可以增加其他文件，用于支持适配。 芯片厂分支内的主分支文件，除 mible_port.h 外不能更改，mible_port.h 用于定义与平台相关的 printf、hexdump、malloc 等。

至少支持 512 bytes HEAP
