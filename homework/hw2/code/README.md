未完成提高题

get_projection_matrix(): 构建透视投影矩阵并返回该矩阵。

rasterizer_triangle(): 执行三角形栅格化算法。创建三角形的二维bounding box，遍历其中所有像素，检查屏幕空间坐标来查看中心点是否在三角形内。如果在三角形内部，则对比当前位置的depth value是否比当前depth buffer更靠近相机。如果更靠近相机，则更新像素颜色与深度缓冲区。

insideTriangle(): 检查某点P是否在三角形ABC内。先求出三个向量PA,PB,PC。计算PA x PB，PB x PC，PC x PA 。如果三组向量叉乘的结果都是同号的，说明P在三角形内部。