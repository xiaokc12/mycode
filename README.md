### 准备数据集

| 数据集     | 下载地址                                                     |
| ---------- | ------------------------------------------------------------ |
| MVTec3D-AD | https://www.mvtec.com/company/research/datasets/mvtec-3d-ad/downloads |
| Eyecandies | https://eyecan-ai.github.io/eyecandies/download              |
| Real3D     | https://drive.google.com/file/d/1oM4qjhlIMsQc_wiFIFIVBvuuR8nyk2k0/view?usp=sharing |

### 生成数据集 JSON

以 MVTec3D-AD 为例（具有多个异常类别）
MVTec 文件夹的结构：

```
mvtec3d-ad/
│
├── carrot/
│   ├── test/
│   │   ├── combined/
│   │   |   └── 2d_3d_cor    # point-to-pixel correspondence
|   |   |   |   └── 000
|   |   |   |   └── 001
|   |   |   |   └── ...
|   |   |   └── 2d_gt        # generated 2D ground truth
|   |   |   └── 2d_rendering # generated 2D renderings
|   |   |   └── gt           # 3D ground truth （png format）
|   |   |   └── gt_pcd       # 3D ground truth （pcd format）
|   |   |   └── pcd          # 3D point cloud （pcd format）
|   |   |   └── rgb          # RGB information （pcd format）
|   |   |   └── xyz          # 3D point cloud （tiff format）
│   |   |
│   |   └── crack/
│   |        └── ...
│   └── ...
└── ...
```

### 运行code

```
bash test.sh
```
