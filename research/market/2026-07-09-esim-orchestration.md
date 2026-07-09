# eSIM オーケストレーション競争環境(SGP.32 / SGP.42 / eIM / RSP)— 2026-07-09

> 作成: market-scout ／ 作成日: 2026-07-09 ／ 対象期間: 2024-10 〜 2026-07(構造理解に必要な過去経緯を含む)／ テーマ: コネクティビティ・ロードマップ議論 T2(eSIM オーケストレーション)
> 位置づけ: `2026-07-09-connectivity-roadmap-briefing.md` C 表 T2 の裏取り + 競争環境スキャン。公開情報のみに基づく参考情報であり投資判断ではない。

## TL;DR(経営向け)

- **SGP.32 の商用化は 2026 年前半に一斉スタートした。** Telenor(2026-04-17 出荷開始)、Tele2×IDEMIA×Cisco(MWC26)、emnify(2026-03)、floLIVE(2026-02)、Eseye(2026-04)、KORE×Kigen(2026-04 発表)が出揃い、日本でも 2026-07 に国内初商用(当社×KDDI、公開発表済み)。「対応の有無」は 2026 年内に差別化要素でなくなる。
- **価値の重心は eIM 単体からその上の「オーケストレーション層」へ移動済み。** GSMA 認証 eIM は既に 6 社超、無償 eIM(TEAL OpenEIM)まで出現しコモディティ化が進行。差別化は MNO プロファイル調達力・ポリシー自動化・マルチ RSP(SGP.02/.22/.32)統合管理に移っている。
- **北米 MNO はプロファイル供与に動いた(AT&T が Rivian R2 へ、Verizon は Aeris 経由)が、Rogers は公開情報なし。** 日本はドコモ・ソフトバンクの公表がなく、KDDI のみ商用化。プロファイル調達競争は「早い者勝ち」の局面。
- **SGP.42(IFPP)は仕様確定前(2026 Q3 見込み)に商用前哨戦が開始。** MWC26 で Tele2×Acceleronix×IDEMIA が量子耐性 IFPP アーリーアクセスを発表。車載 1-SKU は Rivian R2(SGP.32)が先行事例。2027 年の車載・大量出荷 RFP では IFPP 対応が入場券になる公算。
- **M&A 含意: SGP.32 は「回線再販型 MVNO」の堀を消す。** P4 買収スクリーニングに「プラットフォーム IP(SM-DP+/eIM/オーケストレーション)保有」を必須条件として追加すべき。新規候補 4 社(1oT、Acceleronix、コモン・クリエーション、Eseye=モニタ)を deal-desk に提案。

## 1. 主要ファインディング

### 1.1 標準化の現在地(SGP.31/.32/.33/.41/.42)

| 仕様 | 状態 | 日付 | 出典 |
|---|---|---|---|
| SGP.32 v1.0(技術仕様) | 公開 | 2023-05-26 | [Webbing](https://webbingsolutions.com/gsma/)、[GSMA](https://www.gsma.com/solutions-and-impact/technologies/esim/esim-specification/) |
| SGP.32 v1.1 | 公開 | 2024 前半(推定。GSMA 公開 PDF のパス 2024/04 より) | [GSMA PDF](https://www.gsma.com/solutions-and-impact/technologies/esim/wp-content/uploads/2024/04/SGP.32-v1.1.0.pdf) |
| SGP.32 v1.2 | 公開(**現行の商用認証基準**) | 2024-05〜06 頃(推定。PDF パス 2024/06、tracker 逆算 ~2024-05-30) | [GSMA PDF](https://www.gsma.com/solutions-and-impact/technologies/esim/wp-content/uploads/2024/06/SGP.32-v1.2.pdf)、[symb-iot tracker](https://iotconnectivitymarketplace.symb-iot.com/sgp32-tracker) |
| テスト・コンプライアンス・セキュリティ(eSA)体系 | v1.2 と併せ導入 | 2025-01 | [G+D PR 経由](https://iotbusinessnews.com/2025/04/29/61467-gd-becomes-first-company-to-achieve-gsma-esim-compliance-and-certification-for-iot-euicc-product/) |
| **SGP.32 v1.3** | **公開** | **2026-05-28**(GSMA リソースページの日付。一次ページは閲覧不可のため検索スニペット由来。**変更点の詳細は確認不能**) | [GSMA v1.3 ページ](https://www.gsma.com/solutions-and-impact/technologies/esim/gsma_resources/sgp-32-v1-3/) |
| SGP.41 v1.0(IFPP 要件) | 公開 | 2025-02 | [GSMA](https://www.gsma.com/solutions-and-impact/technologies/esim/gsma_resources/esim-ifpp-architecture-and-requirements/)、[Kigen 用語集](https://kigen.com/glossary/sgp42-remote-sim-provisioning/) |
| SGP.42(IFPP 技術仕様) | **未確定**。2026 Q3 確定見込み | — | [Kigen 用語集](https://kigen.com/glossary/sgp42-remote-sim-provisioning/)(検索要約経由、一次ページ閲覧不可) |

- 重要な含意: 業界の商用認証・展開は **v1.2 基準**で構築されており(sgp32.co.uk 2026-05-11 時点でも「v1.2 が設計基準」)、v1.3(2026-05-28)への移行は始まったばかり。v1.3 の変更点は公開ソースで特定できず(確認不能)。[sgp32.co.uk](https://sgp32.co.uk/sgp32-v12-current-specification/)
- テスト仕様(SGP.33)の完全版が使えるのは 2025 年初以降で、フィールド実績は依然浅いという指摘。[sgp32.co.uk FAQ](https://sgp32.co.uk/sgp32-faq/)

### 1.2 商用化の現在地(ローンチ済みプレイヤーと出荷事例)

- **Telenor IoT**: 2025-04 に SGP.32 採用を表明 → **2026-02-27 商用可用性を発表、2026-04-17 から SIM 出荷開始**。「大規模展開向けに完全標準準拠の SGP.32 SIM を提供する世界初級のオペレーター」と自称。出荷数量は非開示。[Telenor IoT PR (2026-02-27)](https://iot.telenor.com/press-release/telenor-iot-announces-commercial-availability-of-sgp-32-sim-cards-enabling-the-next-generation-of-global-iot-deployments/)、[The Fast Mode](https://www.thefastmode.com/technology-solutions/47390-telenor-iot-launches-sgp-32-esims-for-global-iot-deployments)。sgp32.co.uk は「フル商用に至った初のメジャーオペレーター」と評価。[sgp32.co.uk FAQ](https://sgp32.co.uk/sgp32-faq/)
- **Tele2 IoT × IDEMIA × Cisco**: MWC26(2026-03-02〜05)で「商用エンドツーエンド SGP.32 IoT ソリューション」を発表(自動車向け想定)。[IoT Business News (2026-05-27)](https://iotbusinessnews.com/2026/05/27/mwc-2026-signals-a-split-iot-connectivity-market-shaped-by-ai-ntn-and-esim-orchestration/)
- **IDEMIA**: 2025-08-18 に「業界初のフル GSMA 認証 SGP.32 ソリューション」を発表。MWC26 時点で**商用展開 15 件超・PoC 40 件**を開示 — 現時点で最も具体的な「規模」の公開数値。[IDEMIA (2025-08-18)](https://www.idemia.com/news/idemia-launches-industrys-first-fully-gsma-certified-sgp32-esim-solution-2025-08-18)、[IoT Business News](https://iotbusinessnews.com/2026/05/27/mwc-2026-signals-a-split-iot-connectivity-market-shaped-by-ai-ntn-and-esim-orchestration/)
- **Rivian R2(車載 1-SKU の旗艦事例)**: G+D(eSIM+eIM)× AT&T(初期 MNO)で SGP.32・5G 搭載。ハードウェア変更なしに地域拡大時の MNO 追加・変更が可能な設計。[G+D PR](https://www.gi-de.com/en/about-us/press/press-releases/giesecke-devrient-rivian-and-att-collaborate-to-bring-sgp32-and-5g-connectivity-to-rivians-r2-vehicle)、[Automotive World](https://www.automotiveworld.com/news/rivian-partners-with-gd-att-on-r2-connectivity/)
- **Verifone × Thales**: 次世代 POS 端末に Thales eSIM+SGP.32 を採用(2026-03-11)。[IoT Business News](https://iotbusinessnews.com/2026/03/11/verifone-taps-thales-esim-and-sgp-32-to-simplify-global-connectivity-for-pos-terminals/)
- **日本(国内初商用)**: 当社と KDDI が SGP.32 対応 IoT SIM・プロファイル管理機能を共同開発し商用化検証を完了、**当社 2026-07-07 から・KDDI は 2026 年度下期から提供**(国内通信事業者として初の商用提供)。※公開発表ベースの記録。[KDDI (2026-07)](https://biz.kddi.com/topics/2026/news/016/)、[ITmedia (2026-07-03)](https://www.itmedia.co.jp/mobile/articles/2607/03/news059.html)、[Business Wire (2026-07-08)](https://www.businesswire.com/news/home/20260708308506/en/Soracom-Announces-Commercial-Release-of-SGP.32-Compatible-IoT-eSIMs)
- **未達の指標**: 100 万台級など数量を伴う SGP.32 出荷の公開事例は**まだ存在しない**(確認できず)。市場は「商用開始」フェーズで、規模の証明は 2026 下期〜2027 の論点。

### 1.3 市場規模予測(相場観)

- Kaleido Intelligence: IoT SGP.32 eSIM は **490 万(2025-09 時点)→ 2027 年約 5,000 万 → 2028 年 1.928 億(CAGR 240%)**。eSIM が IoT のデファクトになるのは 2028 年頃、2028 年に IoT eSIM の過半が SGP.32 系へ。[RCR Wireless (2025-09-22)](https://www.rcrwireless.com/20250922/internet-of-things/sgp-32-esim-transform-iot)、[IoT Tech News](https://iottechnews.com/news/kaleido-intelligence-forecasts-esim-adoption-surge-iot/)
- ABI Research: SGP.32 プロファイルダウンロード累計 **約 1.94 億(2029 年まで)**、SGP.22/02 とのクロスオーバーは 2027 年頃。[euicc.co.uk (2026-03-24)](https://euicc.co.uk/what-comes-after-sgp-32-the-esim-transition-the-industry-reckoning-and-what-happens-next/)
- TCA(SIM ベンダー業界団体): 2025 年の世界 eSIM 出荷は **6.05 億個(+18%)**、コンシューマープロファイル DL +43%。SGP.32 対応 SM プラットフォームの増加を「移行が進行中」の根拠として提示。[TCA (2026-03)](https://trustedconnectivityalliance.org/trusted-connectivity-alliance-members-confirm-acceleration-of-global-esim-growth-in-2025/)、[IoT Business News (2026-03-04)](https://iotbusinessnews.com/2026/03/04/tca-members-confirm-acceleration-of-global-esim-growth-in-2025/)

### 1.4 eIM の主導権争いと運用課題

- **eIM 認証は既に混雑**: GSMA 認証済み eIM は 1oT(2024-08)、Kigen(2025-01)、Redtea Mobile(2025-03)、Eastcompeace(2025-05)、IDEMIA(2025-08)、Thales(2025-11、SAS-SM)。未認証ながら自社 eIM を持つ事業者として G+D(AirOn360)、Trasna、emnify、BICS、Eseye、Transatel 等が追跡されている。[symb-iot tracker (2026-04-26 更新)](https://iotconnectivitymarketplace.symb-iot.com/sgp32-tracker)
- **無償 eIM の出現**: TEAL が「OpenEIM」を無償・オープン路線で投入(発表日未確認)。eIM 単体の値付けが困難になる先行指標。[TEAL](https://tealcom.io/post/teal-launches-openeim-sgp-32-esim-platform-a-free-and-open-approach-to-esim-management/)
- **主導権は eIM の上へ**: Wireless Logic は eIM/SM-DP+/IPA を抽象化する「eSO(eSIM Orchestrator)」をマネージドサービスとして提示(プロファイル在庫管理・ポリシー自動化・複数 SM-DP+ 集約)。Eseye は SGP.02/.22/.32 の**マルチ RSP 統合管理**を打ち出し、Thales・IDEMIA・Kigen いずれの RSP にも対応と明言。業界メディアも「価値はプロファイル切替そのものではなく、いつ・なぜ切り替えるかを決めるオーケストレーション層」と総括。[Wireless Logic](https://wirelesslogic.com/iot-glossary/what-is-eso)、[Eseye (2026-04-22)](https://www.eseye.com/eseye-strengthens-global-iot-resilience-with-sgp-32-esim-orchestration/)、[IoT Business News (2026-05-27)](https://iotbusinessnews.com/2026/05/27/mwc-2026-signals-a-split-iot-connectivity-market-shaped-by-ai-ntn-and-esim-orchestration/)
- **eIM ポータビリティ**: 規格上は「ハードウェア交換なしに eIM 事業者を変更できる」ことが SGP.02(SM-SR ロックイン)との決定的差分とされる。ただし**異ベンダ間(eUICC OS × eIM × SM-DP+)の相互運用テストは初期段階**で、ベンダー間移行の実運用事例は公開されていない(確認できず)。[euicc.co.uk (2026-02)](https://euicc.co.uk/what-is-sgp-32/)
- **Download Interoperability**: 相互運用の検証インフラ整備が進行 — Comprion×G+D(2026-03-05)、Comprion×Thales のテストベッド提携。「プロバイダーが SGP.32 対応と言っても、真のリモートプロファイル DL・ライフサイクル対応かは要検証」という注意喚起が業界 FAQ に明記される段階。[Comprion×G+D](https://iotbusinessnews.com/2026/03/05/comprion-and-gieseckedevrient-partner-for-interoperable-sgp-32-iot-esim-solutions/)、[Comprion×Thales](https://www.comprion.com/company/press/press-release-detail/comprion-partners-with-thales-to-provide-iot-service-providers-with-advanced-sgp32-esim-testing-solution/)、[sgp32.co.uk FAQ](https://sgp32.co.uk/sgp32-faq/)

### 1.5 SGP.42(In-Factory Profile Provisioning)

- 仕様は**未確定**(2026 Q3 確定見込み、SGP.41 要件は 2025-02 公開)だが、プレ標準の商用プログラムが先行:
  - **Tele2 IoT × Acceleronix × IDEMIA**: MWC26 Barcelona で「世界初の量子耐性 IFPP アーリーアクセスプログラム」を発表(2026-02-27)。単一 eSIM 品番(1 SKU)で製造ライン上にプロファイルを書き込み、出荷即接続。SGP.42 互換を明記。[Tele2 PR](https://www.tele2.com/media/news/2026/tele2-iot-acceleronix-and-idemia-secure-transactions-launch-the-first-in-the-world-quantum-safe-in-factory-profile-provisioning-early-access-program-at-mwc26-barcelona/)、[IDEMIA (2026-02-27)](https://www.idemia.com/news/ist-and-acceleronix-unveil-industrys-first-ifpp-mwc26-tele2-iot-2026-02-27)
  - **MWC 上海(2026-06)**: IDEMIA×Quectel×Tele2 IoT が量子耐性 pre-SGP.42 IFPP のエンドツーエンド実演(GSMA PQC ラウンドテーブル)。[GSMA](https://www.gsma.com/solutions-and-impact/technologies/security/post-quantum/quantum-safe-or-quantum-vulnerable-inside-gsmas-second-pqc-roundtable-at-mwc-shanghai/)
  - **floLIVE × Kigen**: Kigen の IFPP で floLIVE マルチ IMSI ブートストラップを工場書込済み eUICC として出荷可能に(2026-02-19)。[IoT Now](https://www.iot-now.com/2026/02/19/155400-flolive-launches-full-support-for-sgp-32-esim-standard/)
  - **emnify**: CES 2026 で「factory-first connectivity」を発表(2025-12-22)。[IoT Business News](https://iotbusinessnews.com/2025/12/22/emnify-debuts-factory-first-iot-connectivity-at-ces-2026/)
- 自動車 1-SKU: 現時点の旗艦は SGP.32 ベースの Rivian R2(上記)。SGP.42 確定後は「工場書込 + 出荷後 SGP.32 切替」の組合せが車載・超大型案件の標準アーキテクチャになるとの見方。[Transforma Insights IFPP ポジションペーパー](https://transformainsights.com/research/reports/in-factory-profile-provisioning-ifpp-position-paper)、[Eseye IFPP 解説](https://www.eseye.com/resources/iot-explained/what-is-in-factory-profile-provisioning-ifpp/)

## 2. 競合・プレイヤー動向

### 2.1 MNO のプロファイル開放姿勢(温度差マップ)

| 地域/MNO | 姿勢(公開情報) | 出典 |
|---|---|---|
| AT&T(米) | **供与に前向き**。Rivian R2 の初期 MNO として SGP.32 プロファイル供与。tracker では「production ready」9 社の一角 | [G+D PR](https://www.gi-de.com/en/about-us/press/press-releases/giesecke-devrient-rivian-and-att-collaborate-to-bring-sgp32-and-5g-connectivity-to-rivians-r2-vehicle)、[tracker](https://iotconnectivitymarketplace.symb-iot.com/sgp32-tracker) |
| Verizon(米) | **部分的に前向き**。Aeris IoTA Inbound Services が ThingSpace と統合し SGP.32 を活用(2026-02-25)。ただし第三者 eIM への一般的なプロファイル開放を示す発表は未確認 | [IoT Now](https://www.iot-now.com/2026/02/25/155467-aeris-and-verizon-business-simplify-global-iot-expansion-with-unified-connectivity-and-orchestration/) |
| Rogers(加) | SGP.32 に関する公開情報**なし(確認不能)**。tracker では Bell がロードマップ組 | [tracker](https://iotconnectivitymarketplace.symb-iot.com/sgp32-tracker) |
| Telefónica(西) | Kite プラットフォームが SGP.32 下の「コネクティビティ・オーケストレーター」機能を提供と明記。IDEMIA と量子耐性 SGP.32 eSIM をスマートメーターで商用網検証 | [Telefónica Tech Kite](https://telefonicatech.com/en/solutions/iot-connectivity/connectivity-services/kite-platform)、[Telefónica España](https://www.telefonica.es/es/innovacion/quantum-safe-esim/) |
| Vodafone(英) | 標準策定コアグループ。2025 年夏に GSMA 認証・年内商用予定と発言していたが、**実ローンチの確認可能な発表なし(確認不能)** | [Vodafone IoT](https://iot.vodafone.com/news-and-insights/what-you-need-to-know-about-the-new-esim-sgp-32-standard) |
| Telenor(諾) | 商用化第一陣(1.2 節) | 同上 |
| Tele2(瑞) | IDEMIA・Cisco と商用 E2E、IFPP アーリーアクセスも主導 — **「MNO 自らオーケストレーション側に回る」急先鋒** | [Tele2 PR](https://www.tele2.com/media/news/2026/tele2-iot-acceleronix-and-idemia-secure-transactions-launch-the-first-in-the-world-quantum-safe-in-factory-profile-provisioning-early-access-program-at-mwc26-barcelona/) |
| DT(独) | tracker で「実装中」18 社の一角。単独の商用発表は未確認 | [tracker](https://iotconnectivitymarketplace.symb-iot.com/sgp32-tracker) |
| KDDI(日) | 共同開発により **2026 年度下期から商用提供**(国内 MNO 初) | [KDDI](https://biz.kddi.com/topics/2026/news/016/) |
| ドコモ(日) | SGP.32 対応の公開発表**なし(確認不能)** | — |
| ソフトバンク(日) | SGP.32 対応の公開発表**なし(確認不能)** | — |
| IIJ(日・MVNO) | 2025-02-12 に SGP.32 実証実験を公表(商用化時期は未発表) | [IIJ PR](https://www.iij.ad.jp/news/pressrelease/2025/0212.html) |

- 総括: 「MNO はプロファイル開放を渋る」という 2024〜25 年の構図は、**北米(AT&T・Verizon)と北欧(Telenor・Tele2)で崩れ始めた**。一方で「MNO が開放する = 第三者 eIM から自由に使える」ではなく、多くは自社/提携プラットフォーム経由の管理された開放である点に注意。

### 2.2 IoT MVNO / オーケストレーターの SGP.32 対応と打ち出し

| 社 | 発表 | 打ち出し | 出典 |
|---|---|---|---|
| emnify | 2026-03-01 商用開始 | 「The last SIM」。自社 eIM、サードパーティオペレータープロファイル対応、550+ 網 | [emnify blog](https://www.emnify.com/blog/emnify-introduces-sgp.32-esim)、[IoT Business News (2026-03-02)](https://iotbusinessnews.com/2026/03/02/emnify-launches-programmable-sgp-32-esim-connectivity/) |
| floLIVE | 2026-02-19 フル対応 | Kigen 提携。SAS 認証 eIM、エアギャップ環境向け間接プロファイル配信、IFPP 工場書込 | [IoT Now](https://www.iot-now.com/2026/02/19/155400-flolive-launches-full-support-for-sgp-32-esim-standard/) |
| Eseye | 2026-04-22 AnyNet+ に統合 | **マルチ RSP(SGP.02/.22/.32)単一管理**。Thales/IDEMIA/Kigen 対応のベンダー中立。800+ 網 | [Eseye PR](https://www.eseye.com/eseye-strengthens-global-iot-resilience-with-sgp-32-esim-orchestration/) |
| Wireless Logic | 時期不詳(製品ページ) | eSO(eSIM Orchestrator)= eIM の上のポリシー・在庫・自動化層。Thales から IoT エアタイム供給契約も獲得(2025-03-17) | [eSO 解説](https://wirelesslogic.com/iot-glossary/what-is-eso)、[RCR Wireless](https://www.rcrwireless.com/20250317/internet-of-things/thales-wireless-logic-iot) |
| KORE | 2026-04-11 発表 | Kigen と共同ポートフォリオ、商用は 2026 年後半 | [IoT Business News](https://iotbusinessnews.com/2026/04/11/kore-teams-with-kigen-on-sgp-32-esim-to-simplify-global-iot-provisioning/)、[PR Newswire](https://www.prnewswire.com/news-releases/kore-and-kigen-to-deliver-next-generation-sgp32-iot-connectivity-for-global-deployments-302737665.html) |
| Onomondo | 2026-07 上旬発表 | Kigen 認証 eSIM に Onomondo プロファイルを工場プリロード、欧米で顧客展開中 | [New Electronics](https://www.newelectronics.co.uk/content/product-launches/onomondo-and-kigen-launch-interoperable-sgp32-esim-solution-for-iot-deployments) |
| 1oT | eIM を 2024-08 に GSMA 認証(**最初期**) | エストニアの独立系。早期認証を武器に先行 | [tracker](https://iotconnectivitymarketplace.symb-iot.com/sgp32-tracker) |
| Monogoto | 評価キット提供中 | SGP.32-Ready Kit で開発者接点を確保 | [Monogoto](https://monogoto.io/labs/sgp-32-ready-kit/) |
| 1NCE | 個別発表は**未確認** | tracker では「production ready」9 社の一角と分類 | [tracker](https://iotconnectivitymarketplace.symb-iot.com/sgp32-tracker)、[1NCE blog](https://www.1nce.com/en-eu/resources/news/blog/sgp-31-32) |
| Webbing | 対応表明(解説発信中心) | SGP.22 ベース独自 RSP からの移行組 | [Webbing](https://webbingsolutions.com/gsma/) |
| BICS | Valid と提携し SGP.32-ready 接続 | Proximus Global 傘下。SIM ベンダーとの垂直連携 | [Valid PR](https://trustedconnectivity.valid.com/prs/proximus-global-and-valid/) |
| Aeris | Verizon ThingSpace と統合(2026-02-25) | 「キャリアの裏方」ポジションで SGP.32 活用 | [IoT Now](https://www.iot-now.com/2026/02/25/155467-aeris-and-verizon-business-simplify-global-iot-expansion-with-unified-connectivity-and-orchestration/) |

### 2.3 RSP / SIM ベンダー動向(認証・供給網)

- **eUICC 認証の時系列**: G+D(2025-04、**業界初**の GSMA eSIM コンプライアンス+eSA 認証)→ IDEMIA DAKOTA(2025-04)→ STMicroelectronics ST4SIM-300(2025-05)→ Thales(2025-10)→ Kigen(2026-02)。[G+D PR](https://www.gi-de.com/en/group/press/press-releases/giesecke-devrient-becomes-first-company-to-achieve-gsma-esim-compliance-and-certification-for-iot-euicc-product)、[tracker](https://iotconnectivitymarketplace.symb-iot.com/sgp32-tracker)
- **Thales**: eSA 認証(2025-07 発表)+TAC(Thales Adaptive Connect)で eUICC/eIM 両建て。GSMA eSA 認証全体の 53% 超を保有と主張。Wireless Logic へのエアタイム委託、Verifone 獲得と「SIM ベンダーの接続事業接近」が顕著。[Thales blog (2025-07-14)](https://dis-blog.thalesgroup.com/iot/2025/07/14/thales-achieves-gsma-esa-certification-for-sgp-32-specification-revolutionising-iot-connectivity/)
- **IDEMIA**: フル認証ソリューション(2025-08-18)、商用 15 件・PoC 40 件、量子耐性 eSIM(Telefónica)、IFPP(Tele2/Acceleronix)と最も広い布陣。[IDEMIA](https://www.idemia.com/news/idemia-launches-industrys-first-fully-gsma-certified-sgp32-esim-solution-2025-08-18)
- **Kigen**(SoftBank 系): eIM 認証 2025-01(2024-10-03 にコンシューマー eSIM 互換 eIM を発表)、eUICC 認証 2026-02。KORE・floLIVE・Onomondo と提携を量産し「中立インフラ」ポジションを確立中。iSIM の主導者でもある。[Kigen eIM PR](https://iotbusinessnews.com/2024/10/03/52025-kigen-unveils-groundbreaking-eim-solution-for-sgp-32-compatible-with-consumer-esims/)
- **VALID**: SAS-SM 認証 RSP プラットフォームで SGP.02/.22/.32 対応を明記。BICS と SGP.32-ready 接続で提携(日付未確認)。SGP.32 固有の GSMA 認証取得は**確認不能**。[Valid](https://trustedconnectivity.valid.com/solutions/remote-sim-provisioning/)、[Valid×BICS](https://trustedconnectivity.valid.com/prs/proximus-global-and-valid/)
- **中国系**: Eastcompeace(eIM 認証 2025-05)、Redtea Mobile(2025-03)が認証取得済み。欧米系(IDEMIA/Thales/G+D/Kigen)との二極構造。調達の地政学リスク管理(複数ソース化)は前提条件になる。[tracker](https://iotconnectivitymarketplace.symb-iot.com/sgp32-tracker)
- **供給網の定量**: TCA 加盟社の 2025 年 eSIM 出荷 5.23 億個(業界全体 6.05 億個)。工場所在地レベルの公開情報は今回の調査では特定できず(**確認不能**。target-analyst による個社調査が必要)。[TCA](https://trustedconnectivityalliance.org/trusted-connectivity-alliance-members-confirm-acceleration-of-global-esim-growth-in-2025/)
- **業界構造の評価**(アナリスト): 「プラットフォーム能力 = 買収対象、プラットフォームなし = 堀なし」。SIM 物流マージン(在庫・配送・差替)が消失し、サブ MVNO・リセラーが構造的敗者。SM-DP+ 能力を持つ統合者(Cisco/Jasper、Thales/Gemalto、NTT/Transatel 等)と独自プラットフォーム MVNO が勝者という整理。[euicc.co.uk (2026-03-24)](https://euicc.co.uk/what-comes-after-sgp-32-the-esim-transition-the-industry-reckoning-and-what-happens-next/)

## 3. ブリーフィング主張の裏取り結果(C 表 T2 担当分)

| # | 主張 | 判定 | 根拠 |
|---|---|---|---|
| 1 | SGP.32 v1.3 リリース | **支持(日付に注記)** | GSMA が v1.3 を公開済み。リリース日は 2026-05-28(GSMA リソースページ由来、一次ページは 403 で直接閲覧不可)。「2025 末リリース」と読める場合は要修正 — 2026-05 が正。なお商用認証の現行基準は v1.2 のままで、v1.3 の変更点詳細は**確認不能**。[GSMA](https://www.gsma.com/solutions-and-impact/technologies/esim/gsma_resources/sgp-32-v1-3/)、[sgp32.co.uk](https://sgp32.co.uk/sgp32-v12-current-specification/) |
| 2 | Telenor 2026-03 商用化 | **概ね支持(正確には 2026-02-27 発表)** | 商用可用性の発表は 2026-02-27。発注受付は即時開始。[Telenor IoT PR](https://iot.telenor.com/press-release/telenor-iot-announces-commercial-availability-of-sgp-32-sim-cards-enabling-the-next-generation-of-global-iot-deployments/) |
| 3 | Telenor 2026-04 大規模出荷 | **部分支持** | SIM 出荷開始は 2026-04-17 で日付は支持。ただし「大規模」を裏付ける数量の公開はなく、規模は**確認不能**(同社は「大規模展開向け」と位置づけ)。[Telenor IoT PR](https://iot.telenor.com/press-release/telenor-iot-announces-commercial-availability-of-sgp-32-sim-cards-enabling-the-next-generation-of-global-iot-deployments/) |
| 4 | 北米 MNO(AT&T・Verizon・Rogers)のプロファイル供与転換 | **部分支持** | AT&T: 支持(Rivian R2 へ供与、tracker で production ready)。Verizon: 部分支持(Aeris 経由で SGP.32 活用。一般開放の発表は未確認)。Rogers: **確認不能**(公開情報なし)。[G+D](https://www.gi-de.com/en/about-us/press/press-releases/giesecke-devrient-rivian-and-att-collaborate-to-bring-sgp32-and-5g-connectivity-to-rivians-r2-vehicle)、[IoT Now](https://www.iot-now.com/2026/02/25/155467-aeris-and-verizon-business-simplify-global-iot-expansion-with-unified-connectivity-and-orchestration/) |
| 5 | SGP.42 の MWC 2026 発表 | **支持(性質に注記)** | MWC26 Barcelona で Tele2×Acceleronix×IDEMIA が量子耐性 IFPP アーリーアクセスプログラムを発表(2026-02-27、SGP.42 互換を明記)。ただし **SGP.42 仕様自体は未確定**(2026 Q3 確定見込み)で、発表は「プレ標準の商用プログラム」。MWC 上海(2026-06)でも pre-SGP.42 デモ。[Tele2](https://www.tele2.com/media/news/2026/tele2-iot-acceleronix-and-idemia-secure-transactions-launch-the-first-in-the-world-quantum-safe-in-factory-profile-provisioning-early-access-program-at-mwc26-barcelona/)、[IDEMIA](https://www.idemia.com/news/ist-and-acceleronix-unveil-industrys-first-ifpp-mwc26-tele2-iot-2026-02-27) |
| 6 | (G5 補足)「日本キャリアは PoC 止まり」 | **一部矛盾(更新要)** | KDDI は共同開発を経て 2026 年度下期から商用提供へ(国内 MNO 初)。ドコモ・ソフトバンクは公表なしで「PoC 止まり」すら公開情報では確認できず。IIJ(MVNO)は PoC 公表(2025-02-12)。ブリーフィングの記述は 2026-07-03 の発表で更新が必要。[KDDI](https://biz.kddi.com/topics/2026/news/016/)、[IIJ](https://www.iij.ad.jp/news/pressrelease/2025/0212.html) |

## 4. SORACOM への戦略的含意

1. **「SGP.32 対応」自体は 2026 年内に無差別化する。** Telenor・Tele2・emnify・floLIVE・Eseye・KORE が半年以内に商用化を並べた。国内初(2026-07-07 提供開始、公開発表済み)の先行者利益は国内で 6〜12 か月程度と見るべきで、勝負は (a) MNO プロファイルポートフォリオの厚み、(b) マルチ RSP・マルチベンダーを跨ぐオーケストレーション(Connectivity Hypervisor の領域)、(c) 既存 CMP・課金との統合体験に移る。
2. **eIM は「持っていて当然」、収益化は上のレイヤーで。** 認証 eIM 6 社超+無償 OpenEIM の出現で、eIM 単体の外販価値は急速に希薄化。Wireless Logic eSO・Eseye マルチ RSP と同じ土俵で「ポリシー・在庫・自動化・フォールバック」の運用価値を訴求する必要がある。
3. **北米プロファイルの調達は時間との勝負。** AT&T は G+D/Rivian、Verizon は Aeris と既に組んだ。北米 MNO のインテグ枠(車載・大型案件の初期 MNO ポジション)は限られ、遅れるほど条件が悪くなる。Rogers・T-Mobile US・Bell は公開動向がなく、直接対話でしか温度が測れない。
4. **SGP.42/IFPP は 2027 車載・大量出荷 RFP の入場券。** 仕様確定(2026 Q3 見込み)前にアーリーアクセスを押さえた Tele2/IDEMIA/Acceleronix 連合が先行。SIM ベンダー(IDEMIA/Kigen 等)の IFPP 能力と自社プロファイルの工場書込パスを 2026 年内に確保しておくことが、国内文書 J8 の「車載選別受注」の前提になる。
5. **「回線再販」の堀は消える — 自社にも他社にも。** スイッチング自由化は当社の武器(Hypervisor)であると同時に、当社回線もスイッチされうる。解約障壁はプロファイルではなく、デバイス管理・クラウド統合・運用自動化(P2/P3 レイヤー)で作るという全社方針の裏付けがさらに強まった。
6. **相互運用の「実績」が営業資産になる。** 異ベンダ間 Download Interoperability・eIM ポータビリティの実運用事例はまだ公開ゼロ。Comprion 等のテストベッドで先に実績を作り公表すれば、エンタープライズの不安(ロックイン再来への警戒)を取り込める。

## 5. インオーガニック(M&A・出資・提携)の含意

- **P4 スクリーニング基準の改訂提案**: SGP.32 時代の買収評価では「回線収入の継続性」の割引率を上げ、**プラットフォーム IP(SM-DP+/eIM/eSO・ポリシーエンジン)と MNO プロファイル契約の保有**を必須チェック項目に追加すべき(euicc.co.uk の「プラットフォームなし = 堀なし」整理と整合)。→ strategy-planner / deal-desk へ評価基準更新を提案。
- **新規候補(deal-desk への提案、pipeline 重複なし・登録は deal-desk 判断)**:

| 会社 | 地域 | 分野 | 注目理由 | ピラー | 推奨アクション |
|---|---|---|---|---|---|
| 1oT | エストニア | IoT MVNO/eIM | eIM を 2024-08 に業界最初期で GSMA 認証。小規模独立系で機動的、欧州顧客基盤 | P1/P4 | 00_sourcing 登録・初期スクリーニング |
| Acceleronix | 米/中(Quectel 系列との関係は要確認) | IFPP オーケストレーション・工場ツール | SGP.42 前夜の IFPP 商用プログラムを IDEMIA・Tele2 と主導。製造組込レイヤーの要衝 | P1/P2 | まず提携可能性の整理(出自・資本関係の確認を先行) |
| コモン・クリエーション(LibeSIM) | 日本 | SGP.32 準拠 eIM | 国内で希少な eIM 実装者。2026-04-20 から eIM PoC パートナーシッププログラム提供。小型で acqui-hire レンジの可能性 | P1/P5 | 技術評価(Build/Buy/Partner 比較)。国内 SGP.32 エコシステム形成の観点でも接点構築 |
| Eseye | 英国 | マルチ RSP オーケストレーション | SGP.02/.22/.32 統合管理+ベンダー中立(Thales/IDEMIA/Kigen 対応)は当社構想と技術的に補完。PE 保有・再編文脈で資本イベント可能性 | P1/P4 | モニタリング登録(触媒イベント即応) |

- **既存提案の更新(2026-07-06 スキャンのロングリストに対して)**:
  - **Kigen(提携先として重要度上昇)**: KORE・floLIVE・Onomondo と提携を量産中で「中立インフラ」化が加速。競合に囲い込まれる前に提携の深さ(IFPP・iSIM を含む)を再定義すべき。買収は SoftBank 系のため引き続き非現実的(type: partnership 維持)。
  - **Onomondo / floLIVE / emnify**: 3 社とも SGP.32 商用化を完了し資産価値が上がった(= 取得コストも上昇)。floLIVE は SAS 認証 eIM と IFPP 統合まで保有し、P1 適合度が従来評価より高い。
- **供給網の観点(P1 の周辺)**: Thales×Wireless Logic、Valid×BICS と「SIM ベンダー×MVNO」の相互接近が進む。当社の SIM 調達先が競合の接続事業と結びつくリスクを、ベンダー戦略(複数ソース維持)とセットで deal-desk の与件に含めること。

## 6. 未解決の問い

1. SGP.32 v1.3 の技術的変更点(GSMA 一次文書へ直接アクセスできず。GSMA メンバーアクセスでの原文確認を推奨)
2. Vodafone IoT の SGP.32 商用ローンチの実際の時期と形態(2025 年内予定と発言後、公表確認できず)
3. Rogers・Bell・T-Mobile US のプロファイル供与方針(公開情報ゼロ。直接対話・業界会合での確認事項)
4. ドコモ・ソフトバンクの SGP.32 対応計画(公開情報なし。国内競争環境の最大の不確定要素)
5. eIM ポータビリティ・異ベンダ間 Download Interoperability の実運用事例(公開事例ゼロ。GSMA 認証の実効性がエンタープライズ調達の焦点になる)
6. 1NCE の SGP.32 商用状況(tracker 上 production ready だが個別発表未確認)と、Acceleronix の資本関係(Quectel との関係の確認)

## 情報源

**標準化・GSMA**
- [SGP.32 v1.3 — GSMA](https://www.gsma.com/solutions-and-impact/technologies/esim/gsma_resources/sgp-32-v1-3/)(リソースページ、2026-05-28)／[eSIM Consumer and IoT Specifications — GSMA](https://www.gsma.com/solutions-and-impact/technologies/esim/esim-specification/)／[SGP.32 v1.1 PDF](https://www.gsma.com/solutions-and-impact/technologies/esim/wp-content/uploads/2024/04/SGP.32-v1.1.0.pdf)／[SGP.32 v1.2 PDF](https://www.gsma.com/solutions-and-impact/technologies/esim/wp-content/uploads/2024/06/SGP.32-v1.2.pdf)／[SGP.41 v1.0](https://www.gsma.com/solutions-and-impact/technologies/esim/gsma_resources/esim-ifpp-architecture-and-requirements/)
- [What is SGP.32 v1.2? — sgp32.co.uk](https://sgp32.co.uk/sgp32-v12-current-specification/)(2026-05-11)／[SGP.32 FAQ — sgp32.co.uk](https://sgp32.co.uk/sgp32-faq/)／[What Is SGP.32? — euicc.co.uk](https://euicc.co.uk/what-is-sgp-32/)(2026-02)
- [What is SGP.42? — Kigen](https://kigen.com/glossary/sgp42-remote-sim-provisioning/)／[GSMA PQC Roundtable MWC Shanghai — GSMA](https://www.gsma.com/solutions-and-impact/technologies/security/post-quantum/quantum-safe-or-quantum-vulnerable-inside-gsmas-second-pqc-roundtable-at-mwc-shanghai/)(2026-06)
- [SGP.32 tracker — symb-iot IoT Connectivity Marketplace](https://iotconnectivitymarketplace.symb-iot.com/sgp32-tracker)(2026-04-26 更新)

**商用化・MNO**
- [Telenor IoT 商用可用性発表](https://iot.telenor.com/press-release/telenor-iot-announces-commercial-availability-of-sgp-32-sim-cards-enabling-the-next-generation-of-global-iot-deployments/)(2026-02-27)／[The Fast Mode 報道](https://www.thefastmode.com/technology-solutions/47390-telenor-iot-launches-sgp-32-esims-for-global-iot-deployments)
- [MWC 2026 総括 — IoT Business News](https://iotbusinessnews.com/2026/05/27/mwc-2026-signals-a-split-iot-connectivity-market-shaped-by-ai-ntn-and-esim-orchestration/)(2026-05-27)
- [G+D×Rivian×AT&T — G+D](https://www.gi-de.com/en/about-us/press/press-releases/giesecke-devrient-rivian-and-att-collaborate-to-bring-sgp32-and-5g-connectivity-to-rivians-r2-vehicle)／[Automotive World](https://www.automotiveworld.com/news/rivian-partners-with-gd-att-on-r2-connectivity/)(2026-03)
- [Aeris×Verizon — IoT Now](https://www.iot-now.com/2026/02/25/155467-aeris-and-verizon-business-simplify-global-iot-expansion-with-unified-connectivity-and-orchestration/)(2026-02-25)
- [Telefónica Tech Kite](https://telefonicatech.com/en/solutions/iot-connectivity/connectivity-services/kite-platform)／[Telefónica Quantum-Safe eSIM](https://www.telefonica.es/es/innovacion/quantum-safe-esim/)／[Vodafone IoT SGP.32 解説](https://iot.vodafone.com/news-and-insights/what-you-need-to-know-about-the-new-esim-sgp-32-standard)(2025-08 頃)
- [KDDI 発表](https://biz.kddi.com/topics/2026/news/016/)(2026-07)／[ITmedia Mobile](https://www.itmedia.co.jp/mobile/articles/2607/03/news059.html)(2026-07-03)／[Business Wire](https://www.businesswire.com/news/home/20260708308506/en/Soracom-Announces-Commercial-Release-of-SGP.32-Compatible-IoT-eSIMs)(2026-07-08)／[IIJ 実証実験](https://www.iij.ad.jp/news/pressrelease/2025/0212.html)(2025-02-12)

**MVNO/オーケストレーター**
- [emnify SGP.32 発表](https://www.emnify.com/blog/emnify-introduces-sgp.32-esim)(2026-03-01)／[IoT Business News](https://iotbusinessnews.com/2026/03/02/emnify-launches-programmable-sgp-32-esim-connectivity/)／[emnify factory-first CES 2026](https://iotbusinessnews.com/2025/12/22/emnify-debuts-factory-first-iot-connectivity-at-ces-2026/)(2025-12-22)
- [floLIVE フル対応 — IoT Now](https://www.iot-now.com/2026/02/19/155400-flolive-launches-full-support-for-sgp-32-esim-standard/)(2026-02-19)
- [Eseye AnyNet+ SGP.32 — Eseye](https://www.eseye.com/eseye-strengthens-global-iot-resilience-with-sgp-32-esim-orchestration/)(2026-04-22)／[Computer Weekly](https://www.computerweekly.com/news/366642413/Eseye-boosts-global-IoT-resilience-with-SGP32-eSIM-orchestration)
- [Wireless Logic eSO](https://wirelesslogic.com/iot-glossary/what-is-eso)／[Thales×Wireless Logic — RCR Wireless](https://www.rcrwireless.com/20250317/internet-of-things/thales-wireless-logic-iot)(2025-03-17)
- [KORE×Kigen — IoT Business News](https://iotbusinessnews.com/2026/04/11/kore-teams-with-kigen-on-sgp-32-esim-to-simplify-global-iot-provisioning/)(2026-04-11)／[PR Newswire](https://www.prnewswire.com/news-releases/kore-and-kigen-to-deliver-next-generation-sgp32-iot-connectivity-for-global-deployments-302737665.html)
- [Onomondo×Kigen — New Electronics](https://www.newelectronics.co.uk/content/product-launches/onomondo-and-kigen-launch-interoperable-sgp32-esim-solution-for-iot-deployments)(2026-07 上旬)
- [Monogoto SGP.32-Ready Kit](https://monogoto.io/labs/sgp-32-ready-kit/)／[1NCE SGP.31/.32 解説](https://www.1nce.com/en-eu/resources/news/blog/sgp-31-32)／[Webbing GSMA 解説](https://webbingsolutions.com/gsma/)／[TEAL OpenEIM](https://tealcom.io/post/teal-launches-openeim-sgp-32-esim-platform-a-free-and-open-approach-to-esim-management/)

**RSP/SIM ベンダー・IFPP**
- [G+D 業界初認証 — G+D](https://www.gi-de.com/en/group/press/press-releases/giesecke-devrient-becomes-first-company-to-achieve-gsma-esim-compliance-and-certification-for-iot-euicc-product)(2025-04)／[IoT Business News](https://iotbusinessnews.com/2025/04/29/61467-gd-becomes-first-company-to-achieve-gsma-esim-compliance-and-certification-for-iot-euicc-product/)(2025-04-29)
- [IDEMIA フル認証](https://www.idemia.com/news/idemia-launches-industrys-first-fully-gsma-certified-sgp32-esim-solution-2025-08-18)(2025-08-18)／[IDEMIA×Acceleronix×Tele2 IFPP](https://www.idemia.com/news/ist-and-acceleronix-unveil-industrys-first-ifpp-mwc26-tele2-iot-2026-02-27)(2026-02-27)／[Tele2 PR](https://www.tele2.com/media/news/2026/tele2-iot-acceleronix-and-idemia-secure-transactions-launch-the-first-in-the-world-quantum-safe-in-factory-profile-provisioning-early-access-program-at-mwc26-barcelona/)
- [Thales eSA 認証 — Thales blog](https://dis-blog.thalesgroup.com/iot/2025/07/14/thales-achieves-gsma-esa-certification-for-sgp-32-specification-revolutionising-iot-connectivity/)(2025-07-14)／[Verifone×Thales — IoT Business News](https://iotbusinessnews.com/2026/03/11/verifone-taps-thales-esim-and-sgp-32-to-simplify-global-connectivity-for-pos-terminals/)(2026-03-11)
- [Kigen eIM 発表 — IoT Business News](https://iotbusinessnews.com/2024/10/03/52025-kigen-unveils-groundbreaking-eim-solution-for-sgp-32-compatible-with-consumer-esims/)(2024-10-03)
- [Valid RSP](https://trustedconnectivity.valid.com/solutions/remote-sim-provisioning/)／[Valid×BICS](https://trustedconnectivity.valid.com/prs/proximus-global-and-valid/)(日付未確認)
- [Comprion×G+D — IoT Business News](https://iotbusinessnews.com/2026/03/05/comprion-and-gieseckedevrient-partner-for-interoperable-sgp-32-iot-esim-solutions/)(2026-03-05)／[Comprion×Thales](https://www.comprion.com/company/press/press-release-detail/comprion-partners-with-thales-to-provide-iot-service-providers-with-advanced-sgp32-esim-testing-solution/)
- [コモン・クリエーション LibeSIM eIM PoC プログラム — PR TIMES](https://prtimes.jp/main/html/rd/p/000000022.000084723.html)(2026-04-20)

**市場予測・構造分析**
- [Kaleido 予測 — RCR Wireless](https://www.rcrwireless.com/20250922/internet-of-things/sgp-32-esim-transform-iot)(2025-09-22)／[IoT Tech News](https://iottechnews.com/news/kaleido-intelligence-forecasts-esim-adoption-surge-iot/)
- [TCA 2025 出荷統計](https://trustedconnectivityalliance.org/trusted-connectivity-alliance-members-confirm-acceleration-of-global-esim-growth-in-2025/)(2026-03)／[IoT Business News](https://iotbusinessnews.com/2026/03/04/tca-members-confirm-acceleration-of-global-esim-growth-in-2025/)(2026-03-04)
- [What Comes After SGP.32? — euicc.co.uk](https://euicc.co.uk/what-comes-after-sgp-32-the-esim-transition-the-industry-reckoning-and-what-happens-next/)(2026-03-24)
- [IFPP ポジションペーパー — Transforma Insights](https://transformainsights.com/research/reports/in-factory-profile-provisioning-ifpp-position-paper)／[IFPP 解説 — Eseye](https://www.eseye.com/resources/iot-explained/what-is-in-factory-profile-provisioning-ifpp/)

> 注: 本レポートは公開情報のみに基づく参考情報であり投資判断ではない。「未確認」「確認不能」「推定」と付した項目は一次情報での裏取りができていない。外部向け文書化の際は必ず人間レビューを要する。
