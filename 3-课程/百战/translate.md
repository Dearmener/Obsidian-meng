# GPT-Academic Report
# Title:



Single pixel imaging at megahertz switching rates via cyclic Hadamard masks

# Abstract:



Optical imaging is commonly performed with either a camera and wide-field illumination or with a single detector and a scanning collimated beam; unfortunately, these options do not exist at all wavelengths. Single-pixel imaging offers an alternative that can be performed with a single detector and wide-field illumination, potentially enabling imaging applications in which the detection and illumination technologies are immature. However, single-pixel imaging currently suffers from low imaging rates owing to its reliance on configurable spatial light modulators, generally limited to 22 kHz rates. We develop an approach for rapid singlepixel imaging which relies on cyclic patterns coded onto a spinning mask and demonstrate it for in vivo imaging of C. elegans worms. Spatial modulation rates of up to 2.4 MHz, imaging rates of up to 72 fps, and image-reconstruction times of down to 1.5 ms are reported, enabling real-time visualization of dynamic objects.

# Meta Translation

标题：通过循环Hadamard掩模以兆赫兹的切换速率进行单像素成像

作者：Evgeny Hahamovich；Sagi Monin；Yoav Hazan；Amir Rosenthal；T Durduran；R Choe；W B Baker；A G Yodh；O Thouvenin；K Grieve；P Xiao；C Apelian；A C Boccara；W Drexler；J G Fujimoto；W Denk；J H Strickler；W W Webb；A Velten；M Omar；J Aguirre；V Ntziachristos；A Mandelis；L Nicolaides；C Feng；S H Abrams；M F Duarte；M P Edgar；G M Gibson；M J Padgett；N Radwell；M.-J Sun；Y Zhang；M P Edgar；N Radwell；G M Gibson；M J Padgett；V Studera；S S Welsh；A Escobet-Montalbán；V Durán；N Huynh；N Huynh；L Zanotto；R I Stantchev；R I Stantchev；X Yu；T Blu；E Pickwell-Macpherson；D L Donoho；O Katz；Y Bromberg；Y Silberberg；Z.-H Xu；W Chen；J Penuelas；M Padgett；M.-J Sun；Y Hayasaki；R Sato；M Harwit；S Stern；C Kirst；C I Bargmann；K M Czajkowski；A Pastuszczak；R Kotyński；Y Eldar；G Kutyniok；E Hahamovich；A Rosenthal；A Fricke；M Achir；P Le Bars；T Kürner；Y Shao；E Hahamovich；S Monin；Y Hazan；A Rosenthal；E Hahamovich；S Monin；Y Hazan；A Rosenthal

摘要：光学成像通常使用摄像机和广域照明或单个探测器和扫描准直束进行，不幸的是，在所有波长下这些选项并不存在。单像素成像提供了一种替代方案，可以使用单个探测器和广域照明进行，潜在地使得检测和照明技术不成熟的成像应用成为可能。然而，目前的单像素成像由于依赖于可配置的空间光调制器而导致成像速率较低，通常限制在22千赫兹。我们开发了一种快速单像素成像的方法，它依赖于编码到旋转掩模上的循环模式，并且在C. elegans蠕虫的体内成像中进行了演示。报道了高达2.4兆赫兹的空间调制速率、高达72帧每秒的成像速率以及最低1.5毫秒的图像重建时间，从而实现了动态对象的实时可视化。

# D
数字相机是当今光学成像中最广泛使用的工具之一。从手机到先进的显微技术，像电荷耦合器件（CCD）和金属氧化物半导体（CMOS）等相机技术已经彻底改变了成像领域。然而，在许多应用中，数字相机并不适用。成熟的相机技术仅在电磁波谱的一小部分范围内可用，并且其性能特性可能限制一些应用。例如，时间域成像技术通常需要小于1纳秒的响应时间，而在全场光学相干断层扫描术（OCT）等技术中，相机的饱和度限制了动态范围。

当只有一个探测器可用时，可以使用聚焦或定向照明进行成像，这些照明被以光栅扫描的方式移动到被成像的物体上，同时不断监测探测器信号。在许多应用中，光栅扫描是首选的方法，包括OCT、多光子荧光显微镜和飞行时间成像方法等。此外，在仅激发光是光学的混合成像技术中，如光声成像和光热成像中，光栅扫描也很常见。虽然光栅扫描提供了比基于相机的方法更多的检测特性的灵活性，但它对光源的要求更为严格。换句话说，虽然相机可以使用广泛的照明，但光栅扫描需要具有高空间相干性的光源，以实现定向照明和聚焦。

单像素成像（SPI）提供了一种替代相机基础和光栅扫描技术的方法，它只需要一个单一的探测器和广场域照明，潜在地可以在光源和检测技术受限的领域进行成像。在SPI中，可配置的空间光调制器（SLMs）用于对照明进行编码，使用一组空间模式，检测则通过单一探测器进行。来自探测器的信号记录了每个投射在物体上的模式，通过反演算法从这些信号中形成图像。基于SLM的SPI已经在光学领域的许多应用中得到了证明，包括可见光和红外显微镜、3D成像、荧光显微镜、多光谱成像、多光子广场成像、透过散射介质观察，以及混合光辅助技术，如光声成像、超声光学成像和太赫兹成像等。

除了能够与简单的光源和探测器配合使用外，单像素成像（SPI）还具有与压缩感知理论兼容的优势22,23：如果正确选择编码模式，可以用少于N个投影模式来重建具有N个像素的图像。因此，压缩感知在理论上至少可能有助于以比传统方法更高的速率进行成像，传统方法需要N个测量来形成具有N个像素的图像。然而，在实际操作中，压缩感知的优势常常受到大多数空间光调制器（SLMs）刷新速率较慢的影响，这不能与摄像机的并行数据采集或光束扫描技术的速度相竞争。具体而言，在SPI领域最常见的SLMs是数字微镜器件（DMDs），它们通常以高达22 kHz的速率运行，这对于动态成像场景来说是不足够的。

最近，Xu等人提出了一种替代的单像素成像（SPI）方法，其中结构化照明模式是由发光二极管（LED）矩阵创建的，而不是使用空间光调制器（SLM）24。通过使用快速切换的LED，已经演示了高达500 kHz的速率。尽管Xu的方法仅使用单像素探测器，并依赖于SPI的数学原理进行图像形成，但由于其依赖于多像素源，它与SPI范例存在差异。这种差异不仅仅是语义上的。SPI的一个主要优势是它通常与任何光源兼容，而在基于多像素源的方案中，这个优势丧失了。对于复杂的光源，例如多光子显微镜中使用的飞秒激光器15，制造一个独立控制的源矩阵是不切实际的。此外，在空间上不相干的光源，例如LED，以微观分辨率进行成像将需要使用微米级的源像素，因为在聚焦空间上低相干光方面存在基本限制。这样密集的阵列，如果以高开关速率和亮度生产，将涉及到制造和散热方面的挑战。在参考文献24的具体实施中，报告了32×32像素图像的成像分辨率为270 µm。

在这项工作中，我们展示了一种超高速SPI方法，并以每秒高达240万像素的速度进行了演示，而无需使用压缩感知算法。我们提出的方案是基于照明一个预先编码的二进制模式的光掩模来进行空间调制的。切换模式是通过旋转掩模来实现的。尽管在不同代码之间进行机械切换通常会导致低成像速率25，但我们的方案是基于循环代码的，其中通过单个单元的平移会产生一个新的模式26。利用循环代码，可以通过N个单元的移位产生完整的、条件良好的基函数（更多详细信息请参见附录注释2和8）。通过将单元尺寸缩小到波长尺度并使用快速旋转平台，演示了以百万赫兹速率进行的空间调制，图像具有高达25,111像素和像素尺寸低至2 µm。基函数的周期性不仅在实验设置中得到利用，还在重建算法中得到利用，从而实现了具有实时性能的数值高效重建。

# Results
系统配置。我们的实验设置示意图如图1所示。二进制代码，由1和0组成，被编码成圆形图案，位于一块厚度为6.35毫米的镀铬光掩膜上（Toppan Photomasks）。掩膜的一小部分，对应于一个基函数，用一个工作波长为625纳米的LED照明。掩膜输出处的空间光模式通过具有10倍放大倍率的物镜和管状镜头投射到待成像的样本上。透过待成像样本的光被聚焦到单个硅光电二极管上。测试了多个掩膜的性能，包括正方形和六边形单元形状，单元宽度从1.5到5.2微米不等。掩膜以每分钟540-600次的恒定速度旋转。对于距离旋转中心55毫米处制作的图案和1.5微米的单元大小，两个基函数之间的转换时间，用T表示，约为0.43微秒。由于旋转中心没有完全与圆形图案的中心重合，照明光束与掩膜旋转同步扫描，以最小化投射图案的径向漂移。实验设置的详细信息、掩膜几何形状的排列、将1D代码元素转换为2D图案、径向漂移补偿以及由于图案半径变化而引起的单元大小变化等方面在补充说明1、2和3中有详细讨论。补充说明4讨论了在系统稳定性问题的情况下可能使用的额外反馈方法。

采样过程。图2显示了从分辨率掩模获得的测量信号示例以及重建过程的说明。为了将测得信号的N个不同样本有效地转换成具有N个像素的图像，我们利用了采样矩阵的周期性属性和快速傅里叶变换（FFT）（附注5），从而实现了O（NlogN）的图像重建复杂度。由于模型矩阵具有良好的条件，因此在重建过程中不使用正则化。为了充分优化测量的信噪比（SNR），我们使用了模式转换时间T期间的整个信号，而不仅仅是一个单一的离散样本。由于相邻基函数之间的过渡是渐变的，而不是突变的，我们将T期间的信号分为M个离散样本，每个样本对应于掩模和成像对象之间的亚像素移位（图2b）。因此，我们获得了M组N个样本，其中每组用于重建N像素图像（图2c）。由于M个生成的图像并不相同，而是代表成像对象的稍微偏移的版本，因此首先通过亚像素移位将这些图像对齐，然后相加以形成单一图像。有关通过相加亚像素偏移图像在SNR和图像对比度方面的优势，请参阅附注7。

静态图像。图3展示了在各种实验条件下，我们的系统获得的代表性SPI图像，其成像速率高达2.4兆像素/秒（实验参数在补充说明2中指定）。图3a-c显示了一个分辨率目标（3a和3b）和Technion标志（3c）的二值图像，其中白色区域对应于被成像物体的完全透明。为了展示我们的方案生成灰度图像的能力，我们成像了部分吸收或散射光的物体。对于部分吸收光的物体，我们选择了一个旧的胶片，上面捕捉到了复杂的花朵图像（图3d），而对于部分散射光的物体，我们使用了一只活的C. elegans蠕虫（图3e）。在这两种情况下，给定区域内更高的吸收或散射导致SPI中的像素变暗，因为来自该区域的光较少达到光电探测器。

动态视频。我们在两种不同的情境下展示了我们系统进行动态成像的能力。在第一种情境中，成像对象是一个手动垂直扫描的分辨率目标。成像采用了101×103（N = 10,403）像素的矩形照明模式，成像速度为每秒72帧（fps）。在第二种情境中，自由移动的C. elegans蠕虫27以每秒10帧的六边形照明模式进行成像，成像区域近似为圆形，包含N = 25,111像素。单幅图像的重建时间范围从1.5毫秒（对于N = 10,403）到4毫秒（对于N = 25,111），使用未并行化的CPU，即短于采集时间。完整的捕获视频可在补充视频1-3中找到，视频的快照呈现在图4中。有关捕获视频的详细信息请参阅补充说明10。

# Discussion
讨论：

总之，我们开发了一种替代的单像素成像（SPI）方法，其中通过旋转编码有循环模式的光掩模，实现了基函数之间的快速切换。使用我们的系统，我们实现了高达2.4兆像素/秒的成像速率，比传统的数字微镜装置（DMDs）能够实现的速率快了两个数量级，而且重建效率高，为O（NlogN），可实现数据采集和图像重建的实时性能。我们展示了高达72帧/秒的视频成像速率，使我们能够实时捕捉C. elegans蠕虫在体内的运动。

如附录9中所示，通过使用压缩感知算法，可以进一步提高成像速率，但可能会以较慢的图像重建速度为代价，即使对于高效的算法，典型的复杂度也为O（N^2）。为充分利用压缩感知理论的优势，可能有益于用本文中使用的良条件基础的新型循环或半循环基础替代它，以优化非相干性。

与基于DMD的系统相比，我们的空间调制方案不可重配置，照明模式需要在制造掩膜之前确定。然而，由于模式的宽度通常小于一毫米，一个掩模上可以制作数十个模式，使您可以在不同的图像分辨率和大小之间切换。在某些情况下，使用光掩模可能比使用DMD更灵活，因为它可以实现不可配置在DMD上的任意元素几何形状和大小。

我们的快速调制方案和算法可以视为SPI的新范例，不受DMD速度限制，可能在摄像技术受限的领域开启新的应用。与基于多像素源的方案不同，我们的方法是通用的，并且可以用于任何光源，或者通过为这些应用程序制作适当的掩膜来推广到其他波基成像领域，例如，超声波情况下的薄声学阻挡器或太赫兹成像的印刷电路板。另外，我们的方案也可以通过使用元素将光学转化为感兴趣领域来推广到其他领域。例如，已经证明，用空间调制光照射高电阻硅晶片可以实现通过晶片传输的太赫兹光束的空间调制。随着太赫兹SPI的最新进展，这类系统的速度目前受到DMD速率的限制，因此可以通过使用我们的方案来提高速度。

由于我们方法的成像速度主要受到扫描装置的速度和探测器以及采集系统的带宽的限制，原则上它可以实现光栅扫描技术的高成像速率。例如，通过使用声光调制器，它可以以100 MHz的典型速率执行线扫描，并且具有千兆赫带宽的快速探测器，可能可以实现每秒数十亿像素的成像速率，将SPI转变为用于动态成像的高性能方法。

# Methods
统计学和可重复性。如图3中呈现的每一幅图像a-d均独立测量了10次以确认结果的可重复性。每一次捕获的信号都产生了相同的结果图像。本文中呈现的结果仅使用了一次捕获来执行图像重建。图3e仅捕获了一次，因为被成像的蠕虫移动。

# Acknowledgements
我们感谢Ollendorff Minerva中心提供的部分财务支持，感谢Shay Stern教授提供C. elegans样本的图像，并感谢Roni Monin在处理生物样本方面的帮助。

# Data availability
本研究的数据可以通过 Zenodo 33 进行获取。

# Code availability
本研究的代码可以通过Zenodo 34 进行获取。

# Author contributions
E.H. 和 S.M. 设计并构建了系统，执行了实验并分析了数据。Y.H. 协助进行光学设置，A.R. 创意并监督了这个项目。

# Competing interests
作者声明无竞争利益。

# Additional information
附加信息
在线版本包含附加材料，可在https://doi.org/10.1038/s41467-021-24850-x 获取。
有关材料的通信和请求，请联系A.R.。

# Peer review information Nature Communications thanks Rayko Stantchev, Zeev
Nature Communications感谢Rayko Stantchev、Zeev以及其他匿名审稿人对本研究的同行评审所做出的贡献。同行评审报告可供查阅。重印和许可信息可在http://www.nature.com/reprints 获取。出版商声明：Springer Nature在已发表的地图和机构隶属方面保持中立。