---
~
---
# #多组分系统热力学
### #多组分系统和组成表示法
由于组成可变的封闭系统在其某些参数变化的条件下会得到和敞开系统一样的性质，然后这里的封闭系统并不是绝对意义上的封闭系统，仅仅代表着物质守恒
- 组成可变的封闭系统相当于敞开系统

组成可变系统的状态描述
- 容量性质:  $V=(T,p,n_{B},n_{C})$ 共 $k+2$ 个变量
	- 各个物质的摩尔量和温度压强
- 强度性质: $\rho=\rho(T,p,x_B,x_C)$ 共 $k+1$ 个变量
	- 相对含量，所以会少一个变量

### #偏摩尔量 
##### 定义
- 物质的某些量随着摩尔量的变化而产生的变化
- 由于是基于摩尔量，所以是对于物质的容量性质而言
- 偏摩尔量本身又是状态函数，它数值本身已经与 $n$ 无关了
- 常见的偏摩尔量:
$$V_B=\left( \frac{\partial V}{\partial n_B} \right)_{T,p,b_C}\qquad V=\sum_{B}n_{B}V_{B}$$
$$U_B=(\frac{\partial U}{\partial n_B})_{T,p,b_C}\qquad U=\sum_{B}n_{B}U_{B}$$
$$H_B=(\frac{\partial H}{\partial n_H})_{T,p,b_C}\qquad H=\sum_{B}n_{B}H_{B}$$
$$F_B=(\frac{\partial F}{\partial n_B})_{T,p,b_C}\qquad F=\sum_{B}n_{B}F_{B}$$
$$S_B=(\frac{\partial S}{\partial n_B})_{T,p,b_C}\qquad S=\sum_{B}n_{B}S_{B}$$
$$G_B=(\frac{\partial G}{\partial n_B})_{T,p,b_C}\qquad G=\sum_{B}n_{B}G_{B}$$
- 纯物质或组成不变的热力学函数之间的关系对于偏摩尔量同样成立
	- $H_{B}=U_{B}+pV_{B}$
	- $F_{B}=U_{B}-TS_{B}$
	- $G_B=H_{B}-TS_{B}=U_{B}+pV_{B}-TS_{B}=F_{B}+pV_{B}$
	- 可以看出来就是在单位摩尔下的热力学函数关系

##### 集合公式 (Additive formula)
就各组分的和等于总的
- $\sum n_{B}V_{B}=V$

##### Gibbs-Duhem 公式
把物质的某个状态描述求微分，$T,p$ 还有各个组分
 $$dV=(\frac{\partial V}{\partial T})_{p,n_B,n_C,\dots}dT+(\frac{\partial V}{\partial p})_{T,b_B,n_C,\dots}dp+\sum V_Bdn_B$$
### #化学势
##### 定义
$G$ 对 $n$ 的偏导，吉布斯自由能 $G$ 结合了系统的内能和对外界做功的能力，描述化学反应及相变十分有用
 $$\mu_B=(\frac{\partial G}{\partial n_B})_{T,p,b_C,\dots}$$
 - 与偏摩尔量相似，符合上述公式与性质（虽然我觉得那些公式没什么意义）
 - 说实话我觉得它上面讲的很多都是废话
 - $\mu_{B}$ 的绝对值是认为选择的，毕竟是叫势
 - 和热力学的一些基本式子结合
	 - $\mu=(\frac{\partial U}{\partial n_{B}})_{S,V,n_{c},\cdots}$
	 - $\mu=(\frac{\partial H}{\partial n_{B}})_{S,p,n_{c},\cdots}$
	 - $\mu=(\frac{\partial H}{\partial n_{B}})_{T,V,n_{c},\cdots}$
- 若条件不同，化学势也有不同的定义
$$\mu_B=(\frac{\partial G}{\partial n_B})_{T,p,n_C,\dots}$$
$$\mu_B=(\frac{\partial U}{\partial n_B})_{S,V,n_C,\dots}$$
$$\mu_B=(\frac{\partial H}{\partial n_B})_{S,p,n_C,\dots}$$
$$\mu_B=(\frac{\partial F}{\partial n_B})_{T,V,n_C,\dots}$$
##### 与温度和压力的关系
$$
\mu_{B}=f(T,p,x_{B},x_{C},\cdots)
$$
对于 $\mu_{B}=f(T,p)$
- $\mu_{B}$ 与 $T$：
$$
(\frac{\partial \mu}{\partial T})_{p,n_{B},n_{C},\cdots}=[\frac{\partial}{\partial T}(\frac{\partial G}{\partial n_{B}})_{T,p,n_{C},\cdots}]_{p,n_{B},n_{C}}
$$
$$
\qquad \qquad \qquad \qquad=[\frac{\partial}{\partial n_{B}}(\frac{\partial G}{\partial T})_{p,n_{B},n_{C},\cdots}]_{T,p,n_{C},\cdots}
$$
$$
\qquad \quad=[\frac{\partial(-S)}{\partial n_{B}}]_{T,p,n_{C},\cdots}
$$
$$
T \uparrow, \mu_{B}\downarrow
$$
- $\mu_{B}$ 与 $p$：
$$
(\frac{\partial \mu}{\partial p})_{T,n_{B},n_{C},\cdots}=[\frac{\partial}{\partial p}(\frac{\partial G}{\partial n_{B}})_{T,p,n_{C},\cdots}]_{p,n_{B},n_{C}}
$$$$
\qquad \qquad \qquad \qquad=[\frac{\partial}{\partial n_{B}}(\frac{\partial G}{\partial p})_{T,n_{B},n_{C},\cdots}]_{T,p,n_{C},\cdots}
$$$$
\qquad \quad=[\frac{\partial(V)}{\partial n_{B}}]_{T,p,n_{C},\cdots}
$$
$$
T \uparrow, \mu_{B}\uparrow
$$
- 注: 这里用到了某些推导式 $V=(\frac{\partial G}{\partial p})_{T}=(\frac{\partial G}{\partial p})_{S}$ $S=-(\frac{\partial F}{\partial T})_{V}=-(\frac{\partial G}{\partial T})_{p}$
##### 化学势判据
- 定组成系统，等 $T$ 等 $p$, $W'=0$
$$
dG_{T,p,W'=0}\le 0
$$
- 对于多组分均相系统: 
$$
dG=-SdT+Vdp+\sum\mu_{B}dn_{B}
$$
- 等 $T$ 等 $p$ , $W'=0$ 的过程，进行方向及限度的判据:
$$
\sum\mu_{B}dn_{B}\le 0
$$
- 简化，总的结果还是判定 $dG$ 是否小于等于零

