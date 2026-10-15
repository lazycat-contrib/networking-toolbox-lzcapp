# Networking Toolbox - LazyCat App

[Networking Toolbox](https://github.com/lissy93/networking-toolbox)（100+ 离线优先的网络工具集）的懒猫微服（LazyCat）打包。

## 模式

- **镜像模式（mirror）**：`docker.io/lissy93/networking-toolbox` 镜像经 `docker.1ms.run` 加速器拉取，`require_digest_match: true` 校验镜像内容与上游一致。
- **自动跟随上游**：每日检查上游 semver tag（`channel: stable`），发现新版本自动更新版本号与镜像、构建 LPK、发布商店。
- **喵喵商店发布**：仅私有商店（MiaoMiao private store），不发布官方商店。

## 说明

- SvelteKit 单容器，无状态无数据库，无数据卷
- 工具全部离线运行（纯前端计算），`/health` 健康检查
- 非 root 运行（镜像内 sveltekit 用户）

## 所需 Secrets

| Secret | 说明 |
| --- | --- |
| `APPSTORE_URL` / `APPSTORE_TOKEN` | 喵喵商店 API 地址与发布令牌 |
| `APP_ID` | 可选 |
| `PRIVATE_STORE_GROUP_CODES` | 可选，私有分组码 |

## 许可

MIT（上游）
