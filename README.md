# hello world

# About user account
1. init repo helloworld
2. settings and push to wayneshawn/helloword
! commit user on github is waynehpc
causes:
git config --global user.name/email settings before with waynehpc

$git config --list
credential.helper=osxkeychain
user.email=zwx11@mails.tsinghua.edu.cn
user.name=waynehpc

$vim .git/config
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
	ignorecase = true
	precomposeunicode = true
[remote "origin"]
	url = https://github.com/wayneshawn/helloworld.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = origin
	merge = refs/heads/master


Change username and email locally for current repo
$git config user.name "xxx"
$git config user.email "xxx@gmail.com"
this will add contents to .git/config
[user]
	name = wayneshawn
	email = singleon11@gmail.com

remote: error: GH007: Your push would publish a private email address.
remote: You can make your email public or disable this protection by visiting:
remote: http://github.com/settings/emails
To https://github.com/wayneshawn/helloworld.git
 ! [remote rejected] master -> master (push declined due to email privacy restrictions)

be careful that this cmd will cause loss of latest change. backup files before do this.
$git reset --hard HEAD^
delete email in .git/config
commit and push again

