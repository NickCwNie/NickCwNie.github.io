---
title: Stydy Git - work on github
key: 20180701
tags: TeXt
---

# Stydy Git :: work on github

## PREPARE
+ gitbash
  - tell gitbash who you are. git config --global user.name "xxx" (and user.email)
+ github account
+ abbr.
  - [gb] = gitbash-side
  - [gh] = github-side

## STEP  
*[gb]*1. ssh-keygen -C "xxx@xxx.com"   # 注意一定要指定邮箱来生成key pair  
*[gb]*1. cat ~/.ssh/id_rsa.pub, then copy output  
*[gh]*2. github->settings, add ssh pub key  
*[gb]*3. create project, then git remote -v   # 检查提交地址是否正确  
*[gb]*4. commit to local, then push to upstream, git push -u origin master  

## FAQ  
**Q:**  
**A:**  
