# SEU-SIGMLSystem.github.io
### 如何更新：
    git clone https://github.com/SEU-SIGMLSystem/SEU-SIGMLSystem.github.io.git
    cd SEU-SIGMLSystem.github.io.git
    (or: git pull origin main)
#### git绑定账户
    git config --global user.name "yourname"
    git config --global user.email "youremail"
    # 若需要输入passwd，则需要使用生成的token而不是github密码
#### 创建自己的本地分支
    git checkout -b XXX
#### 在远程仓库中生成分支
    git push origin XXX
#### 绑定远程分支和本地分支
    git branch --set-upstream-to=origin/XXX XXX
#### 修改 schedules.js
    {
        "title":"...",
        "conf":"...",
        "presenter":"...",
        "facilitator":"...",
        "date":"...",
        "time":"...",
        "location":"...",
        "links":[
            {
                "title":"TencentMeeting",
                "url":"..."
            },
            {
                "title":"Slides",
                "url":"/slides/..."
            },
            {
                "title":"Videos",
                "url":"http://10.201.0.220:8099"
            }
        ],
        "dblp":{
            "source":"DBLP",
            "url":"..."
        }
    },
#### 修改 index.html (line 60)
    <div class="description">... will present an ... paper on ..., ... at ... .</div>
#### 上传更新至XXX分支 
    git add index.html
    git add schedules.js
    git add /slides/...
    git commit -m "update ... schedule"
    git push origin XXX
#### 在github界面实现pull requests申请，由管理员审批通过后完成merge
#### 查看远程与本地分支 
    git branch -a
#### 删除远程与本地分支
    git checkout main
    git push origin --delete XXX
    git branch -D xxx
