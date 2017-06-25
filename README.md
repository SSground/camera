#标定方案(opencv
1.首先自制一张标定图片，用A4纸打印出来，设定距离，再设定标定棋盘的格子数目，如8×6.
2.然后利用cvFindChessboardCorners找到棋盘在摄像头中的2D位置，这里cvFindChessboardCorners不太稳定，有时不能工作，也许需要图像增强处理。 
3.计算实际的距离，应该是3D的距离。我设定为21.6毫米，既在A4纸上为两厘米。 
4.再用cvCalibrateCamera2计算内参， 
5.最后用cvUndistort2纠正图像的变形。 
