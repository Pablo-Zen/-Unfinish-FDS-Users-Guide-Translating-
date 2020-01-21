# (Unofficial) Translation of Fire Dynamics Simulator (Version 4) - User’s Guide  
(Unofficial) Fire Dynamics Simulator (Version 4) - User’s Guide Chinese version  
非官方翻译 FDS 用户手册  
原文：https://www.nist.gov/publications/fire-dynamics-simulator-users-guide-sixth-edition  
翻译: @Pablo-Zen https://github.com/Pablo-Zen  
声明：
对 FDS User's Guide 翻译是本人自发行为，与NIST无关，目的是方便自己和身边英语能力不足的朋友了解FDS工具的使用方法并锻炼英文能力，不对翻译内容负责。  
在翻译中本人尽可能使用符合中文语言习惯语句，但本人非流体力学、热力学、燃烧和传热领域专业人士，对专业术语、理论等内容没有掌握，而且是第一次翻译，难免存在错误，也未能保证原意的传达，在这里对我的责任态度表示抱歉。文中不确定之处会标注括号并给出原文。  
以下是翻译内容：
## 序言  

&emsp;&emsp;本手册是FDS系统的使用说明手册，内容里并不包含背景知识。
如果想了解具体的控制方程(Governing equations)、数学方法(Numerical methods)和验证等细节，请参考技术参考指南 ——《FDS Technical Reference Guide》。
虽然本手册中已经给出了使用本系统的必要说明，但还是建议您看看技术参考里面的背景知识。本手册只能指导您如何正确的输入参数。  
&emsp;&emsp;另外，本手册中也包含一部分关于SmokeView的使用说明，SomkeView是FDS附带的一个可视化程序，如果要了解这个程序的全部功能，请参考《User’s Guide for Smokeview Version 4》。
本手册只提供了关于如何将SmokeView应用在设计FDS计算中的简短教程。

## 免责声明
&emsp;&emsp;美国商务部(The US Department of Commerce) 不对FDS用户做任何担保，并且对用户的使用不承担任何责任。根据联邦法律，FDS用户对其是否恰当使用本工具自行负责，并且对通过本工具计算而得出的结论以及因使用了本工具分析而采取或未采取的行动自行负责。  
&emsp;&emsp;警告用户，FDS仅供在流体力学、热力学、燃烧和传热领域有专业能力的人使用，并且仅用于辅助合格用户的判断。该软件包是计算机模型，针对特定环境，本软件不一定能具有预测能力。缺少准确性的预测可能会得出有关消防安全的错误结论。所有结果都应由知情用户进行评估。  
&emsp;&emsp;本文件中提及的计算机硬件或商业软件并不受NIST认可，也不表示这些产品是最适合预期用途的产品。

## 致谢(暂未完成)

&emsp;&emsp;各类的火灾动力学模拟器的开发已经有近25年的历史了，然而公开发行的软件在2000年才出现。在许多人都致力于模型的开发和验证时，有一小部分负责起了计算机程序的开发。FDS技术参考指南里包含了大量模型贡献者的列表，而在这里我们表彰那些进行实际的编程的人。  
最初，基本流体动力求解器是由Ronald Rehm和Howard Baum设计的，并且得到了来自NIST计算与应用数学实验室(CAML)的Darcy Barnett、Dan Lozier和Hai Don以及建筑与火灾研究实验室(BFRL)的Dan Corley提供的帮助。

## 目录(暂未完成)
<!--todo 待生成目录 -->

## 第一章 简介
&emsp;&emsp;FDS是一种用来模拟火灾动力(fire-driven)中流体流动的计算流体力学模型(CFD)。
### FDS的功能和特点
## 第二章 获取FDS
&emsp;&emsp;FDS是由FORTRAN90语言开发的程序，用以解决热致流体流动和燃烧的控制方程。对这些方程的详细说明和其对应的数学方法见参考文献[1]。FDS的输出数据可以通过一个叫SmokeView的工具进行可视化，见参考文献[2]。
### 如何获取FDS
&emsp;&emsp;所有与FDS和SmokeView相关的文件能在这个网址中找到：  
&emsp;&emsp;http://fire.nist.gov/fds  
&emsp;&emsp;关于FDS的更新，bug修复等内容都可以在这个网站里找到。请注意FDS可能不会向下兼容，新的可执行文件名会像“FDS#.exe”这种带有版本号。不过SmokeView是向下兼容的，可以把旧版FDS输出用在新版SmokeView上，并且我们提倡使用新版本的SmokeView。  

## 第三章 使用FDS
