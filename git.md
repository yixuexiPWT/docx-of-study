git

![image-20250815170417971](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815170417971.png)

![image-20250815170459462](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815170459462.png)

![image-20250815172232910](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815172232910.png)

!(C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815172743473.png)

![image-20250815172815079](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250815172815079.png)

![image-20250816104228960](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250816104228960.png)

git diff head 2 id id

![image-20250816104800369](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250816104800369.png)

git rm   工作区，暂存区 add。

![image-20250816111850071](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250816111850071.png)

删除 提交

.gitignore

![image-20250817220850904](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250817220850904.png)

注释，口令

库文件不生效

 ![image-20250817221520535](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250817221520535.png)

![image-20250817225019875](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250817225019875.png)

![image-20250817225932501](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250817225932501.png)

![image-20250817233907632](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250817233907632.png)

![image-20250817234257171](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250817234257171.png)

![image-20250818000439915](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818000439915.png)

![image-20250818145706265](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818145706265.png)

![image-20250818150908332](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818150908332.png)

![image-20250818152643850](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818152643850.png)

![image-20250818153924387](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818153924387.png)

git switch

![image-20250818154123520](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818154123520.png)

![image-20250818154227713](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818154227713.png)

git log

![image-20250818154344891](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818154344891.png)

![image-20250818155347850](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818155347850.png)

本地传云端  commit提交到本地（确认）  push推到云端   一个本地仓库可以链接多个远程仓库平台 不同的本地仓库和远程仓库可以强制融合

![image-20250818163653931](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818163653931.png)

![image-20250818165725141](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818165725141.png)

![image-20250818171131117](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818171131117.png)

提交id

![image-20250818172359888](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818172359888.png)

![image-20250818172452797](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818172452797.png)

![image-20250818172522902](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818172522902.png)

![image-20250818172738948](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818172738948.png)

![image-20250818173045967](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818173045967.png)

![image-20250818173127996](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818173127996.png)

![image-20250818173617187](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818173617187.png)

git工作流

常见的 Git 工作流包括集中式工作流、功能分支工作流、Gitflow 工作流和 GitHub Flow、GitLab Flow 等，以下是对它们的详细介绍：

### 集中式工作流

- **特点**：类似于 SVN 等版本控制系统的工作方式，团队成员直接推送和拉取代码到中央仓库的主分支（如`master`或`main`）。
- 工作流程
  1. **克隆仓库**：新成员通过`git clone`命令克隆中央仓库到本地。
  2. **拉取更新**：在开始工作前，使用`git pull`从中央仓库拉取最新代码。
  3. **本地开发**：在本地修改代码，完成功能或修复问题。
  4. **提交更改**：使用`git add`和`git commit`将更改提交到本地仓库。
  5. **推送代码**：最后使用`git push`将本地提交推送到中央仓库的主分支。
- **适用场景**：小型团队或项目周期短、代码变动简单，对分支管理要求不高的场景。

### 功能分支工作流

- **特点**：以功能为单位创建分支，每个成员在自己的功能分支上开发，完成后再合并到主分支，避免了直接在主分支上开发可能导致的代码冲突和不稳定。
- 工作流程
  1. **从主分支拉取**：团队成员从中央仓库的主分支（如`main`）拉取最新代码到本地，作为开发基础。
  2. **创建功能分支**：使用`git checkout -b feature/新功能名`创建功能分支，然后在该分支上进行开发。
  3. **本地提交**：在功能分支上开发完成后，通过`git add`和`git commit`进行本地提交。
  4. **推送分支**：将本地功能分支推送到远程仓库，使用`git push origin feature/新功能名` 。
  5. **发起合并请求**：在远程仓库上创建合并请求（如 GitHub 的 Pull Request ，GitLab 的 Merge Request），请求将功能分支合并到主分支，经过代码审查等流程后，由相关人员执行合并操作。
- **适用场景**：大多数软件开发项目，尤其是团队规模较大、功能迭代频繁的项目。

### Gitflow 工作流

- **特点**：定义了更加严格和规范的分支模型，包含主分支（`master`）、开发分支（`develop`）、功能分支（`feature/*`）、发布分支（`release/*`）、热修复分支（`hotfix/*`），对不同阶段的代码管理更细致。
- 工作流程
  1. **日常开发**：开发人员基于`develop`分支创建功能分支（`git checkout -b feature/新功能名 develop`），在功能分支上开发完成并提交后，将分支推送到远程仓库，然后发起合并请求，将功能分支合并到`develop`分支。
  2. **发布准备**：当`develop`分支上积累了足够多的功能，准备发布时，从`develop`分支创建发布分支（`git checkout -b release/版本号 develop`），在发布分支上进行最后的测试、修改版本号等操作。
  3. **发布上线**：测试通过后，将发布分支合并到`master`分支，并在`master`分支上打标签（标记版本号，`git tag -a v1.0 -m "版本说明"`），同时将发布分支合并回`develop`分支，清理发布分支。
  4. **紧急修复**：线上出现问题时，从`master`分支创建热修复分支（`git checkout -b hotfix/修复名 master`），修复完成后，先合并到`master`分支并打标签，再合并回`develop`分支，清理热修复分支。
- **适用场景**：对版本管理和发布流程要求严格，有明确的发布周期和稳定版本需求的大型项目。

### GitHub Flow

- **特点**：简单轻量，紧密围绕 GitHub 平台，强调基于 Pull Request 进行协作开发，适合快速迭代的 Web 应用开发。
- 工作流程
  1. **创建分支**：开发人员从主分支（`main`）创建新的功能分支，在本地开发。
  2. **提交和推送**：在本地完成开发和测试后，将分支推送到远程仓库，然后在 GitHub 上创建 Pull Request。
  3. **代码审查**：团队成员对 Pull Request 进行代码审查，提出修改意见，开发人员根据意见进行修改。
  4. **合并和部署**：审查通过后，将分支合并到主分支，然后立即部署到生产环境。
- **适用场景**：使用 GitHub 进行代码托管，追求快速迭代、持续交付的互联网项目。

![image-20250818174327839](C:\Users\ER\AppData\Roaming\Typora\typora-user-images\image-20250818174327839.png)

 [GitCheatSheet_byGeekHour_v1.0.0(1).pdf](D:\std\GitCheatSheet_byGeekHour_v1.0.0(1).pdf) 