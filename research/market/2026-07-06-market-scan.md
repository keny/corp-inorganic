# 市場スキャンレポート — 2026-07-06

> 作成: market-scout ／ 作成日: 2026-07-06 ／ 対象期間: 2025-07 〜 2026-06(直近12か月中心、一部それ以前の構造的イベントを含む)／ テーマ: 全般(初回スキャン)

## TL;DR(3〜5行)

- **独立系 IoT MVNO の「買える玉」が急減している。** KORE 非公開化(約$726M)、Telenor Connexion の切り出し(SEK 7.5B ≒ $809M)、Wireless Logic の連続買収(直近12か月で4件)と PE 主導の再編が加速。P4(地理・顧客基盤)は先送りするほど高く・少なくなる。
- **P2(デバイス・エッジ)の魅力資産は半導体・HW 大手が先行取得中。** Qualcomm×Arduino/Edge Impulse、Nordic×Memfault、Digi×Particle($50M ≒ ARR 2.5x)。P2 で動くなら早期。相場観として「サブスク型 IoT インフラ ≒ EV/ARR 2.5x 前後」の実例が得られた。
- **ハイパースケーラーは IoT アプリレイヤーから後退**(AWS が IoT Analytics/Events 等4サービス終了、Azure IoT Central は 2027-03 終了)。P3(データ・アプリ)の空白地帯が拡大しているが、今回スキャンでは P3 候補の発掘が薄く、次回の重点テーマとする。
- **技術面の資産価値の焦点は SGP.32 と衛星 NTN。** SGP.32 は 2026 年に商用化本格入り(Kaleido 予測: 2028 年に1.9億 eSIM)、NTN は SpaceX×EchoStar($17B)で資本戦に突入。P1 の eSIM オーケストレーション/マルチパス統合管理の価値が上がる一方、純粋な回線再販型 MVNO の資産価値は下がる方向。
- **EU CRA の報告義務が 2026-09-11 開始。** IoT セキュリティ/デバイスオブザーバビリティ資産の需要が構造的に増加。Memfault 消滅後の同種独立資産(Golioth 等)は希少化しており、P2 ロングリストに反映済み。

## 1. M&A・資金調達動向

| 日付 | 買い手/投資家 | 対象 | 金額 | 分野 | SORACOM への示唆 |
|---|---|---|---|---|---|
| 2026-05-12 | Verdane(50/50 JV 化) | Telenor Connexion | 評価額 SEK 7.5B(≒$809M)。クロージング後に両者が各 SEK 2B 追加投資 | キャリア IoT 部門 | キャリア IoT 部門が「取引可能な資産」になった。P4 の大型機会だが当社ガードレール超級 → 提携・共同投資の形も比較検討 |
| 2026-02 | Searchlight Capital + Abry Partners | KORE Wireless(上場廃止へ) | $9.25/株、約$726M。FY2025 売上 $285.9M・調整後 EBITDA $63.3M → 概算 EV/売上 ~2.5x、EV/EBITDA ~11.5x | IoT 接続+ソリューション | 上場 IoT MVNO の非公開化。バリュエーションの基準点。クロージング(2026 Q2-Q3)後の非中核資産切り出しをウォッチ |
| 2026-02 | Wireless Logic | Comms365(UK) | 非公開 | IoT/M2M 接続・セキュリティ | 欧州ロールアップ継続。P4 案件では常に競合買い手として想定すべき |
| 2026-01-27 | Digi International | Particle | $50M 現金(ARR 約$20M、二桁成長 → EV/ARR ~2.5x) | エッジ〜クラウド IoT プラットフォーム | P2 の相場観。開発者コミュニティ 25 万人が $50M で取れた事例。デバイスプラットフォームは HW ベンダーに回収されつつある |
| 2026-01-26 | Netmore Group | Actility + Abeeway | 非公開 | LoRaWAN/LPWA | 契約デバイス 1,400 万台の世界最大 LoRaWAN 事業者が誕生。P1 の LPWA は「統合済み市場」となり新規買収妙味は低下、提携対象として扱う |
| 2025-12〜(進行中) | 買い手未定 | Semtech セルラーモジュール事業(旧 Sierra Wireless) | 未定(2026-03 の投資家会議で切り出し方針を説明) | セルラーモジュール | モジュール業界の再々編。当社は対象外領域(HW 量産)だが、顧客接点・接続事業の帰趨は注視 |
| 2025-10-07 | Qualcomm | Arduino | 非公開 | エッジ AI・開発者エコシステム | Edge Impulse(2025-03)、Foundries.io(2024-03)に続く3件目。チップ大手が P2/P5 相当の希少資産を先行確保している |
| 2025-09-08 | SpaceX | EchoStar の AWS-4/H-block 周波数 | $17B(現金 $8.5B+株式 $8.5B)、FCC 承認済み | 衛星 D2C/NTN | NTN は資本集約戦へ。衛星レイヤーの保有は当社レンジ外が確定的 → P1 は「統合管理レイヤー+提携/出資」に絞るべき |
| 2025-08 | Wireless Logic | Zipit Wireless(US) | 非公開 | IoT 接続+課金 | Wireless Logic 初の米国 HQ 企業買収。北米でも P4 競合に |
| 2025-06-06 完了 | Trasna(IE) | u-blox セルラー IoT モジュール事業 | 非公開(2025-03-17 発表) | モジュール+eSIM | チップ設計〜eSIM 製造〜リモート SIM 管理の垂直統合プレイヤーが欧州に出現。P1 領域の新顔として監視 |
| 2025-06 | Nordic Semiconductor | Memfault | 非公開 | デバイスオブザーバビリティ/OTA | P2 の最有力独立資産が消滅。同種資産の希少性が上昇(→ ロングリストの Golioth 等) |
| 2025-04-29 | 既存投資家ほか(DT、SoftBank 等が株主) | 1NCE | $60M(累計約$160M) | IoT 接続 SaaS | 最大手は資金厚く SaaS/AI へ拡張中。接続単価下落をソフトで補う戦略は当社と同方向 = 正面競合の強化 |
| 2025-04-02 | Wireless Logic | Arqia(ブラジル) | 非公開 | IoT MVNO | LATAM への地理拡大。P4 の獲得競争は新興地域にも波及 |
| 2025-03 | 機関投資家(+EIB 融資 €30M は 2024-12) | Sateliot | €70M Series B。2026-04 に €100M Series C 開始(調達中) | 5G NB-IoT NTN(標準準拠 LEO) | 標準準拠 NTN に機関マネー流入。事前契約 €270M・400 顧客と商用化前夜 → P1 のマイノリティ出資候補 |
| 2025-03 | Wireless Logic | Things Mobile(イタリア) | 非公開 | IoT 接続 | 欧州ロールアップの一環 |
| 2025-02-27 | NGP Capital 主導(Intel Capital、BMW i Ventures、Samsung Catalyst 等参加) | Skylo | $30M(応募超過) | NTN(既存 GEO 衛星活用の D2D) | 商用 NTN の中心プレイヤー。当社は既に統合ソリューション GA 済み(公開情報)→ 出資による関係深化はオプション |
| 2025(月未確認) | Montagu(継続ファンド、CVC 等参加) | Wireless Logic(既存株主の持分継続) | €2B 継続ビークル(2024 年の General Atlantic 少数出資時は £3.5B 評価) | IoT MVNO(統合プラットフォーム) | 欧州最大のロールアップ買い手に成長資金が補充された。P4 案件の入札では価格競争を覚悟 |
| 未確認(報道・観測) | 外部投資家(Microsoft の名前が報道で言及) | Vodafone IoT(最大 50% 売却の観測) | 事業評価 ~£1B(報道) | キャリア IoT 切り出し | **未確認**。2024-04 に分社化済みで「最大50%売却可能」は公式方針。成立すれば P4 の競争環境が激変。四半期ごとに追跡 |

- 「Telenor による Tele2 IoT 買収」への言及が一部業界レポート要約に見られたが、一次情報を確認できず **未確認**(今回の検索では Telenor 側の動きは Connexion/Verdane JV のみ確認)。
- マルチプルの記録: Digi/Particle **EV/ARR ~2.5x**、KORE **EV/売上 ~2.5x・EV/調整後EBITDA ~11.5x(概算)**。サブスク比率・成長率で振れるが、P2/P4 案件の値付けの初期アンカーとして使用可。

## 2. 競合・プレイヤー動向

**グローバル独立系(IoT MVNO/CMP)**
- **KORE**: 非公開化合意(上記)。接続数 2,190 万(2026 Q1、前年比+11%)だが売上は減収($65.8M)。Kigen と SGP.32 対応ポートフォリオを共同発表(2026 年内に商用化予定)。→ 非公開化後は身軽になり価格攻勢・買収再開の可能性。
- **1NCE**: 2025 年にエンドポイント 4,000 万超(+33%)、顧客 3 万社。$60M 調達で SaaS/AI(1NCE Insights)へ拡張。Omdia は 1NCE・Cubic3・KORE の3社で世界の管理接続の 28% と推計。
- **Aeris**: 接続デバイス1億台突破(2026-01、Ericsson IoT Accelerator 買収後で約+90%)。Verizon ThingSpace との相互接続(2026-02)、KDDI と接続管理契約(SDxCentral 報道、日付未確認)。→ キャリアの「裏方 CMP」ポジションを急速に確立。
- **Wireless Logic**: 累計 18 件の買収。直近 12 か月で Things Mobile/Arqia/Zipit/Comms365 の 4 件。→ P4 の最大競合買い手。
- **emnify**: CES 2026 で「factory-first connectivity」(単一 eSIM SKU で製造ラインから接続済み出荷)を発表。→ SGP.32 時代の製造組込型接続へ布石。
- **Onomondo**: 新 CEO に Rasmus Jensen(Templafy 元 CRO)。2024 年売上 +115%、顧客 500 社・62 か国。→ 成長加速フェーズ入り。詳細はロングリスト参照。
- **floLIVE / Hologram**: floLIVE は 2023-09 の $47M Series C 以降、大型調達の公表なし(累計 $88.2M)。Hologram も 2021 年以降の大型調達を確認できず(G2 での製品評価は高水準を維持)。→ 資金市場が厳しい中規模独立系は 2026-27 に資本イベント(調達 or 売却)を迎える可能性。

**通信キャリア**
- **Telenor**: 北欧の IoT 事業を Telenor Connexion に集約(2026-01 完了)した上で Verdane と 50/50 JV 化。**Vodafone**: IoT を 2024-04 に分社化、外部資本受け入れ方針。Skylo と NTN ハイブリッド接続で提携。→ 欧州キャリアは IoT を「本体から切り出して資本を入れる」方向で一致。P4 の出物は増えるが、単体で数百億円級。
- 国内: 今回は英語ソース中心のため薄い。KDDI×Aeris(上記)のほか、SoftBank が 1NCE の株主である点は把握。**次回スキャンで日本語ソースによる国内 MVNO/MVNE・SIer の深掘りを行う。**

**ハイパースケーラー**
- **AWS**: IoT Analytics(2025-12-15 終了)、Fleet Hub(2025-10-18 終了)、IoT Events(2026-05-20 終了)、Panorama(2026-05-31 終了)とマネージド IoT 上位レイヤーを整理。
- **Microsoft**: Azure IoT Central を 2027-03-31 で終了(2024-02 の告知時に一時「誤報」と訂正される混乱の後、確定)。IoT Hub/Edge は継続。
- **Google**: IoT Core は 2023 年に終了済み(構造的前提)。
- → **含意**: ハイパースケーラーは「汎用 IoT アプリケーション」から撤退し、接続〜デバイス管理〜アプリの統合価値は独立プラットフォーマー側に移動している。P3 のホワイトスペースが広がる一方、移行需要(IoT Central 難民等)は短期の顧客獲得機会でもある。

**半導体・モジュール**
- Qualcomm(Arduino/Edge Impulse/Foundries.io)、Nordic(Memfault)、Digi(Particle)、Trasna(u-blox モジュール+Workz 等)、Semtech(モジュール事業切り出し)。→ チップ〜デバイス〜クラウドの垂直統合が進み、P2 の独立資産は先に取られていく構図。

## 3. 技術・規制トレンド

- **eSIM/iSIM(SGP.32)**: 商用化が本格化。MWC 2026 で Tele2 IoT×IDEMIA×Cisco がエンドツーエンド商用ソリューションを発表、Rivian が R2 で車載採用を表明、KORE×Kigen も 2026 年内商用化予定。Kaleido は SGP.32 eSIM が 490 万(現在)→ 2028 年 1.928 億に拡大と予測。→ **M&A 含意**: キャリア切替コストが構造的に低下し、(a) eIM/オーケストレーション資産(Kigen、Trasna 等)の価値上昇、(b) 「回線再販」だけの MVNO の価値下落。P4 買収の値付けは回線収入でなく顧客関係・ソフトウェア資産ベースで行うべき。P1 では eIM ケイパビリティの Build/Buy/Partner 判断を 2026 年内に。
- **衛星 NTN**: SpaceX×EchoStar $17B、最大 15,000 機の D2C コンステレーション申請。Skylo は $30M 調達し Vodafone IoT とハイブリッド接続提携。Sateliot は €70M B + €100M C(調達中)、事前契約 €270M。→ **M&A 含意**: 衛星レイヤー自体は資本集約的で対象外。価値が集まるのは「セルラー+衛星の統合管理」= 当社の既存ポジションの延長。Skylo(提携済み)に加え、標準準拠 NTN(Sateliot 等)へのマイノリティ出資は P1 の低リスクなオプション買い。
- **5G RedCap**: 2026-04 時点で 42 オペレーター・27 か国が投資、日本含む 6 か国で商用サービス稼働。モジュール価格は $30-50 → 2026 年末 $15-25 へ低下見込み。eRedCap チップは 2026 年投入、量産は 2027-28。→ **M&A 含意**: 短期は限定的。Cat-1/LTE-M 置き換えの本番は 2027 年以降であり、モニタ継続で足りる。
- **プライベート 5G / エッジ AI**: 今回は重点調査未実施(次回課題)。エッジ AI はチップ大手による開発者エコシステム争奪(Qualcomm 3 連続買収)が最重要シグナル。
- **IoT セキュリティ規制(EU CRA)**: 2024-12-10 発効。**2026-09-11 から報告義務**(悪用された脆弱性・重大インシデントを 24 時間以内に ENISA/国家 CSIRT へ早期警報、72 時間以内に詳細通知)。全面適用は 2027-12-11。EU で製品を販売する域外メーカーにも適用され、SBOM・脆弱性管理体制が事実上の前提要件に。→ **M&A 含意**: デバイスセキュリティ/オブザーバビリティ/SBOM 資産の需要が規制で底上げされ、P2 資産の価値上昇(Nordic×Memfault はこの文脈の先行例)。※CRA の当社自身のコンプライアンス解釈は IS&CorpIT/Legal に確認のこと(本レポートは市場分析目的)。

## 4. 新規候補(ロングリスト提案)

`pipeline/pipeline.yaml` を確認済み — 現状は架空サンプル(SAMPLE-001〜003)のみで実案件との重複なし。以下 8 社を deal-desk への追加候補として提案する。

| 会社 | 地域 | 分野 | 注目理由 | 該当ピラー | 推奨アクション |
|---|---|---|---|---|---|
| Onomondo | デンマーク | ソフトウェア定義 IoT 接続(独自コア、tinyCore) | 2024 年売上 +115%、顧客 500 社・62 か国。成長請負型の新 CEO 就任 = 数年内の資本イベントが視野に入る局面。技術思想(SW 定義・クラウドネイティブ)が当社と近く、欧州顧客基盤も取れる | P1 / P4 | 00_sourcing 登録、初期スクリーニング(技術・顧客重複の確認) |
| floLIVE | イスラエル/英国 | ローカルブレイクアウト型コアネットワーク、マルチ IMSI eSIM | 規制対応(データ主権)に強いアーキテクチャ。2023-09 以降調達なし(累計 $88.2M)→ 2026-27 に資金需要 or 出口の可能性があり、タイミング妙味 | P1 | 財務状況モニタリング+初期スクリーニング |
| Golioth | 米国 | デバイス管理・IoT Infrastructure as Code | Memfault 消滅後の希少な独立系デバイス管理。小規模(シード累計 ~$7M)で acqui-hire〜小型買収レンジ。Zephyr/Nordic エコシステムに強い | P2 / P5 | 技術評価(当社デバイス管理ロードマップとの Build/Buy 比較) |
| Blues | 米国 | セルラー内蔵デバイス→クラウドのデータポンプ(Notecard/Notehub) | Ray Ozzie 創業、累計約 $100M 調達。「接続込みハードウェア+サブスク」モデルは P2 仮説(接続の上下を押さえる)と合致。規模的に買収は重いが提携起点に妙味 | P2 | まず事業提携の可能性を打診対象として整理(Partner→将来 Buy) |
| Hologram | 米国 | 開発者フレンドリーな IoT 接続(米国中心) | 製品評価は高水準(G2)だが 2021 年以降の大型調達を確認できず。統合圧力下の独立系として、米国の開発者・スタートアップ顧客基盤を取得できる可能性 | P4 | 状況調査(トラクション・資本政策の把握)。優先度は中 |
| Sateliot | スペイン | 標準準拠 5G NB-IoT NTN(LEO) | €100M Series C 調達中、事前契約 €270M・400 顧客。既存 NB-IoT デバイスがそのまま衛星接続できる標準準拠路線は当社マルチキャリアモデルと補完的 | P1 | マイノリティ出資の検討(type: investment)。買収ではなくオプション確保 |
| Kigen | 英国 | eSIM/iSIM・SGP.32 eIM オーケストレーション | SGP.32 エコシステムの中核。KORE と共同ポートフォリオを発表しており、競合に紐づく前に関係構築の価値。買収可能性は低い(SoftBank 系)ため提携/出資で | P1 | 提携深化を先行(SGP.32 対応の time-to-market 短縮)。type: partnership |
| emnify | ドイツ | クラウドネイティブ IoT 接続(欧州) | 欧州の有力独立系。factory-first(製造ライン組込接続)など製品面で先行。KORE 非公開化・Wireless Logic ロールアップが進む中、業界再編対応(テーゼ分類3)の観点で最重要モニタ対象 | P4 / P1 | モニタリング登録(再編の触媒イベント発生時に即応できる準備) |

- **P3(データ・アプリレイヤー)の候補が今回未発掘**。ハイパースケーラー撤退で空白は広がっており、次回スキャンで IoT 分析/可視化・業界特化 SaaS を重点調査する(Build vs Buy の観点で Flux/Harvest との重複整理が前提)。

## 5. パイプラインへの示唆

- 既存パイプラインは実案件ゼロ(サンプル SAMPLE-001〜003 のみ)のため、「前提を変えるニュース」への該当なし。上記 8 社の 00_sourcing 登録を deal-desk に提案する。
- 運用上の示唆:
  1. **P2 は時間との勝負**: Memfault・Edge Impulse・Particle・Arduino と、この 18 か月で P2 相当の独立資産が 4 件消えた。P2 案件はスクリーニングの SLA を短く設定すべき。
  2. **KORE クロージング(2026 Q2-Q3)後をウォッチ**: PE 傘下での事業整理により非中核資産(特定地域・特定業種のソリューション事業)が売りに出る可能性。
  3. **キャリア IoT 切り出し(Telenor/Verdane、Vodafone IoT)**: P4 の大型機会だが当社ガードレール超級の規模。共同投資・提携スキームの検討材料として strategy-planner に引き継ぐ。
  4. **相場観の蓄積開始**: EV/ARR ~2.5x(Digi/Particle)、EV/売上 ~2.5x・EV/EBITDA ~11.5x(KORE)を `pipeline` の評価基準の初期アンカーとして記録。

## 情報源

**M&A・資金調達**
- [KORE Announces Agreement to be Acquired by Searchlight Capital Partners and Abry Partners](https://www.prnewswire.com/news-releases/kore-announces-agreement-to-be-acquired-by-searchlight-capital-partners-and-abry-partners-302699482.html) — PR Newswire, 2026-02 ／ [KORE IR 版](https://ir.korewireless.com/news-events/press-releases/detail/262/kore-announces-agreement-to-be-acquired-by-searchlight) ／ [KORE Wireless Acquired for $726M in Going-Private Deal](https://5gstore.com/blog/2026/02/27/kore-wireless-privately-acquired-726m/) — 5Gstore Blog, 2026-02-27
- [Telenor and Verdane form $809m IoT joint venture](https://iottechnews.com/news/telenor-verdane-809m-iot-joint-venture/) — IoT Tech News, 2026-05 ／ [Verdane partners with Telenor to build a global IoT leader](https://verdane.com/verdane-partners-with-telenor-to-build-a-global-iot-leader/) — Verdane, 2026-05-12
- [Netmore Acquires Actility to Form Largest LoRaWAN Operator](https://www.thefastmode.com/solution-vendors-m-a/46823-netmore-acquires-actility-to-form-largest-lorawan-operator) — The Fast Mode, 2026-01 ／ [Actility 公式発表](https://www.actility.com/netmore-group-acquires-actility/) — Actility, 2026-01-26
- [Digi International Acquires Particle to Accelerate ARR Growth](https://www.businesswire.com/news/home/20260127820853/en/Digi-International-Acquires-Particle-to-Accelerate-ARR-Growth-and-Strengthen-Digis-Embedded-as-a-Service-Offering) — Business Wire, 2026-01-27 ／ [Digi Acquires Particle for $50 Million](https://www.electronicdesign.com/technologies/communications/iot/article/55354275/electronic-design-digi-acquires-particle-for-50-million) — Electronic Design, 2026-01
- [Wireless Logic の買収一覧](https://tracxn.com/d/acquisitions/acquisitions-by-wireless-logic/__t-9_OUepMM2rIhkA7CH6vXFBNDOXlBiVtCE8PvyViXI) — Tracxn(2026-02 時点 18 件)／ [Arqia 買収](https://tech.eu/2025/04/02/wireless-logic-expands-reach-in-latin-america-with-acquisition-of-arqia/) — Tech.eu, 2025-04-02 ／ [Zipit Wireless 買収](https://www.zipitwireless.com/blog/wireless-logic-acquires-zipit-wireless) — Zipit, 2025-08 ／ [Montagu €2B 継続ビークル](https://www.cvc.com/media/news/2025/montagu-raises-2-billion-continuation-vehicle-to-support-wireless-logic-s-next-phase-of-global-growth/) — CVC, 2025 ／ [General Atlantic 少数出資(£3.5B 評価)](https://www.insidermedia.com/news/south-east/general-atlantic-backs-iot-services-provider-in-deal-valuing-firm-at-3.5bn) — Insider Media, 2024
- [Trasna acquires u-blox IoT modules](https://iotbusinessnews.com/2025/03/17/71971-trasna-acquires-u-blox-iot-modules/) — IoT Business News, 2025-03-17 ／ [完了(2025-06-06)](https://www.marketscreener.com/quote/stock/U-BLOX-HOLDING-AG-366917/news/Trasna-Solutions-Technologies-Limited-completed-the-acquisition-of-Cellular-IoT-module-business-of-u-50201941/) — MarketScreener
- [Nordic Semiconductor acquires Memfault](https://www.nordicsemi.com/Nordic-news/2025/06/Nordic-Semiconductor-acquires-Memfault) — Nordic Semiconductor, 2025-06
- [Qualcomm reaches for the far edge of AI with Arduino](https://next-curve.com/2025/10/08/qualcomm-reaches-for-the-far-edge-of-ai-with-arduino/) — neXt Curve, 2025-10-08 ／ [Qualcomm IE-IoT Expansion Is Complete](https://www.qualcomm.com/news/releases/2026/01/qualcomm-s-ie_iot-expansion-is-complete--edge-ai-unleashed-for-d) — Qualcomm, 2026-01 ／ [With Arduino deal, Qualcomm pushes deeper into open-source and edge AI](https://www.infoworld.com/article/4069470/with-arduino-deal-qualcomm-pushes-deeper-into-open-source-and-edge-ai-development.html) — InfoWorld, 2025-10(Edge Impulse 2025-03、Foundries.io 2024-03 の経緯を含む)
- [SpaceX strikes $17B deal to buy EchoStar's spectrum](https://techcrunch.com/2025/09/08/spacex-strikes-17b-deal-to-buy-echostars-spectrum-for-starlinks-direct-to-phone-service/) — TechCrunch, 2025-09-08 ／ [EchoStar 公式発表](https://ir.echostar.com/news-releases/news-release-details/echostar-announces-spectrum-sale-and-commercial-agreement-spacex) ／ [FCC 承認](https://www.telecompetitor.com/fcc-approves-att-and-starlink-purchases-of-echostar-spectrum/) — Telecompetitor
- [Semtech at Morgan Stanley Conference: Strategic Moves(セルラーモジュール事業の切り出し方針)](https://www.investing.com/news/transcripts/semtech-at-morgan-stanley-conference-strategic-moves-and-market-expansion-93CH-4539863) — Investing.com, 2026-03-03
- [1NCE raises $60m](https://www.rcrwireless.com/20250430/internet-of-things-4/1nce-ai-iot-creds) — RCR Wireless, 2025-04-30 ／ [1NCE 公式](https://www.1nce.com/en-us/resources/news/press-releases/1nce-raises-60-million-usd-in-new-funding) — 2025-04-29
- [Skylo Raises $30M in Oversubscribed Funding Round](https://www.businesswire.com/news/home/20250227282650/en/Skylo-Raises-%2430M-in-Oversubscribed-Funding-Round-to-Scale-Direct-to-Device-Satellite-Service-Worldwide) — Business Wire, 2025-02-27
- [Sateliot seeks €100 million](https://www.eu-startups.com/2026/04/spains-sateliot-seeks-e100-million-to-accelerate-deployment-of-its-5g-satellite-network) — EU-Startups, 2026-04(€70M Series B: 2025-03 完了に言及)／ [Sateliot launches €100m series C](https://www.computerweekly.com/news/366641696/Sateliot-launches-100m-series-C-financing-round) — Computer Weekly, 2026 ／ [EIB €30M 融資](https://www.rcrwireless.com/20241204/internet-of-things-4/sateliot-eib-nb-iot) — RCR Wireless, 2024-12-04
- [Vodafone IoT 分社化(独立 MVNO 化)](https://www.abiresearch.com/market-research/insight/7784146-worlds-biggest-iot-service-provider-become) — ABI Research, 2024 ／ [Struggling Vodafone looks to sell stake in £1bn IoT unit(Microsoft 言及・未確認)](https://www.mobileeurope.co.uk/struggling-vodafone-looks-to-sell-stake-in-1bn-iot-unit/) — Mobile Europe ／ [Vodafone considers sale of minority stake in IoT business](https://www.telecompaper.com/news/vodafone-considers-sale-of-minority-stake-in-iot-business-report--1463544) — Telecompaper(報道)

**プレイヤー動向**
- [Omdia Market Radar: IoT MVNOs 2026](https://omdia.tech.informa.com/om138813/omdia-market-radar-iot-mvnos-2026) — Omdia, 2026(1NCE/Cubic3/KORE = 28%、KORE の 2026 Q3 までの株主交代見込み)
- [IoT MVNOs: 290 Million Connections Managed in 2025](https://www.iotforall.com/iot-mvno-2025-report) — IoT For All, 2025(2023-12 以降 MVNO 間買収 9 件、Wireless Logic 3 件等)
- [The shifting sands of the IoT MVNO market landscape](https://transformainsights.com/blog/shifting-sands-iot-mvno-market-landscape) — Transforma Insights
- [Aeris Soars Past 100 Million Connected Devices](https://www.businesswire.com/news/home/20260127961011/en/Aeris-Soars-Past-100-Million-Connected-Devices-Delivering-Nearly-90-Percent-Growth-and-Outpacing-IoT-Market) — Business Wire, 2026-01-27 ／ [Aeris and Verizon Business simplify global IoT expansion](https://www.iot-now.com/2026/02/25/155467-aeris-and-verizon-business-simplify-global-iot-expansion-with-unified-connectivity-and-orchestration/) — IoT Now, 2026-02-25 ／ [Aeris signs IoT Accelerator agreement with KDDI](https://www.sdxcentral.com/news/aeris-signs-iot-accelerator-agreement-with-japanese-telecom-kddi/) — SDxCentral(日付未確認)
- [1NCE Continues Growth and Expands Its Software, AI and Services Offering](https://www.businesswire.com/news/home/20260107086987/en/1NCE-Continues-Growth-and-Expands-Its-Software-AI-and-Services-Offering) — Business Wire, 2026-01-07
- [emnify Debuts Factory-First IoT Connectivity at CES 2026](https://iotbusinessnews.com/2025/12/22/emnify-debuts-factory-first-iot-connectivity-at-ces-2026/) — IoT Business News, 2025-12-22
- [Onomondo Reshapes Telecom and Now Accelerates Growth with Strengthened Leadership](https://onomondo.com/blog/onomondo-reshapes-telecom-and-now-accelerates-growth-with-strengthened-leadership/) — Onomondo Blog(掲載日記載なし)／ [IoT For All 版](https://www.iotforall.com/news/onomondo-reshapes-telecom-and-now-accelerates-growth-with-strengthened-leadership)
- [floLIVE — Crunchbase](https://www.crunchbase.com/organization/flo-live) ／ [Tracxn(累計 $88.2M、直近 2023-09-12 Series C $47M)](https://tracxn.com/d/companies/flolive/__7LDgpamVfVN5_df8QeWLEO3eKzE0rO61Ipy6YQTpR88)
- [Hologram — CB Insights](https://www.cbinsights.com/company/hologram) ／ [G2 における評価(emnify 代替 1 位)](https://www.g2.com/products/emnify/competitors/alternatives)
- [Telenor targets IoT growth with consolidation move](https://www.telecomtv.com/content/access-evolution/telenor-targets-iot-growth-with-consolidation-move-54293/) — TelecomTV ／ [Telenor IoT, Telenor Connexion Join Forces](https://www.thefastmode.com/mobile-network-operators-m-a/45859-telenor-iot-telenor-connexion-join-forces-to-build-a-global-iot-platform) — The Fast Mode(統合完了 2026-01)

**ハイパースケーラー**
- [AWS IoT Analytics end of support(2025-12-15)](https://docs.aws.amazon.com/iotanalytics/latest/userguide/iotanalytics-end-of-support.html) ／ [AWS IoT Events end of support(2026-05-20)](https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-end-of-support.html) — AWS 公式ドキュメント ／ [Fleet Hub 終了(2025-10-18)](https://wizzdev.com/blog/aws-fleet-hub-shutdown/) — WizzDev ／ [AWS 2025 Retirements まとめ(Panorama 2026-05-31 等)](https://dev.to/muhammad_zeeshan_6499a22a/aws-2025-retirements-charting-the-course-through-service-sunsets-and-seamless-migrations-n3l) — DEV Community
- [Microsoft 'retires' Azure IoT Central in platform rethink](https://www.theregister.com/2024/02/15/microsoft_retires_azure_iot_central/) — The Register, 2024-02-15 ／ [Microsoft Announces Retirement of Azure IoT Central Service by 2027](https://winbuzzer.com/2024/02/16/microsoft-announces-retirement-of-azure-iot-central-service-by-2027-xcxwbn/) — WinBuzzer, 2024-02-16(告知直後の混乱含む)

**技術・規制トレンド**
- [How the new SGP.32 eSIM standard will transform IoT connectivity](https://www.rcrwireless.com/20250922/internet-of-things/sgp-32-esim-transform-iot) — RCR Wireless, 2025-09-22 ／ [IoT eSIM Trends 2026(Kaleido 予測、Rivian R2、MWC 2026 の Tele2 IoT×IDEMIA×Cisco)](https://spenza.com/esim/iot-esim-trends/) — Spenza, 2026 ／ [What next for eSIM? — SGP.32 era](https://www.gsma.com/solutions-and-impact/technologies/esim/gsma_resources/what-next-for-esim-challenges-and-opportunities-in-the-sgp-32-era/) — GSMA ／ KORE×Kigen SGP.32 共同ポートフォリオ: [KORE Press Center](https://www.korewireless.com/press-center/) — 2026
- [Skylo partners with Vodafone IoT(NTN NB-IoT)](https://www.skylo.tech/newsroom/skylo-partners-with-vodafone-iot-to-bring-ntn-nb-iot-satellite-connectivity-to-customers) — Skylo Newsroom ／ [Soracom×Skylo 統合ソリューション GA(公開情報)](https://www.skylo.tech/newsroom/soracom-announces-general-availability-of-integrated-satellite-iot-connectivity-solution-with-skylo) — Skylo Newsroom, 2025-10
- [5G RedCap: The Smart IoT Path Forward for 2026(42 オペレーター・27 か国等)](https://5gstore.com/blog/2026/04/21/5g-redcap-iot-connectivity-2026/) — 5Gstore Blog, 2026-04-21 ／ [5G RedCap: What Reduced Capability Means for IoT Deployments](https://iotbusinessnews.com/2026/03/18/5g-redcap-what-reduced-capability-means-for-iot-deployments/) — IoT Business News, 2026-03-18
- [Cyber Resilience Act(欧州委員会公式)](https://digital-strategy.ec.europa.eu/en/policies/cyber-resilience-act) ／ [CRA Reporting obligations(公式)](https://digital-strategy.ec.europa.eu/en/policies/cra-reporting) — European Commission ／ [EU CRA: September 11, 2026 Reporting Deadline](https://www.crowell.com/en/insights/client-alerts/eu-cyber-resilience-act-countdown-11-september-2026-incidentvulnerability-reporting-deadline-is-less-than-100-days-away) — Crowell & Moring, 2026-06

**ロングリスト関連**
- [Golioth $4.6M シード](https://blog.golioth.io/may-2023-golioth-seed-round/) — Golioth Blog, 2023-05 ／ [初期シード $2.5M](https://www.prnewswire.com/news-releases/golioth-a-cloud-platform-for-iot-announces-private-beta-and-2-5m-seed-301304014.html) — PR Newswire, 2021-06
- [Blues Raises $33M(累計約 $100M)](https://blog.tmcnet.com/blog/rich-tehrani/iot/blues-raises-33m-to-scale-secure-iot-connectivity-platform.html) — TMCnet(掲載日記載なし)

> 注: 本レポートは公開情報のみに基づく。「未確認」と付した項目は一次情報での裏取りができていないため、意思決定に用いる前に deal-desk での追加検証を要する。
