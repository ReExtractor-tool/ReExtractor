# ReExtractor
## Introduction
ReExtractor is an independently developed software refactoring detection tool by the bit-se lab, capable of detecting refactoring behaviors based on commit histories in local Git repositories.

![image](https://github.com/user-attachments/assets/f00f0011-b4b9-4611-96ff-d9ffc0036f74)

![image](https://github.com/user-attachments/assets/382ea044-a36b-4601-9ce3-9129d3297dba)

![image](https://github.com/user-attachments/assets/4e6ae4c3-6a0b-4b80-8dad-c431bf1d3de6)

![image](https://github.com/user-attachments/assets/2b37b5e2-4a84-4ccf-815d-971dc74c037d)


## How to Use ReExtractor?
**1. Select the Git repository for refactoring detection. (Note: The repository must be cloned locally in advance.)**

![image](https://github.com/user-attachments/assets/95936fa6-5b04-4b83-bfe0-7d84ab084375)


**2. Choose the refactoring detection method. ReExtractor currently supports 5 detection modes.**

![image](https://github.com/user-attachments/assets/e56bfa9a-48ef-4dbe-91db-e6bff95efd7f)


Using the following commit history as an example, the differences between the 5 detection modes are explained:

![image](https://github.com/user-attachments/assets/c39066c9-e1f1-46f2-a0d7-0276b12843af)

(1)**Specific Commit**: Detects refactoring operations in a specific commit. If commit C2 is selected, it analyzes changes between C1 and C2.

(2)**Commit-to-Commit**：Detects refactoring between two selected commits. If C1 and C3 are chosen, it analyzes all refactoring operations from C1 to C3.

(3)**Commit Range**：Detects refactoring across all consecutive commits between two selected commits. If C1 and C3 are chosen, it separately analyzes C1→C2 and C2→C3.

(4)**Tag-to-Tag**：Similar to Commit-to-Commit, but operates at the release level (tag-to-tag comparison).

(5)**Tag Range**：Similar to Commit Range, but operates at the release level (analyzing consecutive tags).


**3.After selecting the detection mode and commits, the software will display commit messages and diffs.**
![image](https://github.com/user-attachments/assets/76c98fcb-859b-4875-b5f5-d6c1e78cc1bf)

**4.Click the "Detect" button to generate a refactoring summary list. You can explore files of interest and refactoring types using the file tree and pie chart.**
![image](https://github.com/user-attachments/assets/9e986c92-4ef5-4da6-9756-f2487d64c928)

**5.Click the "Location" button to navigate to the refactored code in the source files.**
![image](https://github.com/user-attachments/assets/4f176f69-c08e-40a6-bb18-38e3f3775e67)

![image](https://github.com/user-attachments/assets/eebe5308-396a-4165-9d72-ec497721cd29)

## Requirement
Java 17 or newer
