# Siemens Opcenter 調査まとめ

調査日：2026-11-15
対象：Siemens Digital Industries Software の製造オペレーション管理（MOM）ポートフォリオ「Opcenter」

> 注記：本資料は公開Web情報（Siemens公式ブログ、プレス、業界メディア、第三者レビュー）をもとにしています。出典の多くは Siemens 自身のマーケティング情報です。バージョン番号や機能の詳細は、導入検討の際に Siemens 公式のリリースノートや営業窓口で確認してください。

---

## 1. 概要

- **Opcenter** は、Siemens の製造オペレーション管理（MOM: Manufacturing Operations Management）向けの統合ソフトウェア群です。
- 対象領域は **生産計画・スケジューリング（APS）**、**製造実行（MES）**、**品質管理（QMS）**、**研究開発・ラボ管理（RD&L / LIMS）**、**製造インテリジェンス（分析・レポート）** です。
- Siemens のデジタル化ポートフォリオ **Siemens Xcelerator** の一部です。PLM（Teamcenter）、シミュレーション（Simcenter）、IoT・分析（Insights Hub、旧 MindSphere）、ローコード（Mendix）と連携し、「デジタルスレッド」（設計から製造・品質までデータをつなぐ仕組み）を実現する位置づけです。

## 2. 沿革

| 時期 | 出来事 |
|---|---|
| 2014年 | Siemens が米 Camstar を買収（約3.8億ドルと報道）。エレクトロニクス・医療機器向け MES の中核に |
| 〜2018年 | SIMATIC IT（MES）、Camstar、Preactor（スケジューリング）、SIMATIC IT R&D Suite、QMS Professional などが別ブランドで存在 |
| 2019年6月 | これらを統合し **「Siemens Opcenter」** として新ブランドで発表。MES は **Opcenter Execution**（旧 SIMATIC IT / Camstar）に改称 |
| 2020年代前半 | Mendix ローコードを MES に組み込み、クラウド対応を強化 |
| 2023年頃〜 | SaaS 版 **Opcenter X** シリーズを展開（中堅・中小製造業の入口） |
| 2025〜2026年 | AI 機能（Copilot、チャット機能等）を各製品に搭載。Opcenter X Laboratory（SaaS LIMS）を提供開始（2026年8月発表） |

**旧製品名との対応（主なもの）**

| 旧名称 | 現在の Opcenter 製品 |
|---|---|
| SIMATIC IT / Camstar | Opcenter Execution（各業種版） |
| Preactor | Opcenter APS |
| QMS Professional（IBS） | Opcenter Quality |
| SIMATIC IT R&D Suite / Unilab / Interspec | Opcenter RD&L |
| SIMATIC IT Intelligence 等 | Opcenter Intelligence |

※ Unilab・Interspec の対応関係は一般的に知られた情報ですが、今回の検索では一次ソースを確認できていません。

## 3. 製品構成

### 3.1 Opcenter Execution（MES）
製造指図の実行、作業手順、トレーサビリティ、電子作業記録などを扱う中核 MES です。業種ごとの版があります。

| 製品 | 主な対象 |
|---|---|
| Opcenter Execution **Discrete** | 組立型の製造（機械、自動車部品など）。2607 では資材搬送・輸送計画を強化 |
| Opcenter Execution **Process** | プロセス産業（食品・飲料、化学など） |
| Opcenter Execution **Pharma** | 医薬品（GMP、電子バッチ記録） |
| Opcenter Execution **Electronics** | 電子機器・SMT実装。2604 で AI 機能と、構成済みのバッテリー製造ソリューションを追加 |
| Opcenter Execution **Medical Device & Diagnostics（MDD）** | 医療機器（規制対応、DHR）。2604 で Mendix ベースの拡張、チャット機能を追加 |
| Opcenter Execution **Semiconductor** | 半導体前工程・後工程 |
| Opcenter Execution **Core / Foundation** | 共通の MES 基盤（業種版の土台、独自に作り込むための基盤） |

### 3.2 Opcenter APS（Advanced Planning & Scheduling）
- 旧 Preactor の技術がベースで、有限能力スケジューリングと生産計画を行います。
- 2025年に IDC MarketScape でリーダーに選定。最近のリリースは 2510（2025年10月）、2606（2026年6月）。

### 3.3 Opcenter Quality（QMS）
- 統合品質管理：SPC、不適合（NC）・CAPA、FMEA、監査、検査計画などを扱います。
- SaaS 版 **Opcenter X Quality** があります（2607 で SPC の検査・評価タイプを拡張し、不適合管理を改善）。
- Verdantix Green Quadrant（品質管理ソフトウェア 2025）でリーダーに選定。

### 3.4 Opcenter RD&L（Research, Development & Laboratory）
- 配合・仕様管理、ラボ情報管理（LIMS）、試験管理、知財やナレッジの管理を扱います。主にプロセス産業向けです。
- SaaS 版 **Opcenter X Laboratory**（クラウド型 LIMS）を2026年8月に発表。

### 3.5 Opcenter Intelligence
- 製造データの集約、KPI 可視化、レポーティングを行います。クラウド版 Opcenter Intelligence Cloud もあります。

### 3.6 Opcenter Intra Plant Logistics
- 工場内物流（資材供給・搬送）の管理。2601、2607 がリリース済み。

### 3.7 Opcenter X（SaaS）
- クラウドネイティブな共通基盤の上で、MES、品質、スケジューリング、LIMS を提供する SaaS シリーズです。
- 中堅・中小企業でも、小さく始めて段階的に広げやすいことを狙っています。
- 最新：**Opcenter X 2607**（2026年8月）。Track & Trace の改善（Work Order グリッドに Type 列を追加など）、Visual Information Navigator のヘッダー刷新、製品間の連携強化。

## 4. 技術的な特徴

- **バージョン体系**：「YYMM」形式（例：2604 = 2026年4月、2607 = 2026年7月）。多くの製品が年数回リリースされます。
- **Mendix ローコード統合**：MES に Mendix を組み込み、UI や業務アプリを低コードで拡張できます。業種別のローコードテンプレートも提供。Siemens は導入事例（DAB Pumps）で開発工数30%削減と報告しています（ベンダー発表値）。
- **Xcelerator 連携**
  - Teamcenter（PLM）：設計 BOM・工程情報を MES に連携（closed-loop manufacturing）
  - Insights Hub：時系列・検査データを MES/PLM のコンテキストと結びつけて分析・AI 化
  - Simcenter / Tecnomatix：シミュレーション、デジタルツイン
- **AI / Copilot**
  - Insights Hub Production Copilot：生産データから問題の特定、根本原因分析、現場作業の支援
  - Copilot Studio：ユーザーが独自スキルを定義
  - Siemens は Teamcenter・Polarion・Opcenter 向けに9つの新しい AI Copilot を発表（2026年 CES 前後）
- **導入形態**：オンプレミス、プライベートクラウド、SaaS（Opcenter X）。

## 5. 市場評価

| 評価 | 内容 |
|---|---|
| Gartner Magic Quadrant for MES | 2017年の初版から連続でリーダー。2023年版で6回連続。主な競合は Dassault（DELMIA Apriso）、SAP など。※2024年以降の版は今回の調査で未確認 |
| Nucleus Research | 2026 MES Technology Value Matrix でリーダー |
| IDC MarketScape | 2025年、APS 分野でリーダー（Opcenter APS） |
| Verdantix Green Quadrant | 品質管理ソフトウェア 2025 でリーダー |

## 6. 主な導入業種と事例

- 対象業種：自動車、航空宇宙・防衛、エレクトロニクス・半導体、医療機器、医薬品、食品・飲料、化学、産業機械など
- 公開事例の例：Zimmer Biomet（医療機器、次世代製造のデジタル基盤）、Rolls-Royce（Teamcenter・Opcenter・Insights Hub・Simcenter・Mendix によるデジタルスレッド）、DAB Pumps（Mendix による拡張）

## 7. 導入検討時のポイント

1. **製品選定**：業種版 MES（Discrete / Process / Pharma など）か、SaaS の Opcenter X かで、導入規模・カスタマイズ性・コストが大きく変わります。
2. **連携範囲**：ERP（SAP 等）、PLM（Teamcenter）、設備（PLC/SCADA、OPC UA）とのインタフェース設計が工数の大半を占めがちです。
3. **規制対応**：医薬・医療機器では FDA 21 CFR Part 11、GMP、バリデーション（CSV/CSA）への対応が必要です。
4. **バージョンアップ**：リリースが頻繁なため、カスタマイズは Mendix 等の拡張ポイントに寄せ、アップグレードしやすさを保つのが推奨されます。
5. **導入パートナー**：Siemens 本体だけでなく、認定 SI パートナー（日本国内含む）経由の導入が一般的です。

## 8. 未確認・要追加調査の事項

- Gartner MES Magic Quadrant 2024年以降の評価
- Opcenter Connect MOM 等の製品が現在どう位置づけられているか
- 日本国内の導入事例、価格体系（ライセンス／サブスクリプション）
- Opcenter X 2607 より新しいリリースの有無

---

## 出典

- [Siemens Opcenter Blog – Product Updates](https://blogs.sw.siemens.com/opcenter/category/product-updates/)
- [What's New in Opcenter X 2607](https://blogs.sw.siemens.com/opcenter/whats-new-in-opcenter-x-2607/)
- [What's new in Opcenter X Quality 2607](https://blogs.sw.siemens.com/opcenter/whats-new-opcenter-x-quality-2607/)
- [What's new in Opcenter Execution Electronics 2604](https://blogs.sw.siemens.com/opcenter/whats-new-in-opcenter-execution-electronics-2604/)
- [What's new in Opcenter Execution MDD 2604](https://blogs.sw.siemens.com/opcenter/whats-new-in-opcenter-execution-mdd-2604/)
- [Opcenter Execution Discrete (blog)](https://blogs.sw.siemens.com/opcenter/product/opcenter-execution-discrete/)
- [Siemens Opcenter Blog – News](https://blogs.sw.siemens.com/opcenter/category/news/)
- [CIMdata: Siemens launches Siemens Opcenter (2019)](https://www.cimdata.com/en/industry-summary-articles/item/12163-siemens-launches-siemens-opcenter-a-new-unified-portfolio-of-manufacturing-operations-management-solutions)
- [Automation.com: Siemens announces Siemens Opcenter](https://www.automation.com/article/siemens-announces-siemens-opcenter-software-soluti)
- [TeepTrak: What Is Siemens MES Called in 2026?](https://teeptrak.com/en/siemens-mes-software-name-explained/)
- [Siemens: MES leader 2021 Gartner Magic Quadrant](https://blogs.sw.siemens.com/opcenter/mes-leader-2021-gartner-magic-quadrant/)
- [Siemens Newsroom: Gartner Magic Quadrant MES 2023](https://newsroom.sw.siemens.com/zh-CN/gartner-magic-quadrant-mes-23)
- [Siemens and Mendix recognized as Leaders](https://blogs.sw.siemens.com/opcenter/siemens-and-mendix-recognized-as-leaders-in-manufacturing-execution-systems-and-low-code-application-development/)
- [Mendix: Opcenter Uses Low-Code to Scale Front-End Customizations](https://www.mendix.com/partners/stories/opcenter-uses-low-code-to-scale-meaningful-front-end-customizations/)
- [Unleash the power of the Opcenter MES platform with Mendix](https://blogs.sw.siemens.com/opcenter/unleash-the-power-of-the-opcenter-mes-platform-with-mendix-low-code-capabilities/)
- [AI shaping the future of autonomous operations](https://blogs.sw.siemens.com/opcenter/ai-shaping-the-future-of-autonomous-operations/)
- [Powering manufacturing's future: AI, IIoT and MES](https://blogs.sw.siemens.com/opcenter/powering-manufacturings-future-how-ai-iiot-and-mes-drive-the-smart-factory/)
- [Automation World: Siemens unveils three major AI initiatives / nine new copilots](https://www.automationworld.com/factory/digital-transformation/news/55343456/siemens-unveils-three-major-ai-initiatives-physical-ai-deployment-with-nvidia-digital-twin-composer-release-and-nine-new-copilots)
- [Tech-Clarity: Siemens Opcenter's TCO and scalability](https://tech-clarity.com/siemens-opcenters-tco-and-scalability-help-fuel-digital-thread/22956)
- [Verdantix: Siemens Opcenter MOM](https://atlas.verdantix.com/siemens/opcenter-mom)
- [Verdantix: Opcenter X Quality](https://atlas.verdantix.com/siemens/opcenter-x-quality)
- [Siemens News: QMS Verdantix 2025](https://news.siemens.com/de-de/siemens-qms-verdantix-2025/)
- [Lokad: Review of Siemens（第三者評価）](https://www.lokad.com/review-of-siemens-com/)
