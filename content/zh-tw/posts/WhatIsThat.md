---
title: "蛤"
date: 2026-10-14T12:00:00+08:00
draft: false # true = draft, will not appear on the website; change to false to publish
tags: [example]
ShowToc: true
---

# 電子學筆記精簡版
>高二電子學

**本筆記為精簡版本，僅收錄部分重點，不涵蓋電子學全範圍，後續亦無擴充規劃。
*完整內容請參考課本***
內容僅供參考，可能會有一些錯誤，參考時請再自行核對

# 筆記編著者

[張博雅老師](https://hackmd.io/@nick15028)
![博雅](https://hackmd.io/_uploads/BkmCZOM-ze.png)

[wavevoid](https://hackmd.io/@voidSTU)

# 波形
| 波形 | 平均值${V}_{DC}$ (面積概念) | 有效值${V}{rms}$ (跟功率有關) |
| -------- | -------- | -------- |
| 正弦波 | $\dfrac{2}{\pi}{V}_{m}$ | $\dfrac{1}{\sqrt{2}}{V}_{m}$ |
| 鋸齒波 | $\dfrac{1}{2}{V}_{m}$ | $\dfrac{1}{\sqrt{3}}{V}_{m}$ |
| 方波 | ${V}_{m}$ | ${V}_{m}$ |

| 特殊名詞 | |
| -------- | -------- |
| 波形因數$F.F.$ | $\dfrac{{V}_{rms}}{{V}_{DC}}$ |
| 波峰因數$C.F.$ | $\dfrac{{V}_{m}}{{V}_{rms}}$ |

# 二極體
* PN接面為空乏區，P區帶負離子，N區帶正離子(帶電)

* 障蔽電壓$-2.5mV/^\circ C$

* 靜態電阻
> ${R}_{D} = \dfrac{ {V}_{D} }{ {I}_{D} }$

* 動態電阻
> ${r}_{D} = \dfrac{ {V}_{T} }{ {I}_{D} }$

* 電容特性
> ![二極體-電容特性](https://hackmd.io/_uploads/S1fvgQkVfg.jpg)

* 順向擴散電流
> $I_D = I_S \times ( e ^ { \dfrac{V_D}{ \eta V_T}} - 1)$
> 
> 濃度不同造成(多數載子)

* 逆向飽和電流(漂移電流)
> $I_{S2} = I_{S1} \times 2 ^ { \dfrac{T_2-T_1}{10} }$
> 
> 電場造成(少數載子)，固定值

* 溫度每上升$10^\circ C$，逆向飽和電流增加一倍

* 溫度 :arrow_up_small: ，導電性 :arrow_up_small: 

# 稽納二極體
* 只有逆向且崩潰時作為定電壓原

* 溫度係數$TC_{(T1)} = \dfrac{ V_{Z(T2)} - V_{Z(T1)} }{ V_{Z(T1)} \times (T_2-T_1) }$

# 整流濾波電路
>變壓 :arrow_right: 整流 :arrow_right: 濾波 :arrow_right: 穩壓

電壓調整率$VR = \dfrac{ V_{NL} - V_{FL}}{V_{FL}}$

漣波因數$r(\%) = \dfrac{V_{r(rms)}}{V_{DC}}$

## 半波整流
![整流濾波電路-半波整流](https://hackmd.io/_uploads/Sy9YIXkVfx.jpg)

$V_{DC} = \dfrac{1}{\pi} V_m$

$V_{rms} = \dfrac{1}{2} V_m$

$PIV = V_m$

## 中心抽頭全波整流
![整流濾波電路-中心抽頭全波整流](https://hackmd.io/_uploads/SkL1_QJVzl.jpg)

$V_{DC} = \dfrac{2}{\pi} V_m$

$V_{rms} = \dfrac{1}{\sqrt{2}} V_m$

$PIV = 2V_m$

## 橋式全波整流
![整流濾波電路-橋式全波整流](https://hackmd.io/_uploads/SypBq7kEMe.jpg)

$V_{DC} = \dfrac{2}{\pi} V_m$

$V_{rms} = \dfrac{1}{\sqrt{2}} V_m$

$PIV = V_m$

## 濾波
$V_{r(p-p)} = \dfrac{V_m}{ \tau f_o}$

$V_{r(rms)} = \dfrac{V_{r(p-p)}}{2 \sqrt{3}}$
> 若漣波類似三角波

## 漣波因數
* 半波整流$r=121\%$

* 半波整流濾波$r=\dfrac{4.8}{R_L C}$，$R_L$以$k \Omega$，$C$以$\mu F$

* 全波整流$r=48\%$

* 全波整流濾波$r=\dfrac{2.4}{R_L C}$，$R_L$以$k \Omega$，$C$以$\mu F$

* 加電容：輕負載

* 加電感：重負載

# BJT
>雙載子、電流控制

![BJT](https://hackmd.io/_uploads/rJbBy4kEGe.jpg)

* BE接面空乏區 < BC接面
> $W = \sqrt{ 2 \dfrac{\epsilon_s}{q} ( \dfrac{1}{N_A} + \dfrac{1}{N_D}) (V_{bi} - V_a) }$
> 
> | 符號 | 物理量名稱 |
> | -------- | -------- |
> | $W$ | 空乏區寬度 |
> | $\epsilon_s$ | 半導體介電係數 |
> | $q$ | 基本電荷量$1.6 \times 10^{-19} C$ |
> | $N_A$ | P參雜濃度 |
> | $N_D$ | N參雜濃度 |
> | $V_{bi}$ | 障壁電壓 |
> | $V_a$ | 外加偏壓 |

* BE接面電容量 > BC接面
> $C = \epsilon \dfrac{A}{d}$

* 由於BE接面濃度較BC接面高，$V_{BE} (0.7V) > V_{BC} (0.5V)$

* 電阻係數：C > B > E

* 多級串接，BW :arrow_down_small: 

# MOSFET
>單載子、電壓控制

![MOSFET](https://hackmd.io/_uploads/SkbMssgVMx.jpg)

* 飽和區$I_D = I_{DSS} \times ( 1 - \dfrac{V_{GS}}{V_{P}} )^2$

* 飽和區$I_D = K \times ( V_{GS} - V_T )^2$

* 歐姆區、飽和區、截止區判斷

|  | 歐姆區 | 飽和區 | 截止區 |
| -------- | -------- | -------- | -------- |
| $V_{GS}$ 在 $V_{GS}$ - $I_D$ 圖中的線上 | :white_check_mark: | :white_check_mark: | :x: |
| $V_{GD}$ 在線上 | :white_check_mark: | :x: |  |

* 歐姆區$I_D = K \times ( 2 (V_{GS}-V_T) V_{DS} - {V_{DS}}^2 )$

* DMOS、EMOS轉換：$K=\dfrac{I_{DSS}}{{V_P}^2}$

* $g_m = 2 \sqrt{K I_D}$
> $g_m = 2 K (V_{GS} - V_T)$
> $g_m = \dfrac{ 2 I_{DSS} }{ |V_P| } \times (1- \dfrac{V_{GS}}{V_P})$

# OPA
>運算放大器

## 構造
![OPA-構造](https://hackmd.io/_uploads/B1Uy12lNGg.jpg)

## 轉動率
轉動率$SR = \dfrac{d v_o}{d t}|_{\max}$

$v_o$為正弦波時，$f_{Max} = \dfrac{SR}{2 \pi V_m}$

## 微分電路
>瞬時斜率

![OPA-微分電路-電路](https://hackmd.io/_uploads/B17kE3xNfe.jpg)

* $v_o(t) = - \tau \times \dfrac{d v_i(t)}{d t}$

![OPA-微分電路-波形](https://hackmd.io/_uploads/rJI7bTeNMx.jpg)

* $\dfrac{d \sin(\omega t)}{d t} = \cos(\omega t)$

* $\dfrac{d \cos(\omega t)}{d t} = - \sin(\omega t)$

## 積分電路
>累積量

![OPA-積分電路-電路](https://hackmd.io/_uploads/HJ8xlYRPzl.jpg)

* $v_o(t) = - \dfrac{1}{\tau} \times \int_{0}^{t} v_i(t') \, dt'$

![OPA-積分電路-波形](https://hackmd.io/_uploads/BJrEQ6x4Mx.jpg)

* $\int \sin(\omega t) \, dt = -\frac{1}{\omega} \cos(\omega t)$

* $\int \cos(\omega t) \, dt = \frac{1}{\omega} \sin(\omega t)$

# 振盪電路

## 弦波

### RC相移
* 「至少」需要三組RC

* $A=-29$

* $\beta = - \dfrac{1}{29}$

>![振盪電路-弦波-RC相移-領先型](https://hackmd.io/_uploads/BkYmokcEzx.jpg)
>
>領先型RC相移$f = \dfrac{1}{ 2 \pi \sqrt{6} RC }$
>
>$\dfrac{1}{2 \pi \sqrt{6}} \approx 0.065$

>![振盪電路-弦波-RC相移-落後型](https://hackmd.io/_uploads/HJJGwx04Mg.jpg)
>
> 落後型RC相移$f = \dfrac{\sqrt{6}}{ 2 \pi RC }$
>
> $\dfrac{\sqrt{6}}{2 \pi} \approx 0.39$

### 韋恩橋式
![振盪電路-弦波-韋恩橋式](https://hackmd.io/_uploads/SJwOT-JrGg.jpg)

* 若 $R_1=R_2=R$ 且 $C_1=C_2=C$ ，則 $f = \dfrac{1}{ 2 \pi RC }$

* $A=3$

* $\beta = \dfrac{1}{3}$

* $\dfrac{R_f}{R_i} \geq \dfrac{R_1}{R_2} + \dfrac{C_2}{C_1}$
> $R_1、C_1$ 串聯，$R_2、C_2$ 並聯

### 考畢子
* 2C + 1L

* $f = \dfrac{1}{ 2 \pi \sqrt{L C_T} }$

### 哈特萊
* 2L + 1C

* $f = \dfrac{1}{ 2 \pi \sqrt{L_T C} }$

### 石英晶體
* 壓電效應產生振盪

* $f = \dfrac{1}{ 2 \pi \sqrt{L C_S} }$

* 特色：穩定、便宜

## 施密特
* 計算三步驟：

1. 列出$V_- =$

2. 列出$V_+ =$

3. $V_- = V_+$ 時，得轉折電壓

>反向施密特
>![振盪電路-施密特-反向施密特](https://hackmd.io/_uploads/BJ6GvQyBGe.jpg)

>同向施密特
>![振盪電路-施密特-同向施密特](https://hackmd.io/_uploads/BkQEDmySMl.jpg)

## 方波

### OPA
* 電路結構：微分電路(充放電)+反向施密特(方波產生)

![振盪電路-方波-OPA](https://hackmd.io/_uploads/HklNhXkHfl.jpg)

* $T = 2 RC \times \ln( 1 + \dfrac{2R_2}{R_1} )$
> $R_2$ 接地

### NE555無穩態
![振盪電路-方波-NE555無穩態](https://hackmd.io/_uploads/rJa5smmrMg.jpg)

* 高準位時間$T_H = 0.7 \times (R_1+R_2) \times C$

* 低準位時間$T_L = 0.7 \times R_2 \times C$

* 工作週期$D(\%) = \dfrac{R_1+R_2}{R_1+2R_2}$

* $T = 0.7 \times (R_1+2R_2) \times C$

* 若要完整方波( $T_H=T_L$ )，則加入二極體

* 提升 $R_2$ 電阻值( $R_2 >> R_1$ )，會越接近完整方波

### NE555單穩態
>單穩態和無穩態的差別，在於單穩態的「觸發」，例如：按鈕

* 正脈波輸出維持時間$t = 1.1 \times RC$

## 三角波
* 電路結構：同向施密特+積分(方波 :arrow_right: 三角波)

![振盪電路-三角波](https://hackmd.io/_uploads/SkMip-XHGx.jpg)

**記得檢查 $R_1、R_2$ 能否讓電路振盪**

* $T = 4 RC \times \dfrac{R_1}{R_2}$
> $R_2$ 跨接施密特

## 濾波

### 低通濾波
>高頻濾波器

![振盪電路-濾波-低通濾波](https://hackmd.io/_uploads/ry6ac18Bfg.jpg)

* 高頻截止頻率$f_H = \dfrac{1}{ 2 \pi R C }$

* $f = f_H$ 時，增益為原本的0.707倍( $\dfrac{1}{\sqrt{2}}$ )

* 頻率高於$f_H$ ，頻率每增加10倍，增益-20dB( x$\dfrac{1}{10}$ )

### 高通濾波
>低頻濾波器

![振盪電路-濾波-高通濾波](https://hackmd.io/_uploads/H1OkiyLrGx.jpg)

* 高頻截止頻率$f_L = \dfrac{1}{ 2 \pi R C }$

* $f = f_L$ 時，增益為原本的0.707倍( $\dfrac{1}{\sqrt{2}}$ )

* 頻率低於$f_L$ ，頻率每降低10倍，增益-20dB( x$\dfrac{1}{10}$ )

### 帶通濾波
>$A_v$ - $f$ 圖呈現「 布丁🍮 」狀

* 高通濾波、低通濾波「串接」

* 條件：$f_H > f_L$

### 帶拒濾波
>$A_v$ - $f$ 圖呈現「 凹槽¯\\__/¯ 」狀

* 高通濾波、低通濾波「加法器連接」

* 條件：$f_H < f_L$

## 整理表格
![doc00798520260612172758 1 of 1](https://hackmd.io/_uploads/r11GzUKbGe.jpg)