# SelfHostingPhotoStorage

## 構成
```bash
.
├─ compose.yaml
├─ .env.example            # ❶ 環境変数の見本（本番は .env を別配布）
├─ Caddyfile               # 任意
├─ scripts/
│  ├─ backup.sh            # ❷ rsync + pg_dump（本番・開発で動く）
│  └─ notify-discord.sh    # ❸ Webhook用（汎用）
├─ ops/
│  ├─ immich.service       # ❹ systemd unit（本番）
│  └─ immich-backup.{service,timer}
└─ Makefile                # ❺ よく使う操作をコマンド化
```
