---
title: TEST_CASE
date: '2024-11-22 17:17:18'
updated: '2024-11-26 09:52:48'
permalink: /post/testcase-1q40la.html
comments: true
toc: true
---

# TEST_CASE

# 生成工程

* 准备工作

1、在<span data-type="text" style="background-color: var(--b3-font-background2);">MCAL_release\test_suite\system_test\Adc\e3_dev_kit_e3118</span>中创建工程，可以直接复制已有工程，但是要加以改动，如test110

​![image](assets/image-20241122191843-0sl9gcl.png)​

2、在 <span data-type="text" style="background-color: var(--b3-font-background2);">MCAL_release\test_suite\system_test\yaml-projects</span>中更改对应的<span data-type="text" style="background-color: var(--b3-font-background2);">test_project</span>(如Adc_test_project.yaml)添加对应的工程配置yaml路径，如3118_adc_test110，此外还要加上编译需要的库
![image](assets/image-20241122172156-zoivfie.png)​

​![image](assets/image-20241122190839-ifxljuk.png)​3、在<span data-type="text" style="background-color: var(--b3-font-background2);">MCAL_release\test_suite\system_test\yaml-config</span>中创建或修改对应工程的配置yaml,如3118_adc_test110

​![image](assets/image-20241122183847-h32si3i.png)​

        下图中1是EB生成的头文件与源文件

​![image](assets/image-20241122191543-edeis7j.png)​

‍

* 进入路径

```lua
cd /mnt/d/Semidrive/E3/Semidrive_AutoSAR_MCAL_package_v4.0.0/MCAL_release
```

* 指令示例

```lua
../project_generator/progen generate -f ./test_suite/system_test/yaml-projects/Dma_test_project.yaml -t iar_arm -p e3_dev_kit_e3119_dma_test101
```

# 自动化

‍

‍

cd /mnt/d/Semidrive/E3/Semidrive_AutoSAR_MCAL_package_v4.0.0/MCAL_release/test_suite/system_test/Adc/e3_dev_kit_e3118/test110/testshell

‍

‍

‍

ipython.exe unit_test.ipy

‍

‍

‍

​![image](assets/image-20241125150412-yc5pumw.png)​

1是烧录pac包，2是将拨码切换到正常(运行)模式
