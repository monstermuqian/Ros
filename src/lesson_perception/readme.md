# 点云滤波分割聚类识别
        pipeline 流水线

        【1】点云算法头文件
        【2】初始化 ROS节点
        【3】私有节点获取参数
        【4】发布处理识别后点云消息topic
        【5】监听 源电云 话题数据获取点云
        【6】 将相机坐标系下的点云 转换到 世界坐标系下
        【7】ROS点云格式 转换到 PCL点云格式 
        【8】体素滤波下采样  + 去除 NAN点   
             直通滤波保存特点范围内的点
             PLANE平面分割 
             欧式距离分类
             统计学滤波剔除外点
             多边形分割
        【10】 PCL点云格式 转换到 ROS点云格式     
              PCL->ROS方便发布点云数据 提供RVIZ可视化显示
        【11】广播坐标变换 (可选)
