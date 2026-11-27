# ポーズ人形メーカー

人物写真1枚（2人まで）から、デッサン人形風のポーズ線画を作って保存する個人用Webアプリ。
写真は端末内だけで処理されます。

https://realbon1-max.github.io/pose-doll/

## 使用している解析モデル・ライブラリ
- 全身の骨格：Ultralytics YOLO11-pose（L / X、ONNX fp16 に変換・分割して `models/` に配置） — AGPL-3.0
- 足先・奥行き・手指・顔：Google MediaPipe Tasks Vision 1.2.2（モデルは Google の公式URLから読み込み） — Apache-2.0
- 深度推定（ControlNet Depth・前後補正）：Depth Anything Small（ONNX fp16、`models/da1s.part*`） — Apache-2.0
- 実行エンジン：onnxruntime-web 1.31.1 — MIT
