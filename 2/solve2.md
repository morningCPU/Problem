# 2. 如何把本地仓库放到github

### 1. **创建GitHub仓库**
1. 创建仓库
2. 勾选“Initialize this repository with a README”（可选，如果你本地仓库已经有一个`README.md`文件，可以不勾选）。

### 2. **在本地仓库中配置远程仓库地址**
在你的本地仓库目录中，打开终端或命令行工具，执行以下命令：
```bash
# 查看当前的远程仓库地址（如果有）
git remote -v
# 如果有默认的远程仓库地址，先移除
git remote remove origin
# 添加GitHub仓库的远程地址
git remote add origin https://github.com/your-username/your-repo-name.git
```
- `your-username` 是你的GitHub用户名。
- `your-repo-name` 是你在GitHub上创建的仓库名称。
- `https://github.com/your-username/your-repo-name.git` 是GitHub仓库的远程地址。(其实有可以直接复制)

### 3. **推送**
第一次推送要用 `git push -u origin main` ， 从而建立对应关系
后面就可以直接 `git push` 了

### 注意事项
- 如果你的GitHub仓库已经初始化了`README.md`文件，可能会出现冲突。解决方法是先从GitHub拉取最新的代码，然后合并本地代码：
```bash
git pull origin main --allow-unrelated-histories
```
如果有冲突，手动解决冲突后，再次提交并推送。