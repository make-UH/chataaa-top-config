# chataaa-top-config

Chat AAA ログイン前トップページの A/B テスト設定（`guest_top.json`）。
アプリ起動時に raw.githubusercontent.com から読み込む（デプロイ不要で差し替え可能）。
AI社員（03 マーケ）が毎朝、前日の登録率（app_config/ab_results）を見て更新する。
UI の文言と画像/動画 URL 以外は含めない（秘密情報は絶対に置かない）。

- 使えるキーと制約: `chataaa/lib/services/analytics/guest_top_ab_service.dart` の先頭コメント参照。
- `experimentId` を変えると端末の振り分けが引き直される。同じ実験を続ける間は変えない。
- 画像/動画 URL は https かつ許可ホスト（firebasestorage.googleapis.com / raw.githubusercontent.com / chat-aaa.com / makeuh.co.jp）のみ有効。
