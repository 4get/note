
= 本地镜像 =
- http://172.16.55.54/
- curl http://172.16.55.54/repo > /bin/repo
- chmod a+x /bin/repo

- repo init -u git://172.16.55.54/aosp/platform/manifest --repo-url=git://172.16.55.54/aosp/tools/repo
- repo sync

= android version control =
== 查看可切换的分支 ==  
- cd .repo/manifests  
- git branch -a

== 检出一个分支 ==
- git tag
- repo init -b android-xxx
- repo sync (not needed if your local copy is up to date)
- repo start yyy --all   

== repo操作git ==
- repo forall -c git co -f 
- repo branches 

== 再次mirror ==
- repo init -u git://172.16.55.54/aosp/platform/manifest -b master --repo-url=git://172.16.55.54/aosp/tools/repo --mirror
- repo sync

- repo init -u /workspace/aosp_mirror/platform/manifest.git --repo-url=/workspace/aosp_mirror/tools/repo.git/ -b android-xxx
- repo sync
- repo start yyy --all
- repo branches

#在checkout的时候会有一些仓库不在manifest.xml中列出来，可以在/workspace/aosp_mirror/.repo/manifests中用git checkout出相应的版本，然后在mirror里面执行repo sync
#真是折腾 ?

- repo init -u ssh://172.16.55.90/aosp/platform/manifest --repo-url=ssh://172.16.55.90/aosp/tools/repo

