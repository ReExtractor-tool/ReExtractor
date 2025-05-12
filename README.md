# ReExtractor
## 软件介绍
ReExtractor是bit-se实验室独立开发的一款软件重构检测工具，可以基于本地Git仓库内的提交历史进行重构行为的检测。

![image](https://github.com/user-attachments/assets/2eec3dc7-49bd-4df0-b64f-0b2519c97954)
![image](https://github.com/user-attachments/assets/fc5e436e-999c-4e6d-a525-9f29549787c9)
![image](https://github.com/user-attachments/assets/06e53300-c7a1-45d3-acfb-833ac509d08a)
![image](https://github.com/user-attachments/assets/888fddd7-4dc2-40f9-967c-a44c040b24e1)


## 如何使用 ReExtractor ?
**1.选择要进行重构检测的Git仓库。（注：仓库必须预先克隆到本地）**
![image](https://github.com/user-attachments/assets/8bd5f7fc-2253-4895-98f8-212fb4abd80f)

**2.选择重构检测方式，ReExtractor当前支持5种检测方式。**
![image](https://github.com/user-attachments/assets/6f8481e8-de63-437c-8b4d-2f2406397214)

以下图提交历史为例，说明5种检测方式的区别。

![image](https://github.com/user-attachments/assets/c39066c9-e1f1-46f2-a0d7-0276b12843af)

(1)**Specific Commit**:特定提交的重构检测，若选择提交C2，则检测C1到C2间的重构操作。

(2)**Commit-to-Commit**：两个提交间的重构检测，若选择提交C1和C3，则检测C1到C3之间的重构操作。

(3)**Commit Range**：两个提交间的所有连续提交的重构检测，若选择提交C1和C3，则检测C1到C2和C2到C3之间的重构操作。

(4)**Tag-to-Tag**：类比Commit-to-Commit，是release跨度级别的检测。

(5)**Tag Range**：类比Commit Range，是release跨度级别的检测。


**3.选择检测方式和commit后，软件会显示提交信息和diff**
![image](https://github.com/user-attachments/assets/3c5370fc-48db-4f12-afc2-24d0d1066eb3)

**4.点击“Detect”按钮，出现重构总结列表，可以通过文件树和饼图来查看感兴趣文件和感兴趣类型的重构。**
![image](https://github.com/user-attachments/assets/72c5750a-fde0-492d-ae8d-c7a695a05ac3)

## Requirement
Java 17 or newer
