# ReExtractor
## 软件介绍
ReExtractor是bit-se实验室独立开发的一款软件重构检测工具，可以基于本地Git仓库内的提交历史进行重构行为的检测。

![image](https://github.com/user-attachments/assets/f00f0011-b4b9-4611-96ff-d9ffc0036f74)

![image](https://github.com/user-attachments/assets/382ea044-a36b-4601-9ce3-9129d3297dba)

![image](https://github.com/user-attachments/assets/4e6ae4c3-6a0b-4b80-8dad-c431bf1d3de6)

![image](https://github.com/user-attachments/assets/2b37b5e2-4a84-4ccf-815d-971dc74c037d)


## 如何使用 ReExtractor ?
**1.选择要进行重构检测的Git仓库。（注：仓库必须预先克隆到本地）**

![image](https://github.com/user-attachments/assets/95936fa6-5b04-4b83-bfe0-7d84ab084375)


**2.选择重构检测方式，ReExtractor当前支持5种检测方式。**

![image](https://github.com/user-attachments/assets/e56bfa9a-48ef-4dbe-91db-e6bff95efd7f)


以下图提交历史为例，说明5种检测方式的区别。

![image](https://github.com/user-attachments/assets/c39066c9-e1f1-46f2-a0d7-0276b12843af)

(1)**Specific Commit**:特定提交的重构检测，若选择提交C2，则检测C1到C2间的重构操作。

(2)**Commit-to-Commit**：两个提交间的重构检测，若选择提交C1和C3，则检测C1到C3之间的重构操作。

(3)**Commit Range**：两个提交间的所有连续提交的重构检测，若选择提交C1和C3，则检测C1到C2和C2到C3之间的重构操作。

(4)**Tag-to-Tag**：类比Commit-to-Commit，是release跨度级别的检测。

(5)**Tag Range**：类比Commit Range，是release跨度级别的检测。


**3.选择检测方式和commit后，软件会显示提交信息和diff**
![image](https://github.com/user-attachments/assets/76c98fcb-859b-4875-b5f5-d6c1e78cc1bf)

**4.点击“Detect”按钮，出现重构总结列表，可以通过文件树和饼图来查看感兴趣文件和感兴趣类型的重构。**
![image](https://github.com/user-attachments/assets/9e986c92-4ef5-4da6-9756-f2487d64c928)

**4.点击“Location”按钮，在代码中定位重构**
![image](https://github.com/user-attachments/assets/4f176f69-c08e-40a6-bb18-38e3f3775e67)

![image](https://github.com/user-attachments/assets/eebe5308-396a-4165-9d72-ec497721cd29)

## Requirement
Java 17 or newer
