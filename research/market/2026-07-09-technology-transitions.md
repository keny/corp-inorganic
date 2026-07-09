# 技術遷移スキャン — 2G/3G サンセット / VoLTE / 5G SA・RedCap / Cat.1bis / LPWA / NTN(2026-07-09)

> 作成: market-scout ／ 作成日: 2026-07-09 ／ 対象期間: 2024-11 〜 2026-07(構造理解に必要な過去経緯を含む)／ テーマ: コネクティビティ・ロードマップ議論 T6(技術遷移)
> 位置づけ: `2026-07-09-connectivity-roadmap-briefing.md` C 表 T6 の裏取り + 技術遷移の商機・リスク整理。公開情報のみに基づく参考情報であり投資判断ではない。外部向け文書化の際は必ず人間レビューを要する。

## TL;DR(経営向け)

- **2G/3G 停波は最終局面。日本は 3G 完了(ドコモ 2026-03-31)、米国は T-Mobile 2G が 2026-08-03 に停波し主要国レガシー網がほぼ消滅。** 欧州 2G は 2026〜2030 に分散停波。2026-27 が「最後のマイグレーション需要」の集中期で、移行先の事実上の本命は Cat.1bis(2025 年の世界モジュール出荷の 2 個に 1 個)。
- **SMS 到達性が静かな時限爆弾。** 停波後に MSC/SGs(Combined Attach)が撤去されると SMS over SGs は持続不能(Transforma/GSMA)。代替は SGd か IMS(SMSoIP)だが多くの IoT 機器は IMS 非対応。VoLTE ローミングは Transatel が 73 か国まで拡大、EU NG-eCall 規制(新型式 2026-01-01〜)が RTC/IMS 需要を規制で底上げ。
- **5G は NSA ローミング主流が当面続く**(Kaleido: 2026 年の 5G ローミング 3.75 億接続は NSA 牽引、SA は 2030 年でも 20-25%)。RedCap は AT&T が 2025-07 に全国商用化したが、Omdia は「本格普及は eRedCap(2027-29)」と慎重。**Verizon の「4G を 2049 年まで維持」は公開情報で確認不能**(サンセット計画なし、までは支持)。
- **NB-IoT は米国で明確に退潮**(AT&T 2025-Q1 停波)だが、欧州は網維持・中国は依然大規模。LTE-M は AT&T/Verizon が維持を明言し 2030 年代も存続見通し(Ericsson: 2030 年もセルラー IoT の 40% が NB-IoT/LTE-M)。
- **衛星 NTN は「地上の代替」ではなく「到達性の保険」で確定。** 価格は地上比 3〜4 桁高(EUR 0.70-0.90/KB)。Skylo は MNO/MVNO を束ねる標準 NTN 陣営を拡大、Starlink D2C は 12 キャリア超と提携し 2025-10 からアプリデータ対応。1 SIM/1 コンソールでの地上+衛星統合管理の価値が上がる。

## 1. 主要ファインディング

### 1.1 2G/3G サンセットの主要国スケジュール

| 地域 | 状況(出典は情報源一覧) |
|---|---|
| 日本 | 3G 全滅: KDDI 2022-03-31、SoftBank 2024-04-15、NTT ドコモ FOMA 2026-03-31 終了(emnify 一覧 2026-06-22 更新)。2G は 2012 年までに消滅済み |
| 米国 | 3G: AT&T 2022-02、T-Mobile(UMTS)2022-07、Verizon 2022-12 で完了。2G: AT&T 2017 年停波済み、**T-Mobile GSM が 2026-08-03 停波**(公式)— 米国のレガシー網が完全消滅。T-Mobile が 2G を長く残した理由は「VoLTE 未対応のインバウンドローマー」とレガシー IoT(Fierce Network) |
| カナダ | Rogers 3G 2025-08-07、TELUS 3G 2026-03-31(emnify) |
| 欧州 | 3G 先行・2G 長残しが基本形。3G: Vodafone ルーマニア 2026-03-24、O2 スロバキア 2026-01-31 完了等。2G: Orange フランス 2026 年末開始(南西部 9 県で 2026-03〜06 に先行)、スペイン各社 2026〜2027、**DT ドイツは 2028 夏(IoT・緊急用途は特例延長)、Vodafone ドイツは 2028-09 開始・完全撤去は 2031-01 から**(2025-09 発表で前倒し)、Telia スウェーデン 2027 年末、ベルギー Orange 2028 年末、エストニア/モンテネグロ 2029 年末 |
| アジア他 | 中国: China Unicom 3G 2026-06-30、China Mobile 2G 2026-06-23。ベトナム 2G 完全終了 2026-09-30。香港 China Mobile 2G 2026-06-23。豪州は 3G を 2024 年に全社停波済み。インドは 2G 残存(明確な停波計画なし、BSNL 3G のみ計画) |

- 停波は「無線停止」と「コア(MSC/HLR)撤去」の二段階で、IoT 事業者は**二つの波**に直面する(Tech Times 2026-07-07: T-Mobile 2G 停波の分析)。
- 帯域は 4G/5G へ再割当(DT は 900MHz を 4G/5G へ)。移行推奨先はどのアグリゲーターも共通して「LTE-M / NB-IoT / Cat.1 / 4G/5G」。

### 1.2 Combined Attach(SMS over SGs)廃止と SMS 到達性

- **SMS over SGs は MME→MSC 連携に依存する暫定策で、2G/3G コア(MSC 機能)が完全撤去されると持続不能**(Transforma Insights 2025-11-07)。GSMA は (1) SMS over Diameter(SGd)を最も将来性ある解、(2) SMS over SGs は暫定解、(3) SMS over IMS(SMSoIP)は IMS スタック必須で「現場の多くの IoT 機器が非対応」と整理。
- 停波で影響を受ける具体例として「コネクテッドカーの遠隔制御」「スマートメーターの検針」が名指しされ、事業者へは IR.21 更新とローミングパートナーへの早期通知が推奨されている(Transforma)。
- ホームオペレーターが IMS/VoLTE ローミング未対応のままだと訪問網の 3G 停波で音声・SMS が失われるため、**VoLTE ローミング未対応こそが停波遅延の主因**という指摘(Mobileum)。T-Mobile US が 2G を 2026 年まで残した理由と同型。
- 含意: EPS only 化が進むほど「SMS で起こす/制御する」設計は世界的に壊れていく。SMS 依存機器の棚卸しと、IP ベース到達性(デバイス起点接続+オンデマンドリモートアクセス)への移行が構造需要になる。

### 1.3 VoLTE ローミングの IoT 対応

- **Transatel: VoLTE/SMSoIP ローミングを 73 か国・約 200 ネットワークで提供**(公式 docs、2026-06-22 更新。日本は ドコモ/KDDI/SoftBank、米国は T-Mobile/AT&T/Verizon を含む)。「フットプリントは今後も拡大」と明記。
- Orange Wholesale: Roaming Sponsor for IoT が「5G・VoLTE・LPWA・eSIM 対応」を明記し、VoLTE/5G をスポンサードローミング基盤に追加済み。ただし**対応 MNO 数の公表なし**。
- 業界全体では BICS がスポンサードローミング首位で、VoLTE・5G・IoT が成長ドライバー(TelecomLead 2026)。
- 音声/RTC が必要な IoT ユースケース(2G/3G 停波で強制移行が発生):
  - **エレベーター緊急通話**: EU/UK では常時通話可能な遠隔アラームが法定要件。VoLTE ソリューションが商品化(Robustel 等)。
  - **NG-eCall(EU)**: **2026-01-01 以降、M1/N1 新型式は PS 網(4G/5G IMS)eCall 必須。2027-01-01 以降は旧 CS eCall のみの車両は EU で新規登録不可**(EN 17240:2024 へ規格昇格)。RTC 需要を規制が底上げする代表例。
  - 警備・アラームパネル、mPERS/ヘルスケア端末、車両 SOS、POS の音声確認等(Webbing、Wireless Logic)。
- 判定メモ: ブリーフィング G6 の「ローミングパートナーの VoLTE 対応が急拡大」は公開情報でも明確に支持(Transatel の国数、Orange のスポンサー基盤対応、GSMA/EENA の移行圧力)。

### 1.4 5G: NSA 主流・SA ローミング・RedCap・Verizon の 4G 長期維持

- **NSA 主流は当面継続**: Kaleido Intelligence は「2026 年の 5G ローミング接続 3.75 億超は NSA が牽引、**SA は 2030 年でも全 5G ローミングの 20-25%**」と予測。
- SA ローミング準備状況: 商用 SA ローミング開始意向は約 25 MNO(2026 年)だが、**約 80% が「準備不足」を自認**(Kaleido/Syniverse ウェビナー)。国内 SA 商用は約 90 件/45+ か国、SA ローミングトライアルは 15+ 市場。課題は BCE(SEPP 等の境界装置)対応・IPX 容量・課金。→「SA 要件はローカルプロファイル(SGP.32)で満たす」という当社系の整理は公開情報の構図とも整合的(SA ローミングが未成熟な間、SA 必須案件は現地プロファイルが現実解)。
- **RedCap**: AT&T が 2025-07-17 に全国商用化(200M POPs、初の商用認証デバイスは Franklin RG350 ホットスポット。Semtech/Telit/Rhino がモジュール認証中)。GSA 集計で **42 事業者/27 か国が投資(2026-04 時点、2025-09 の 34 から増加)**。商用化済み: AT&T、Telefónica/DT(独)、SoftBank(日)、M1(星)、MasOrange(西)、e&(UAE)等。モジュール価格は USD 30-50 → 2026 年末 USD 15-25 見込み。
- ただし **Omdia(2026-07)は「RedCap は採用に課題、本命は eRedCap」**: ABI は 2029 年までの RedCap 系モジュール累計 8,000 万個のうち **71% が eRedCap(Rel-18)** と予測。eRedCap チップは 2026 年投入・モジュール 2027 年・量産 2027-28 → **普及の本番は 2027-29**。RedCap は 5G SA コア前提のため、SA 展開と連動。
- **Verizon**: 「4G LTE をサンセットする計画はない」(5Gstore 2025-06 等)、NB-IoT も「700MHz LTE 上で停波の差し迫った計画なし」(Light Reading)。5G SA を全国展開し Apple Watch 向け RedCap を開始、2026 年中に都市部から RedCap 拡大(Fierce Network)。**「2049 年まで維持」という年限は公開情報で確認できず**(→ 3 章)。
- T-Mobile US: LTE 帯域(B2/4/66/12/71)の 5G SA 転用を 2028 年めどに進め、**LTE 完全終了は 2035 年前後**という報道(Tech Times 2026-07-07、「社内ロードマップ」引用)— **未確認**(公式発表なし)。

### 1.5 Cat.1bis: 価格・エコシステム・採用状況

- **Counterpoint(2026-02 頃発表の 2025 年通年集計): 世界セルラー IoT モジュール出荷 +15%、出荷の 2 個に 1 個が Cat.1bis** — マスマーケットの明確な主流。IoT Analytics も Q3 2025 に Cat.1bis +49% 成長と報告。
- ABI Research: **2029 年までに Cat.1 市場の約 70% を Cat.1bis が置換**(u-blox 等が引用)。
- 価格: モジュール単価 **USD 2.50-12.50**、中国の大型入札では **USD 4 未満**まで下落(Alibaba 調達ガイド 2026、IoT Analytics)。NB-IoT との価格差が縮小し、LPWA を選ぶ理由が消えつつある(Hologram 2026 トレンド)。
- エコシステム: Quectel(モジュールシェア約 40%、Q1 2025)、Fibocom(+28% 成長、MG661 等)、SIMCom、Telit、u-blox(LEXI-R10)。**上位 5 社で 74%、中国勢が支配的**(IoT Analytics Q3 2025)→ 米中摩擦・調達集中はリスク。
- 採用理由: 単一アンテナで Cat.1 同等性能・**通常の LTE ネットワークでそのまま全球ローミング可能**(LPWA のような国別デプロイ差がない)。2G/3G 停波後の移行先およびグローバル SKU の第一候補という業界整理(Eseye、Telenor IoT、u-blox)。APAC が採用を主導し中国が域内需要の 60% 超(Intel Market Research)。

### 1.6 LPWA: NB-IoT の減退と LTE-M の存続

- **米国**: AT&T が NB-IoT を 2024-11 に新規販売停止 → **2025-Q1 に停波完了**(業界初の主要国 LPWA 停波。RCR 2024-11-20、Counterpoint)。LTE-M への移行を誘導。Verizon・T-Mobile は NB-IoT 網を維持(「停波計画なし」、Light Reading)だが、Verizon の NB-IoT は固定用途中心で拡張の動きなし。
- **欧州**: 停波事例はなし。DT・Vodafone は NB-IoT を維持・推進。ただし新規デザインインは Cat.1bis/LTE-M へ流れ、「NB-IoT は中国以外で減退、Cat.1bis との価格差縮小が主因」という業界評価(Hologram 2026、Velos、Monogoto 2025-01)。
- **グローバル**: Ericsson Mobility Report は NB-IoT 展開 177 事業者・LTE-M(Cat-M)81 事業者、セルラー IoT 接続は 2025 年末 45 億 → 2031 年約 80 億、**2030 年時点でも NB-IoT/LTE-M が全体の 40%**(ブロードバンド IoT 60%)と予測 — 「消える」のではなく「新規成長が細る」構図。
- **LTE-M**: AT&T は LTE-M を「5G Massive IoT へのアップグレードパス」として維持を明言。Orange も 2G/3G 移行先として LTE-M を推奨(Telco Magazine)。日本は 3MNO とも LTE-M 提供中。LTE-M の中期存続は堅い。

### 1.7 衛星 NTN: 商用状況・提携・価格差

- **Skylo(GEO 上の 3GPP Rel-17 NB-NTN、商用中)**: 対応スマホ/モジュールは既存セルラーチップのまま接続。2026 年に **NTN 音声ゲートウェイ**まで発表し、10 億台超のデバイスが接続可能と主張。提携網が急拡大: Vodafone IoT(ハイブリッド 1 SIM)、Tele2 IoT(スウェーデン初の商用 3GPP D2D)、Orange(Pixel 9/10 向け)、Deutsche Telekom(IoT タリフ+Digitanimal 家畜トラッカー)、o2 Telefónica(独初の衛星 IoT タリフ)、G+D、Transatel(Skylo/Sateliot/Stellar と 3 提携)、Verizon 等。
- **価格差は 3〜4 桁**: o2 Business **EUR 0.70/KB**、DT **EUR 0.90/KB**、Blues Notecard for Skylo は **USD 0.00075/byte(≒USD 0.75/KB)+ パケット最低 50 bytes**。地上 IoT 回線(概ね USD 数〜数十/GB)に対し、**KB 単価でみると桁が 3〜4 つ違う** → 常用回線ではなく「圏外時フォールバック・低頻度テレメトリ・到達性の保険」として設計される(Skylo 自身も TN+NTN 併用が前提とコメント)。
- **Starlink Direct-to-Cell**: T-Mobile「T-Satellite」が 2025-07-23 商用開始(メッセージング、USD 10/月 or 上位プラン込み)→ **2025-10-01 からアプリデータ対応**(WhatsApp、Google Maps 等)。D2C 衛星 650 機超(2026-01)。**IoT デバイス対応は「今後の予定」段階**(農業・輸送・海事を想定)。キャリアパートナーは 12 超: T-Mobile、KDDI、Optus、Telstra、Rogers、One NZ、Salt、VMO2、Kyivstar、Entel(智・秘)、Airtel Africa 等。SpaceX は EchoStar 周波数を USD 17B で取得済み(2025-09、前回スキャン)で、V2 衛星(Starship 打上げ、データ密度 100 倍)を 2027 年央から計画。
- **標準 NTN のモジュール側**: Blues Notecard for Skylo(5G NTN 衛星+NB-IoT/LTE-M+Wi-Fi+GNSS、2026-03)など「地上+衛星のマルチパスを 1 モジュールで」が製品化フェーズ。LEO 店舗&フォワード型の Sateliot は Series C EUR 100M 調達中(前回スキャン済み)。
- 構図: **衛星レイヤー自体は資本戦(SpaceX/EchoStar/AST)**、IoT 事業者の価値は「地上+衛星を 1 SIM・単一コンソールで統合管理し、用途別に使い分けさせる」オーケストレーション側に集まる。

## 2. 競合・プレイヤー動向(技術遷移への各社の構え)

- **IoT MVNO 各社はサンセット・マイグレーションを商機として前面化**: 1NCE・emnify・Onomondo・Wireless Logic・Telenor IoT・Eseye・Pelion が移行ガイド/特設ページを常設し、移行先として Cat.1bis+LTE-M を推奨。移行需要の刈り取り競争は既に激しい。
- **Transatel(NTT 傘下)が「音声+衛星」の統合で先行**: VoLTE ローミング 73 か国に加え、Skylo/Sateliot/Stellar と NTN 3 提携(SatNews)。スポンサーローミング勢の中で RTC と NTN の品揃えが最も広い部類。
- **キャリアの分化**: AT&T = NB-IoT 停波 + RedCap 全国 + LTE-M 維持(5G SA 移行に積極的)。Verizon = 4G 長期維持を示唆しつつ SA/RedCap を漸進展開。T-Mobile = 2G 停波(2026-08)+ LTE 帯域の 5G SA 転用加速(2028 圧縮・2035 LTE 終了は未確認報道)。欧州 = 2G 長残し・NB-IoT 網維持(エレベーター・スマメ・eCall の残存需要)。日本 = 3G 完了、RedCap は SoftBank が商用先行。
- **モジュール**: Quectel/Fibocom の中国勢が Cat.1bis の価格と量を支配。Semtech のモジュール事業切り出し(前回スキャン)と合わせ、西側サプライチェーンの選択肢が狭まっている。
- **衛星**: Skylo(標準 NTN・キャリア束ね)vs Starlink(独自波形→3GPP 化、キャリア直接提携)の二陣営が確立。Viasat/ORBCOMM 等レガシー衛星 IoT は標準 NTN へ寄せる動き。

## 3. ブリーフィング主張の裏取り結果(C 表 T6 担当分)

| # | 文書中の主張 | 判定 | 根拠(出典) |
|---|---|---|---|
| 1 | Verizon は 4G を 2049 年まで維持する決定 | **確認不能** | 「2049」への言及は Verizon 公式・業界メディア・SEC 資料のいずれからも発見できず(7 通りの検索で不検出)。**「4G LTE のサンセット計画なし」「NB-IoT も停波の差し迫った計画なし」までは支持**(5Gstore 2025-06-25、Light Reading)。年限「2049」は非公開の商談・イベント由来の可能性が高く、一次出所の社内確認を推奨。矛盾する公開情報もなし |
| 2 | AT&T の 5G RedCap 商用ローンチ | **支持** | 2025-07-17 に全国 200M POPs で商用化(AT&T 公式ブログ、RCR Wireless 2025-07-17、Fierce Network)。初の商用認証デバイスは Franklin RG350。なお 5G SA 全国発表は 2025-11 |
| 3 | Transatel(TL)50 MNO の VoLTE 対応 | **方向は支持・数値は公開情報の方が大きい** | 公式 docs(2026-06-22 更新)は VoLTE/SMSoIP ローミングを **73 か国・約 200 ネットワーク**と記載。「50 MNO」は集計時点・集計単位(国/網)の違いの可能性。急拡大トレンド自体は明確に支持 |
| 4 | Orange 52 MNO の VoLTE 対応 | **確認不能(対応自体は支持)** | Orange Wholesale は Roaming Sponsor for IoT の VoLTE/5G 対応を明記するが、**対応 MNO 数は非公表**。52 という数値の公開裏付けなし |
| 5 | NB-IoT の欧米での減退 | **部分支持** | 米国: AT&T が 2025-Q1 停波で明確に支持(RCR 2024-11-20、Counterpoint)。ただし Verizon/T-Mobile は網維持。欧州: 停波事例なし・DT/Vodafone は継続だが、新規需要は Cat.1bis へシフト(Hologram、Velos)。「網の消滅」ではなく「新規採用の減退」と読むのが正確 |
| 6 | LTE-M は長寿命(存続) | **支持** | AT&T は LTE-M 維持を明言(5G Massive IoT への継続パス)、Verizon も LTE-M 全国網を維持。Ericsson: Cat-M 商用 81 事業者、2030 年もセルラー IoT の 40% が NB-IoT/LTE-M |
| 7 | Cat.1bis が 2G/3G マイグレ・グローバル案件の最適解(主流) | **支持** | Counterpoint: 2025 年出荷の 2 個に 1 個が Cat.1bis。ABI: 2029 年までに Cat.1 市場の約 70% を置換。単価 USD 2.50-12.50(中国入札で USD 4 未満)。移行先推奨としても業界標準の整理(Eseye、Telenor IoT、u-blox) |
| 8 | (関連)日本 3MNO の 3G 完了・米国は T-Mobile 除き完了・5G は NSA 主流で SA ローミング未成熟 | **支持** | 日本: ドコモ 2026-03-31 で完了(emnify)。米国 2G/3G は T-Mobile 2G のみ残存で 2026-08-03 停波予定(T-Mobile 公式)。Kaleido: 2026 年も 5G ローミングは NSA 牽引、SA ローミング商用意向 25 MNO の 8 割が準備不足 |

## 4. SORACOM への戦略的含意

1. **2026-27 は「最後の 2G/3G マイグレ波」の刈り取り期**: T-Mobile US 2G(2026-08)、中国 3G/2G(2026-06)、ベトナム 2G(2026-09)、欧州 2G(2026-28)が連続。移行先の本命 Cat.1bis はプロファイル/ローミングの面で通常 LTE と同じに扱えるため、当社ローミング SIM・SGP.32 eSIM の増分需要に直結する。移行支援(推奨モジュール認定・評価キット・接続プロファイル切替)をパッケージ化して商流(機器メーカー・SIer)に載せる好機。
2. **SMS 到達性の崩壊は「到達性」戦略(J7)の追い風**: EPS only 化と MSC 撤去で「SMS で起こす・制御する」運用が世界的に壊れていく。SMS 依存顧客の棚卸しと、(a) VoLTE/SMSoIP 対応ローミング(スポンサー経由)、(b) IP ベースのオンデマンド到達性(デバイス起点+リモートアクセス)への移行提案は、既存資産の延長で差別化できる領域。NG-eCall(2026-01 規制)は車載 RTC 需要の規制ドリブンな下限を作る — 車載戦場(J10-①)の提案材料。
3. **NSA 主流の長期化は現行ローミングモデルの寿命を延ばす**: SA ローミングは 2030 年でも少数派の見通しであり、SA 必須案件(ネットワークスライシング等)はローカルプロファイル(SGP.32)で対応する二段構えが公開情報とも整合。RedCap の採用判断は eRedCap(2027-29)+SA コア成熟まで急ぐ必要なし — 慌てて RedCap 対応を打ち出す競合との差別化は「時期の正確さ」で十分。
4. **NTN は「単価の高い保険」としてマルチパス統合管理の価値を上げる**: 地上比 3〜4 桁の価格差が続く限り、顧客は「常時は地上・圏外/障害時のみ衛星」を求める。1 SIM・単一コンソールで TN/NTN を使い分けさせる統合管理(既に Skylo 統合を GA 済み・公開情報)は先行優位。Starlink D2C の IoT データ対応が商用化した時点で、対応可否がグローバル案件の RFP 要件に入るリスク/機会の両面を注視。
5. **リスク**: (i) Cat.1bis モジュールの中国集中(Quectel/Fibocom で過半)は輸出規制・調達途絶の外生リスク。(ii) T-Mobile US の LTE 圧縮観測(未確認)が現実化すると、米国で LTE 前提の長寿命 IoT の再設計問題が 2030 年前後に再来 — 米国パートナー戦略の前提として確度を継続確認。(iii) 欧州 2G の「特例延長」(DT/Vodafone のエレベーター・eCall 向け)は移行需要を後ろ倒しにする可能性。

## 5. インオーガニック(M&A・出資・提携)の含意

- **P1(コネクティビティ深化)— NTN**: 衛星レイヤー自体は資本戦で対象外(前回スキャン結論を再確認)。価値は TN/NTN 統合管理側に集まるため、**Skylo との提携深化(既存)+ 標準準拠 LEO(Sateliot、既存ロングリスト)へのマイノリティ出資**という現行方針を本スキャンは支持。Starlink D2C の IoT 商用が近づいた場合、D2C 対応 MNO(KDDI 含む)経由でのアクセス確保を提携課題として strategy-planner に引き継ぐ。
- **P1/P5(ケイパビリティ)— VoLTE/IMS**: SMS 到達性・NG-eCall の潮流で **クラウド IMS/VoLTE スタックの技術チーム**の価値が上がる。独立系の「買える玉」は希少(Working Group Two は 2024 年に Cisco が買収済みで消滅)。→ 買収より **スポンサーキャリア(Transatel/Orange)経由の Partner + 小規模 acqui-hire の機会監視**が現実的。IMS テスト・RTC ゲートウェイ領域の少人数チームは P5 候補として継続スキャン。
- **P2(デバイス・エッジ)**: マイグレ需要の入口は「モジュール選定・認定」。モジュール HW はガードレール対象外だが、**Blues(既存ロングリスト、Notecard for Skylo で TN+NTN 統合を製品化)の優先度は本スキャンで上昇** — 接続込みデバイス+衛星フォールバックは当社マルチパス戦略と補完的。提携起点(Partner→将来 Buy)の現行整理を維持。
- **P4(地理・顧客基盤)**: 欧州 2G 停波(2026-28)は、移行投資を負担できない**中堅 M2M/MVNO の売り時**を作る。停波直前の国(西・仏・独・北欧)の地域 M2M 事業者は「顧客基盤ごと移行を請け負う」型のロールアップ機会 — Wireless Logic が同じ論理で動いているため、案件化するなら速度勝負。新規の具体候補は今回未特定(deal-desk への新規追加提案なし。既存候補の優先度メモのみ)。
- **相場観**: 本テーマからの新規バリュエーションデータポイントなし(ディール検出なし)。

## 6. 未解決の問い

1. **「Verizon 2049」の一次出所は何か** — 公開情報に存在しない。原本作成者に出所(Verizon の非公開ロードマップ資料か、イベントでの口頭言及か)の確認を依頼したい。
2. **Orange の VoLTE 対応 MNO 数(52)の裏付け** — 公表なし。Orange Wholesale への直接確認事項。
3. **SGs/MSC 撤去(EPS only 化)の国別タイムライン** — IR.21 レベルの情報は公開されない。スポンサーキャリア経由で「SMS over SGs が使えなくなる網」の棚卸しが必要(どの国で・いつ SMS 到達性が切れるかの実務マップ)。
4. **T-Mobile US の LTE 圧縮(2028)・LTE 終了(~2035)観測の確度** — 未確認報道。米国向け長寿命 IoT 案件の設計前提に関わるため四半期ごとに追跡。
5. **Starlink D2C の IoT データ商用(モジュール/API 対応)の時期と価格** — 「計画段階」から進捗したら、地上 IoT 回線との価格差・補完関係の再評価が必要。
6. **eRedCap の日本展開時期** — SoftBank の RedCap 商用に続く国内キャリアの SA コア+eRedCap 計画(2027 年以降の国内 IoT 中速帯の主導権に直結)。

## 情報源

**2G/3G サンセット**
- [T-Mobile Network Evolution(公式)](https://www.t-mobile.com/support/coverage/t-mobile-network-evolution) — T-Mobile ／ [T-Mobile sets an official end date for its 2G network](https://www.androidauthority.com/t-mobile-2g-shutdown-date-3683679/) — Android Authority, 2026 ／ [T-Mobile to shut down 2G GSM network this summer](https://www.fierce-network.com/wireless/t-mobile-shut-down-2g-gsm-network-summer) — Fierce Network, 2026
- [T-Mobile 2G GSM Ends August 3: IoT Operators Face Two Migration Waves, Not One](https://www.techtimes.com/articles/319869/20260707/t-mobile-2g-gsm-ends-august-3-iot-operators-face-two-migration-waves-not-one.htm) — Tech Times, 2026-07-07
- [Global 2G/3G Phase-Out Timeline for IoT Devices](https://www.emnify.com/blog/global-2g-3g-phase-out) — emnify(2026-06-22 更新。日本 3MNO・米加の日付)
- [2G/3G network sunset update (Global IoT 2026)](https://thingsdata.com/news/2g-3g-sunset-update-global-iot-2026/) — Thingsdata, 2026-04-10(中国・ベトナム・欧州各国の日付)
- [2G / 3G shutdown: Who is affected?](https://whereversim.com/en/3g-sunset) — WherEver SIM(DT 2028・Vodafone DE 2028-09/2031-01・欧州各国)／ [2G sunset by country — updated 2026 timeline](https://iot.cards/en/resources/guides/sunset-2g) — iot.cards
- [Orange Phases Out 2G and 3G For Future Networks](https://telcomagazine.com/news/orange-phases-out-2g-and-3g-for-future-networks) — Telco Magazine(仏 2026 年・LTE-M/VoLTE への移行支援)

**Combined Attach / SMS**
- [SMS for IoT after 2G/3G shutdown](https://transformainsights.com/blog/sms-for-iot-after-2g3g-shutdown) — Transforma Insights, 2025-11-07(SGs 持続不能・SGd 推奨・IR.21)
- [Ensuring SMS Continuity for IoT after 2G/3G Shutdown](https://www.gsma.com/solutions-and-impact/technologies/internet-of-things/gsma_resources/ensuring-sms-continuity-for-iot-after-2g-3g-shutdown/) — GSMA(本文は 403 のため Transforma 経由の要旨)
- [How CSPs without VoLTE Roaming can avoid 2G/3G Sunset Disruption](https://blog.mobileum.com/how-csps-without-volte-roaming-can-avoid-2g3g-sunset-disruption) — Mobileum ／ [Voice & SMS transformation following 2G 3G sunset](https://www.ericsson.com/en/reports-and-papers/white-papers/voice-service-and-sms-transformation-following-2g-3g-sunset) — Ericsson

**VoLTE / RTC**
- [VoLTE Roaming Footprint](https://docs.transatel.com/getting-started/iot-latest-coverage-updates/volte-roaming-footprint/) — Transatel Docs(2026-06-22 更新、73 か国)／ [IMS services (VoLTE/VoWiFi/SMSoIP)](https://docs.transatel.com/services/volte-vowifi/ims-services-volte-vowifi-smsoip/) — Transatel Docs
- [Roaming Sponsor for IoT](https://wholesale.orange.com/france/en/our-solutions/mobile/roaming-sponsor-for-iot/) — Orange Wholesale(VoLTE/5G/LPWA/eSIM 対応)／ [BICS Tops Global Sponsored Roaming Market](https://telecomlead.com/telecom-services/bics-tops-global-sponsored-roaming-market-as-volte-5g-and-iot-drive-international-connectivity-growth-126578) — TelecomLead, 2026
- [Elevator VoLTE Emergency Call Solution](https://www.robustel.com/smart-cities/elevator-iot-smart-cities/elevator-volte-emergency-call-solution/) — Robustel ／ [Transitioning from eCall to NG-eCall](https://www.keysight.com/blogs/en/inds/auto/2024/07/25/ng-ecall-post) — Keysight, 2024-07-25 ／ [New Rules for EU NG eCall Mandatory Safety Certification](https://www.blueasialabs.com/shouyehuandeng/new-rules-for-eu-ng-ecall-mandatory-safety-certification) — Blue Asia Labs(2026-01-01/2027-01-01 期限)／ [Automotive OEMs must prepare for 2G/3G switch off](https://www.wirelessmobility.com/blog/automotive-oems-must-prepare-for-2g-3g-switch-off-ecall-specifications-have-been-amended-and-a-deadline-is-looming/) — Wireless Mobility
- [The 2G/3G Sunset: What It Means for IoT Deployments](https://webbingsolutions.com/the-2g-3g-sunset-and-iot-deployments/) — Webbing ／ [VoLTE or VoIP? Making the right choice for your IoT solutions](https://wirelesslogic.com/blog/volte-or-voip-making-the-right-choice-for-your-iot-solutions) — Wireless Logic

**5G NSA/SA・RedCap・Verizon/AT&T**
- [5G Roaming: 375M+ Consumer and IoT Connections Driven by NSA in 2026, SA Scaling to 20–25% by 2030](https://kaleidointelligence.com/5g-roaming-375-consumer-iot-connections-driven-by-nsa-in-2026/) — Kaleido Intelligence, 2026 ／ [Making 5G SA Roaming Work in 2026](https://www.syniverse.com/webinar/5g-roaming/making-5g-sa-roaming-work-in-2026-from-capability-to-commercial-adoption) — Syniverse/Kaleido(25 MNO・80% 準備不足)
- [AT&T Achieves Nationwide 5G RedCap Coverage](https://about.att.com/blogs/2025/5g-redcap.html) — AT&T 公式, 2025 ／ [AT&T intros nationwide 5G RedCap for mid-tier IoT in the US](https://www.rcrwireless.com/20250717/internet-of-things/att-intros-5g-redcap) — RCR Wireless, 2025-07-17 ／ [AT&T ups its IoT game with nationwide 5G RedCap coverage](https://www.fierce-network.com/wireless/att-ups-its-iot-game-nationwide-5g-redcap-coverage) — Fierce Network ／ [AT&T 5G Standalone Nationwide Launch](https://5gstore.com/blog/2025/11/05/att-5g-standalone-nationwide-launch/) — 5Gstore, 2025-11-05
- [5G RedCap faces adoption challenge while eRedCap shows stronger promise](https://omdia.tech.informa.com/blogs/2026/july/5g-redcap-faces-adoption-challenge-while-eredcap-shows-stronger-promise) — Omdia, 2026-07 ／ [5G RedCap in the UK: State of Play (May 2026 Update)](https://5gredcap.co.uk/uk-redcap-status-may-2026/) — 5gredcap.co.uk(GSA 42 事業者/27 か国、商用リスト)／ [5G RedCap: The Smart IoT Path Forward for 2026](https://5gstore.com/blog/2026/04/21/5g-redcap-iot-connectivity-2026/) — 5Gstore, 2026-04-21
- [Here's a 5G SA update on the Big 3 US mobile operators](https://www.fierce-network.com/wireless/big-3-mnos-us-5g-sa-update) — Fierce Network ／ [Apple and operators hone in on 5G RedCap smartwatches](https://www.fierce-network.com/wireless/apple-and-operators-hone-5g-redcap-smartwatches) — Fierce Network(Verizon の RedCap/SA)
- [4G Shutdown(未定・計画なしの整理)](https://5gstore.com/blog/2025/06/25/4g-shutdown/) — 5Gstore, 2025-06-25 ／ [AT&T to discontinue NB-IoT, but T-Mobile and Verizon keep the faith](https://www.lightreading.com/iot/at-t-to-discontinue-nb-iot-but-t-mobile-and-verizon-keep-the-faith) — Light Reading

**Cat.1bis・モジュール市場**
- [Global Cellular IoT Module Shipments Up 15% YoY in 2025 Driven by 4G Cat-1 bis and 5G](https://counterpointresearch.com/en/insights/global-cellular-iot-module-shipments-in-2025) — Counterpoint Research, 2026(出荷の 2 個に 1 個が Cat.1bis)
- [Cellular IoT market Q1 2025: Module shipments up 23%](https://iot-analytics.com/cellular-iot-market-q1-2025-module-shipments-23-percent-us-china-tensions-vendor-impact/) — IoT Analytics(Quectel 40% 等)／ [Cellular IoT Module and Chipset Market Tracker (Q3 2025)](https://iot-analytics.com/product/cellular-iot-module-chipset-market-tracker-forecast/) — IoT Analytics(Cat.1bis +49%、上位 5 社 74%)
- [Cellular Module Price Guide 2026: NB-IoT, Cat.1 bis & 5G RedCap](https://electronics.alibaba.com/product/price-of-cellular-module) — Alibaba Electronics(USD 2.50-12.50、中国入札 USD 4 未満)
- [LTE Cat-1 Bis for IoT and M2M: Everything You Need to Know](https://www.eseye.com/resources/iot-explained/lte-cat-1-bis-for-iot-and-m2m-everything-you-need-to-know/) — Eseye ／ [LTE Cat 1bis](https://www.u-blox.com/en/blogs/insights/lte-cat-1bis) — u-blox(ABI: 2029 年までに Cat.1 の ~70% 置換)／ [LTE Cat 1: Optimized Connectivity for IoT Devices](https://iot.telenor.com/technologies/connectivity/lte-cat-1/) — Telenor IoT ／ [LTE Cat 1.bis Communication Module Market Outlook](https://www.intelmarketresearch.com/lte-cat-bis-communication-module-market-5190) — Intel Market Research

**LPWA(NB-IoT / LTE-M)**
- [AT&T quits NB-IoT – sales stopped ahead of network shut-down](https://www.rcrwireless.com/20241120/internet-of-things-4/att-quits-nb-iot) — RCR Wireless, 2024-11-20 ／ [AT&T to Decommission NB-IoT Network by 2025](https://www.counterpointresearch.com/insight/post-insight-research-notes-blogs-att-to-decommission-nbiot-network-by-2025-due-to-limited-adoption-market-shifts) — Counterpoint
- [Cellular IoT trends for 2026: RedCap, NTN, and eSIM rise](https://www.hologram.io/blog/cellular-iot-trends/) — Hologram(NB-IoT は中国外で減退・Cat.1bis へ)／ [NB-IoT: Is It Here to Stay, or Time to Move On?](https://velosiot.com/blog/nb-iot-is-it-here-to-stay-or-time-to-move-on/) — Velos ／ [A heart-felt break-up? Life beyond NB-IoT](https://monogoto.io/2025/01/13/a-heart-felt-break-up-life-beyond-nb-iot/) — Monogoto, 2025-01-13
- [IoT connections forecast – Ericsson Mobility Report](https://www.ericsson.com/en/reports-and-papers/mobility-report/dataforecasts/iot-connections-outlook) — Ericsson(NB-IoT 177/Cat-M 81 事業者、2030 年 40%)
- [LTE-M & LPWA Network Solutions at AT&T Business](https://www.business.att.com/products/lpwa.html) — AT&T(LTE-M の 5G Massive IoT 継続)

**衛星 NTN**
- [Skylo Newsroom: Voice Gateway for NTN Voice Calling](https://www.skylo.tech/newsroom/skylo-introduces-voice-gateway-for-ntn-voice-calling-on-its-commercial-network) ／ [Skylo × Vodafone IoT](https://www.skylo.tech/newsroom/skylo-partners-with-vodafone-iot-to-bring-ntn-nb-iot-satellite-connectivity-to-customers) ／ [Transatel × Stellar/Skylo/Sateliot](https://www.skylo.tech/newsroom/satnews-transatel-signs-3-strategic-partnerships-with-stellar-skylo-and-sateliot) ／ [o2 Business 衛星 IoT タリフ(EUR 0.70/KB)](https://www.skylo.tech/newsroom/mobile-communications-via-satellite-o2-business-launches-first-tariff-for-satellite-iot) — Skylo Newsroom
- [Globally connected: tariffs for satellite connectivity in the IoT(EUR 0.90/KB)](https://www.telekom.com/en/media/media-information/archive/tariffs-for-satellite-connectivity-1061254) — Deutsche Telekom
- [Blues Notecard for Skylo(USD 0.00075/byte、TN+NTN 統合モジュール)](https://www.cnx-software.com/2026/03/11/blues-notecard-for-skylo-iot-module-offers-5g-ntn-satellite-nb-iot-lte-m-cellular-wifi-and-gnss-connectivity/) — CNX Software, 2026-03-11
- [T-Satellite Is Here: And Now It's Powering Apps!](https://www.t-mobile.com/news/network/t-satellite-data-ready-app-expansion) — T-Mobile Newsroom, 2025-10-01 ／ [Starlink T-Satellite: Cost, Compatible Phones & Coverage (2026)](https://www.satelliteinternet.com/providers/starlink/starlink-direct-to-cell/) — SatelliteInternet.com(650+ 衛星・22 か国)／ [Starlink Direct to Cell Becomes the World's Largest 4G Coverage Provider](https://techafricanews.com/2025/10/08/starlink-direct-to-cell-becomes-the-worlds-largest-4g-coverage-provider/) — TechAfrica News, 2025-10-08(キャリアパートナー一覧)／ [T-Mobile T-Satellite Is Getting a Huge Upgrade](https://5gstore.com/blog/2026/03/07/t-mobile-tsatellite-starlink-v2/) — 5Gstore, 2026-03-07(V2/Starship 計画)

> 注: 本レポートは公開情報のみに基づく。「未確認」「確認不能」と付した項目は一次情報での裏取りができていない。意思決定に用いる前に該当箇所の追加検証(社内出所確認・キャリアへの直接確認)を要する。
