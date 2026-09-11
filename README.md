# LiveVote

长期可复用实时投票系统的最小可用版本。

- DISPLAY：访问 GitHub Pages 根路径。
- VOTE：访问 `?vote=1`。
- 当前候选人：张三、李四、王五。
- 数据结构：`polls/class-demo/votes/{firebaseAuthUid}`。
- 实时显示：Firestore `onSnapshot`。
- 一人一票：Firestore Rules 只允许匿名登录用户 create 自己 UID 对应的投票文档，不允许 update/delete。

## Firebase

需要启用：

- Cloud Firestore
- Anonymous Authentication
- Web App config

需要部署：

- `firestore.rules`

GitHub Pages workflow 通过 repository secrets 注入 Firebase Web config。
