# Chapter4 位移塔尔博特光刻分辨率极限：逐句翻译与精读

**原文**：P. J. P. Chausse, E. D. Le Boulbar, S. D. Lis, P. A. Shields. *Understanding resolution limit of displacement Talbot lithography*. *Optics Express*, 2019, 27(5): 5918–5930.  
**阅读定位**：上一篇 Solak 2011 说明“DTL 为什么不怕初始间隙”；本篇进一步回答“DTL 最小能做多小，以及掩模怎样设计”。

> 说明：按论文结构给出正文的英文句子、中文译文与学习提示；参考文献清单不逐条翻译。公式采用易复制的 ASCII 表示。

---

## 先用两分钟建立问题

DTL 的最终图样不是掩模孔的简单投影，而是**掩模衍射场在 z 方向积分后的 aerial image（空中像）**。所以要评价一个掩模，不能只问“孔能不能做得很小”，还要同时问：

1. 主图形的理论宽度是否小；
2. 背景光强是否低（否则胶底也会被曝光）；
3. 次峰是否低（否则出现额外孔、环或图样粘连）；
4. 透过率是否足够高（否则曝光太久）。

这四项常常互相冲突，是本篇论文的主线。

---

## 题目与摘要

### 题目

**EN** Understanding resolution limit of displacement Talbot lithography.  
**中** 理解位移塔尔博特光刻的分辨率极限。

### 摘要逐句翻译

1. **EN** Displacement Talbot lithography (DTL) is a new technique for patterning large areas with sub-micron periodic features with low cost.  
   **中** 位移塔尔博特光刻（DTL）是一种能够以低成本在大面积上制作亚微米周期特征的新技术。
2. **EN** It has applications in fields that cannot justify the cost of deep-UV photolithography, such as plasmonics, photonic crystals, and metamaterials and competes with techniques, such as nanoimprint and laser interference lithography.  
   **中** 它适用于等离激元、光子晶体、超材料等无法承担深紫外光刻成本的领域，并与纳米压印和激光干涉光刻竞争。
3. **EN** It is based on the interference of coherent light through a periodically patterned photomask.  
   **中** 它基于相干光穿过周期图案光掩模后产生的干涉。
4. **EN** However, the factors affecting the technique’s resolution limit are unknown.  
   **中** 但是，影响该技术分辨率极限的因素尚不明确。
5. **EN** Through computer simulations, we show the mask parameter’s impact on the features’ size that can be achieved and describe the separate figures of merit that should be optimized for successful patterning.  
   **中** 通过计算机仿真，作者展示了掩模参数对可实现特征尺寸的影响，并说明成功图形化需要分别优化的性能指标。
6. **EN** Both amplitude and phase masks are considered for hexagonal and square arrays of mask openings.  
   **中** 研究考虑了六角阵列和方形阵列开孔的振幅掩模与相位掩模。
7. **EN** For large pitches, amplitude masks are shown to give the best resolution; whereas, for small pitches, phase masks are superior because the required exposure time is shorter.  
   **中** 对大周期，振幅掩模可给出最佳分辨率；对小周期，相位掩模更优，因为所需曝光时间更短。
8. **EN** We also show how small changes in the mask pitch can dramatically affect the resolution achievable.  
   **中** 作者还表明，掩模周期的微小变化就可能显著改变可达到的分辨率。
9. **EN** As a result, this study provides important information for choosing new masks for DTL for targeted applications.  
   **中** 因而，该研究为面向特定应用选择新的 DTL 掩模提供了重要依据。

### 摘要小结

本篇不是提出新的 DTL 动作，而是建立一个**掩模设计选择表**。请先记住结论不是“永远选某一种掩模”，而是由周期、开孔尺寸、曝光时间和允许的寄生图样共同决定。

---

## 1. 引言：为什么要研究分辨率极限

1. **EN** Periodic organisations of structures are useful for the creation of devices in many different fields such as plasmonics, photonic structures or metamaterials.  
   **中** 周期性结构排列可用于制造等离激元器件、光子结构和超材料等众多器件。
2. **EN** Existing techniques are capable of easily patterning periodic sub-micron features, but each has their advantages and disadvantages.  
   **中** 现有技术都能制作周期性亚微米特征，但每种技术各有优缺点。
3. **EN** Deep-ultraviolet immersion lithography using a 193 nm excimer laser is widely used in industry and is capable of achieving a resolution of 14 nm.  
   **中** 使用 193 nm 准分子激光器的深紫外浸没式光刻已广泛用于工业，分辨率可达 14 nm。
4. **EN** Extreme ultraviolet sources with a wavelength of 13.2 nm are on the horizon to further decrease the minimum feature sizes.  
   **中** 波长 13.2 nm 的极紫外光源也正在发展，以进一步减小最小特征尺寸。
5. **EN** However, the very high cost of these techniques limits their penetration into lower volume industries and research organisations.  
   **中** 但这些技术成本极高，限制了它们在小批量工业和科研机构中的普及。
6. **EN** Electron beam lithography is versatile and can achieve very high resolutions (<10 nm), but the cost is prohibitive for full wafer patterning due to the long patterning time.  
   **中** 电子束光刻用途灵活且分辨率很高（小于 10 nm），但因写入时间长，整片晶圆图形化成本高得难以接受。
7. **EN** However, reaching such high resolutions is not necessary for all applications.  
   **中** 不过，并非所有应用都需要这么高的分辨率。
8. **EN** Nanoimprint lithography is a promising technology for large-area patterning of features below 10 nm.  
   **中** 纳米压印是很有前景的大面积 10 nm 以下特征图形化技术。
9. **EN** Thanks to the mechanical pattern transfer, the resolution is not limited by an optical system.  
   **中** 由于是机械图形转移，其分辨率不受光学系统限制。
10. **EN** However, the main drawback is the lifetime of the 3D master mould.  
    **中** 但其主要缺点是三维母模的寿命问题。
11. **EN** Another approach is to use interference lithography, in which coherent sources of electrons or photons interfere, creating a periodic array of intensity.  
    **中** 另一种方法是干涉光刻：相干电子源或光子源相互干涉，形成周期性强度阵列。
12. **EN** Since maintaining control of the sources before they interfere with each other can be a challenge, a solution is to derive the multiple sources close to the region of interference through diffraction from a periodic mask.  
    **中** 因为在相互干涉前保持多个光源受控很困难，解决办法是用周期掩模衍射，在干涉区域附近产生多个等效光源。
13. **EN** Displacement Talbot lithography is a recently developed technique for patterning large areas with sub-micron periodic features.  
    **中** 位移塔尔博特光刻是一种新近发展的、用于大面积亚微米周期特征图形化的技术。
14. **EN** It is an extension of Talbot lithography, which uses the three-dimensional interference pattern created when monochromatic light diffracts through a periodic mask.  
    **中** 它是塔尔博特光刻的扩展，利用单色光穿过周期掩模时形成的三维干涉图样。
15. **EN** Coherent light passing through a mask patterned with a periodic structure creates different diffraction orders that subsequently interfere causing a self-imaging of the mask.  
    **中** 相干光穿过具有周期结构的掩模后产生不同衍射级次，随后它们相互干涉，形成掩模的自成像。
16. **EN** This phenomenon is well-known and called the Talbot effect.  
    **中** 这一熟知现象称为塔尔博特效应。
17. **EN** Characteristic of the interference pattern is its repeating nature along the axis perpendicular to the mask, with a spatial period called the Talbot length.  
    **中** 该干涉图样的特征是沿垂直于掩模的方向重复，其空间周期称为塔尔博特长度。
18. **EN** By itself, this interference pattern is difficult to use for photolithography directly due to the size and complexity of the pattern.  
    **中** 单独使用这种干涉图样难以直接光刻，因为图样尺寸和结构都很复杂。
19. **EN** However, introducing a displacement during a photolithography exposure along the axis perpendicular to the mask integrates the optical field and solves these problems.  
    **中** 但在曝光时沿垂直掩模的方向引入位移，会对光场进行积分，从而解决这些问题。
20. **EN** This technique is called Displacement Talbot Lithography (DTL) and has the advantage of a theoretical infinite depth of field.  
    **中** 这项技术称为 DTL，具有理论上无限景深的优势。
21. **EN** The main disadvantages are low contrast between exposed and unexposed regions due to mixing of the self-image and secondary constructive-interference features, and restriction to simple periodic features.  
    **中** 主要缺点是：自像和次级相长干涉特征混合，使曝光区与未曝光区对比度低；并且图形受限于简单周期结构。
22. **EN** Nevertheless, the illumination process will not be sensitive to surface roughness, imperfect parallelism, or depth of field.  
    **中** 不过，照明过程对表面粗糙度、掩模与样品不完全平行和景深都不敏感。
23. **EN** Recently more complex periodic structures have also been obtained using DTL as well as sub-wavelength patterning.  
    **中** 近期也已用 DTL 获得更复杂的周期结构和亚波长图形。
24. **EN** The minimum feature size is dependent on source wavelength, with 125–300 nm features achieved for near-UV laser sources and 75 nm features for a deep-UV source.  
    **中** 最小特征尺寸依赖光源波长：近紫外激光已实现 125–300 nm 特征，深紫外光源已实现 75 nm 特征。
25. **EN** However, for any particular source wavelength, the resolution limit of this method has not yet been reported.  
    **中** 但是，对某一确定光源波长，这种方法的分辨率极限尚未见报道。
26. **EN** In this paper, we analyse the resolution limit using computer simulations of the intensity pattern seen by the sample, first validated by comparison with existing experimental data.  
    **中** 本文用样品所见光强图样的计算机仿真分析分辨率极限，并先以已有实验数据验证模型。
27. **EN** We determine the smallest feature size as a function of mask type, mask pitch and feature diameter, and discuss the conditions required to optimize resolution.  
    **中** 作者确定最小特征尺寸如何随掩模类型、掩模周期和特征直径变化，并讨论优化分辨率所需条件。

### 引言小结

2011 论文解决“是否能稳定曝光”；2019 论文转而解决“什么掩模参数能得到最小且干净的图样”。理论无限景深不等于无限分辨率，真正的瓶颈来自波长、衍射级次、透过率和光刻胶阈值。

---

## 2. DTL 建模

### 2.1 空中像仿真

1. **EN** A MATLAB computer model was developed to simulate a DTL machine (PhableR 100, EULITHA) using a 375 nm UV laser.  
   **中** 作者开发了 MATLAB 模型，模拟使用 375 nm 紫外激光的 DTL 设备（EULITHA PhableR 100）。
2. **EN** The optical system generates a plane wave illuminating a conventional mask at normal incidence, so light arriving at the mask is homogeneous, unpolarised, and in phase.  
   **中** 光学系统产生正入射平面波照明常规掩模，因此到达掩模的光均匀、非偏振且同相。
3. **EN** The complex field distribution has been represented by a scalar field.  
   **中** 复杂光场分布用标量场表示。
4. **EN** This allows calculation of the field distribution in any plane parallel to the mask using free-space propagation in Fourier space.  
   **中** 这使得可以利用傅里叶空间中的自由空间传播，计算任意平行于掩模平面上的场分布。
5. **EN** Both amplitude and phase masks are considered, while the impact of metal or phase-shift layer thickness is neglected.  
   **中** 模型同时考虑振幅掩模和相位掩模，但忽略金属层或相移层厚度对电场的影响。
6. **EN** Consequently, the propagating contributions of mask regions have amplitudes 1 and 0 for a chrome amplitude mask and 1 and −1 for a phase mask.  
   **中** 因而，对铬振幅掩模，各区域传播贡献的振幅取 1 和 0；对相位掩模取 1 和 −1。
7. **EN** Experimentally, integration was performed 100 μm away from the mask, therefore Fraunhofer conditions can be applied to calculate the three-dimensional field behind the mask, known as the Talbot carpet.  
   **中** 实验中在距掩模 100 μm 处进行积分，因此模型可采用夫琅禾费条件计算掩模后的三维光场，即塔尔博特地毯。
8. **EN** The Fourier transform of the mask and the 2D spatial wave vectors in the mask plane are calculated.  
   **中** 计算掩模的傅里叶变换以及掩模平面内的二维空间波矢。
9. **EN** The electric-field amplitude at a coordinate is calculated from the inverse Fourier transform of the 3D wave vectors, mask transform and depth positions.  
   **中** 某一坐标处的电场振幅，由三维波矢、掩模变换和深度位置组合后作逆傅里叶变换得到。
10. **EN** The electric field is then multiplied by its conjugate to obtain the surface light intensity.  
    **中** 再将电场乘以其复共轭，得到表面光强。
11. **EN** For a 600 nm-period amplitude grating with 200 nm openings, moving through an integer number of Talbot lengths integrates the intensity and removes z-dependence.  
    **中** 对周期 600 nm、开孔 200 nm 的振幅光栅，移动整数个塔尔博特长度会积分光强并去除 z 向依赖。
12. **EN** The Talbot length is `L_T = lambda / (1 - sqrt(1-(lambda/p)^2))`, where p is pitch and lambda is wavelength.  
    **中** 塔尔博特长度为 `L_T = lambda / (1 - sqrt(1-(lambda/p)^2))`，其中 p 是周期，lambda 是波长。
13. **EN** A vertical step of one hundredth of the Talbot length is sufficient for small-pitch masks, but larger pitches require finer steps because more diffraction orders make the carpet more complex.  
    **中** 对小周期掩模，z 向步长取塔尔博特长度的 1/100 已足够；对大周期则需更细步长，因为更多衍射级次使塔尔博特地毯更复杂。
14. **EN** Therefore, a step resolution of one two-hundredth was selected.  
    **中** 因此作者选择了 1/200 的步长分辨率。
15. **EN** Further increasing resolution only increases computational time with no change in the simulated pattern.  
    **中** 继续提高步长分辨率只会增加计算时间，并不会改变仿真图样。
16. **EN** The resulting intensity in the x-y plane transferred into resist is called the aerial image.  
    **中** 最终在 x-y 平面上、将被转移进光刻胶的强度分布称为空中像。
17. **EN** The 600 nm-pitch grating mask produces a 300 nm-period grating on the sample.  
    **中** 周期 600 nm 的光栅掩模会在样品上产生周期 300 nm 的光栅。

### 2.2 三个评价指标

1. **EN** Computer simulation can determine the aerial image for any mask, which is important because the results are not intuitive.  
   **中** 计算机仿真可得到任意掩模的空中像；这很重要，因为结果并不直观。
2. **EN** As pitch, filling factor and mask type change, the aerial image evolves dramatically.  
   **中** 当周期、填充因子和掩模类型改变时，空中像会显著变化。
3. **EN** This study focuses on square and hexagonal arrangements of circular features.  
   **中** 本研究聚焦于圆形特征的方形阵列和六角阵列。
4. **EN** Since the results are similar, hexagonal patterns are primarily discussed and square-mask results are placed in appendices.  
   **中** 因为两类结果相似，正文主要讨论六角图形，方形掩模结果放在附录。
5. **EN** To compare aerial images, three figures of merit are defined: theoretical achievable width, relative background intensity, and relative intensity of unwanted secondary maxima.  
   **中** 为比较空中像，定义三个性能指标：理论可实现宽度、相对背景强度、以及不需要的次峰的相对强度。
6. **EN** The background is the intensity at the location indicated by the orange circle in Fig. 2(b), and the secondary maximum is the peak of unwanted patterns.  
   **中** 背景是图 2(b) 橙色圆所示位置的强度；次峰是不需要图样的峰值强度。
7. **EN** To define width, a threshold relative intensity level representing illumination dose at which photoresist fully develops must be specified.  
   **中** 为定义宽度，必须给定一个相对强度阈值，它代表使光刻胶完全显影所需的照明剂量。
8. **EN** A lower dose does not fully develop resist, whereas higher dose illuminates more resist above threshold and increases feature size.  
   **中** 剂量过低时光刻胶不会完全显影；剂量升高时，超过阈值的胶区域增多，特征尺寸会变大。
9. **EN** Conversely, feature size can be reduced by raising the threshold, with maximum resolution when only the top of an intensity peak lies above threshold.  
   **中** 反过来，提高阈值可以减小特征尺寸；当只有强度峰顶超过阈值时，理论分辨率最高。
10. **EN** A key factor limiting how high the threshold can be raised is resist contrast, defined as the ratio of dose range over which resist is partially developed.  
    **中** 限制阈值可提高到多高的关键因素是光刻胶对比度，它定义为光刻胶部分显影所跨越的剂量范围之比。
11. **EN** Typical contrast values are about 10% for ULTRA-i 123; higher-contrast resists can permit lower values.  
    **中** ULTRA-i 123 的典型对比度约为 10%；更高对比度的光刻胶可允许更低数值。
12. **EN** The finite slope of the intensity curve makes resolution strongly dependent on illumination homogeneity, laser collimation and finite source divergence.  
    **中** 强度曲线的有限陡峭度使分辨率高度依赖照明均匀性、激光准直度和有限光源发散角。

### 建模小结

本篇将“分辨率”从一个模糊词拆成三个可计算指标。**宽度小**不等于**工艺好**：如果背景高或次峰高，实际显影会出现底胶、额外孔或粘连。因此做光路/掩模设计时要先决定你最重视的是最小 CD、均匀性还是缺陷抑制。

---

## 2.3 实验验证模型

1. **EN** Experiments using a hexagonal mask were performed to determine the minimum feature size achievable and to select a suitable threshold for the modelling.  
   **中** 作者使用六角掩模进行实验，以确定可实现的最小特征尺寸并为模型选取合适阈值。
2. **EN** The layer stack comprised 240 nm ULTRA-i 123 resist on a bottom antireflection layer WIDE 30C.  
   **中** 膜层结构是在底部抗反射层 WIDE 30C 上制备 240 nm 厚的 ULTRA-i 123 光刻胶。
3. **EN** SEM images were obtained for 1 μm- and 1.5 μm-pitch hexagonal amplitude masks at two exposure doses.  
   **中** 对周期为 1 μm 与 1.5 μm 的六角振幅掩模，在两种曝光剂量下获得了 SEM 图像。
4. **EN** At low exposure dose, a large dispersion of hole diameters and even closed holes are observed.  
   **中** 曝光剂量低时，观察到孔径离散度很大，甚至有闭合孔。
5. **EN** Higher doses produce larger openings with better uniformity.  
   **中** 更高剂量产生更大的开孔且均匀性更好。
6. **EN** The top 20% and 10% of the aerial-image peak correspond to critical doses at which resist reaches 80% and 90% development, respectively.  
   **中** 空中像峰值的顶部 20% 与 10%，分别对应光刻胶达到 80% 与 90% 显影的临界剂量。
7. **EN** A threshold of 80%, determined experimentally, balances high resolution and high homogeneity.  
   **中** 实验确定的 80% 阈值，在高分辨率与高均匀性之间取得平衡。
8. **EN** This lower threshold makes the simulated minimum width robust against imperfect collimation, local mask variation and illumination inhomogeneity not included in the model.  
   **中** 较低阈值使仿真的最小宽度对模型中未包含的准直不完美、局部掩模变化和照明不均匀更稳健。

---

## 3. 掩模设计对分辨率的影响

### 3.1 振幅掩模

1. **EN** Aerial images were simulated for pitches from 0.5 to 3.2 μm and opening diameters from 20 nm to 90% of pitch, in 20 nm steps.  
   **中** 对周期 0.5–3.2 μm、开孔直径从 20 nm 至周期的 90% 的振幅掩模进行空中像仿真，步长为 20 nm。
2. **EN** Integration over four Talbot lengths was used to prevent artefacts caused by grid definition.  
   **中** 采用跨越四个塔尔博特长度的积分，以防止网格定义造成的伪影。
3. **EN** Theoretical width, relative background, and secondary-pattern maximum were extracted and plotted as functions of pitch and mask-feature diameter.  
   **中** 提取理论宽度、相对背景和次峰最大值，并绘制为周期和掩模特征直径的函数。
4. **EN** The smallest features are obtained when mask openings are smaller than the wavelength.  
   **中** 当掩模开孔小于波长时，可得到最小特征。
5. **EN** For such feature sizes diffraction can be considered to arise from point sources with hemispherical wavefronts.  
   **中** 对这类尺寸，衍射可视为来自具有半球面波前的点光源。
6. **EN** However, transmission is highly reduced for subwavelength holes, scaling approximately as `T(lambda) proportional to (d/lambda)^4`.  
   **中** 但是，亚波长孔的透过率会显著降低，近似满足 `T(lambda) 正比于 (d/lambda)^4`。
7. **EN** A second valley of small theoretical width appears near a 50% filling factor, though its width is not quite as small.  
   **中** 在约 50% 填充因子附近还出现第二个小理论宽度谷值，但宽度并不如前者小。
8. **EN** Sharp lines occur periodically at multiples of the laser wavelength because additional diffraction orders are incrementally added.  
   **中** 在激光波长的若干倍处会周期性出现锐利线条，因为新的衍射级次逐步加入。
9. **EN** Background is lower for smaller mask openings, so high-resolution features can be achieved simultaneously with low background.  
   **中** 开孔越小，背景越低；因此高分辨率特征可以同时具有低背景。
10. **EN** Low secondary maxima occur either for small openings at particular pitches or for masks with a 33% filling factor.  
    **中** 次峰较低有两种情况：特定周期下的小开孔，或填充因子为 33% 的掩模。
11. **EN** By tuning opening diameter, some diffraction orders can be cancelled and secondary patterns reduced.  
    **中** 通过调节开孔直径，可以抵消某些衍射级次，从而减弱次级图样。
12. **EN** For small openings, all diffraction orders are represented with more similar amplitudes, which helps explain improved resolution.  
    **中** 对小开孔，各衍射级次均被表示且振幅更接近，这有助于解释分辨率提高。

### 3.2 相位掩模

1. **EN** Corresponding phase-mask calculations were performed over the same range of pitches and feature sizes.  
   **中** 作者对相同周期和特征尺寸范围进行了相位掩模计算。
2. **EN** The most significant difference from amplitude masks is the much higher background level.  
   **中** 与振幅掩模相比，最显著差异是相位掩模的背景水平高得多。
3. **EN** Because a large background difference is essential to process quality, theoretical width and secondary-pattern maxima were extracted only when background was below 70% of peak.  
   **中** 因为足够的背景差对工艺质量至关重要，作者仅在背景低于峰值 70% 时提取理论宽度和次峰。
4. **EN** Larger openings lead to better resolution for phase masks, unlike amplitude masks.  
   **中** 与振幅掩模不同，相位掩模的较大开孔会带来更好的分辨率。
5. **EN** For phase masks, valleys of background and secondary maxima do not perfectly coincide, so all figures of merit cannot be optimized simultaneously.  
   **中** 对相位掩模，背景谷值与次峰谷值并不完全重合，因此无法同时优化所有性能指标。
6. **EN** A constant ratio of feature size to pitch of 66% gives a background valley, explained by destructive interference between the two phases of the mask.  
   **中** 特征尺寸与周期之比为 66% 时出现背景谷值，可由掩模两种相位之间的相消干涉解释。
7. **EN** A minimum of secondary maxima occurs near a 33% filling factor.  
   **中** 次峰最小值出现在约 33% 填充因子附近。
8. **EN** Because those positions differ, resolution is compromised.  
   **中** 因为两者位置不同，分辨率必须作折中。

### 设计部分小结

振幅掩模：小开孔可把主特征做得最小、背景也低，但亚波长孔透光很弱，曝光时间会很长。相位掩模：小周期时分辨率相近而透过率高，曝光更快；但背景和次峰的最佳点不重合，需要折中。**33% 填充因子**是降低次峰的重要记忆点，**约 66% 特征/周期比**是相位掩模降低背景的记忆点。

---

## 4. 讨论、结论与附录实验条件

1. **EN** For a 375 nm laser and specific resist/developer, minimum feature sizes of around 75–100 nm are predicted for amplitude masks with openings smaller than the laser wavelength.  
   **中** 对 375 nm 激光和特定光刻胶/显影液，仿真预测：开孔小于波长的振幅掩模可实现约 75–100 nm 最小特征。
2. **EN** Using a 193 nm source should improve resolution to the sub-50 nm range.  
   **中** 使用 193 nm 光源预计可将分辨率提高到 50 nm 以下范围。
3. **EN** A higher contrast resist permits smaller features.  
   **中** 更高对比度的光刻胶可获得更小特征。
4. **EN** The model neglects mask-metal thickness, dark erosion, resist finite thickness, developer flow and the full 3D resist profile, so it may underestimate the real resolution limit.  
   **中** 模型忽略了掩模金属厚度、暗侵蚀、光刻胶有限厚度、显影液流动和完整三维胶形貌，因此可能低估真实分辨率极限。
5. **EN** Experimental high-dose secondary patterns can merge into ring structures, and their shape agrees qualitatively with the model.  
   **中** 实验中高剂量下的次级图样会合并为环状结构，其形状与模型在定性上吻合。
6. **EN** A 1.5 μm hexagonal amplitude mask with 800 nm openings allows resist features from 250 to 650 nm by changing exposure dose.  
   **中** 周期 1.5 μm、开孔 800 nm 的六角振幅掩模，只需改变曝光剂量即可在光刻胶中得到 250–650 nm 的特征。
7. **EN** For this flexible-dose application, low background and weak secondary pattern are more important than minimum resolution, and phase masks satisfy these conditions better.  
   **中** 对这种利用剂量调节尺寸的应用，低背景和弱次峰比最小分辨率更重要，而相位掩模更能满足这些条件。
8. **EN** For mask pitches smaller than two wavelengths, phase and amplitude masks achieve the same resolution.  
   **中** 当掩模周期小于两个波长时，相位和振幅掩模达到相同分辨率。
9. **EN** In that case a phase mask is preferred because its higher transmission gives shorter illumination time.  
   **中** 此时应优先选择相位掩模，因为它透过率更高、曝光时间更短。
10. **EN** For higher pitches, an amplitude mask offers the smallest features but at the expense of long exposure time.  
    **中** 对更大周期，振幅掩模可给出最小特征，但代价是较长曝光时间。
11. **EN** DTL can pattern periodic features over large areas quickly and cheaply, but the conditions for the smallest features are non-trivial and can conflict with optimizing other metrics.  
    **中** DTL 能快速、低成本地在大面积上制作周期特征，但获得最小特征的条件并不简单，且可能与其他性能指标的优化相冲突。
12. **EN** With conventional i-line resist and illumination, sub-100 nm features can be achieved over large areas.  
    **中** 使用常规 i 线光刻胶和照明，可在大面积上实现 100 nm 以下特征。

### 附录实验条件（逐条提取）

1. **EN** Silicon wafers were coated with Wide 30 bottom antireflective layer before a 240 nm positive ULTRA-i 123 resist.  
   **中** 硅晶圆先涂覆 Wide 30 底部抗反射层，随后涂覆 240 nm 正性 ULTRA-i 123 光刻胶。
2. **EN** Hexagonal amplitude masks used either 1.5 μm pitch with 800 nm openings or 1 μm pitch with 550 nm openings.  
   **中** 六角振幅掩模参数为：周期 1.5 μm、开孔 800 nm，或周期 1 μm、开孔 550 nm。
3. **EN** Their Talbot lengths were 8.80 μm and 3.80 μm, respectively.  
   **中** 它们对应的塔尔博特长度分别为 8.80 μm 与 3.80 μm。
4. **EN** Gaussian-velocity integration and travel over eight Talbot lengths were used to make integration homogeneous over several Talbot motifs.  
   **中** 使用高斯速度积分，并跨越八个塔尔博特长度运动，以在多个塔尔博特重复单元上实现均匀积分。
5. **EN** Dose series were 70–100 mJ/cm² for 1.5 μm pitch and 130–180 mJ/cm² for 1 μm pitch, in 10 mJ/cm² steps.  
   **中** 周期 1.5 μm 的剂量系列为 70–100 mJ/cm²；周期 1 μm 的为 130–180 mJ/cm²，步长均为 10 mJ/cm²。
6. **EN** Wafers were developed for 210 s in MF CD26 developer.  
   **中** 晶圆在 MF CD26 显影液中显影 210 秒。
7. **EN** Feature statistics were obtained from three SEM images per sample, near wafer centre, each showing about one hundred features.  
   **中** 每个样品在晶圆中心附近取三张 SEM 图像，每张约观察一百个特征，由此得到尺寸统计数据。

### 全文小结：用最浅显的话说

把 DTL 掩模理解为“决定衍射级次配方的元件”。孔变小不一定最好：会使图样更细，但也会让透光极低、曝光变慢。相位掩模让更多光通过，适合小周期和快速曝光；振幅掩模在大周期时更容易拿到极小尺寸。实际设计必须同时看主峰宽度、背景、寄生次峰和曝光时间，不能只拿“最小 CD”做判断。

---

## 重点专业词汇

| 英文 | 中文 | 本文中的含义 |
|---|---|---|
| resolution limit | 分辨率极限 | 在给定波长、掩模和工艺下可得到的最小可靠特征 |
| aerial image | 空中像 | 进入光刻胶前、样品平面的累计强度分布 |
| amplitude mask | 振幅掩模 | 用透光/遮光差异调制光；模型振幅为 1/0 |
| phase mask | 相位掩模 | 用相位反转调制光；模型振幅为 1/−1 |
| pitch | 周期 / 节距 | 阵列重复单元间距 |
| opening diameter | 开孔直径 | 掩模圆孔的直径 |
| filling factor | 填充因子 | 开孔尺寸相对周期的比例 |
| Talbot carpet | 塔尔博特地毯 | x-z 平面上重复变化的三维干涉强度图 |
| Talbot length | 塔尔博特长度 | z 向重复长度；本文用精确传播表达式 |
| background intensity | 背景强度 | 主图样之外区域的相对曝光强度 |
| secondary maximum | 次峰 / 寄生峰 | 非目标位置的局部强度峰，可造成额外图形 |
| figure of merit | 性能指标 | 用于比较掩模设计的量化标准 |
| threshold | 阈值 | 光刻胶开始充分显影对应的相对剂量水平 |
| resist contrast | 光刻胶对比度 | 光刻胶从不显影到显影的剂量过渡陡峭程度 |
| collimation | 准直度 | 光束接近平行的程度 |
| Fraunhofer condition | 夫琅禾费条件 | 远场近似条件，用于简化传播计算 |
| diffraction order | 衍射级次 | 周期掩模生成的 0、±1、±2 等空间频率分量 |
| destructive interference | 相消干涉 | 波峰与波谷抵消，使背景或某级次变弱 |
| subwavelength opening | 亚波长开孔 | 尺寸小于波长的孔；高分辨但透过率很低 |
| bottom antireflective coating, BARC | 底部抗反射层 | 减少衬底反射对光刻胶曝光的影响 |
| dark erosion | 暗侵蚀 | 未曝光区域在显影中也被消耗的现象 |

---

## 给老师提问时可直接回答

### 问：为什么本篇说 DTL 分辨率不能只看光源波长？

答：波长决定大方向的下限，但在固定 375 nm 光源下，掩模类型、周期、孔径、衍射级次、光刻胶阈值和照明均匀性都会改变最终空中像。相同波长也可能因次峰和背景不同而得到完全不同的可用图形。

### 问：振幅掩模与相位掩模如何选择？

答：掩模周期小于约两个波长时，两者分辨率相近，应选透过率更高、曝光更短的相位掩模；周期较大时，振幅掩模能给出更小的特征，但曝光时间较长。若任务重视低背景和剂量调尺寸，相位掩模往往更合适。

### 问：为什么小孔不总是更好？

答：小于波长的孔可以产生极小特征且背景低，但透过率近似按 `(d/lambda)^4` 迅速下降，导致曝光很慢、能量利用率很差。设计上要在尺寸与吞吐量之间取舍。

### 自测

1. 本文的三个性能指标是什么？  
   **答**：理论宽度、相对背景强度、寄生次峰的相对强度。
2. 80% 阈值的意义是什么？  
   **答**：它由实验选出，用来在分辨率和图形均匀性之间折中。
3. 375 nm 光源、小周期情形优先选什么掩模，为什么？  
   **答**：优先相位掩模，因为分辨率相近而透过率更高、曝光时间更短。

---

## 与“光路设计”课题的连接

本篇会直接影响你的光路参数取舍：

1. **波长与可达尺寸**：375 nm 方案仿真预测 75–100 nm；换用 193 nm 深紫外有望进入 50 nm 以下。
2. **准直度和均匀性**：会改变强度阈值附近的有效宽度，因此是分辨率稳定性的核心，不只是“光够不够亮”。
3. **运动轨迹与积分长度**：实验用了跨越八个塔尔博特长度的高斯速度积分，说明实际系统要考虑运动权重，而非仅移动一次。
4. **掩模与曝光时间**：振幅/相位掩模是光学效率和图样质量之间的设计选择。
5. **评价方法**：设计照明系统时应同时报告主图样 CD、背景、次峰、均匀性和剂量窗口。
