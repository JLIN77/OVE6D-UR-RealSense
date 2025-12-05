# OVE6D-UR-RealSense

Original Project Name: **"Grasping of Bearing Workpieces Based on 3D Vision"**.

This project is designed for Bin-Pick task with UR Robot and RealSense scanner. Demo and code will be released soon...

# Update:

- Bilibili 演示视频（实验室）: [点击观看](https://www.bilibili.com/video/BV1Xn2VBuEWU/?vd_source=dcc12a6fc4b4581b6a4578b624a7e6e6)

- Bilibili 演示视频（现场）: [点击观看](https://www.bilibili.com/video/BV1VE2VBrEBw/?vd_source=dcc12a6fc4b4581b6a4578b624a7e6e6)

# Main Steps:

- 利用 Intel RealSense D435 深度相机采集深度图和 RGB 图，并制作工件 3D 模板，生成 2000 个 viewpoint codebook；
- 开发了 6D 位姿估计模型进行特征提取，并在 ShapeNet 上预训练；
- 先利用 MaskRCNN 分割出 2D 图像 mask，再利用 mask 分割出 3D 点云，送入模型提取特征，并与 codebook 中的viewpoint 比较找出最接近的位姿，再通过 ICP 算法优化位姿；
- 利用 UR5 机械臂设置路径，并用磁吸式探头吸取，将工件放入指定位置；
- 在西门子实验室及苏州勤美达达精密仪器工厂现场部署演示。
