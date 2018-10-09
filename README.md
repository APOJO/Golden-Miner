# Golden-Miner
王者荣耀自动获取金币

## 使用准备
- MuMu模拟器（请选择默认分辨率1440x810！）
- 模拟器设置中的开发者选项需勾选`USB调试模式`
- 运行以下任意版本的脚本（脚本和模拟器均可后台运行）

## 收益说明
- 通关一次可获得19金币。
- 通关222次可获得周上限4200金
- 铭文等级为150时，刷满需要两小时

## 注意事项
- 请确保**第一次**战斗进入了自动战斗模式，否则所有操作可能会延后
- 脚本未正常工作时，请务必关闭脚本重新启动
- 铭文等级不够高时，需要延长战斗时间
- 铭文等级为150时，一般仅需修改加载时间即可达到最佳效果

## 版本说明
- C++版操作简单，无需下载运行库
- Python版方便修改参数

## C++版本
- 模拟器进入冒险模式，选择`魔女的回忆`，进入带有闯关的按钮的界面。
![pic](https://github.com/Henvy-Mango/Golden-Miner/raw/master/pic.png)
- 运行`run.exe`即可。
- C++版本默认刷满222次


## C++版参数调整方法
- 使用文本编辑器打开`run.cpp`
- 修改`device_x` `device_y`调整分辨率
- 修改`step_wait`以调整等待时间
- 修改后重新编译`run.cpp`生成可执行程序即可
- 脚本重复`加载 -> 战斗 -> 结算`三个流程
- 建议调整多次以获取最佳效果
```c++
	//屏幕分辨率
	int device_x = 1440, device_y = 810;

	int wait[] = { 10,24,3 };
	// 各步骤等待间隔
	//step_wait[0]为加载时间，不同手机加载速度不同
	//step_wait[1]为战斗时间
	//step_wait[2]为结算时间
```

## Python版本
- 电脑上需要安装[Python3.4以上的版本](https://www.python.org/downloads/)，并在安装界面勾选Add to PATH。
![Add to PATH](https://imgsa.baidu.com/exp/w=480/sign=b0e60784a1d3fd1f3609a332004f25ce/80cb39dbb6fd5266e27ba8bea218972bd50736c3.jpg)
- 模拟器进入冒险模式，选择`魔女的回忆`，进入带有闯关的按钮的界面，运行`run.bat`。
![pic](https://github.com/Henvy-Mango/Golden-Miner/raw/master/pic.png)
- 根据脚本提示输入数字后回车(直接回车默认刷4200金币)

## Python版参数调整方法 
- 使用文本编辑器打开`run.py`
- 修改`x` `y`调整分辨率
- 修改`wait_times`以调整等待时间
- 脚本重复`加载 -> 战斗 -> 结算`三个流程
- 建议调整多次以获取最佳效果
```python
	# 屏幕分辨率
	x,y = 1440, 810

	# 各步骤等待间隔
	#step_wait[0]为加载时间，不同手机加载速度不同
	#step_wait[1]为战斗时间
	#step_wait[2]为结算时间
	wait_times = [10,24,3]
```