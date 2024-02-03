# git-bash 配置

## 配置 `.bash_profile`

> 如果不存在该文件，则创建。

```bash
source ~/.bashrc

# Github Token for release-it
export GITHUB_TOKEN="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"

# Shows Git branch name in prompt.
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
# 显示 用户 @ 主机
# export PS1="\u@\h \W\[\033[32m\]\$(parse_git_branch)\[\033[00m\] $ "
# 隐藏用户 @ 主机，显示当前文件夹
#export PS1="\W\[\033[32m\]\$(parse_git_branch)\[\033[00m\]"

# 只显示当前文件夹
export PS1="\[\e[32;1m\]\W $\[\e[0m\]\[\033[32m\]\$(parse_git_branch)\[\033[00m\] "

# 显示全路径
#export PS1="\[\e[32;1m\]\w $\[\e[0m\]\[\033[32m\]\$(parse_git_branch)\[\033[00m\] "
```

## 配置 `.bashrc`

> 如果不存在该文件，则创建。

配置常用别名:

```bash
alias hs="http-server ."
alias gh="cd /d/www/github"
alias t="treei"
alias demo="cd /d/www/demo"
```

## 参考

- [Windows下的Git Bash配置，提升你的终端操作体验](https://zhuanlan.zhihu.com/p/418321777)