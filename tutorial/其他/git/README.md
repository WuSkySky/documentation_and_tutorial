#### 模型
- working tree 工作区
- commit 提交
- branch 分支

#### 特点与关系
- working tree 是当前文件管理器加载的内容，是能直接修改的
- commit 是 git 中的一个对象，保存了某时刻的 working tree中的文件内容
- branch 是指针或者引用，不记录内容，只指向一个 commit
- working tree 只能在不同 branch 间切换，进而间接在 commit 间切换，不能直接在 commit 间切换

#### 最基本操作
##### branch
- 创建
- 删除 需满足 working tree 不在这个brach上
- 重命名
- 移动 需满足 working tree 在这个brach上

##### commit
- 创建并立刻移动branch 需满足 working tree 在这个brach上

#### 基本操作
- merge 合并 作用是创建一个 commit 使其包含两个 commit 的内容
- rebase 变基 作用是移动一系列 commit

#### conflict 冲突
- 发生冲突意味着什么？ 在进行某些操作时(如 merge 或 rebase)会产生冲突，意味着相关的 commit 中有两个修改了同一处，并且无法根据逻辑顺序判断该使用谁
- 会发生什么？ 一般会暂停当前的操作，向工作区的文件中写入提示文本
- 我们应该做什么？ 通过 IDE 提供的快捷方式修改文件，或手动修改文件，保证文件中没有冲突提示符，然后继续进行未完成操作
