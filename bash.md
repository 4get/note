
ctrl+r 搜索以前输入过的命令。

ctrl+w 向后删除一个词(到一个空格)

export PROMPT_COMMAND='{ msg=$(history 1 | { read x y; echo $y; });user=$(whoami); echo $msg:$PWD:$(date "+%Y-%m-%d %H:%M:%S"):$user:$(who am i); } >> /workspace/.history-$(date "+%Y-%m")'

