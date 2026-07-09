# グローバル規制・コスト構造の変化: MRC / Permanent Roaming / Data Localization — 2026-07-09

> 作成: market-scout ／ 作成日: 2026-07-09 ／ テーマ: コネクティビティ・ロードマップ議論向けテーマ特化調査(T1)
> 対象期間: 2024〜2026(構造理解に必要な過去経緯を含む)／ 本レポートは公開情報のみに基づく参考情報であり、規制の確定解釈は Legal / IS&CorpIT / 外部アドバイザーの確認を要する。

## TL;DR(経営向け)

- **「在圏コストほぼゼロ」時代の終焉は公開情報からも方向として支持**。IoT ローミング機器の 70% は月 2MB 未満・売上 EUR 0.01 未満(MACH)であり、MNO は従量課金からデバイス単位(per-IMSI)課金・BCE 精算へ移行中。ただし**個別 MNO の MRC 料率・導入率の網羅的な公開データは存在せず**、ブリーフィングの「Kaleido 34%」「10-30 セント/月」は公開情報では確認不能(矛盾する証拠もない)。
- **規制の主戦場が「恒久ローミング禁止」から「eSIM プロビジョニングの国内化」へ拡大**。トルコ(BTK、2025-07 に海外 eSIM 事業者 30 社超をブロック・プロファイルデータ国内保管義務)、インドネシア(Permen Komdigi 7/2025 で eSIM/IoT/M2M のローカル IMSI 管理を明文化)が先行。ロシアも 2026-06 に M2M SIM 規制案が浮上。
- **Kaleido/floLIVE 調査(2025-09)では「規制コンプライアンス」が IoT 接続事業者の課題 #1**(回答者の 59% がトップ 3 に選択)、「ローミング SIM が今後も有効」と考える事業者はわずか 2%、78% が Local Breakout を重視。業界はマルチ IMSI ローミングから「eSIM ローカルプロファイル+LBO+現地免許」への移行で一致。
- **帰結**: ローカルプロファイル供給網(SGP.32/eIM)、LBO/ローカルコア、規制対応済み現地法人・免許が「値上がりする資産」。回線再販だけのグローバル SIM 事業は売上フロア(MRC)とコンプライアンスコストの二重圧力で構造的に不利になる。

## 1. 主要ファインディング(出典付き)

### 1.1 MRC(per-IMSI 月額課金)— 公開情報で分かること・分からないこと

**構造的ドライバー(確認済み)**
- IoT ローミング機器の 70% は月 2MB 未満しか使わず、発生させる卸売上は月 EUR 0.01 未満。従量(TAP)精算では管理コスト割れするため、オペレーターは「IMSI 月額課金」から発展した device-based charging(IMSI 単位の月額・日額・ミニマムコミット、IMSI セグメント単位課金、シグナリング課金)を模索している。[IoT Roaming – How Do Operators Reap the Benefits?](https://mach.com/mach-insights/iot-roaming-how-do-operators-reap-the-benefits) — MACH Insights(閲覧 2026-07-09)
- Kaleido Intelligence は、BCE(Billing & Charging Evolution)により低帯域の恒久ローミング IoT デバイスを収益化でき、2026 年までに USD 20 億超の未開拓卸収益が生まれると試算。[6 Reasons MNOs Need BCE Roaming Settlements](https://www.csgi.com/insights/six-reasons-mobile-network-operators-need-bce-roaming-settlements/) — CSG(Kaleido 引用)
- Kaleido の Wholesale Roaming 2026 MNO Survey(Tier1/2 の MNO 68 社)では、音声・SMS 卸収益は 2026-2030 に 70% 超減少見込み、データが唯一の成長源。インバウンドデータは 96% が「増加または横ばい」を見込む — インバウンド IoT トラフィックの収益化圧力は強まる方向。[Kaleido: eSIM and AI Reshape Global Wholesale Roaming](https://www.thefastmode.com/technology-and-solution-trends/49382-kaleido-esim-and-ai-reshape-global-wholesale-roaming-market-operator-strategies) — The Fast Mode, 2026-07-01

**導入率・料率(確認不能な点)**
- 「MNO の約 1/3 が per-IMSI MRC 導入(Kaleido 34%)」に一致する公開統計は今回発見できず。公開資料で確認できた「34%」は「2028 年までに卸ローミング精算の 34% が BCE へ移行」という**別文脈の数値**([The Fast Mode 前掲]、Kaleido 引用)。該当統計はペイウォール内レポート([Monetising IoT Wholesale Roaming 2024](https://kaleidointelligence.com/product/monetising-iot-wholesale-roaming-2024-kaleido-insights/))に存在する可能性があり、原典確認を推奨。
- 卸の per-IMSI 料率は NDA 下にあり非公開。**小売側の状況証拠**として、Things Mobile はネットワークアクセス料 EUR 0.25/月(UK EE は USD 0.30 相当)を「SIM がそのオペレーター網に接続した月」に課金([Things Mobile pricing](https://www.thingsmobile.com/private/plans/pay-per-use-rate))、Onomondo は USD 0.33/SIM/月、Hologram USD 1/月、Telnyx USD 2/月([各社料金ページ、iot.cards まとめ](https://iot.cards/en/landings/iot-roaming))。卸 MRC が「数十セント/月」レンジという相場観と整合的だが、直接の裏付けではない。

**個別 MNO のポリシー(公開されているもの)**
- **Telstra(豪)**: 公式の「Permanent inbound roaming policy」で恒久インバウンドローミングを「サポートしない」と明記。定義は「12 か月中 6 か月以上在圏」または「単一アカウント/APN で 500 台以上」。60 日前通知で切断可、**5,000 台超は即時切断+商務条件合意まで再接続禁止**。料率は非公開(個別協議)。[Telstra Permanent Inbound Roaming Policy](https://www.telstra.com.au/business-enterprise/support/permanent-inbound-roaming-policy) — Telstra(閲覧 2026-07-09)
- **Verizon(米)**: Global IoT Roaming の約款で「3 か月連続でトラフィックの 60% 以上が Roaming Region 外なら恒久在圏とみなす」→ 是正非協力なら**回線解約**。MRC 徴収ではなく排除型。[Verizon Global IoT Roaming service guide](https://www.verizon.com/business/service_guide/reg/Global_IoT_Roaming.pdf) — Verizon
- **Vodafone**: グループとして per-IMSI MRC を課している/いないの公開情報はなし(確認不能)。ただし Vodafone はインバウンド IoT ローミング収益で世界首位(Juniper Research 2023 ランキング 1 位)であり、Global SIM+(ローミング SIM を GDSP 経由で現地プロファイルに転換)で「ブロックせず収益化する」立場。ブリーフィングの「大手で唯一の例外」と整合的な状況証拠。[Vodafone holds onto its IoT roaming crown](https://www.mobileeurope.co.uk/vodafone-holds-onto-its-iot-roaming-crown-for-now/) — Mobile Europe, 2023-09-11 ／ [A global solution for multi-country IoT deployments](https://www.vodafone.com/news/newsroom/technology/a-global-solution-for-multi-country-io-t-deployments) — Vodafone
- DT・Telefónica・Three・Telia・TIM・T-Mobile US・Rogers・Claro・SoftBank・ドコモの per-IMSI 卸課金は**いずれも公開情報なし(確認不能)**。米では AT&T/T-Mobile が恒久利用を監視し数週間で排除しうるとの業界記述([iot.cards](https://iot.cards/en/resources/blog/roaming-permanente)、2026-04)。日本キャリアのインバウンド IoT ローミング課金も公開情報なし。

### 1.2 Permanent Roaming 規制 — 国別最新状況(2025〜2026)

| 国/地域 | 状況(2026-07 時点) | 根拠・出典 |
|---|---|---|
| ブラジル | **禁止(米州で唯一の明示禁止)**。Anatel は 2025 年に長年の禁止方針を再確認。実務上の許容は連続 90 日程度、超過で遮断リスク。ローカル SIM または国内でダウンロードした eUICC プロファイルが必要。背景は 2012 年来の税・規制の不均衡論。 | [Cullen International 2026-02](https://www.cullen-international.com/news/2026/02/IoT-regulation-in-the-Americas-diverges-on-roaming--authorisation-and-SIM-registration.html) ／ [Cullen 2025-01](https://www.cullen-international.com/news/2025/01/Brazil-applies-tougher-rules-for-IoT-than-other-countries-in-the-Americas.html) ／ [1oT blog](https://www.1ot.com/blog/overcoming-roaming-restrictions-in-brazil-with-1ot-esim) |
| トルコ | **禁止+eSIM 国内化**。BTK は 2019 年規制を 2025 年に全面執行。2025-07-10 に Airalo/Holafly 等の海外 eSIM 事業者(報道により 8〜30 社超)のサイト/アプリをブロック。RSP(リモート SIM プロビジョニング)はトルコ事業者経由に限定、**プロファイルデータの国内保管義務**。外国端末 IMEI は 120 日以内登録、未登録はブラックリスト化。 | [floLIVE: Understanding Turkey's eSIM Ban](https://flolive.net/blog/understanding-turkeys-esim-ban-what-btks-2025-regulation-means-for-global-providers-and-iot-deployments/) — 2025 ／ [Holafly news](https://esim.holafly.com/news/esim-ban-turkey/) ／ [yesim.app](https://yesim.app/blog/esim-ban-turkey/) |
| インド | **恒久ローミング不可(IoT)**。恒久稼働には DoT 認可の M2MSP 登録+KYC が必要、外国 SIM はトランジット/短期パイロットのみ。TRAI 勧告(2024-03-21)は外国 eUICC 搭載輸入機器の**インドプロファイルへの 3 年以内転換**の維持を勧告(**DoT の実装は未了**)。2025-07 に外国 SIM/eSIM 規制の追加コンサルテーション、2026-01 に「輸出向け M2M 機器への外国 SIM 組込み」に軽量な別枠認可を勧告。根拠はセキュリティ(合法的傍受)・KYC・内外事業者の対等競争。 | [TRAI Recommendations 2024-03-21](https://www.trai.gov.in/sites/default/files/2024-09/Recommendations_21032024_0.pdf) ／ [Medianama 2025-07](https://www.medianama.com/2025/07/223-trai-consultation-foreign-sim-esim-regulation-indian-policy-explained/) ／ [Medianama 2026-01](https://www.medianama.com/2026/01/223-explained-trai-separate-regulation-framework-foreign-sim-cards-esim-cards/) ／ [iot.cards 2026-04](https://iot.cards/en/resources/blog/roaming-permanente) |
| インドネシア | **eSIM/IoT/M2M の法制明文化が進行**。Permen Komdigi(通信デジタル省令)No. 7/2025(2025-04-10 施行)が GSMA 仕様に整合する eSIM プロビジョニングの正式枠組みを規定: 事業者は**ローカル IMSI/MSISDN を管理するプロビジョニングシステム**の提供義務、第三者プロビジョニングは PSE(電子システム運営者)登録+データセキュリティ認証が必須、IoT/M2M 専用番号帯を導入。 | [Legal Centric summary of Reg 7/2025](https://legalcentric.com/content/view/199373) ／ [Jakarta Post 2025-04-15](https://www.thejakartapost.com/indonesia/2025/04/15/govt-pushes-for-esim-adoption-through-new-regulation.html) ／ [原文(JDIH Komdigi)](https://jdih.komdigi.go.id/produk_hukum/unduh/id/964/t/peraturan+menteri+komunikasi+dan+digital+nomor+7+tahun+2025) |
| 中東 | サウジ(CST): **2020 年から恒久ローミング禁止**、ローカルパートナー必須、M2M 専用番号帯の使用義務、厳格な本人確認。カタール(CRA): 2025 年に方針明確化、**二国間合意なき場合 90 日制限**の枠組みを示唆。UAE(TDRA): 登録済みローカル SIM での稼働要求。域内 9 法域で規制は不均一だが監視強化方向。 | [Cullen International 2026-03](https://www.cullen-international.com/news/2026/03/Middle-East-tightens-oversight-of-IoT-connectivity-as-roaming-and-licensing-frameworks-evolve.html) ／ [iot.cards 2026-04](https://iot.cards/en/resources/blog/roaming-permanente) ／ [Access Partnership: Saudi IoT Regulations](https://accesspartnership.com/opinion/access-alert-introducing-saudi-arabias-updated-iot-regulations/) |
| ロシア | **2025-10-06 から外国 SIM のデータ/SMS を網登録から 24 時間ブロック**(2025-11-21 から本人確認で解除可)。名目はドローン遠隔操作等のセキュリティ対策。**2026-06-23 報道(Kommersant/Meduza)**: M2M SIM を独立カテゴリ化し追加本人確認・音声/SMS 禁止・国外での eSIM 登録禁止を検討中(ロシアの SIM の約 20% が M2M、2025-08 時点)。 | [RCC 2025-10](https://en.rcc.org.ru/events-copy/sobytiya-copy_1288.html) ／ [Meduza 2026-06-23](https://meduza.io/amp/en/news/2026/06/23/kommersant-russia-mulls-tighter-controls-on-iot-sim-cards-and-a-ban-on-registering-esims-from-abroad)(**規制案は未確定**) |
| 中国 | 生産用途の M2M 恒久ローミングは技術的に不成立(パイロットのみ黙認)。中国 3 キャリアとのローカル契約が必要。 | [iot.cards 2026-04](https://iot.cards/en/resources/blog/roaming-permanente) |
| 豪州 | **規制上の禁止はなし**。Telstra が商務ポリシーで実質排除(前掲 1.1)。 | [Telstra policy](https://www.telstra.com.au/business-enterprise/support/permanent-inbound-roaming-policy) ／ [iot.cards](https://iot.cards/en/resources/blog/roaming-permanente) |
| カナダ | **規制上の禁止はなし**(契約ベースでキャリアが制限)。Rogers/Telus の明文公開ポリシーは発見できず。傍証: KORE はカナダで native TELUS プロファイル(KTELUS)を使い恒久ローミング制約を回避。CRTC 2024-238 はエンタープライズ/IoT 市場が全国 3 キャリアに高度集中と認定。 | [Cullen 2026-02](https://www.cullen-international.com/news/2026/02/IoT-regulation-in-the-Americas-diverges-on-roaming--authorisation-and-SIM-registration.html) ／ [KORE Local Carrier SIMs](https://www.korewireless.com/local-carrier-sims/) ／ [CRTC 2024-238](https://crtc.gc.ca/eng/archive/2024/2024-238.htm) |
| 米国 | 連邦レベルの禁止なし。キャリアが契約で制限(Verizon 60%/3 か月ルール前掲、AT&T/T-Mobile は監視・排除の業界記述)。 | [Verizon service guide](https://www.verizon.com/business/service_guide/reg/Global_IoT_Roaming.pdf) ／ [iot.cards](https://iot.cards/en/resources/blog/roaming-permanente) |
| EU/EEA | 容認(Regulation (EU) 531/2012 系、フェアユース前提)。 | [iot.cards 2026-04](https://iot.cards/en/resources/blog/roaming-permanente) |

規制根拠の類型: ①税・規制の対等性(ブラジル)②データ主権・国内保管(トルコ、サウジ、UAE)③合法的傍受・KYC・安全保障(インド、ロシア、サウジ)④番号資源・ネットワーク管理(サウジ M2M 番号帯、インドネシア専用番号帯)。

### 1.3 データローカライゼーション — IoT 接続事業者の実務への影響

- **EU**: Data Act が 2025-09-12 から適用(コネクテッド製品データのユーザーアクセス権・共有義務・クラウドスイッチング容易化。設計義務は 2026-09-12 から)。GDPR・AI Act と合わせ、IoT データの保管場所・移転・アクセス権が製品設計要件になった。[European Commission: Data Act](https://digital-strategy.ec.europa.eu/en/policies/data-act) ／ [Skadden 2025-06](https://www.skadden.com/insights/publications/2025/06/eu-data-act)
- **UK**: 2025-10 更新の National Data Strategy が「データインフラ主権」を明記。Procurement Act 2023 下の National Procurement Policy Statement(2025-02 発効)がサプライチェーン/国家安全保障リスク管理を調達要件化、G-Cloud 15(2026 秋予定)では Cyber Essentials Plus が必須要件に。公共案件(スマートメーター等)はデータ所在地+法的管轄の双方が問われる方向。[Civo: UK Sovereign Cloud 2026](https://www.civo.com/blog/public-sector-uk-sovereign-cloud-compliance-2026) ／ [techUK](https://www.techuk.org/resource/from-data-residency-to-decision-rights-what-the-uk-actually-needs-from-digital-sovereignty.html)
- **米国**: 2026 年時点で**包括的州プライバシー法が 20 州で施行**(制定ベースでは 24 州)。連邦法不在のまま州法パッチワークが拡大し、コンプライアンスは事実上「最厳州基準」に収斂。政府調達では FedRAMP 認証がクラウド/IoT サービスの参入条件。[MultiState 2026-02-04](https://www.multistate.us/insider/2026/2/4/all-of-the-comprehensive-privacy-laws-that-take-effect-in-2026) ／ [Byte Back 2026-06](https://www.bytebacklaw.com/2026/06/u-s-state-privacy-law-landscape-expands-to-24-states-what-the-latest-legislative-wave-means-for-businesses/)
- **中国**: データ安全法/PIPL 体制は維持しつつ、CAC「データ越境流動の促進・規範化規定」(2024-03-22)で越境移転を一部緩和(重要データ+個人情報のみ規制、2025-04-09 の CAC FAQ で明確化)。自由貿易試験区のネガティブリスト(北京 2024-08: 自動車等)がコネクテッドカーの実務基準。[Library of Congress 2024-05-13](https://www.loc.gov/item/global-legal-monitor/2024-05-13/china-new-rules-on-cross-border-data-transfers-released/) ／ [Arnold & Porter 2025-06](https://www.arnoldporter.com/en/perspectives/advisories/2025/06/china-clarifies-cross-border-data-transfer-rules)
- **インド**: DPDP Rules 2025 が 2025-11-13/14 に告示。越境移転はネガティブリスト方式(2026-05 時点で制限国リストなし)だが、**Significant Data Fiduciary には政府指定カテゴリのデータの国内保持義務を課しうる**条項が残る(内容未確定 = 将来のローカライゼーションリスク)。[India Briefing](https://www.india-briefing.com/news/dpdp-rules-2025-india-data-protection-law-compliance-40769.html/) ／ [PIB 2025-11-14](https://www.pib.gov.in/PressReleasePage.aspx?PRID=2190014&reg=3&lang=2)
- **ベトナム**: 個人データ保護法(Law 91/2025/QH15、2025-06-26 成立)が 2026-01-01 施行、越境移転違反に**売上高の最大 5% の制裁金**。Decree 53/2022 は通信・ネットサービスのユーザーデータ国内保存を義務化(外国事業者は公安省要請から 12 か月以内に国内保存+拠点設置、最低 24 か月保持)。[DFDL 2026](https://www.dfdl.com/insights/legal-and-tax-updates/vietnam-personal-data-protection-2026-what-foreign-organizations-need-to-know/) ／ [Freshfields: Decree 53](https://technologyquotient.freshfields.com/post/102iulg/data-localisation-in-vietnam-highlights-under-decree-53-and-decree-13)
- **サウジ**: CST の IoT 規制フレームワークは **IoT サービス提供に用いる全サーバー・網構成要素・データホストの国内設置**を要求。NDMO/SDAIA 基準は機微・政府データのオンショア保持を原則化(ECC-2 で一部緩和も SAMA 等セクター規制は国内保持を要求)。[Baker McKenzie: KSA data localization](https://resourcehub.bakermckenzie.com/en/resources/global-data-and-cyber-handbook/emea/saudi-arabia/topics/data-localization-and-regulation-of-non-personal-data) ／ [trade.gov](https://www.trade.gov/market-intelligence/saudi-arabia-ict-cross-border-data-transfer-rules-now-under-enforcement)
- **UAE**: IoT Regulatory Policy(2018-03-22)が secret/sensitive/confidential 区分データの UAE 内(または同等保護国)保管を義務化。医療データは完全オンショア。[Clifford Chance 2025-03](https://www.cliffordchance.com/insights/resources/blogs/talking-tech/en/articles/2025/03/doing-business-in-the-middle-east--data-transfers-in-the-uae-and-ksa.html)
- **ブラジル**: LGPD の越境移転規則(ANPD Resolution CD/ANPD 19/2024、2024-08)の SCC 移行猶予が **2025-08-23 に満了**。以降、SCC 等の承認メカニズムなしの越境移転は違法。十分性認定はまだゼロ。[Mayer Brown 2025-08](https://www.mayerbrown.com/en/insights/publications/2025/08/end-of-grace-period-implementation-of-brazils-standard-contractual-clauses-in-international-transfers-of-personal-data)
- **業界への総合的影響**: Kaleido/floLIVE の 2025 年 IoT コネクティビティ調査(回答 200 超)で「規制コンプライアンス」が課題 #1(59% がトップ 3 に選択、コスト・セキュリティより上位)、**78% が Local/Regional Breakout を「非常に/極めて重要」**と回答。LBO・ローカルコア・ソブリンクラウドは「性能要件」から「参入要件」に変わった。[floLIVE/Kaleido 2025-09-03](https://flolive.net/blog/kaleido-intelligence-report-finds-regulatory-compliance-to-be-1-connectivity-challenge-for-iot-providers/)

## 2. 競合・プレイヤー動向(公開されている対応策)

| プレイヤー | 対応アーキテクチャ | 出典 |
|---|---|---|
| Vodafone | Global SIM+: ローミング SIM を GDSP 経由で現地プロファイルへ OTA 転換(単一契約・単一 SKU で「規制があればローカル化」)。約款で規制国での恒久ローミングを禁止。 | [Vodafone](https://www.vodafone.com/news/newsroom/technology/a-global-solution-for-multi-country-io-t-deployments) ／ [Fierce Network](https://www.fierce-network.com/wireless/vodafone-iot-data-sovereignty-around-globe) |
| floLIVE | ローカルコア+LBO を各国設置する「ハイパーローカル」網。トルコ規制対応(現地プロファイル自動切替+国内データ保管)を明示的に商品化。規制対応を最大の差別化軸に据える。 | [floLIVE 2025](https://flolive.net/blog/understanding-turkeys-esim-ban-what-btks-2025-regulation-means-for-global-providers-and-iot-deployments/) |
| 1NCE | ブラジルで **Anatel のフル MVNO 免許を取得**し、サンパウロ拠点・現地課金/税務/物流を整備(Brazil+、マルチ IMSI)。eUICC「Freedom to Switch」で規制国はローカルプロファイルに切替。 | [1NCE Brazil+](https://www.1nce.com/en-us/1nce-connect/coverage/brazil-plus) |
| Wireless Logic | 自社コア Conexa+オペレーター契約 50 超/750 網。SGP.02/22/32 とマルチ IMSI を全部持ち「国ごとに最適な localisation」を提供(soft localisation = ローカル IMSI、hard localisation = 現地 SIM)。 | [Wireless Logic blog](https://wirelesslogic.com/blog/overcome-iots-permanent-roaming-challenge-with-remote-sim-provisioning) |
| Eseye | AnyNet Federation に **Verizon を追加(米国内で OTA ローカライズ)**。ブートストラップ+現地プロファイル DL の「federated localization」構想。 | [IoT For All](https://www.iotforall.com/news/eseye-partners-with-verizon-to) ／ [Eseye](https://www.eseye.com/resources/blogs/federated-localization-revolutionizing-global-iot/) |
| KORE | 規制/商務制約市場向けに「Local Carrier SIMs」(例: カナダの native TELUS プロファイル KTELUS)を提供。 | [KORE](https://www.korewireless.com/local-carrier-sims/) |
| Onomondo | 単一プロファイル+自社コアの「グローバル MVNO」路線を維持しつつ、プロファイルローテーションによる規制回避を「bad faith」と批判(= 業界がローカルプロファイル正攻法へ移る論拠)。SoftSIM も提示。 | [Onomondo blog](https://onomondo.com/blog/iots-struggle-with-permanent-roaming-and-potential-solutions/) |
| 1oT | ブラジル向けに現地プロファイル DL 型 eSIM を商品化(90 日制限の回避を明示)。 | [1oT blog](https://www.1ot.com/blog/overcoming-roaming-restrictions-in-brazil-with-1ot-esim) |

**構造変化の読み**: ①「マルチ IMSI ローミング」は過渡期技術となり、eSIM(SGP.32)ローカルプロファイル+LBO が本流(Kaleido 調査で「ローミング SIM 有効」2% が示す通り)。②規制対応は「回避技術」から「現地免許・現地法人・現地インフラ」という資本・時間のかかる資産に移行 — 1NCE のブラジル免許取得、floLIVE のローカルコア網がその先行例。③この資産は後発が 18 か月以内に自力構築しにくく、M&A/提携の対象価値が上がる。

## 3. ブリーフィング主張の裏取り結果(C 表 T1 担当分)

| # | 主張 | 判定 | 根拠 |
|---|---|---|---|
| 1 | MRC 導入 MNO 約 1/3(Kaleido 34%) | **確認不能** | 一致する公開統計なし。公開資料の「34%」は「2028 年までに卸精算の 34% が BCE 移行」という別文脈([The Fast Mode 2026-07-01](https://www.thefastmode.com/technology-and-solution-trends/49382-kaleido-esim-and-ai-reshape-global-wholesale-roaming-market-operator-strategies))。該当数値はペイウォール内([Kaleido Monetising IoT Wholesale Roaming 2024](https://kaleidointelligence.com/product/monetising-iot-wholesale-roaming-2024-kaleido-insights/))の可能性大。**矛盾する証拠もなし**。原典レポートの購読確認を推奨 |
| 2 | MRC 相場 10-30 セント/月 | **確認不能(整合的)** | 卸料率は非公開。小売の per-network アクセス料 EUR 0.25-0.30/月([Things Mobile](https://www.thingsmobile.com/private/plans/pay-per-use-rate))、USD 0.33/SIM/月(Onomondo)等はレンジと整合。矛盾する公開証拠なし |
| 3 | Vodafone は大手で唯一 MRC 非導入 | **確認不能(状況証拠は整合)** | 各社とも卸課金は非公開のため直接比較不能。Vodafone がインバウンド IoT ローミング収益世界一([Mobile Europe 2023-09-11](https://www.mobileeurope.co.uk/vodafone-holds-onto-its-iot-roaming-crown-for-now/))で「排除でなく収益化」戦略(Global SIM+)である点は主張と整合 |
| 4 | インドネシアで法施行(ローカルプロファイル管理の明文化含む) | **支持** | Permen Komdigi No. 7/2025(2025-04-10)が eSIM/IoT/M2M プロビジョニングを法制化。ローカル IMSI/MSISDN 管理義務・PSE 登録・専用番号帯([Legal Centric](https://legalcentric.com/content/view/199373)、[Jakarta Post 2025-04-15](https://www.thejakartapost.com/indonesia/2025/04/15/govt-pushes-for-esim-adoption-through-new-regulation.html))。※SGP.02/22/32 の個別引用の有無は省令原文の逐条確認が未了 |
| 5 | インドで法施行が始まりつつある(3 年ルール) | **部分支持** | 恒久ローミング不可・M2MSP 登録・KYC は現行制度として支持([iot.cards](https://iot.cards/en/resources/blog/roaming-permanente))。ただし「外国 eUICC の 3 年以内国内転換」は TRAI 勧告(2024-03-21)段階で **DoT 実装は未了**([TRAI PDF](https://www.trai.gov.in/sites/default/files/2024-09/Recommendations_21032024_0.pdf))。2026-01 に輸出向け別枠認可の最終勧告([Medianama 2026-01](https://www.medianama.com/2026/01/223-explained-trai-separate-regulation-framework-foreign-sim-cards-esim-cards/))。「施行が始まった」はやや先行表現 |
| 6 | 豪: Telstra が実質排除 | **支持(ただし手段の表現に留保)** | 公式ポリシーで恒久インバウンドローミング不支持・6 か月/500 台定義・5,000 台超即時切断([Telstra](https://www.telstra.com.au/business-enterprise/support/permanent-inbound-roaming-policy))。「**超高額 MRC** で排除」の料金水準は公開情報で確認不能(公式には切断+個別商務協議) |
| 7 | 加: Rogers/Telus が実質排除 | **部分支持/確認不能** | 両社の明文公開ポリシーは発見できず。傍証: 規制禁止はない中で KORE が native TELUS プロファイルを「恒久ローミング制約の回避策」として商品化([KORE](https://www.korewireless.com/local-carrier-sims/))、CRTC 2024-238 が IoT 市場の 3 社集中を認定。実務上ローミング困難という趣旨は業界記述と整合 |
| 8 | ブラジル 90 日・トルコ・サウジ 120 日等の PR 規制 | **概ね支持** | ブラジル 90 日([Cullen 2026-02](https://www.cullen-international.com/news/2026/02/IoT-regulation-in-the-Americas-diverges-on-roaming--authorisation-and-SIM-registration.html) 等)、トルコ禁止+IMEI 120 日([floLIVE](https://flolive.net/blog/understanding-turkeys-esim-ban-what-btks-2025-regulation-means-for-global-providers-and-iot-deployments/))は支持。**サウジ「120 日」の日数**は一次確認できず(確認できたのは 2020 年来の禁止+ローカルパートナー必須。業界記事に 90-120 日でローカル SIM 登録要との記述 — [Cullen 2026-03](https://www.cullen-international.com/news/2026/03/Middle-East-tightens-oversight-of-IoT-connectivity-as-roaming-and-licensing-frameworks-evolve.html)、[webbing](https://webbingsolutions.com/iot-connectivity-regulations/)) |

## 4. SORACOM への戦略的含意

1. **「1 回線あたり売上フロア」の出現は方向として正しい前提に置いてよい**。MNO 側の経済合理性(70% のデバイスが月 EUR 0.01 未満)と BCE 移行が公開情報で裏付けられ、低容量ばらまき型グローバル SIM の粗利は構造的に圧縮される。大容量・高 ARPU シフト、および国内 MNO 接続との二本柱戦略の妥当性を補強する。
2. **規制の重心が「在圏日数」から「プロビジョニング主権」へ**。トルコ・インドネシアは eSIM プロファイルの管理主体・保管場所まで規制し始めた。SGP.32 でプロファイルを切り替えられる能力だけでなく、**国別のローカルプロファイル調達網と国内ホスティング(SM-DP+/eIM の設置国)**が競争条件になる。マルチプロファイル・オーケストレーション型のアーキテクチャには追い風だが、国ごとの供給網整備が前提。
3. **LBO・ローカルコアは「性能オプション」から「参入要件」へ**(Kaleido: 78% が重視)。UK/US に続き、中東・アジア展開では国別 LBO+データ国内保管の提供可否が案件の入口条件になる。
4. **規制対応そのものが商品になる**(コンプライアンス課題 #1、floLIVE/1NCE が規制対応を前面に)。「この国でこの構成なら合法に動く」を製品として保証できる事業者が選ばれる — 単価下落を規制プレミアムで補う余地。
5. **アジア大型案件のリスク管理**: インドは勧告段階(3 年ルール未実装)だが方向は不可逆。インドネシアは省令施行済み。ロシアは M2M SIM 規制案が浮上。展開国別の「規制トリガー(施行日・猶予期限)」を案件パイプラインに紐付けて監視すべき。
6. 注意: 本レポートの規制解釈は市場分析目的の参考情報。個別案件の適法性判断は Legal / IS&CorpIT / 現地アドバイザーに確認のこと。

## 5. インオーガニック(M&A・出資・提携)の含意

- **P1(コネクティビティ深化)— 価値が上がる資産**: ①国別ローカルプロファイル供給網と eIM/SM-DP+ 運用能力(SGP.32)②ローカルコア/LBO 技術。floLIVE(前回 2026-07-06 スキャンでロングリスト提案済み)は本テーマで最も理にかなう資産であり、規制動向はその優先度を**引き上げる**方向。Kigen(提携提案済み)も同様。
- **P4(地理・顧客基盤)— 「規制上の地位」を買う**: ma-thesis の「獲得困難な資産(周波数・規制上の地位)」に該当するのは、規制強化市場のローカル免許・登録・現地法人。具体例: ブラジル(Anatel フル MVNO 免許 — 1NCE は自力取得に至るまで現地拠点整備を要した)、インド(M2MSP 登録+現地 TSP 関係)、インドネシア(PSE 登録プロビジョニング事業者)。**買収は「回線」でなく「免許+現地オペレーション+MNO 関係」の取得**と定義すべき。なお有力候補だったブラジル Arqia は Wireless Logic が 2025-04 に既に買収(前回スキャン記載)— 出遅れの実例。
- **新規候補(deal-desk への提案、pipeline.yaml 重複なし・追加はしない)**:
  | 会社 | 地域 | 分野 | 注目理由 | ピラー | 推奨アクション |
  |---|---|---|---|---|---|
  | Eseye | 英国 | eSIM localization(AnyNet Federation) | Verizon 網への OTA ローカライズ等、MNO 連合型のローカライゼーション IP と顧客基盤。規制テーマで資産価値上昇中 | P1/P4 | 00_sourcing 登録の初期スクリーニング |
  | Webbing | イスラエル | 規制対応特化のグローバル接続(マルチプロファイル eSIM) | 規制コンプライアンスを主戦場とするニッチ。規模的に小型買収〜提携レンジの可能性 | P1 | 状況調査(規模・顧客・技術の把握) |
  | 1oT | エストニア | eSIM 管理・規制国対応(ブラジル等) | 独立系で SGP.32/現地プロファイル対応を商品化。小規模でスクリーニングコスト低 | P1/P5 | 状況調査 |
- **提携(Partner)を先行すべき領域**: 規制国のローカルプロファイル供給は、買収より「国別に複数 MNO/アグリゲーターと契約を束ねる」方が資本効率が良いケースが多い(Build/Buy/Partner 枠組みでは Partner 優位)。買収が正当化されるのは、①供給契約が排他化し始めた国 ②eIM/オーケストレーション技術と顧客基盤が一体で手に入る場合。
- **相場観**: 本テーマでの新規バリュエーション事実は今回なし(MRC はディールでなくコスト構造の話)。規制対応資産のプレミアムは、KORE 非公開化(EV/売上 ~2.5x)等の既存アンカーに対する上乗せ要因として今後観測する。

## 6. 未解決の問い

1. Kaleido「34%」の原典特定 — どのレポートの何の分母か(MRC 導入率か BCE 移行率か)。レポート購読または Kaleido への直接照会で解消可能。
2. 主要 MNO グループ(DT/Telefónica/Telia/TIM/Three/T-Mobile/Rogers/Claro/SB/ドコモ)の per-IMSI 課金の実勢料率と適用条件 — 公開情報では取得不能。業界カンファレンス・卸交渉の場でのヒアリング事項。
3. インド DoT が TRAI 勧告(3 年転換・輸出向け認可)をいつ・どの形で法制化するか。進行中のアジア案件の前提に直結。
4. インドネシア Permen Komdigi 7/2025 の逐条(SM-DP+ の国内設置義務の有無、SGP.02/22/32 の引用箇所、経過措置)— 省令原文の法務確認が必要。
5. ロシアの M2M SIM 規制案(2026-06 報道)の帰趨 — 成立すれば外国 eSIM 登録禁止まで踏み込む可能性(未確定)。
6. カタール CRA の 90 日枠組みの正式規則化時期と、サウジ CST の「120 日」の一次規則上の根拠。

## 情報源一覧(主要)

**MRC・卸ローミング経済**
- [IoT Roaming – How Do Operators Reap the Benefits?](https://mach.com/mach-insights/iot-roaming-how-do-operators-reap-the-benefits) — MACH Insights(閲覧 2026-07-09)
- [Kaleido: eSIM and AI Reshape Global Wholesale Roaming Market & Operator Strategies](https://www.thefastmode.com/technology-and-solution-trends/49382-kaleido-esim-and-ai-reshape-global-wholesale-roaming-market-operator-strategies) — The Fast Mode, 2026-07-01
- [6 Reasons MNOs Need BCE Roaming Settlements](https://www.csgi.com/insights/six-reasons-mobile-network-operators-need-bce-roaming-settlements/) — CSG(Kaleido 引用)
- [Monetising IoT Wholesale Roaming in 2024](https://kaleidointelligence.com/product/monetising-iot-wholesale-roaming-2024-kaleido-insights/) — Kaleido Intelligence(ペイウォール)
- [Global IoT Connectivity Report 2025(規制コンプライアンス #1)](https://flolive.net/blog/kaleido-intelligence-report-finds-regulatory-compliance-to-be-1-connectivity-challenge-for-iot-providers/) — floLIVE/Kaleido, 2025-09-03
- [Things Mobile 料金(ネットワークアクセス料 EUR 0.25/月)](https://www.thingsmobile.com/private/plans/pay-per-use-rate) ／ [iot.cards: IoT roaming](https://iot.cards/en/landings/iot-roaming)
- [Vodafone holds onto its IoT roaming crown](https://www.mobileeurope.co.uk/vodafone-holds-onto-its-iot-roaming-crown-for-now/) — Mobile Europe, 2023-09-11

**Permanent Roaming 規制**
- [Telstra Permanent Inbound Roaming Policy](https://www.telstra.com.au/business-enterprise/support/permanent-inbound-roaming-policy) — Telstra
- [Verizon Global IoT Roaming service guide](https://www.verizon.com/business/service_guide/reg/Global_IoT_Roaming.pdf) — Verizon
- [IoT regulation in the Americas diverges…](https://www.cullen-international.com/news/2026/02/IoT-regulation-in-the-Americas-diverges-on-roaming--authorisation-and-SIM-registration.html) — Cullen International, 2026-02 ／ [Brazil applies tougher rules…](https://www.cullen-international.com/news/2025/01/Brazil-applies-tougher-rules-for-IoT-than-other-countries-in-the-Americas.html) — 2025-01
- [Middle East tightens oversight of IoT connectivity](https://www.cullen-international.com/news/2026/03/Middle-East-tightens-oversight-of-IoT-connectivity-as-roaming-and-licensing-frameworks-evolve.html) — Cullen International, 2026-03
- [Permanent roaming in IoT: what's allowed and what isn't in 2026](https://iot.cards/en/resources/blog/roaming-permanente) — iot.cards, 2026-04
- [Understanding Turkey's eSIM Ban(BTK 2025)](https://flolive.net/blog/understanding-turkeys-esim-ban-what-btks-2025-regulation-means-for-global-providers-and-iot-deployments/) — floLIVE ／ [Holafly: Turkey bans global eSIM providers](https://esim.holafly.com/news/esim-ban-turkey/)
- [TRAI Recommendations on M2M(2024-03-21)](https://www.trai.gov.in/sites/default/files/2024-09/Recommendations_21032024_0.pdf) ／ [Medianama: TRAI consultation(2025-07)](https://www.medianama.com/2025/07/223-trai-consultation-foreign-sim-esim-regulation-indian-policy-explained/) ／ [Medianama: TRAI final recommendations(2026-01)](https://www.medianama.com/2026/01/223-explained-trai-separate-regulation-framework-foreign-sim-cards-esim-cards/)
- [Permen Komdigi No. 7/2025 原文](https://jdih.komdigi.go.id/produk_hukum/unduh/id/964/t/peraturan+menteri+komunikasi+dan+digital+nomor+7+tahun+2025) ／ [Legal Centric 要約](https://legalcentric.com/content/view/199373) ／ [Jakarta Post 2025-04-15](https://www.thejakartapost.com/indonesia/2025/04/15/govt-pushes-for-esim-adoption-through-new-regulation.html)
- [RCC: ロシアの外国 SIM 24 時間ブロック(2025-10)](https://en.rcc.org.ru/events-copy/sobytiya-copy_1288.html) ／ [Meduza: M2M SIM 規制案(2026-06-23)](https://meduza.io/amp/en/news/2026/06/23/kommersant-russia-mulls-tighter-controls-on-iot-sim-cards-and-a-ban-on-registering-esims-from-abroad)
- [CRTC Telecom Decision 2024-238](https://crtc.gc.ca/eng/archive/2024/2024-238.htm)

**データローカライゼーション**
- [EU Data Act(European Commission)](https://digital-strategy.ec.europa.eu/en/policies/data-act) ／ [Skadden 2025-06](https://www.skadden.com/insights/publications/2025/06/eu-data-act)
- [Civo: UK Sovereign Cloud compliance 2026](https://www.civo.com/blog/public-sector-uk-sovereign-cloud-compliance-2026) ／ [techUK: digital sovereignty](https://www.techuk.org/resource/from-data-residency-to-decision-rights-what-the-uk-actually-needs-from-digital-sovereignty.html)
- [MultiState: 20 State Privacy Laws in Effect in 2026](https://www.multistate.us/insider/2026/2/4/all-of-the-comprehensive-privacy-laws-that-take-effect-in-2026) ／ [Byte Back 2026-06](https://www.bytebacklaw.com/2026/06/u-s-state-privacy-law-landscape-expands-to-24-states-what-the-latest-legislative-wave-means-for-businesses/)
- [Library of Congress: China CBDT rules(2024-05-13)](https://www.loc.gov/item/global-legal-monitor/2024-05-13/china-new-rules-on-cross-border-data-transfers-released/) ／ [Arnold & Porter 2025-06](https://www.arnoldporter.com/en/perspectives/advisories/2025/06/china-clarifies-cross-border-data-transfer-rules)
- [India Briefing: DPDP Rules 2025](https://www.india-briefing.com/news/dpdp-rules-2025-india-data-protection-law-compliance-40769.html/) ／ [PIB 2025-11-14](https://www.pib.gov.in/PressReleasePage.aspx?PRID=2190014&reg=3&lang=2)
- [DFDL: Vietnam PDP 2026](https://www.dfdl.com/insights/legal-and-tax-updates/vietnam-personal-data-protection-2026-what-foreign-organizations-need-to-know/) ／ [Freshfields: Decree 53/13](https://technologyquotient.freshfields.com/post/102iulg/data-localisation-in-vietnam-highlights-under-decree-53-and-decree-13)
- [Baker McKenzie: KSA data localization](https://resourcehub.bakermckenzie.com/en/resources/global-data-and-cyber-handbook/emea/saudi-arabia/topics/data-localization-and-regulation-of-non-personal-data) ／ [trade.gov: KSA ICT cross-border rules](https://www.trade.gov/market-intelligence/saudi-arabia-ict-cross-border-data-transfer-rules-now-under-enforcement) ／ [Clifford Chance: UAE/KSA transfers(2025-03)](https://www.cliffordchance.com/insights/resources/blogs/talking-tech/en/articles/2025/03/doing-business-in-the-middle-east--data-transfers-in-the-uae-and-ksa.html)
- [Mayer Brown: Brazil SCC grace period end(2025-08)](https://www.mayerbrown.com/en/insights/publications/2025/08/end-of-grace-period-implementation-of-brazils-standard-contractual-clauses-in-international-transfers-of-personal-data)

**プレイヤー対応策**
- [Vodafone Global SIM+](https://www.vodafone.com/news/newsroom/technology/a-global-solution-for-multi-country-io-t-deployments) ／ [Fierce Network: Vodafone data sovereignty](https://www.fierce-network.com/wireless/vodafone-iot-data-sovereignty-around-globe)
- [1NCE Brazil+](https://www.1nce.com/en-us/1nce-connect/coverage/brazil-plus) ／ [Wireless Logic: RSP と恒久ローミング](https://wirelesslogic.com/blog/overcome-iots-permanent-roaming-challenge-with-remote-sim-provisioning) ／ [Eseye×Verizon(IoT For All)](https://www.iotforall.com/news/eseye-partners-with-verizon-to) ／ [KORE Local Carrier SIMs](https://www.korewireless.com/local-carrier-sims/) ／ [Onomondo blog](https://onomondo.com/blog/iots-struggle-with-permanent-roaming-and-potential-solutions/) ／ [1oT: Brazil eSIM](https://www.1ot.com/blog/overcoming-roaming-restrictions-in-brazil-with-1ot-esim) ／ [Webbing: IoT connectivity regulations](https://webbingsolutions.com/iot-connectivity-regulations/)

> 注: 「確認不能」と付した項目は公開情報での裏取りができていない。意思決定に用いる前に一次レポート購読・専門家照会・deal-desk での追加検証を要する。外部向け文書化の際は必ず人間レビューを経ること。
