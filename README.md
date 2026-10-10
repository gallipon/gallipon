バックエンド・インフラを中心に開発しているエンジニアです。仕事では PHP / AWS / コンテナを軸に、サービスの改修・運用やレガシーシステムの刷新を手がけています。開発には GitHub Copilot / Claude Code を併用しています。

趣味では Raspberry Pi や ESP32 系マイコンで自宅用のデバイスを作っています。

### 自宅 IoT

| リポジトリ | 内容 |
|---|---|
| [interphone-doorbell-webhook](https://github.com/gallipon/interphone-doorbell-webhook) | インターホン親機の移報出力を ESP32 で監視し、呼出をスマホに通知（本体無改造） |
| [raspiwol](https://github.com/gallipon/raspiwol) | MQTT 経由で外出先から PC を起動する Wake-on-LAN デーモン（Raspberry Pi）。GPIO による電源ボタン操作のフォールバック付き |
| [m5stackwol](https://github.com/gallipon/m5stackwol) | raspiwol のマイコン版（Wio Terminal / M5Stack）。ボタン・HTTP API・MQTT の3経路 |
| [m5atom-clock](https://github.com/gallipon/m5atom-clock) | M5Atom Matrix + 7セグ LED の NTP 時計。人感センサー内蔵。毎時53分は WiFi を切る省電力運用 |
| [housemonitor](https://github.com/gallipon/housemonitor) | 自宅の温湿度・気圧・在室状況の収集・可視化（Raspberry Pi → PHP API → MySQL → Chart.js） |
| [tapo-power-monitor](https://github.com/gallipon/tapo-power-monitor) | スマートプラグの消費電力を LAN 内で直接収集し、VPS の自作ダッシュボードで可視化。1分粒度の記録・推定電気代・収集停止の通知（Raspberry Pi → PHP API → MySQL → Chart.js） |

デバイス間の連携:

```
m5atom-clock（人感センサー）──→ housemonitor（収集・可視化・死活監視）
raspiwol ⇄ m5stackwol（同一機能の Raspberry Pi 版 / マイコン版）
```

### その他

- [tumblr-dashboard-bookmark-helper](https://github.com/gallipon/tumblr-dashboard-bookmark-helper) — Tumblr の既読位置ブックマークを強調表示するブラウザ拡張
