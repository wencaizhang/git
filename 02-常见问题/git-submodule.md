# Git Submodule - 子模块

## Git  子模块

在开发过程中，我们经常会遇到一种情况：某个项目需要包含并使用另一个项目，这个项目可能是第三方库，也可能是同事小伙伴独立开发维护的公共库。那么现在的问题就是：既想要让它们保持独立，又想在一个项目中使用另一个项目。

通过 Git  子模块可以解决这个问题，子模块允许你将一个  Git  仓库作为另一个  Git  仓库的子目录。它能让你将另一个仓库克隆到自己的项目中，同时还保持独立地提交代码。

## 添加子模块

```git
git submodule add https://github.com/chaconinc/DbConnector
```

添加完成之后，你会发现在项目根目录下多出一个 `.gitsubmodule`  文件，这个配置文件保存了刚才添加的子模块的  URL  和本地目录之间的映射关系。

### 克隆含有子模块的项目

如果你克隆一个含有子模块的项目，默认会包含子模块的目录，但只是一个空目录，其中没有任何文件。
此时，你需要运行两个命令来拉取子模块代码。

```git
git submodule init

git submodule update
```

当然，还有一个 **简单点的方法**：给 `git clone`  命令加上 `--recursive`  参数，它会自动初始化并更新仓库中的每一个子模块代码。

```git
git clone https://example.git --recursize
```

### 更新子模块

```git
git submodule update --remote
```

### 参考

- [Git 工具 - 子模块](https://git-scm.com/book/zh/v2/Git-工具-子模块)
