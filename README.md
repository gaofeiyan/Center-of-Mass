# Center-of-Mass

#这条命令将质心设置为 (0, 0, 0)，并把蛋白质/配体系统放置在盒子中心。

gmx editconf -f complex.gro -o newbox.gro -center 0 0 0 -box 6.560 4.362 12


#如果您已经有了模拟的轨迹文件，并希望提取某一组原子的质心位置，可以使用 gmx trjconv 命令。例如：

gmx trjconv -f traj.xtc -s topol.tpr -center -pbc mol -o center_trajectory.xtc

#GROMACS 提供了 gmx com 命令，直接计算某一组原子的质心。例如：

gmx com -f traj.xtc -s topol.tpr -center

#GROMACS 提供了 gmx com 命令，直接计算某一组原子的质心。例如：
