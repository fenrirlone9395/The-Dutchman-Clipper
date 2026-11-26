# Changelog

## 1.0.1

- VST3／AU／StandaloneをUniversal（arm64＋x86_64）へ統合。
- Apple Silicon版とIntel版を選ばず、同じバンドルをインストールできる配布形式へ変更。
- バージョン表記を1.0.1へ更新。DSPとパラメータの仕様は1.0.0から変更なし。
- arm64ネイティブ／Rosetta x86_64で検証。Intel実機での動作・CPU負荷は未確認。

## 1.0.0

- ステレオリンク100%のLimiter／Maximizer。Drive 0〜+18 dB、Ceiling、Release、Lookahead。
- Oversampling ×1／×2／×4／×8、独立したTrue Peak検出と最終出力の保護。
- Adaptive Knee／Active Transient Shaperと介入量の可視化。
- ステレオInput／Output Peak、GR、True Peak、Short-Term／Integrated LUFS。
- 4つのファクトリープリセット、状態保存・復元、4ノブのホイール操作。
- macOS 14以降のApple Silicon向けVST3／AU／Standalone。

TP保護の安全余裕は0.15 dB。48 kHzでの報告遅延は721サンプル（約15.02 ms）。詳細な試験条件と未検証項目はREADMEを参照。

旧状態の負のDrive値は0 dBへ変換する。ホストが正規化値で記録した旧Driveオートメーションは再確認が必要。
