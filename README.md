# 控制：一种视角

大师经典连载第1期 控制：一种视角（第1部分），后续译文正在进行将陆续放出

翻译团队：。。。。、爻King灬、夜行、有梦才能飞翔、luoshi006、yestoday、进、TT、Hu1-Hui、黎明、阿伦、一字并肩王

审校：一字并肩王

编排：姚尧

联系邮箱：1063603770@qq.com

交流群号：239920039

**欢迎大家批评、建议，更欢迎更多同道中人加入翻译组！**

译者序

我们生活在一个信息技术主导发展的时代，计算机基础技术的革命几乎是这个时代所有技术进步的根本动力。而现代的控制科学和控制工程同计算机技术互相影响，使得这些学科融合为信息技术整体中无孔不入的成分。但凡信息技术能够波及的领域，都如燎原之火一般引发了各自的技术革命，航空技术就是其中一个典型。航空技术发轫于上世纪初，而它的几次重大技术变革都来源于电子信息领域的影响，特别是飞行控制。最近，信息技术在电子消费品领域的飞速发展让业已成熟的航空领域再次焕发生机。新元素与传统航空媾和，使无人机相关领域在短短的近几年内爆发出空前的高潮。商业资本的灵敏嗅觉也成为了这次高潮的催化剂，大量投机者跟随着金融浪潮卷入无人机江湖。

由于飞控系统是无人机的核心，对飞控开发人员的需求也因这次高潮而突然增加。因此，大势所趋大量IT界人士转入了飞控开发的大军，并因为人数优势成为了主力。而原本的控制和自动化专业的人才却沦为大军中的小众。因为IT人士不熟悉控制学科背景，导致很多在其他应用领域成熟而好用的控制学科宝贵遗产没有在飞控开发中承接过来，传统有人机飞行控制也没有在无人机飞控领域得到全面继承。同时，由于社会历史渊源，控制学界盛行的沽名钓誉、华而不实之风造成理论与应用间的鸿沟日益扩大，以至于很多控制专业的人默认了这种割裂，更多自诩为“学控制”的人则沦为所谓“学术声望”的奴隶。这样堪忧的态势也让一些控制学界的领袖们做出了振聋发聩的呼吁，本文的第一作者K.J. Åström就是毕生致力于构建连接鸿沟两岸桥梁的大师。真正理论与应用的统一才是控制的至美之境，哪怕现在仅能取得一小点贯通都令人欣喜若狂。而最近的无人机高潮却为隔岸相对的两类人提供了水到渠成的沟通契机。这两类人不应因学科语言差异而互相歧视，因为只有两者紧密合作、加强交流才可能从各自的此岸顺利到达彼岸，才能利用现在这个历史机遇期接近至美之境。不拘财富、名声与权位，这些真正向往技术、追求真理、渴望至美之境的人才是人类文明的真正推进者，才是贵族精神的代表。

翻译小组水平有限，翻译大师的作品难免流于孤陋，只希望以此译作让更多初心未泯的芸芸众生略微公平地享有接近至美之境的权利，让这些人类文明的真正推进者不再因孤军奋战中遭遇的全方位打击、排挤和重重困难而感到走投无路。

一字并肩王

**作者简介：**

**Karl J. Åström** 早年就读于斯德哥尔摩的皇家理工学院 (KTH) 。为IBM研究院工作了5年后于1965年在隆德理工大学/隆德大学创建了自动控制系，被聘为该系的客座教授。他现在是隆德大学的高级教授。Åström对于控制的兴趣广博，位于国际自动化学会高引作者之列（ISAHighlyCited）。是IEEE终身会士，他的Erdös数为3。他收获了众多殊荣，包括1987年的国际自动控制联合会（IFAC）Quazza奖章、1990年IEEE控制系统奖、1993年IEEE荣誉奖章和6个荣誉博士学位。他是瑞典皇家科学院、瑞典皇家工程科学院以及美国工程院的院士。

**P.R. Kumar** 来自德州农工大学。之前曾在马里兰大学巴尔的摩郡分校（UMBC）的数学系、伊利诺伊大学厄巴纳-香槟分校（UIUC）的电子和计算机工程专业（ECE）与该校的计算机科学实验室（CSL）效力。他是IEEE会士、美国工程院院士和发展中国家科学院（the Academy of Sciences of the Developing World）院士。他曾被苏黎世联邦理工大学（ETH）授予荣誉博士学位，获得过国际计算机学会（ACM）可移动系统特殊兴趣团体（SIGMOBILE）的突出贡献奖、IEEE控制系统领域奖、IEEE通信学分会的Ellersick奖、美国自动控制委员会（AACC）Eckman奖。他是印度理工学院孟买分校（IIT Bombay）的D.J. Gandhi杰出访问教授、印度理工学院海得拉巴分校（IIT Hyderabad）的荣誉教授，还是清华大学无线通信客座教授组的带头人。他获得了印度理工学院马德拉斯分校（IIT Madras）的杰出校友奖、华盛顿大学校友成就奖和UIUC的Drucker Eminent教师奖。

控制：一种视角

**Karl J. Åström <sup>a</sup>, P.R. Kumar <sup>b</sup>**

（a 瑞典隆德大学自动控制系、b 美国德州农工大学电子与计算机工程系）

电子邮箱：kja@control.lth.se (K.J. Åström), prk@tamu.edu (P.R. Kumar)

**摘要**

反馈是个古老的想法，但反馈控制却是个年轻的领域。很久以前，大自然就发现了反馈，因为它是生命与机体平衡所必需的。在工业革命中，反馈控制对于利用能源至关重要，而今天反馈控制在我们身边随处可见。这个领域的发展涉及工程师、数学家、经济学家和物理学家所做的贡献。反馈控制是第一个系统学科；它代表了一种思想变革，因为反馈控制不仅深刻影响了诸如航空、化学、社会、电气和机械等工程学科，也深刻影响了经济学和决策研究。控制的视野使得它成为经典的多学科领域。这个学科发展历程的复杂故事引人入胜，本文给出的视角关乎这个学科的成长。本文还讨论了工业、应用、技术、理论和研究这几者之间的交互影响。

1.  简介

很久以前，大自然就发现了反馈。它创造了反馈机制并且在各个层次利用这些机制，它是机体平衡和生命的核心。控制作为一项技术至少可以追溯到两千年前。古代有很多控制的例子（Mayr，1969）。Ktesibios（公元前285-222年）发展了一种调节水流的反馈机制来改善水钟的精度。在现代，吉姆斯.瓦特（James Watts）把离心调速器用于蒸汽机成为了工业革命的基础。从此以后，自动控制成为了如下的十九和二十世纪工程体系得以成功的关键。这些工程体系包括：发电和输电、远程通讯、过程控制、船舶驾驶、车辆和飞机的控制、生产决策和仓储系统以及互联网上数据包流量的调节。它照例连同大系统中的传感器和执行器等工业部件共同使用。今天，控制无孔不入地存在于我们的家庭、汽车和基础设施中。在如今的后基因组时代里，系统生物学研究者的关键目标是理解如何干扰导致疾病的有害生物学路径的反馈。控制的理论和应用正在各个领域快速增长。

控制从一个古老技术到现代领域引人入胜的发展历程是现代工业社会繁荣的缩影。这个调研除了本身的乐趣外，还洞察了理论、技术和应用在学科发展中如何互动的细节。关于控制的发展以及它如何出现、如何发展起来，本文提供了一个视角，但绝不是包罗万象的。为了描述这个领域，我们已经些许随机地选取1940年、1960年和2000年作为四个时期的分界点，后面章节的题目概括了这四个时期：初尝反馈控制威力（1940年前）、领域初现（1940年-1960年）、黄金年代（1960年-2000年）和未来体系（2000年后）。我们将理论与应用交互的复杂性反映在后续的章节中。

直至20世纪中叶，自动控制才作为独立但多学科的学科出现。国际自动控制联合会（IFAC）成立于1956年（Kahne，1996；Luoto，1978；Oldenburger，1969），第一次IFAC国际大会于1960年在莫斯科召开，而《自动化》期刊（Automatica）出现于1962年（Axelby，1969；Coales，1969）。截至2000年，IFAC已经扩大至66个技术委员会。控制作为一些技术领域的关键必备因素，是多学科的典型。这种多学科性明显反映在在各色组织中，如美国航空航天学会（AIAA）、美国化学工程师学会（AIChE）、美国机械工程师协会（ASME）、美国电气电子工程师学会（IEEE）、国际自动化学会（ISA）、国际建模仿真学会（SCS）和美国工业与应用数学学会（SIAM），这些组织都包含在美国自动控制委员会（AACC）和IFAC中。

控制的多学科性的另一层含义是，当为控制搜罗可用的理论和原理时，物理学家、工程师、数学家、经济学家和其他人都对它的发展做出过贡献。物理学家麦克斯韦（Maxwell）奠定了调速器的理论基础（Maxwell，1868）。后来，James、尼克尔斯（Nichols）和Phillips分别作为物理学家、数学家和工程师合著了最早的一部控制书籍（James, Nichols, & Phillips, 1947）。数学家理查德.贝尔曼（Bellman, 1957b），Solomon Lefschetz（Grewal & Andrews, 2010） 和L.S.庞特里亚金（Pontryagin, Boltyanskii, Gamkrelidze, & Mischenko, 1962）对现代控制理论的早期发展做出了贡献。确实，对于数学严谨性的尊重是控制系统研究的特质，这一点或许从电路理论那继承而来（Bode, 1960; Guillemin, 1940）。

控制理论就像工程科学的很多其他分支一样，它的发展模式和诸多自然科学相同。虽然自然科学与工程科学有强烈的相似性，但也存在一些基本的差别。一方面，自然科学的目标是理解自然现象。其核心目的向来是发现自然定律、赢得盛名和诺贝尔奖。自然科学向来大力强调简化主义，需要对特殊的现象分离，一个极端的例子就是粒子物理学。但另一方面，工程科学要理解、发明、设计和维护人造工程系统。一个主要挑战是发现那些有助于有效地理解和设计复杂物理系统的系统原理。反馈，作为控制的核心，就是这样的原理。虽然纯粹的简化主义已经在自然科学取得极大的成功，但它对于工程科学却不那么给力，因为对于工程系统互动是必需的。

已经做出的很多对于控制的综述都会联系到各种周年纪念。IFAC于2006年9月在Heidelberg举办了一个研讨会来庆祝它成立50周年（IFAC, 2006）。《自动化》期刊于2014年庆祝了它成立50周年（Coales, 1969）。一篇通俗的关于传感器和工业控制器的综述发表在国际自动化学会（ISA）的59周年庆典上（Strothman, 1995）。美国机械工程师协会（ASME）在1993年发表了一系列关于控制历史的论文，这些发表与《Journal Dynamic Systems, Measurement, and Control》杂志的50周年庆典有关（Rabins, 1993）。IEEE控制系统学会支持了由编委会挑选出的25篇经典控制理论论文的重印工作（Başar, 2001）。《The European Journal of Control》杂志在2007年1月发表了一个专栏：X世纪控制科学的黎明和发展，在专栏中研究者们反映了他们关于控制科学发展的看法（Bittanti & Gevers, 2007）。一篇关于控制系统工程历史的专栏发表于1984年，正值IEEE百周年纪念。IEEE控制系统学会2009年在德国的Berchtesgaden组织过一次关于控制影响的研讨会：过去、现在和未来。来自研讨会的材料汇集了大量的成功案例和重大挑战，被总结进一个通俗报告（Samad & Annaswamy, 2011）。美国工程院（National Academy of Engineering）发表了两本则关于世纪之交未来工程的调研报告（NAE, 2004, 2005).）他们指出了系统与日俱增的重要性和建模仿真在基于计算机设计与工程中所担当的角色。美国空军科研办公室（AFSOR）支持了关于控制、动力学与系统未来方向的一系列调研，得出了一个通俗报告（Murray, 2003），这个报告是由Murray,、Åström、Boyd、Brockett和 Stein (2003) 总结的。

控制这个领域甚至在吸引历史学家，或许这意味着控制的复杂发展过程需要被澄清。有的书关于控制历史(Bennett, 1979, 1993; Bissell, 2009)， 有的书关于个人研究者(Hughes, 1993)， 还有的关于组织和工程(Mackenzie, 1990; Mindell, 2002, 2008)。在很多控制会议中也安排有关于这个领域历史的分会。

有违常理的是，尽管控制被广泛应用，但在专家群体外却不常被论及；实际上，控制有时被叫做“隐性技术”(Åström, 1999)。其中一个原因可能就是它成功隐形以至于全部注意力都被钉在了最终的设备产品上。相比于讨论设备，讨论反馈观点更加困难。另一个原因是控制科学家还没有对于科普写作给予足够的关注；但1952年的科学美国人却青睐于“自动控制”这个专题，是个突出的例外(Brown & Campbell, 1952; Tustin, 1952)。

截至1940年，控制被大范围地应用于电气系统、过程控制、远程通信和船舶驾驶。数千的调节器、过程控制器、陀螺-罗盘系统和陀螺驾驶仪被生产。基于机械、液压、气动和电动技术，控制器被用作特殊目的的模拟设备。为了从非线性器件中获得鲁棒线性行为，反馈被大范围地使用；最初发明它是用来模拟控制系统(Holst, 1982)。过程控制和火力控制系统对于中心控制机房的需要驱动了通信发展(Holst, 1982)，从控制威力中得到的收益成为了驱动力。

在这个时期，虽然不同工业中的基本原则是相似的，而系统的共性却没有被广泛理解。一个震撼的例子就是，诸如积分和微分作用的特点在不同应用领域反复被发明和多次申请专利，而它们的理论基础是线性化模型和劳斯-赫尔维茨（Routh–Hurwitz）稳定性判据。一些教材已经出现 (Joukowski, 1909; Tolle, 1905)。这时期的研发主要在工业部门进行。

由于控制经历了第二次世界大战的发展，它在1960年产生为一个领域。伺服控制理论成为了理论基础。基于数据的建模工具即频率响应的使用，连同分析与综合方法这时都得到确立。模拟计算机既用作一种控制器应用技术，也用作仿真工具。很多发展是由应用和实际需求所驱动的。经历了长期和复杂的进化后，才终于出现了理论与应用乃至不同领域应用的整体性观点。控制系统被大量生产，大公司有了控制部门，而且有的公司专营控制。国际组织IFAC成立了，它的第一次世界大会于1960年在莫斯科召开。这个时期主要的研发是在研究所，或以一些大学同工厂合作的方式完成的。截至1960年，60多本关于控制的书籍已经被出版。

但是，很多改变起始于1960年前后；数字计算机、动态规划(Bellman, 1957b)、控制的状态空间方法(Kalman, 1961a)和线性二次型调节器(Kalman, 1960)出现了，而卡尔曼（Kalman）滤波器也即将登场(Kalman, 1961b)。控制的发展开始活跃，因而这个时期被誉为黄金时代。这个时代的挑战来源于太空竞赛和计算机控制在过程工业和其他很多应用中的引入，例如汽车和便携电话。这个时期，应用增长快速、理论进展非常活跃且很多附属专业也随之发展。相关大学教育在本科生和研究生层次迅速扩大。这些现象导致的一个结果是经历数十年而取得的理论与实践间的平衡被再次破坏，但这一次失衡的方向却与上次相反。纯理论很大程度上抓住了人们的注意力，并且在一些人中出现了一种观念：“鸿沟”出现(Axelby, 1964)，整体观点已经丢失(Bergbreiter, 2005)。

关于最近的事件当然很难提供一个好视角，但我们的观点是：有迹象表明还有其他的重要发展和突破正在进行。截至大约2000年，由于有线和无线网络的出现和增殖、传感器的发展、计算机的强大和软件的复杂，技术方向已经出现了变迁。那么在世纪之交出现了新的挑战：网络控制与通过网络控制、可验证的安全嵌入式系统设计以及复杂系统的基于模型设计和自主性。那么技术能力戏剧性的增长提供了很多机遇，也呈现出很多挑战，应对这些挑战需要控制同计算机科学和通信紧密集成到一起。这个认识产生很多重要研究项目，例如欧盟的ARTIST2 (0000)和ArtistDesign (0000)项目聚焦于嵌入式系统，还有美国的信息物理系统（Cyber–Physical Systems）(Baheti & Gill, 2011)。

物理、生物和医药正在更加紧密地互动。控制在诸如自适应光学和原子力显微镜等设备中成为关键因素。量子和分子系统的控制也正在被探索。使用系统与控制的观点可能获得更深的生物学视野，对于这类需要和兴趣业已增加。系统生物学领域已经诞生，而且创建了控制科学家和生物学家的共同团队；值得一提的是工程学院设立了生物工程系。

1.  初尝反馈控制威力（。。。。译）

工业革命的推行需要动力，尤其需要可控的蒸汽动力。因此控制在工业革命期间获得极大发展。反馈控制是一种强有力的工具，它能减小外部干扰和过程变化的影响，从而可以用性能差的组件构建一个性能良好的系统或者使不稳定的系统稳定。反馈控制的主要问题是会产生系统的不稳定性，在识别和解决这些问题的时候使得控制得到重大发展。随着工业革命进行，新的工业和技术革新让控制学成为电子、化工、电信和其他工业的核心部分。从此控制革命和工业革命就紧紧的联系到一起。

**2.1.离心调速器（。。。。译）**

对控制设备的需要此时已经出现在风车的操作上。回溯到1745年，当时发明的离心调速器就是为了风车保持恒定转速运行(Mayr,1969)。类似的需求也出现在使用蒸汽动力的纺织业，他们需要使织布机和其他机器保持恒定转速。吉姆斯.瓦特成功地改造了离心调速器，并将其用于蒸汽机并在1788申请了专利。

离心调速器包含传感、执行和控制。设计调速器是一个折中办法：需要重的飞球产生大的驱动力，但是也会导致反应迟缓。实践上还遇到了机械设施中摩擦力和间隙的难题。基本的调速器产生比例作用，因为飞球连杆与转轴的角度同转轴速度成比例关系。这样的调速器会产生稳态误差，但是附有积分作用的控制器却具有总能接近正确稳态的特质，如果闭环系统是稳定。1790年左右，Pérrier兄弟设计的调速器中引入了积分作用。他们使用了一个液压装置，在装置中流入容器的液体量和速度成比例关系，而且蒸汽阀由液位控制(Mayr, 1969, p. 110–113)。1845年，Werner和William Siemens通过差速齿轮引入了积分作用(Bennett, 1979, p. 21–22)。Siemens兄弟还基于惯性轮引入了微分作用。自此调速器成了蒸汽机不可分割的一部分，而在18世纪末的后200年调速器也得到了发展。Bennett对此进行了详细的描述 (Bennett. 1979) 。

调速器的理论研究是从麦克斯韦（Maxwell） 的论文开始的 (Maxwell. 1868) 。他分析了线性模型还证明了积分作用的优点。他同时发现可以通过闭环系统特征方程的根确定系统的稳定性。麦克斯韦推导出三阶系统的稳定性判据并求助于劳斯（Routh），后者解决了一般性的问题 (Routh, 1877)。Vyshnegradskii独立于麦克斯韦分析了带有调速器的蒸汽机，也开发出一个三阶系统的稳定性判据(Vyshnegradskii, 1876)。Vyshnegradskii的工作是工程导向的，而且与调速器的设计紧密结合。他被训练成为一名数学家还是圣彼得堡国立技术学院的主任。在那里他开创了有强大科学基础的机械制造课程。他在沙皇俄国财政部长的任上结束了他的事业生涯(Andronov, 1978)。

Vyshnegradskii的研究成果被Stodola用来设计水轮机调速器。他用到了更复杂的模型还求助了他在苏黎士联邦理工学院（ETH）的同事赫尔维茨（Hurwitz），后者主要帮助做稳定性分析。赫尔维茨用不同于劳斯的其他方法推导出一个一般性的稳定性判据(Hurwitz, 1895)，即今天众所周知的结论—劳斯-赫尔维茨判据。Stodola还引入了无量纲变量和时间常数。Andronov(1978)、Bennett(1979)、Bissell(1989)和Profos(1976)提供了关于麦克斯韦和Vyshnegradskii工作的有趣观点。这时的科学家们很少互动(Gantmacher, 1960, p.172–173)。劳斯和赫尔维茨没有意识到彼此的贡献，而且他们也采用了不同的数学技巧 (Lyapunov,1892)。Stodola只是在他后来的文章中提到了劳斯(Andronov, 1978)。

19世纪初期牢固建立了控制带调速器机器的工程学基础。许多公司发明和制造了调速器。据Bennett(1979, page74)说，在1868年，英格兰安装了75000多台调速器。人们理解了比例积分和微分的作用并将其应用在机械和液压装置上。这些理论基础是建立在麦克斯韦、Vyshnegradskii和劳斯-赫尔维茨判据的研究成果上。控制的教育是从少数大学开始的。Tolle在1905年将研究成果编辑到教科书《Der Regelung der Kraftmaschinen (Control of Power Machines)》中。分析和设计都是在线性化和检验特征方程根的基础上。在1909年，莫斯科大学的空气动力学家Joukowski出版了第一本控制方面的俄文书《The Theory of Regulating the Motion of Machines》。

**2.2 发电和输电（爻King灬译）**

电力工业出现于十九世纪后期，并在二十世纪初飞速增长。最初，电是由水涡轮或锅炉-涡轮机组产生的，并分布于本地的直流电网中。涡轮和锅炉的控制是2.1节讨论内容的主要应用领域。虽然调速器的早期发展很大程度依赖于经验，但是电力行业需要开始发展和应用系统的方法和理论。Vyshnegradskii的论文(Vyshnegradskii, 1876)对工程实践具有重大影响，并广泛应用于涡轮控制系统（Andronov, 1978）。Tolle的书(Tolle, 1905)在1909和1929重印了2次，并在很长一段时间内作为电力控制的标准文献。

生产和消耗差额的增加产生了新的控制问题。许多发电机接入大型电网，目的是提供充足的电力和提高可靠性。随着电网的扩张，挑战出现了。所有发电机经直流转交流传输后都必须进行同步，因而在频率和电压控制方面就会遇到稳定性问题。为了安全运行，必须了解发电机对负载变化、故障、雷击等干扰的响应。在18世纪后期，Charles Steinmetz通过在交流电分析中引入“复数”和相量，奠定了交流电分析的基础(Steinmetz, 1916)。但这项工作只能解决稳态行为，并不能处理动态系统。针对这一情况，工作于麻省理工学院Vannevar Bush手下的Harold Hazen在上世纪20年代末构建了一个“网络分析仪”。分析仪是一个电力系统的实验室模型，由相移变压器和输电线路构成，它可以利用电话交换机的插线板重构。通用电气（General Electric）和其他电力公司仿制了这套系统。

电力行业的出现改变了以前的竞争规则，因为它是由大型工业同扮演重要角色的公共和国家公用事业联合发展的。由于需要安全地运营大型网络，公用事业和电力公司都设立了用以理解、设计和运营电网的研发团队。这些公司包括通用电气，西屋电气（Westinghouse），瑞典通用电气（ASEA），英国广播公司（BBC），阿尔斯通（Alstom），以及欧洲很多公共和国家公用事业公司，如意大利国家电力公司（ENEL）、法国电力公司（EDF）和瑞典国家电力局。作为研发团队中的一例，由托马斯.爱迪生（Thomas Edi）、Willis R. Whitney和Charles Steinmetz在1900年创立的通用电气研究实验室，是美国第一个工业研究实验室。

**2.3 工业过程控制（夜行译）**

过程和制造工业的自动化发轫于十九世纪末期，并在二十世纪初加速发展。化工、石油、造纸、制药工业的生产过程需要精确地控制压力、温度和流量来得到好的产品质量。锅炉、反应堆、精馏塔、混合器和搅拌器是典型的工业过程。多种用来测量不同物理量的传感器被研制了出来。典型的控制机构是阀门和气泵，利用气动设备完成感知、执行和控制功能是 常用的技术。传感器和执行器必须安装在工业过程的环境中。最开始，控制器也和工业过程设备安装在一起。他们通过压力信号同传感器和驱动器通信。连接器、压力管以及信号水平（3-15psi）成为标准，从而使得不同厂商的设备可以协同工作。后来，控制器被合并移动到中央控制室，也在那里提供仪器记录信号，这样极大地简化了操作人员的工作环节与工作环境。

那时的控制器发展并不是由理论推动的，而是基于工程应用的考量。通过修葺，人们重新发现了积分和微分的效用。对泰勒仪器公司（Taylor Instrument Company）齐格勒（John Ziegler）的采访(Blickley, 1990)给出了这样的观点:

“研发部的一些人在修葺一种称为Fulscope的气动比例积分控制器，反馈给容器的线路以某种方式得到了限制，这个限制产生了波纹管中的跟随特性。他注意到这个方法对于输出有奇特而显著的作用。他们在人造纤维粉碎机上试验了这个方法，获得了完美的温度控制结果。”

控制器组件也被用作气动模拟控制器来仿真工业过程。因为模拟器使用了气动信号，所以可以很方便地连接到气动控制器。反馈在传感器、执行器和控制器本身中广泛使用。关键思想是用高增益的气动放大器以限制量的形式把被动部件组合起来，从而产生优良的线性行为。这同后面2.6节讨论的反馈放大器十分相似。

控制器开始变成一种标准化的通用型设备，而不再是为像调速器这样的特殊过程而构造，并且它们还配备了刻度盘来调节PID控制器的参数。最早的通用型PID控制器是由Foxboro研发的Stabilog，它的增益可以在0.7~100之间调节。它在1931年出现，很快其他厂商就开发了相似的产品。因为同一个过程可能会用到很多控制器，因此人们需要一种为不同过程的控制器寻找合适参数值的方法。齐格勒和尼克尔斯发展了一套整定准则(1942)，仅需在这些过程中做一些简单的实验就可以确定控制参数。

传感器、仪表和控制器的出现使得一些新公司随之诞生。工业界变得高度多样化，到二十世纪三十年代中期已有超过600家控制公司，其中的领先者包括Bailey、Brown、Fisher & Porter、Foxboro、Honeywell、Kent、Leeds & Northrup、西门子（Siemens）、泰勒仪器和Yokogawa(Strothman, 1995)。Bennett (1993, p. 28)估计在1925-1935年间美国共卖出了约75000个控制器。

过程控制的工业结构与通信和电力行业是不同的。想法并没有得到广泛传播，而是作为商业机密被保护起来。过程控制领域有大量的公司。通信和电力行业可获得的集中资源正是过程工业所缺少的，就像前两者缺少理论基础一样。

**2.4船舶驾驶（有梦才能飞翔译）**

在船舶驾驶中有很多有趣的发展故事。由于大型船舶需要很大的力量去转动船舵，所以驱动成为了一个关键的问题。“伺服电机”一词由发明液压舵机的法国工程师Farcot所创造(Bennett, 1979)。这些提供驱动的装置是实现船舶驾驶自动化的重要组成部分，控制也得益于传感器的进步。

在船舶驾驶方面取得的重大进展受到了探究陀螺效应的启发。基于陀螺效应收集的想法和发明的装置已经产生了重要的影响，被标志为“陀螺文化”(Mackenzie, 1990; Mindell, 2002, 2008)。

首个陀螺罗经是由Anschütz-Kaempfe设计的，他在1905年创立了安修茨（Anschütz）公司。这个公司与Max Schule合作，Max Schuler是哥廷根大学应用力学研究所的负责人.他发明了一种巧妙的技术使得陀螺罗经对于船舶运动不敏感（Schuler tuning）(Schuler, 1923)，同时他也在大学教授控制课程(Magnus, 1957; Schuler, 1956)。

1910，Sperry创立了Sperry陀螺仪公司，该公司主要研究陀螺罗经与基于陀螺仪的很多其他装置。几年以后，Brown公司也开发了陀螺罗经，并因为知识产权同Anschütz打了几场官司(Mackenzie, 1990)。Sperry把陀螺罗经与电机连接到方向盘上获得了陀螺驾驶仪，通过观察有经验的领航员，Sperry发现：

“一个有经验的舵手应该会‘压舵’，也就是先回舵再将舵盘停在与回舵方向反向一点的位置，从而防止船舶的角动量过大使船舶错过它期望的航向。”

Sperry尝试利用这种方式开发了一个机电设备，这个设计被妥善记录在Bennett(1979),Hughes(1993),和Mindell (2002)的著作中，他设计的是一个典型的PID控制器。压舵的函数通过微分作用获得，积分作用通过电机驱动方向盘获得。作用的大小常常基于开关设备，利用反馈获得线性行为。Sperry陀螺驾驶仪缓解了舵手通过调整舵来保持航向的乏味工作。陀螺驾驶仪可以调整控制器参数，也可以设置目标航向，还有一个杠杆可以连接和断开陀螺驾驶仪。Sperry的陀螺驾驶仪绰号为“Metal-Mike”，它是非常成功的。Sperry还提供了记录仪以便对比自动和手动驾驶的误差。在1932年，该系统安装超过了400个 (Hughes, 1993)。

在船舶驾驶方面，一些有趣的理论进展归功于在圣彼得堡皇家技术学院就读的Minorsky (1922)。他提出了控制器的分类，并推荐在船舶航向控制中使用PID控制器。他的设计方法基于简单的线性模型，即今天我们所谓的极点配置法。Minorsky 测试了组建的自动驾驶仪，但是它没有商品化，而是把他的这个专利卖给Bendix (Bennett, 1993)。后来Minorsky成为了斯坦福大学的教授，并写了一本关于非线性振动的书 (Minorsky, 1962)，在Bennett的书 (Bennett, 1979, p.147–148)和文章(1984)中，有趣地讨论了Sperry、Minorsky和Anschütz的贡献以及他们在自动驾驶仪设计方面的影响。

船舶驾驶中新的控制问题出现在第一次世界大战期间，同海军现代化的强化计划有关(Bassett, 1950)：

“由陀螺罗经和数据发送中继器触发，自动将目标方位，炮塔角度，真方位角和船舶航向从甲板发送到绘图室再到炮的可能性开拓出新的广阔领域。”

目标方位和距离通常由船上瞻前顾后的光学设备测得。目标的预期位置可以计算得到，大型炮塔可以通过伺服机构瞄准。同步电机将信息从光学设备发送到计算机，或从模拟计算机发送到伺服机构。那时的计算机是使用盘-轮式积分器的模拟机电设备(Mindell, 2002)，由福特仪器公司（Ford Instrument Company），通用电气公司和Sperry公司生产。

**2.5飞行控制（luoshi006译）**

19世纪已经有许多载人飞行试验。莱特（Wright）兄弟成功的一个原因是他们理解了动力学和控制之间的关系。1901年，威尔伯.莱特（Wilbur Wright）在美国西部工程师学会（Western Society of Engineers）演讲时，如下表述了这个观点（McFarland, 1953）：

“人类已经知道怎样制造机翼 ... 人类也知道怎样制造引擎 ... 研究飞行问题的学生面对平衡和操纵仍然无能为力...当这个问题被解决的时候，飞行的时代也将到来，因为其他的问题都是次要的。”

莱特兄弟通过将他们的洞察力与熟练的试验技巧相结合，在1905年实现了第一次成功飞行。1955年5月19日，Charles Stark Draper在皇家航空学会（Royal Aeronautical Society）举办的第43届威尔伯.莱特纪念演讲（Draper, 1955）中给出了他们成功的一个有趣的观点：

“莱特兄弟否定了‘飞行器应该天生稳定以便飞行员只需操纵飞行，而不需要维持稳定’的理论。相反，他们特意制作了不稳定的飞机，依靠飞行员操纵可动舵面使得“飞行员+飞机”整个飞行系统稳定。最终，机动性和能控性增加了。”

莱特飞行器（Wright Flyer）的不稳定现象刺激了自动驾驶仪的发展（Hughes, 1993）。Sperry根据他对陀螺仪和船舶自驾仪的理解设计了飞机自驾仪。姿态的偏差由陀螺仪感知，方向舵和副翼由气动部件驱动。1912年在巴黎举办了规模宏大的自驾仪竞赛，Sperry的儿子Lawrence不用手操作实现了贴地飞行。同时，他的机修工在翅膀上行走来展示自驾仪能够应对干扰。

莱特兄弟的成功是我们现在所谓的集成的过程和控制设计的早期案例。其核心思想就是自动控制给予设计者额外的的自由度。莱特兄弟制造了机动性强的飞机，这种飞机依靠飞行员稳定。Minorsky也深刻体会到这些问题，他一语道破（Minorsky, 1922）：“古谚云：稳定的船只难驾驶。”人们观察到的有趣现象是，现代高性能战斗机被设计成不稳定的；这类飞机依赖于自动控制系统来稳定。

随着自驾仪的发展，德国兴起了强大的陀螺仪文化（Oppelt, 1976）。Lufthansa于20世纪20年代进行了国际长途飞行，于是有了方向控制的需求以便在所有天气条件下安全飞行。德国的Askania、西门子和Möller–Patin公司开发了与Sperry设备竞争的自驾仪。

Sperry继续开发自驾仪，精炼后的A-2模型使用了空气驱动陀螺仪和气动液压执行器。1993年，Sperry的A-2自驾仪用于Wiley邮政（Wiley Post）的单人环球飞行，这次飞行公开展示了自驾仪的优势。早在20世纪30年代，航空公司就开始引入自驾仪，像Bendix和Honeywell这些公司也开始制造自驾仪。

自驾仪在分立组件和整个系统中都大量使用了反馈。虽然早在1911年，基于线性方程和特征方程分析的飞行动力学已经有了良好的理论基础。但是，直到20世纪50年代中期，理论工作才对实际的自驾仪设计产生影响（McRuer & Graham,1981）。原因之一是缺少计算工具。就像船舶驾驶一样，那时的工程能力比理论更重要。

**2.6长途电话（yestoday译）**

Graham Bell 在1876年为电话申请了专利。最初，电话是通过转接板连线到中转中心的。电话的数量急剧增长。许多通话是用分频的方法在同一线路中传输的。电话行业集中程度之高甚于电力行业，因为它是由私有公司或国家垄断组织和行业所推动的。

横贯美国大陆的电话行业的增长是通信，也是控制间接而深刻的驱动力之一(Mindell, 2002)。1887年左右，Oliver Heaviside表明增加线路中的电感可以减少信号传输中的失真。1899年，哥伦比亚大学的 Mihajlo Pupin申请了加感线圈（loading coil）的专利(Pupin, 1899)，与此同时，AT&T的George Campbell在1900年将加感线圈改进并应用在了电话线路上。这项技术随后被用于长途线路和线缆上。但是，长途信号是被动传输的，同时加感线圈技术在1911年左右达到了它允许的信号失真和衰减的极限。该项技术在纽约丹佛的线路上进行了使用。在1913年，AT&T买下了当时由Lee de Forest在1907年发明的三极管技术(Lee_De_Forest, 1906)，并将其由Harold Arnold进一步开发。它使用了八个中继放大器连接纽约和旧金山，将线路从丹佛延长到了加利福尼亚。中继器的数量因更多的城市互联而增加，但就像Bode所指出的(1960)，失真在这之后成为了一个主要的问题：

“大家都毫无疑问对自家高保真系统的音频放大器感到骄傲，但是我估计你们当中不会有很多人乐意听信号经过几十甚至几百个你们家里那种良好的放大器串联后得到的声音。”

因此，利用多路复用技术增加电话线路的负载能力就有了巨大的动力，这项技术连同电缆的使用大大增加了对中继器的需求，也需要高质量的低失真放大器。在当时，主要的放大装置还是电子管，但是它有着非常严重的缺陷，如随着时间变化的非线性特性。在当时，有很多人尝试着去解决这个问题，但直到1927年贝尔实验室的Harold Black开发了负反馈放大器才取得实质性进展(Black, 1934)。其核心思想是利用无源线性原件为放大器提供反馈以减小失真。在这里引用Bode的一段文字(1960)：

“引起失真的原因有很多种，包括电源噪声，增益变化等。但决定性问题却是由终端管子的轻微非线性引起的互调（inter-modulation）。为了改善该状况做了很多种不同的尝试，如选择不同的管子，仔细调节偏移量，通过匹配管子的推拉来提供补偿特性。但在Black的发明出现之前，没有一个方法对这种情况做出彻底改善。”

值得注意的是，Black指的“稳定”是用来描述放大器的增益不因温度变化、下雨、天气和原件老化等原因而变化的常值性，却不是描述它对“啸叫”或者振荡的免疫性(Black, 1934)。反馈可以利用有不良特征的原件制作优良的放大器。在这项发明五十年之后，Black在他的论文中对他的发明给出了这样的观点：

“我突然意识到，如果我把放大器的输出以相反地相位反馈给输入，并且保持设备不振荡（那时也被我们称之为啸叫），我将得到我正想要的一种消除输出失真的方法。 …构建一个增益被刻意定制的放大器，也就是说比必要的高出40分贝，接着将输出反馈于输入从而抛弃了多余的增益，我们发现这样对放大的常值性和摆脱非线性产生了异常的提高。”

Black的专利花费了九年才被授权，一定程度上是因为专利授予官员不愿相信放大器能够正常工作。他们不相信一个高达数百回路增益的反馈回路是稳定的(Black, 1977)。

不稳定或“啸叫”常常出现在反馈放大器的试验中。因此，长途电话通信的技术挑战带来了反馈回路的稳定性问题。1932年，亨利.奈奎斯特（Harry Nyquist）就遇到了这个问题，当时他和Black参与了一个联合计划，要测试新的载波系统中的负反馈放大器。为了解决这个问题，奈奎斯特用了与麦克斯韦和Vyshnegradskii稳定性结果完全不同的方法。他探索了正弦信号如何沿着控制回路传播，而不是分析特征方程，由此产生了“奈奎斯特判据”。电子放大器的稳定性是由Kupfmüller (1938)独立研究的。他引入了信号流图，并用积分方程分析电路。

通信的性能要求需要反馈回路的设计进一步发展。Hendrik. Bode在1934年设计均器网络时，深入洞察了反馈放大器。他研究了衰减和相位之间的关系，并引入了增益裕度和相位裕度以及最小相位的概念(Bode, 1940)。他还证明了控制系统设计的基本局限性。特别是，他证明了灵敏度函数幅值的对数积分是常值，这意味着控制本质上是一种折衷：减小一个频率的灵敏度，就会增加另外一个频率的灵敏度。他还证明了如果系统不是最小的相位的，甚至存在更加严格的限制。Bode还发展了基于图方法（Bode图）设计反馈放大器的工具，即今天所谓的环路整型。处理三极管增益的大变化特别困难。他表明，对于很大的增益变化，通过整形环路传递函数可以保持恒定的相位裕度，使得Nyquist曲线贴近一条经过原点的直线，他称其为“理想截断特性”。Bode的设计方法是鲁棒控制的第一个案例。他的研究结果基于复变函数理论，汇总在他的重要著作(Bode, 1945)中。

AT&T公司开始把工业研究实验室作为其控制美国电信行业战略的一部分。为了执行这一战略，他们想要通过获取或防止他人获得关键专利来控制技术变革的速率和方向。他们的研究实验室在确保AT&T持有技术和专利权的控制方面发挥了重要作用(Bennett, 1993, p. 70–71)。在贝尔实验室的环境里，混合着像Bode、香农（Shannon）和奈奎斯特一类的科学家和像Black一类的工程师，这里是技术发展和基础研究的沃土。贝尔实验室已经有13位诺贝尔奖获得者。对这些人物和研究环境的观察体现在Mindell的书中(Mindell, 2002)。

控制用于电信行业和其他行业的主要区别在于，前者是由研究实验室和许多有资质的研究人员支持的。在这个行业中，理论与实践相互交织，用于陆地线路和水下电缆的中继设备被批量生产。

**2.7 早期的机电计算机（进译）**

人们很早就认识到，计算机可以在缺少数学解时用来模拟动态系统，并了解其行为。实际上，对微分方程积分的机械设备已经在1876年由威廉汤姆斯(开尔文勋爵) (Thomson,1876, 1878)设计出来了，他使用了球盘摩擦式积分器来执行积分运算。为了模拟电力系统网络， Vannevar. Bush显著地改善了机械设计，并设计了扭矩放大器来避免过载(Paynter, 1989) 。Bush的第一个机械式微分分析仪具有六个积分器(Bush, 1931)。在麻省理工学院，该微分分析仪还被用在了电力系统以外的各种应用中。

第一步是“乘积分器”，这是一个用来对两个函数的乘积积分的设备(Bush, Gage, & Stewart, 1927)，它在网路分析中是一个重要的组成部分。这个设备需要人工跟踪函数的每一个输入波形，波形接着会产生一个电子信号送到电能表，电能表的输出则是一个转轮。 如果此次计算的输出要用作下一次的输入，为了避免轮子过载，一个伺服电机被用来复制此动作。它在电话网络中作为放大器中继器的机械模拟。在1931年进步到下一阶段，这时是将伺服机构后面的积分器输出信号反馈到输入端，这样就具有了求解微分方程的功能。伺服机构在连接计算各环节中发挥了关键作用。因此，控制在早期的机电模拟计算机的构建中扮演了核心角色，

反过来，那时 “计算机 ” 的开发促进了Hazen （Hazen，1934a） 继续进一步研究伺服机构。然而这项研究表面上并没有同更早时的奈奎斯特和Bode的工作关联起来。但他引用了更早的Minorsky的工作，后者曾引入了PID控制器同美国海军船只的驾驶相联系(Minorsky,1922)。贝尔实验室(Bomberg &Weber,1941;MacColl,1945)在早期也进行了伺服系统的研究工作。

下一代微分分析器是“洛克菲勒(Rockefeller )”微分分析器，此微分分析器用电子装置传输数据，因此可以通过重置电话交换机而不是通过更耗时的机械转轴对系统进行重新配置。，这个项目是在麻省理工学院由洛克菲勒基金会的Warren.Weaver资助的，这种合作伙伴关系在后来的防空火力控制发展中扮演了非常重要的角色。穿孔的纸带可以用来对这台计算机'编程 '，使它成为' 复合 '的数字/模拟系统。受此启发，克劳德.香农（Claude Shannon）研究了在他麻省理工学院硕士毕业论文中的开关电路问题并且展示了布尔代数如何用于设计(Shannon, 1938)。后来，George. Sibitz 以他的工作为基础，在数字计算机方向取得了进展。香农后来研究了可以被微分分析仪解决的一类问题（Shannon，1941年）。

几所大学和研究机构制造了微分分析器的复制品。在麻省理工学院时，尼克尔斯使用了微分分析仪，开发了用于PID控制的整定规则(Blickley,1990)。曼彻斯特大学使用了模拟计算机来分析带延迟系统的控制(Callender, Hartree, & Porter, 1935)。

1938年,Foxboro公司的George. Philbric发明了电子模拟计算机，名为Polyphemus，用于仿真过程控制系统(Holst, 1982)。该系统被广泛用于Foxboro公司的培训和演示。模拟计算后来将在控制领域产生重大影响。