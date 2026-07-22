# 現役バス運転士 × Python — 運行管理を「動くコード」で検証する

首都圏で路線・空港リムジンバスを運転しています。運転職通算25年(バス19年、クレーン車2年、海上コンテナ約1年、一般貨物3年)、運行管理有資格者です。

## いま作っているもの

**[tenkobo-system](https://github.com/masao-traffic-mobility/tenkobo-system)** — 乗務割当と点呼記録の検証システムです。改善基準告示(2024年改正)の拘束時間・休息期間・連続運転のチェックを決定論的なPythonで実装し、pytest 37件がパスしています(合成データのみ使用、SEED=42)。

設計思想はひとつ: **コンプライアンス判定はLLMに任せず、決定論的なコードで行う。** AIは開発の加速に使い、法令適合の判断そのものには使いません。

## なぜ運転士がコードを書くのか

運行管理の現場には、仕様書に書かれていない制約が無数にあります。点呼の実務、交番の組み方、改善基準告示の解釈——これらを一次情報として持つ人間が自分で実装すれば、机上の要件定義では拾えない検証ロジックが書けます。フロントラインの暗黙知を、再現可能なコードに変換することがこのアカウントの目的です。

## 関心領域

- 自動運転移行期における人間の役割
- GTFS-JPと公共交通オープンデータ
- 労務コンプライアンスの決定論的検証
- 現場ドメイン知識 × AI駆動開発

---

# A Bus Driver Who Writes Python

I've spent **25 years behind the wheel** — 19 of them driving route and airport limousine buses in the Tokyo metropolitan area — and I hold a Japanese transport operations manager qualification (運行管理者). Now I turn that frontline knowledge into working code.

## Current project

**[tenkobo-system](https://github.com/masao-traffic-mobility/tenkobo-system)** — a crew assignment and roll-call (tenko) record validation system for bus operations. It implements compliance checks against Japan's 2024-revised driver working-hour regulations (Kaizen Kijun Kokuji): daily restraint time, rest periods, and continuous-driving limits — all in deterministic Python, with 37 passing pytest cases. Synthetic data only (SEED=42); no operational data ever enters this repository.

**Design principle:** compliance-critical decisions belong in deterministic code, not LLM judgment. I use AI to accelerate development, never to decide whether an operation is legal.

## Why this matters

Transport operations are full of constraints that never make it into spec documents. Having performed roll-calls, driven the schedules, and lived inside these regulations, I can write validation logic that desk-based requirements gathering would miss. My goal is to convert frontline tacit knowledge into reproducible code — and to explore what the human role looks like during the transition to autonomous driving.

## Interests

- The human role in the autonomous-driving transition era
- GTFS-JP and open public-transport data
- Deterministic validation of labor compliance
- Domain expertise × AI-assisted development
