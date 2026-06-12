# about 目录

公众号发布助手「关于」页远程资源，应用启动时会拉取本目录下的文件。

## 文件

| 文件 | 说明 |
|------|------|
| `about_info.json` | manifest：文案、链接、`update_flags` |
| `about_qr.png` | 公众号二维码 |

## 日常更新（git push）

本地仓库缓存路径（首次由应用自动 clone）：

```
wechat_publisher/.cache/github_repos/Liwhappy_Image/
```

```bash
cd .cache/github_repos/Liwhappy_Image

# 编辑 about/about_info.json 或替换 about/about_qr.png
# 需要提示用户时，把 update_flags 对应项 +1

git add about/
git commit -m "chore: update about"
git push origin main
```

也可先改项目内 `github_upload/about/`，再复制到上述目录后 commit。
