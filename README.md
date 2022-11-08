## 摘要

这是对辐射传输模型用最小二乘法求得甲烷羽流理论值的项目。

## 项目结构

### branch

- master：稳定分支，只发布稳定版本
- dev：开发分支，在上面进行操作

### 文件目录

- doc：存放了目前整理的资料

## 目前问题

$$
m_{SBMP}(\Delta \Omega) = {T_{12}(\Omega + \Delta \Omega) - T_{12}(\Omega) \over T_{12}(\Omega)}
$$

1. 论文中提到使用高斯牛顿法通过最小化$F(\Omega) = \Delta R_{SBMP} - m_{SBMP}(\Delta \Omega)$来寻找最合适$\Delta \Omega$，按照常识去想的话，此处的最小化应是趋近于0。但高斯牛顿法是逼近函数的最低点，是趋近于最小值而不是0。究竟是哪个情况还要讨论。
2. $T_{12}(\Omega)$是模拟甲烷柱浓度$\Omega$(mol m^-2)的模拟TOA光谱辐射在 band-12 光谱范围内积分，包括CO2和H2O的吸收，本句话中提到了光谱辐射和光谱范围，这与前面给的波长与光学深度的图之间具体名词的关系不清楚，需要查具体的英文释义。
3. 许多英文名词的含义及其单位还未知。
4. 甲烷浓度的改变改变了6s模型的哪些初始参数？
5. 究竟如何使用高斯牛顿法，究竟是高斯牛顿法找到最小化参数还是高斯牛顿迭代法求拟合曲线参数还未知。
6. 暂定认为不同的甲烷浓度会得到不同输入参数的6s传输模型，进而得到不同的曲线，积分得到不同的值。