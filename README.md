# 测试博客

## Azure Web App 运行建议

- 建议部署到 Linux Web App，启动命令保持 `npm start`。
- 在 Azure Portal 开启 `Always On`，Health check path 配置为 `/healthz`。
- 运行时文件默认写入 `/home/argoblog`，可通过环境变量 `ARGO_RUNTIME_DIR` 覆盖。
- `/healthz` 只检查 Node 进程是否存活；`/readyz` 会额外检查 Xray 和 Cloudflared 进程状态。
- 启动和重启服务会立即返回，实际进度通过页面状态、`/suoha-status`、`/logs` 查看。




## 免责声明:
* 本程序仅供学习了解, 非盈利目的，请于下载后 24 小时内删除, 不得用作任何商业用途, 文字、数据及图片均有所属版权, 如转载须注明来源。
* 使用本程序必循遵守部署免责声明。使用本程序必循遵守部署服务器所在地、所在国家和用户所在国家的法律法规, 程序作者不对使用者任何不当行为负责。
