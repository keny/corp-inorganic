# グローバル IoT MVNO / CMP 業界の再編・M&A・バリュエーション動向 — 2026-07-09

> 作成: market-scout ／ 作成日: 2026-07-09 ／ テーマ: コネクティビティ・ロードマップ議論向けテーマ特化調査(T3)
> 対象期間: 2023〜2026-07(直近 12 か月を重視、構造理解に必要な過去経緯を含む)
> 本レポートは公開情報のみに基づく参考情報であり投資判断ではない。外部向け文書化の際は必ず人間レビューを要する。姉妹レポート: T1(`2026-07-09-global-regulation-mrc.md`)、全般スキャン(`2026-07-06-market-scan.md`)。

## TL;DR(経営向け)

- **キャリア IoT 部門が「取引可能な資産」になった**。Telenor は IoT 専業子会社 Telenor Connexion の株式 50% を PE の Verdane へ売却(2026-05-12 発表、EV SEK 7.5B ≒ USD 809M、**2025 年 EBITDA の 18 倍**)。両者が各 SEK 2B を追加投資し「価値創造型の買収」を明言 — 欧州に Wireless Logic に続く第 2 のロールアップ・プラットフォームが誕生する。
- **ブリーフィング C 表(T3 担当分)の 4 主張はすべて支持〜概ね支持**。1NCE 4,000 万(公式発表は「エンドポイント」表記)、Telenor/Verdane の 50%・EV 75 億 SEK・18x、Wireless Logic 1,000 万超(公開値はさらに上の 1,800 万超)、Vodafone IoT 2.3 億(公開値 2.0〜2.15 億+のレンジと整合、2.3 億ちょうどの一次確認は不能)。
- **CMP レイヤーは「装備品ベンダー撤退 → 独立系集約」がほぼ完了**。Ericsson IoT Accelerator は Aeris 傘下で 1 億デバイス超へ成長し、KDDI も 2026-06 に契約継続を発表。Cisco IoT Control Center(旧 Jasper)は Lite ティアを EoL(受注終了 2025-10-24)にして低価格帯を刈り込む一方、SGP.32 対応を MWC 2026 で商用化 — 「全面撤退ではなく選別的継続」。
- **バリュエーションは二極化**: 高成長・キャリアグレード資産は 18x EBITDA(約 5.8x 売上)、減収局面のロールアップ資産は約 11.5x EBITDA(約 2.5x 売上、KORE 非公開化)。PE のドライパウダーが相場を押し上げており、P4(顧客基盤)の「買える玉」は先送りするほど高く・少なくなる。
- **衛星 NTN は地上 IoT MVNO の「破壊者」ではなく「単一 SIM 統合の部品」として吸収されるフェーズ**(Vodafone×Iridium/Skylo、Tele2×Skylo、Monogoto×OQ、Eseye×Sateliot)。ただし Starlink D2C(V2 衛星、2027 年〜)は Cat-1 相当の低軌道直収でミッドレンジ IoT を侵食しうる中期リスク。

## 1. 主要ファインディング(出典付き)

### 1.1 Telenor Connexion × Verdane — 本テーマの中心ディール

| 項目 | 内容 |
|---|---|
| 発表日 | 2026-05-12(クロージングは 2026 年中見込み・規制承認待ち。2026-06 時点で完了報道なし) |
| ストラクチャー | 50/50 の共同保有会社を設立(Telenor は持分法適用会社化)。取締役会は各 2 名+独立会長(Pekka Lundmark 元 Nokia CEO) |
| バリュエーション | **EV SEK 7.5B(≒ USD 809M)= 2025 年プロフォーマ EBITDA(約 SEK 415M)の 18 倍**。2025 年売上約 SEK 1.3B → EV/売上 約 5.8x(算出値) |
| 対価 | Telenor は現金約 SEK 3.8B+売り手クレジット約 SEK 0.8B を受領、売却益約 SEK 7.2B を計上。新規銀行借入約 SEK 2.2B、取引後の株式価値約 SEK 5.3B |
| アーンアウト | 商業目標達成で EV +SEK 0.3B |
| 追加投資 | **両者が各 SEK 2B(計 SEK 4B)を成長投資にコミット。「オーガニック成長+価値創造型の買収」を明言** |
| 事業規模 | IoT SIM 3,100 万回線・200 か国以上へ提供・「中国外でグローバル top 10」 |

出典: [Telenor Connexion プレスリリース(Mynewsdesk)](https://telenor-connexion-com.mynewsdesk.com/pressreleases/telenor-partners-with-verdane-to-build-a-global-iot-leader-3447891) 2026-05-12 ／ [The Fast Mode](https://www.thefastmode.com/technology-solutions/48540-telenor-verdane-form-joint-ownership-structure-for-telenor-connexion-valued-at-sek-7-5-billion) ／ [IoT Tech News](https://iottechnews.com/news/telenor-verdane-809m-iot-joint-venture/) ／ [Telecompaper](https://www.telecompaper.com/news/telenor-spins-off-connexion-as-50-50-joint-venture-with-investment-firm-verdane-to-exploit-iot-market-growth--1570776) ／ [Bloomberg](https://www.bloomberg.com/news/articles/2026-05-12/telenor-sells-stake-in-internet-of-things-business-to-verdane) 2026-05-12

**業界的意味(分析)**:
1. キャリアの IoT 部門に PE が 18x EBITDA を付けた初の公開事例。Vodafone IoT(2024 年分社化・最大 50% 外部売却方針)に続き、「キャリア IoT のカーブアウト+外部資本」がテンプレート化した。
2. 買収資金 SEK 4B を持つ新たな統合主体の誕生。欧州の中堅独立系 MVNO(下記 2 章)の争奪戦が激化する方向。
3. **Verdane は Onomondo の 2022 年 USD 21M 成長ラウンドのリード投資家でもある**([Onomondo ブログ](https://onomondo.com/blog/iot-connectivity-pioneer-raises-growth-investment/) 2022-06)。同一 PE が「キャリア級回線資産(Telenor Connexion)+ソフトウェア定義コア(Onomondo)」の両方を保有する構図であり、両者の組み合わせ・統合は自然な仮説(**推測。統合計画の公開情報はなし・未確認**)。

### 1.2 Ericsson IoT Accelerator → Aeris(2023)のその後 — 「Thin CMP 撤退」の帰結

- 取引は 2022-12-07 発表、**2023-03-31 クローズ**。Ericsson は赤字の IoT 事業(2022 年見込み売上 SEK 0.8B)を切り離し、四半期 SEK 0.25B の損失を解消。Ericsson は Aeris の少数株式を取得し移行サービスを提供。売却時点の IoT Accelerator は 9,000 社超・9,500 万デバイス・eSIM 2,200 万、Connected Vehicle Cloud は 600 万台/180 か国。[Ericsson 公式](https://www.ericsson.com/en/news/2023/3/ericsson-announces-closing-of-the-transfer-of-iot-accelerator-and-connected-vehicle-cloud-businesses-to-aeris) 2023-03 ／ [Business Wire](https://www.businesswire.com/news/home/20221207005574/en/Aeris-to-Acquire-IoT-Business-from-Ericsson) 2022-12-07 ／ [Light Reading](https://www.lightreading.com/iot/aeris-to-acquire-iot-business-from-ericsson)
- 買収後の Aeris は 2026-01 に接続デバイス 1 億台突破(約 +90% 成長)。[Business Wire](https://www.businesswire.com/news/home/20260127961011/en/Aeris-Soars-Past-100-Million-Connected-Devices-Delivering-Nearly-90-Percent-Growth-and-Outpacing-IoT-Market) 2026-01-27
- **KDDI は 2026-06 に Aeris と IoT Accelerator の接続管理契約(継続・移行完了)を発表**。KDDI は 2017 年から(Ericsson 時代を含め)同プラットフォームを利用。現時点のプラットフォーム規模は 1.04 億 IoT デバイス+4,200 万コネクテッドカー。[Business Wire](https://www.businesswire.com/news/home/20260615619101/en/KDDI-Signs-IoT-Accelerator-Connectivity-Management-Agreement-with-Aeris) 2026-06-15 ／ [Computer Weekly](https://www.computerweekly.com/news/366644577/KDDI-inks-Aeris-IoT-accelerator-connectivity-management-agreement) ／ [The Fast Mode](https://www.thefastmode.com/technology-solutions/49090-aeris-completes-kddi-iot-connectivity-transition-expanding-global-iot-accelerator-platform)
- Verizon ThingSpace との相互接続も 2026-02 に発表済み([IoT Now](https://www.iot-now.com/2026/02/25/155467-aeris-and-verizon-business-simplify-global-iot-expansion-with-unified-connectivity-and-orchestration/))。→ Aeris は「MNO の裏方 CMP」ポジションを確立。ブリーフィング G8 の「Ericsson は Thin CMP コモディティ化で売却」という整理は公開情報(赤字・低売上での売却)と整合する。

### 1.3 Cisco IoT Control Center(旧 Jasper)の現況 — 「EoL ではなく選別」

- **全体の EoL・売却・縮小を示す公開情報は見つからず(確認不能)**。逆に継続投資の証跡あり: MWC 2026(2026-03-02〜05)で Tele2 IoT・IDEMIA と「世界初の商用 SGP.32 エンドツーエンド IoT ソリューション」を発表。Cisco Mobility Services Platform(IoT Control Center を含む)が SGP.32 オーケストレーションを担う。[Tele2 公式](https://www.tele2.com/media/news/2026/tele2-iot-idemia-secure-transactions-and-cisco-launch-first-commercial-sgp-32-end-to-end-iot-solution/) 2026-03 ／ [Telecompaper](https://www.telecompaper.com/news/tele2-iot-launches-commercial-service-based-on-sgp32-standard-with-idemia-and-cisco--1563867)
- ただし **Lite ティアは EoL**: 受注・更新終了 2025-10-24、サポート終了 2028-10-31。上位ティア(Essentials Flat / Basic 等)への移行を案内 — 低価格・小規模セグメントからの撤退と読める。[Cisco EoL 告知](https://www.cisco.com/c/en/us/products/collateral/networking/software/iot-control-center/lite-tier-of-iot-control-center-eol.html)
- 経緯: Cisco は 2016-02 に Jasper を USD 1.4B で買収。AT&T が最大のアンカー顧客(サービスプロバイダー経由モデル)。[The Fast Mode](https://www.thefastmode.com/technology-solutions/10847-cisco-jasper-unveils-major-upgrade-to-iot-platform-at-t-first-to-deploy-the-enhanced-features) ／ [Cisco Blogs](https://blogs.cisco.com/industrial-iot/cellular-iot-at-scale)
- 判定: ブリーフィング G8 の「AT&T = Cisco 依存」構図は現在も有効。「Cisco の IoT CC 縮小・EoL」という観測は**現時点では裏付けなし**。

### 1.4 バリュエーション相場(マルチプルの記録)

| ディール | 発表 | 取引規模 | EV/売上 | EV/EBITDA | 性格 |
|---|---|---|---|---|---|
| Telenor Connexion 50% → Verdane | 2026-05 | EV SEK 7.5B(USD 809M) | 約 5.8x(算出) | **18x(公表)** | 高成長・キャリアグレード・車載/グローバル大企業顧客 |
| KORE 非公開化(Searchlight+Abry) | 2026-02 | 約 USD 726M | 約 2.5x(概算) | 約 11.5x(概算、FY2025 調整後 EBITDA USD 63.3M) | 減収局面・リストラ後のロールアップ資産 |
| Wireless Logic(General Atlantic 少数出資) | 2024 | 評価額 GBP 3.5B | n/a(売上非公開) | n/a | PE 保有の欧州最大ロールアップ。2025 年に Montagu が EUR 2B 継続ビークル組成 |
| Digi × Particle | 2026-01 | USD 50M | 約 2.5x ARR | n/a | 参考(P2 系デバイスプラットフォーム) |
| Ericsson IoT-A → Aeris | 2022-12 | 非公開 | n/a | n/a | 赤字事業の撤退型売却(値付けの下限例) |

出典: 上記 1.1〜1.3 の各リリースに加え、[KORE 非公開化リリース](https://www.prnewswire.com/news-releases/kore-announces-agreement-to-be-acquired-by-searchlight-capital-partners-and-abry-partners-302699482.html) 2026-02-27 ／ [Alternatives Watch](https://www.alternativeswatch.com/2026/03/02/abry-partners-searchlight-capital-take-iot-provider-kore-private/) 2026-03-02 ／ [Insider Media(GA 出資・GBP 3.5B)](https://www.insidermedia.com/news/south-east/general-atlantic-backs-iot-services-provider-in-deal-valuing-firm-at-3.5bn) 2024 ／ [CVC(Montagu 継続ビークル)](https://www.cvc.com/media/news/2025/montagu-raises-2-billion-continuation-vehicle-to-support-wireless-logic-s-next-phase-of-global-growth/) 2025

- 市場全体の参考値(信頼度中・二次情報): 2026 年央のグローバル M&A EV/EBITDA 中央値は約 10.7x、PE 主導案件は約 12.6x と事業会社主導(9.8x)を上回る。[Current M&A Multiples 2025-2026](https://ibinterviewquestions.com/guides/valuation-investment-banking/current-ma-multiples-across-sectors-2025-2026)(閲覧 2026-07-09)
- **含意**: 「成長率×キャリアグレード×顧客基盤の質」でマルチプルが 6〜7 turn 変わる。P4 案件の値付けは KORE 型(〜11.5x)をベースに、車載・大企業顧客・ソフトウェア比率でプレミアムを査定するのが妥当。
- 統合ペースの参考: Transforma Insights は 2024-06 時点で「MVNO 間買収は 2023-12 以降 9 件と、直前 2 年間の 28 件から減速。ただしスケール獲得圧力による統合は継続」と分析(その後 2025〜26 に Wireless Logic 4 件・KORE 非公開化・Telenor JV と PE 主導の大型化に移行)。[Transforma Insights](https://transformainsights.com/blog/shifting-sands-iot-mvno-market-landscape) ／ [IoT For All(2025 年に MVNO 管理回線 2.9 億)](https://www.iotforall.com/iot-mvno-2025-report)

## 2. 競合・プレイヤー動向

### 2.1 独立系 IoT MVNO / CMP

| プレイヤー | 状況(2026-07 時点) | 出典 |
|---|---|---|
| **KORE**(米・上場→非公開化中) | Searchlight+Abry による USD 726M・USD 9.25/株の非公開化に合意(2026-02-27、クローズ 2026 Q2-Q3 見込み。Abry は既に普通株約 28% 保有、Searchlight は優先株 USD 275M)。前史として 2024-08 に人員約 25% 削減・年間 USD 20M 超のコスト削減。FY2024 売上 USD 286.1M。非公開化後の非中核資産切り出しに注視 | [PR Newswire](https://www.prnewswire.com/news-releases/kore-announces-agreement-to-be-acquired-by-searchlight-capital-partners-and-abry-partners-302699482.html) 2026-02-27 ／ [KORE 2024-08 リストラ](https://www.korewireless.com/company/news/kore-reports-second-quarter-2024-results) ／ [IT Europa](https://iteuropa.com/news/iot-services-firm-kore-cuts-quarter-its-staff) |
| **Wireless Logic**(英・PE 保有) | Montagu 主導+General Atlantic 少数出資(2024 年評価 GBP 3.5B)。買収累計 18 件超(Tracxn、2026-02 時点)。直近 12 か月: Things Mobile(2025-03)→ Arqia/ブラジル(2025-04)→ Zipit/米(2025-08)→ Comms365/英(2026-02)。公称 1,800 万デバイス超/165 か国・直接契約 50 MNO+ | [Wireless Logic](https://wirelesslogic.com/news/wireless-logic-acquire-comms365) 2026-02-20 ／ [Montagu](https://montagu.com/wireless-logic-acquires-comms365/) ／ [Tracxn](https://tracxn.com/d/companies/wireless-logic/__t-9_OUepMM2rIhkA7CH6vXFBNDOXlBiVtCE8PvyViXI) |
| **1NCE**(独) | 2025 年に 1,000 万回線純増、**エンドポイント 4,000 万超・顧客 3 万社・170 か国+**(2026-01-07)。株主は DT(創業時からの出資者)と SoftBank(2021 Series B リード、2022 に SB 株式取得+アジア太平洋 19 市場の独占販売代理)。2025-04 に USD 60M 調達しソフトウェア/AI(1NCE Insights)へ拡張 | [Business Wire](https://www.businesswire.com/news/home/20260107086987/en/1NCE-Continues-Growth-and-Expands-Its-Software-AI-and-Services-Offering) 2026-01-07 ／ [RCR Wireless](https://www.rcrwireless.com/20220608/carriers/softbank-takes-equity-stake-in-1nce-as-the-only-company-that-can-deliver-global-iot) 2022-06 ／ [1NCE](https://www.1nce.com/en-us/resources/news/press-releases/1nce-raises-60-million-usd-in-new-funding) 2025-04-29 |
| **emnify**(独) | 2026 Gartner MQ(Managed IoT Connectivity)で初の **Visionary** 選出(2026-05-07)。CES 2026 で factory-first(製造ライン組込 bootstrap プロファイル+BYOC)発表。資金は 2022-01 の Series B USD 57M(One Peak)以降大型調達なし。創業者 CEO(Frank Stoecker)体制 | [Business Wire](https://www.businesswire.com/news/home/20260507642325/en/emnify-named-a-Visionary-in-the-2026-Gartner-Magic-Quadrant-for-Managed-IoT-Connectivity-Services-Worldwide) 2026-05-07 ／ [Business Wire](https://www.businesswire.com/news/home/20251222300752/en/Power-On.-Connected.-emnify-Debuts-Factory-First-Instant-Connectivity-for-IoT-Devices-at-CES-2026) 2025-12-22 |
| **Eseye**(英) | 累計調達約 USD 81.8M、直近ラウンドはデット(Virgin Money 等)— エクイティ大型調達は途絶。AT&T と Global SIM Advanced を MWC 2025 で発表、Sateliot(2024-11)・OQ(2026-01)と NTN 提携。売上は第三者推計 USD 26.5M(信頼度低) | [Tracxn](https://tracxn.com/d/companies/eseye/__7GfoOXs1yk1ahiDJKRZNfLMKxNdHyPMXjtNqgIy108Y) ／ [Computer Weekly](https://www.computerweekly.com/news/366616388/Eseye-looks-to-Sateliot-to-revolutionise-global-IoT) 2024-11 ／ [prospeo 推計](https://prospeo.io/c/eseye-revenue) |
| **Onomondo**(デンマーク) | 累計調達 USD 31.5M。2022-06 の USD 21M 成長ラウンドは **Verdane がリード**。2024 年売上 +115%・顧客 500 社(前回スキャン)。成長請負型の新 CEO 就任済み。Verdane の Telenor JV 参画により戦略的位置づけが変化(1.1 参照) | [Onomondo](https://onomondo.com/blog/iot-connectivity-pioneer-raises-growth-investment/) 2022-06 ／ [Tracxn](https://tracxn.com/d/companies/onomondo/__eVUVeuqcjxmJP1CgRZo0kAKOERzV85i16HlxdUpHAZ8) |
| **Monogoto**(イスラエル) | 2024-10 に Series A USD 27M(**Toyota Ventures リード**、Samsung Next 等)。Terrestar(加、2025-03)・OQ Technology(2026-01)と衛星ハイブリッド提携、CES 2026 出展。累計 USD 38M | [Monogoto](https://monogoto.io/2024/10/15/monogoto-raises-27-million-in-series-a-funding-to-lead-the-software-defined-connectivity-revolution/) 2024-10-15 ／ [Monogoto News](https://monogoto.io/news/) |
| **Velos IoT**(英/ジャージー) | PE の Perwyn が 2021-07 に JT Group からカーブアウトして過半取得。NextM2M(デンマーク)・Top Connect(エストニア)を追加買収。2025-02 に IDEMIA と提携。保有 5 年経過であり、一般的な PE 保有期間からは**出口(売却)ウィンドウに入っている可能性(推定。売却プロセスの公開情報はなし)** | [Perwyn](https://www.perwyn.com/investments/velos-iot) ／ [The Deal](https://www.thedeal.com/private-equity/perwyn-acquires-control-of-jersey-telecoms-iot-business/) 2021 |
| **Pod Group**(英、G+D 傘下) | 2021 年に G+D(独・SIM/eSIM 大手)が買収し「Enterprise Network Operator」として運営継続。G+D は Sateliot・Skylo と衛星 NTN 連携を拡大 — SIM ベンダーがコネクティビティ事業を垂直統合する動き | [G+D](https://www.gi-de.com/en/group/press/press-releases/giesecke-devrient-acquires-global-iot-specialist-pod-to-enlarge-connectivity-business-portfolio) 2021 ／ [Skylo Newsroom](https://www.skylo.tech/newsroom/g-d-expands-iot-connectivity-with-cellular-satellite-services-for-seamless-global-network-coverage) |
| **floLIVE**(イスラエル/英) | ホワイトレーベル CMP/MVNE(「MVNO in a Box」)を軸に、NLT Telecom・TNS と組み LatAm で SGP.32 eSIM 展開(2026-03)。MWC 2026 出展。資金は 2023-09 Series C USD 47M(累計 USD 88.2M)以降、大型調達の公表なし | [floLIVE](https://flolive.net/blog/nlt-tns-and-flolive-join-forces-to-expand-esim-deployments-in-latin-america/) 2026-03 ／ [floLIVE MWC 2026](https://www.einpresswire.com/article/894974449/flolive-to-showcase-a-network-beyond-at-mwc-2026) |
| **Aeris**(米) | 1.2 参照(1 億デバイス超、KDDI・DT・Verizon の裏方 CMP)。Ericsson が少数株主 | 1.2 の各出典 |

### 2.2 キャリア系 IoT

- **Vodafone IoT**: 2024-04 に分社化(独立 MVNO 化)。「最大 50% を第三者に売却可能」が公式方針で、**Microsoft が有力候補と報道されたが成立の公開情報はなし(未確認・2026-07 時点で進展確認できず)**。規模は 2025-04 に 2 億接続到達、2025-11 の Iridium 提携リリースでは「2.15 億デバイス超/180 か国」。NTN は Skylo(2025)に加え Iridium NTN Direct(2025-11-04 発表、商用 2026 年予定)と二本立て。[ABI Research](https://www.abiresearch.com/market-research/insight/7784146-worlds-biggest-iot-service-provider-become) 2024 ／ [RCR Wireless](https://www.rcrwireless.com/20240417/internet-of-things-4/vodafones-big-bet-to-hive-off-and-hyper-scale-iot-with-microsoft) 2024-04-17 ／ [Advanced Television](https://www.advanced-television.com/2025/04/08/vodafone-hits-200m-iot-connections/) 2025-04-08 ／ [PR Newswire(Iridium)](https://www.prnewswire.com/news-releases/vodafone-iot-partners-with-iridium-to-provide-its-customers-with-ntn-nb-iot-connectivity-302602765.html) 2025-11-04
- **Tele2 IoT**: IoT を B2B 成長ニッチと位置づけ。MWC 2026 で IDEMIA・Cisco と世界初の商用 SGP.32 E2E ソリューション、2025 年に Skylo とスウェーデン初の商用衛星 IoT。**「価格攻勢」自体の公開証跡は確認不能**(料金は per-SIM 月額+データバンドルの標準型)。ブリーフィング G1 の記述は MWC 等での相対情報と思われ、公開情報では判定不能。[Tele2](https://www.tele2.com/media/news/2026/tele2-iot-idemia-secure-transactions-and-cisco-launch-first-commercial-sgp-32-end-to-end-iot-solution/) 2026-03 ／ [Tele2×Skylo](https://www.tele2.com/media/news/2025/tele2-first-swedish-operator-to-launch-satellite-iot-connectivity-with-skylo/) 2025
- **Telenor IoT**: 北欧 IoT 資産を Telenor Connexion に集約(2026-01 完了)→ Verdane と JV 化(1.1)。なお一部業界レポート要約に「Telenor による Tele2 IoT 買収」への言及があるが一次情報を確認できず(**未確認**、前回スキャンから変化なし)。
- **KDDI**: グローバル IoT の CMP を Aeris(旧 Ericsson IoT-A)に外部依存継続(1.2)。国内 MNO が CMP を自前化せず外部調達する構図の代表例。

### 2.3 衛星 NTN プレイヤー(地上 IoT 接続への破壊/補完)

| プレイヤー | 資金・提携(直近) | 地上 IoT への含意 |
|---|---|---|
| **Skylo**(米、GEO ベース NTN NB-IoT) | 2024-02 に USD 37M(Intel Capital/Innovation Endeavors 共同リード)、2025-02 に USD 30M(NGP 主導・応募超過)、累計約 USD 183M。Vodafone IoT・Tele2 IoT・Orange・G+D と提携、Qualcomm モデム認証 | **補完が主**。MVNO/MNO の「単一 SIM ハイブリッド」の標準部品化。既存 GEO 衛星活用のため設備投資が軽く、提携密度で先行 |
| **Sateliot**(西、5G NB-IoT LEO) | **EUR 100M(最大 116M)Series C を 2026-04 に開始、2026 年夏クローズ予定**(最大 50% 公的共同出資)。衛星 6 機運用中・2026 年に +5 機・調達で 16 機追加。事前契約 EUR 270M・400 顧客/60 か国。Telefónica・DT・VIVO と合意、Eseye・G+D/Pod と提携 | 補完(標準準拠で既存 NB-IoT デバイスがそのまま接続)。**出資参加のタイミングが 2026 夏に接近** |
| **OQ Technology**(ルクセンブルク、5G NB-IoT LEO) | Series B 目標 EUR 35-40M(ルクセンブルク政府・Aramco 系 Wa'ed 等)、EIC 最大 EUR 17.5M(2025-02)、**EIB デット EUR 25M(2026-02-26)**。KPN・Monogoto と提携。2026 年末までに衛星 20 機追加計画 | 補完。欧州公的資金が NTN IoT を下支えする構図 |
| **Starlink D2C(SpaceX)** | T-Mobile「T-Satellite」商用開始 2025-07(SMS)→ 2025-10 データ対応。2026-03 に「Starlink Mobile」へリブランド、DTC 衛星 650 機超・22 か国展開。**IoT(Cat-1 相当)は「今後提供」でテスト完了段階**。V2 衛星(データ密度 100 倍)は Starship で 2027 年央から約 1,200 機計画。EchoStar 周波数 USD 17B 取得(2025-09)で資本戦へ | **中期的な破壊リスク**。V2 大量配備後(2027〜)は「地上圏外のミッドレンジ IoT」を直接刈り取る可能性。当面は米国中心・スマホ優先 |
| **AST SpaceMobile**(米、D2C ブロードバンド) | 手元流動性 USD 3.9B 超(2025 年末)、契約収益コミット USD 1.2B 超、stc から前受 USD 175M(10 年契約)。2026 年末までに衛星約 45 機目標、stc(サウジ)で 2026 Q4 商用開始予定。Orange・Telefónica・楽天以外にも通信事業者提携多数 | スマホ・ブロードバンド優先で **IoT への直接影響は当面限定的**。ただし周波数・資本の集中は NTN 全体の値付けを押し上げる |

出典: [Skylo/Intel Capital](https://www.intelcapital.com/skylo-technologies-raises-37-million-from-intel-capital-innovation-endeavors-bmw-i-ventures-samsung-catalyst-next47-seraphim-space/) 2024-02-13 ／ [Skylo USD 30M](https://www.skylo.tech/newsroom/skylo-raises-30m-in-oversubscribed-funding-round-to-scale-direct-to-device-satellite-service-worldwide) 2025-02-27 ／ [IoT Business News(Sateliot)](https://iotbusinessnews.com/2026/04/13/sateliot-raises-e100m-to-scale-5g-iot-satellite-network/) 2026-04-13 ／ [DCD(Sateliot EUR 116M)](https://www.datacenterdynamics.com/en/news/sateliot-launches-116-million-publicprivate-series-c-to-fund-its-constellation-deployment/) 2026-04 ／ [Advanced Television(OQ/EIB)](https://www.advanced-television.com/2026/02/26/oq-technology-receives-e25m-in-eib-funding/) 2026-02-26 ／ [Space Intel Report(OQ Series B)](https://www.spaceintelreport.com/satellite-iot-startup-oq-technology-13m-series-a-in-hand-series-b-planned-betting-on-open-5g-standards-over-proprietary-tech/) ／ [SatelliteInternet.com(T-Satellite)](https://www.satelliteinternet.com/providers/starlink/starlink-direct-to-cell/) 2026 ／ [Fierce Network(MWC 2026 Starlink Mobile)](https://www.fierce-network.com/wireless/mwc-starlink-mobile-unveils-plans-v2-satellites-and-more) 2026-03 ／ [Business Wire(AST Q1 2026)](https://www.businesswire.com/news/home/20260511685431/en/AST-SpaceMobile-Provides-Business-Update-and-First-Quarter-2026-Results) 2026-05-11 ／ [TechCrunch(SpaceX×EchoStar)](https://techcrunch.com/2025/09/08/spacex-strikes-17b-deal-to-buy-echostars-spectrum-for-starlinks-direct-to-phone-service/) 2025-09-08

## 3. ブリーフィング主張の裏取り結果(C 表・T3 担当分)

| # | 主張 | 判定 | 根拠 |
|---|---|---|---|
| 1 | 1NCE 4,000 万回線 | **支持**(表記注意) | 1NCE 公式発表(2026-01-07)「40+ million intelligent products / endpoints・顧客 3 万社」。公式表記は「エンドポイント」であり、課金アクティブな SIM 回線数と同一かは不明(社数比較に使う際は脚注推奨)。[Business Wire](https://www.businesswire.com/news/home/20260107086987/en/1NCE-Continues-Growth-and-Expands-Its-Software-AI-and-Services-Offering) |
| 2 | Telenor/Verdane 50%・EV 75 億 SEK・EBITDA 18 倍 | **支持** | Telenor Connexion 公式リリース(2026-05-12): 50/50 共同保有、EV SEK 7.5B、2025 年 EBITDA の 18 倍と明記。[Mynewsdesk](https://telenor-connexion-com.mynewsdesk.com/pressreleases/telenor-partners-with-verdane-to-build-a-global-iot-leader-3447891) ／ [The Fast Mode](https://www.thefastmode.com/technology-solutions/48540-telenor-verdane-form-joint-ownership-structure-for-telenor-connexion-valued-at-sek-7-5-billion) |
| 3 | Wireless Logic 1,000 万回線超 | **支持**(公開値はさらに上) | 2026-02-20 の Comms365 買収リリースで「1,800 万デバイス超/165 か国」。会社サイトは「約 2,000 万接続」。「1,000 万超」は保守的で正しい。[Wireless Logic](https://wirelesslogic.com/news/wireless-logic-acquire-comms365) ／ [wirelesslogic.com](https://wirelesslogic.com/) |
| 4 | Vodafone IoT 2.3 億回線 | **概ね支持** | 公開値: 2 億接続(2025-04)→「2.15 億デバイス超」(2025-11、Iridium 提携リリース)。2.44 億への言及も業界メディアにあるが日付・根拠を確認できず。「2.3 億」ちょうどの一次確認は不能だが、2026 年時点のレンジ(2.0〜2.4 億)として整合的。[Advanced Television](https://www.advanced-television.com/2025/04/08/vodafone-hits-200m-iot-connections/) ／ [PR Newswire](https://www.prnewswire.com/news-releases/vodafone-iot-partners-with-iridium-to-provide-its-customers-with-ntn-nb-iot-connectivity-302602765.html) ／ [Light Reading](https://www.lightreading.com/iot/vodafone-iot-looks-to-satellites-to-connect-more-things) |
| 5 | (関連)Ericsson IoT-A → Aeris 売却(2023) | **支持** | 2022-12-07 発表・2023-03-31 クローズ。赤字解消目的も公式に確認。[Ericsson](https://www.ericsson.com/en/news/2023/3/ericsson-announces-closing-of-the-transfer-of-iot-accelerator-and-connected-vehicle-cloud-businesses-to-aeris) |
| 6 | (関連)Cisco IoT Control Center の現況 | **継続を支持** | 全体の EoL・撤退報道は発見できず。Lite ティアのみ EoL(2025-10-24 受注終了)。SGP.32 対応を MWC 2026 で商用化しており、投資は継続(1.3 参照) |
| 7 | (関連)Tele2 の価格攻勢(G1) | **確認不能** | 公開情報に価格攻勢の直接証跡なし。SGP.32・衛星での商品面の攻勢は確認(2.2) |

## 4. SORACOM への戦略的含意

**価値が上がっている資産クラス**
1. **キャリアグレード CMP+大企業/車載顧客基盤**: Telenor Connexion 18x EBITDA、Aeris の 1 億デバイス(うち車載 4,200 万)が示す通り、「解約しにくい大型顧客+車載」がマルチプルの源泉。国内でも車載・映像(ブリーフィング J1/J8)へのシフトはグローバル相場と同方向。
2. **eSIM オーケストレーション(SGP.32)資産**: Tele2×IDEMIA×Cisco、floLIVE の LatAm 展開、emnify factory-first と、2026 年は「SGP.32 を実運用に載せた者」が差別化される年。回線そのものより「プロファイル切替とローカル準拠を運用できる能力」に価値が移動(T1 レポートと整合)。
3. **規制対応済みローカルアクセス(LBO・現地免許・現地 IMSI)**: floLIVE/NLT のブラジル型モデルが典型。PR 規制・データローカライゼーションが強まるほど希少化。
4. **衛星-セルラー統合レイヤー**: 衛星コンステレーション自体は資本集約(AST は手元 USD 3.9B)で保有対象外だが、「単一 SIM で地上+衛星」を運用する統合レイヤーは全プレイヤーが部品として買いに来ている(Vodafone、Tele2、G+D、Monogoto、Eseye)。当社の既存ポジション(Skylo 統合済み)は相場的に正しい位置。

**価値が下がっている資産クラス**
1. **純回線再販(thin pipe)MVNO**: MRC・PR 規制で売上フロアとコンプラコストが上がり、SGP.32 でスイッチングコストが下がる二重圧力。KORE の減収・約 11.5x はこの証跡。
2. **低価格・セルフサーブ CMP ティア**: Cisco Lite ティア EoL が象徴。小規模接続の管理は 1NCE 型の超低価格 SaaS か、プラットフォーム統合型に二極化。
3. **単独の中規模独立系**: emnify・Eseye・floLIVE・Hologram など 2022〜23 年以降エクイティ調達が途絶えた層は、2026-27 に資本イベント(調達 or 売却)が不可避との見立てを維持(前回スキャンから変化なし。Eseye はデット調達で継命中)。

**競争環境への示唆**
- 買い手として当社が P4 案件で対峙するのは Wireless Logic(Montagu/GA)、Verdane/Telenor JV(SEK 4B)、非公開化後の KORE(Searchlight/Abry)の 3 系統の PE マネー。入札では価格で勝てない前提で、「技術統合力・PMI の速さ・創業者リテンション」を差別化軸にすべき。
- KDDI×Aeris の契約継続は、国内 MNO がグローバル CMP を外部依存し続けることを示す。国産でフル MVNO 基盤+CMP を垂直統合している事業者の希少性は上がっている(相対的な当社のポジション強化材料)。
- Verdane が Onomondo(ソフトウェア定義コア)と Telenor Connexion(回線資産)の両方に関与する構図は、「コア技術×キャリア顧客基盤」の組み合わせに PE が価値を見ている証拠。当社の垂直統合テーゼと同型であり、同じ発想の買い手が欧州に現れたと解釈すべき。

## 5. インオーガニック(M&A・出資・提携)の含意

| 論点 | ピラー | 推奨(deal-desk / strategy-planner への提案) |
|---|---|---|
| Sateliot Series C(EUR 100M、2026 夏クローズ予定) | P1 | マイノリティ出資(type: investment)の検討期限が事実上 2026 夏。既にロングリスト掲載済み(2026-07-06)。参加可否の判断を 7 月中に strategy-planner へ | 
| Onomondo | P1/P4 | Verdane の Telenor JV 参画で「取り合い/取り込まれ」リスクが上昇。既存ロングリスト案件の優先度引き上げと、Verdane 側の動き(JV クロージング、追加買収)の四半期トラックを提案 |
| floLIVE / Eseye(資本イベント接近組) | P1/P4 | 調達停滞+デット依存(Eseye)は 12〜24 か月内の資本イベント示唆。財務モニタリング継続。floLIVE は当社 planP3 連携先(G7)でもあり、出資・関係強化はディフェンシブにも機能 |
| KORE 非公開化後の資産切り出し | P4 | クローズ(2026 Q2-Q3)後、PE 流の事業整理で地域・業種特化資産が売りに出る可能性。ウォッチ継続(前回スキャンから変化なし) |
| Velos IoT(Perwyn 保有 5 年) | P4 | 出口ウィンドウ入りの可能性(推定)。売りに出た場合の顧客基盤(欧州・多国籍)の評価準備だけ先行しておく |
| Verdane/Telenor JV・Wireless Logic | (再編対応) | 買収競合としての動向トラッキングをパイプライン運用に組み込む(ma-thesis 分類 3「業界再編対応」)。欧州中堅の争奪が 2026 後半に激化する前提で、P4 の優先案件は早めのアプローチを |

- 新規候補の追加提案: 今回のテーマ調査では、前回スキャン(2026-07-06)のロングリスト 8 社に追加すべき新顔は発見せず。既存候補のうち **Onomondo(優先度上げ)・Sateliot(期限設定)・floLIVE(財務モニタ強化)** の 3 件の扱い変更を deal-desk に提案する。パイプライン(`pipeline/pipeline.yaml`)は現在サンプルのみで実案件への影響なし。
- 相場観の更新: P4 の値付けアンカーを「ベース 〜11.5x EBITDA(KORE 型)/ プレミアム 18x(Telenor Connexion 型: 高成長・車載・キャリアグレード)」の 2 点張りに更新(従来は KORE の 1 点)。

## 6. 未解決の問い

1. **Telenor/Verdane JV のクロージング時期と最初の買収ターゲット** — SEK 4B の初弾がどこに向かうか(Onomondo か、第三者か)。
2. **Vodafone IoT の 50% 売却** — Microsoft 観測(未確認)の帰趨。成立すればハイパースケーラー×最大手 IoT MVNO の垂直連合となり P4 環境が一変する。
3. **Cisco IoT Control Center の中期戦略** — SGP.32 対応で再投資に見えるが、AT&T 依存構造の解消(マルチキャリア化)まで踏み込むか。Cisco が CMP を売却する場合の受け皿は誰か(未確認の観測すら現状なし)。
4. **1NCE「4,000 万エンドポイント」の中身** — 課金アクティブ回線比率・ARPU。低単価前払モデルの経済性が MRC コスト上昇(T1)にどこまで耐えるか。
5. **Starlink D2C の IoT 商用条件** — Cat-1 相当の直収がいつ・いくらで開放されるか。V2 配備(2027〜)前に地上 MVNO 側が取るべきヘッジ(提携・再販権)の選択肢。
6. **MVNO 間の中小型 M&A の再加速時期** — Transforma の言う統合減速(2024)から PE 大型化(2025-26)に移行した後、中小の「売り玉」が市場に出るトリガーは何か(MRC コスト、SGP.32 対応投資負担が有力候補)。

## 情報源一覧

**Telenor/Verdane**
- [Telenor partners with Verdane to build a global IoT leader](https://telenor-connexion-com.mynewsdesk.com/pressreleases/telenor-partners-with-verdane-to-build-a-global-iot-leader-3447891) — Telenor Connexion(Mynewsdesk), 2026-05-12
- [Telenor, Verdane Form Joint Ownership Structure for Telenor Connexion Valued at SEK 7.5 Billion](https://www.thefastmode.com/technology-solutions/48540-telenor-verdane-form-joint-ownership-structure-for-telenor-connexion-valued-at-sek-7-5-billion) — The Fast Mode, 2026-05
- [Telenor and Verdane form $809m IoT joint venture](https://iottechnews.com/news/telenor-verdane-809m-iot-joint-venture/) — IoT Tech News, 2026-05
- [Telenor spins off Connexion as 50-50 joint venture](https://www.telecompaper.com/news/telenor-spins-off-connexion-as-50-50-joint-venture-with-investment-firm-verdane-to-exploit-iot-market-growth--1570776) — Telecompaper, 2026-05
- [Telenor Sells Stake in Internet-of-Things Business to Verdane](https://www.bloomberg.com/news/articles/2026-05-12/telenor-sells-stake-in-internet-of-things-business-to-verdane) — Bloomberg, 2026-05-12
- [Verdane partners with Telenor to build a global IoT leader](https://verdane.com/verdane-partners-with-telenor-to-build-a-global-iot-leader/) — Verdane, 2026-05(2026-07-09 時点でサイト一時 503)

**Ericsson IoT-A / Aeris / KDDI**
- [Ericsson announces closing of the transfer of IoT Accelerator and Connected Vehicle Cloud businesses to Aeris](https://www.ericsson.com/en/news/2023/3/ericsson-announces-closing-of-the-transfer-of-iot-accelerator-and-connected-vehicle-cloud-businesses-to-aeris) — Ericsson, 2023-03
- [Aeris to Acquire IoT Business from Ericsson](https://www.businesswire.com/news/home/20221207005574/en/Aeris-to-Acquire-IoT-Business-from-Ericsson) — Business Wire, 2022-12-07 ／ [Light Reading](https://www.lightreading.com/iot/aeris-to-acquire-iot-business-from-ericsson) ／ [WCA(赤字事業の売却)](https://wca.org/ericsson-is-exiting-iot-and-has-agreed-to-sell-its-loss-making-iot-accelerator-business-to-aeris/)
- [Aeris Soars Past 100 Million Connected Devices](https://www.businesswire.com/news/home/20260127961011/en/Aeris-Soars-Past-100-Million-Connected-Devices-Delivering-Nearly-90-Percent-Growth-and-Outpacing-IoT-Market) — Business Wire, 2026-01-27
- [KDDI Signs IoT Accelerator Connectivity Management Agreement with Aeris](https://www.businesswire.com/news/home/20260615619101/en/KDDI-Signs-IoT-Accelerator-Connectivity-Management-Agreement-with-Aeris) — Business Wire, 2026-06-15 ／ [Computer Weekly](https://www.computerweekly.com/news/366644577/KDDI-inks-Aeris-IoT-accelerator-connectivity-management-agreement) ／ [The Fast Mode](https://www.thefastmode.com/technology-solutions/49090-aeris-completes-kddi-iot-connectivity-transition-expanding-global-iot-accelerator-platform) — 2026-06
- [Aeris and Verizon Business simplify global IoT expansion](https://www.iot-now.com/2026/02/25/155467-aeris-and-verizon-business-simplify-global-iot-expansion-with-unified-connectivity-and-orchestration/) — IoT Now, 2026-02-25

**Cisco IoT Control Center**
- [End-of-Sale and End-of-Life Announcement for the Cisco Lite Tier of IoT Control Center](https://www.cisco.com/c/en/us/products/collateral/networking/software/iot-control-center/lite-tier-of-iot-control-center-eol.html) — Cisco(受注終了 2025-10-24、サポート終了 2028-10-31)
- [Tele2 IoT, IDEMIA Secure Transactions and Cisco launch first commercial SGP.32 end-to-end IoT solution](https://www.tele2.com/media/news/2026/tele2-iot-idemia-secure-transactions-and-cisco-launch-first-commercial-sgp-32-end-to-end-iot-solution/) — Tele2, 2026-03 ／ [Telecompaper](https://www.telecompaper.com/news/tele2-iot-launches-commercial-service-based-on-sgp32-standard-with-idemia-and-cisco--1563867)
- [Cisco Jasper Unveils Major Upgrade to IoT Platform; AT&T First to Deploy](https://www.thefastmode.com/technology-solutions/10847-cisco-jasper-unveils-major-upgrade-to-iot-platform-at-t-first-to-deploy-the-enhanced-features) — The Fast Mode(Jasper 買収 USD 1.4B・AT&T 関係の経緯)

**KORE / Wireless Logic / 1NCE / その他独立系**
- [KORE Announces Agreement to be Acquired by Searchlight Capital Partners and Abry Partners](https://www.prnewswire.com/news-releases/kore-announces-agreement-to-be-acquired-by-searchlight-capital-partners-and-abry-partners-302699482.html) — PR Newswire, 2026-02-27 ／ [Alternatives Watch](https://www.alternativeswatch.com/2026/03/02/abry-partners-searchlight-capital-take-iot-provider-kore-private/) 2026-03-02 ／ [StockTitan(8-K)](https://www.stocktitan.net/sec-filings/KORE/8-k-kore-group-holdings-inc-reports-material-event-cbe93aa6fcfe.html)
- [KORE Reports Second Quarter 2024 Results; Announces Restructuring Plan](https://www.korewireless.com/company/news/kore-reports-second-quarter-2024-results) — KORE, 2024-08 ／ [IT Europa(25% 削減)](https://iteuropa.com/news/iot-services-firm-kore-cuts-quarter-its-staff) ／ [KORE Q4/FY2024 8-K](https://www.sec.gov/Archives/edgar/data/0001855457/000185545725000021/ex991koreq424earningsrelea.htm)
- [Wireless Logic Acquire Comms365](https://wirelesslogic.com/news/wireless-logic-acquire-comms365) — Wireless Logic, 2026-02-20 ／ [Montagu](https://montagu.com/wireless-logic-acquires-comms365/) ／ [Tracxn(買収 18 件)](https://tracxn.com/d/companies/wireless-logic/__t-9_OUepMM2rIhkA7CH6vXFBNDOXlBiVtCE8PvyViXI) ／ [Insider Media(GBP 3.5B 評価)](https://www.insidermedia.com/news/south-east/general-atlantic-backs-iot-services-provider-in-deal-valuing-firm-at-3.5bn) 2024 ／ [CVC(Montagu EUR 2B CV)](https://www.cvc.com/media/news/2025/montagu-raises-2-billion-continuation-vehicle-to-support-wireless-logic-s-next-phase-of-global-growth/) 2025
- [1NCE Continues Growth and Expands Its Software, AI and Services Offering](https://www.businesswire.com/news/home/20260107086987/en/1NCE-Continues-Growth-and-Expands-Its-Software-AI-and-Services-Offering) — Business Wire, 2026-01-07 ／ [SoftBank 出資](https://www.rcrwireless.com/20220608/carriers/softbank-takes-equity-stake-in-1nce-as-the-only-company-that-can-deliver-global-iot) — RCR Wireless, 2022-06-08 ／ [SoftBank 独占代理(日本)](https://www.softbank.jp/en/corp/news/press/sbkk/2022/20221026_02/) 2022-10-26 ／ [1NCE USD 60M](https://www.1nce.com/en-us/resources/news/press-releases/1nce-raises-60-million-usd-in-new-funding) 2025-04-29
- [emnify named a Visionary in the 2026 Gartner MQ](https://www.businesswire.com/news/home/20260507642325/en/emnify-named-a-Visionary-in-the-2026-Gartner-Magic-Quadrant-for-Managed-IoT-Connectivity-Services-Worldwide) — Business Wire, 2026-05-07 ／ [emnify factory-first(CES 2026)](https://www.businesswire.com/news/home/20251222300752/en/Power-On.-Connected.-emnify-Debuts-Factory-First-Instant-Connectivity-for-IoT-Devices-at-CES-2026) 2025-12-22 ／ [Series B USD 57M](https://www.prnewswire.com/news-releases/cellular-iot-connectivity-provider-emnify-raises-57m-50m-in-series-b-funding-from-one-peak-301461188.html) 2022-01
- [Eseye — Tracxn](https://tracxn.com/d/companies/eseye/__7GfoOXs1yk1ahiDJKRZNfLMKxNdHyPMXjtNqgIy108Y) ／ [Eseye×Sateliot](https://www.computerweekly.com/news/366616388/Eseye-looks-to-Sateliot-to-revolutionise-global-IoT) — Computer Weekly, 2024-11 ／ [prospeo 売上推計(信頼度低)](https://prospeo.io/c/eseye-revenue)
- [Onomondo: Verdane leads $21M growth investment](https://onomondo.com/blog/iot-connectivity-pioneer-raises-growth-investment/) — Onomondo, 2022-06 ／ [Tracxn](https://tracxn.com/d/companies/onomondo/__eVUVeuqcjxmJP1CgRZo0kAKOERzV85i16HlxdUpHAZ8)
- [Monogoto Raises $27 Million in Series A](https://monogoto.io/2024/10/15/monogoto-raises-27-million-in-series-a-funding-to-lead-the-software-defined-connectivity-revolution/) — Monogoto, 2024-10-15 ／ [Monogoto News(OQ・Terrestar・CES 2026)](https://monogoto.io/news/)
- [Perwyn: Velos IoT](https://www.perwyn.com/investments/velos-iot) ／ [The Deal(2021 カーブアウト)](https://www.thedeal.com/private-equity/perwyn-acquires-control-of-jersey-telecoms-iot-business/)
- [G+D acquires global IoT specialist Pod](https://www.gi-de.com/en/group/press/press-releases/giesecke-devrient-acquires-global-iot-specialist-pod-to-enlarge-connectivity-business-portfolio) — G+D, 2021 ／ [G+D×Skylo](https://www.skylo.tech/newsroom/g-d-expands-iot-connectivity-with-cellular-satellite-services-for-seamless-global-network-coverage)
- [NLT, TNS and floLIVE join forces to expand eSIM deployments in Latin America](https://flolive.net/blog/nlt-tns-and-flolive-join-forces-to-expand-esim-deployments-in-latin-america/) — floLIVE, 2026-03 ／ [floLIVE at MWC 2026](https://www.einpresswire.com/article/894974449/flolive-to-showcase-a-network-beyond-at-mwc-2026)

**Vodafone IoT / Tele2 IoT**
- [World's Biggest IoT Service Provider Becomes Independent MVNO](https://www.abiresearch.com/market-research/insight/7784146-worlds-biggest-iot-service-provider-become) — ABI Research, 2024 ／ [RCR Wireless(Microsoft 観測・未確認)](https://www.rcrwireless.com/20240417/internet-of-things-4/vodafones-big-bet-to-hive-off-and-hyper-scale-iot-with-microsoft) 2024-04-17 ／ [Telecompaper(少数株売却検討・報道)](https://www.telecompaper.com/news/vodafone-considers-sale-of-minority-stake-in-iot-business-report--1463544)
- [Vodafone hits 200m IoT connections](https://www.advanced-television.com/2025/04/08/vodafone-hits-200m-iot-connections/) — Advanced Television, 2025-04-08 ／ [RCR Wireless](https://www.rcrwireless.com/20250409/internet-of-things/vodafone-iot-good-green) 2025-04-09
- [Vodafone IoT Partners with Iridium(2.15 億デバイス超)](https://www.prnewswire.com/news-releases/vodafone-iot-partners-with-iridium-to-provide-its-customers-with-ntn-nb-iot-connectivity-302602765.html) — PR Newswire, 2025-11-04 ／ [Light Reading](https://www.lightreading.com/iot/vodafone-iot-looks-to-satellites-to-connect-more-things)
- [Tele2 first Swedish operator to launch satellite IoT connectivity with Skylo](https://www.tele2.com/media/news/2025/tele2-first-swedish-operator-to-launch-satellite-iot-connectivity-with-skylo/) — Tele2, 2025 ／ [Tele2 Q4/FY2025 決算](https://www.tele2.com/investors/reports-and-presentations/tele2-reports-q4-and-fullyear-2025-results-delivering-42-efcf-growth-and-proposing-65-dividend-increase-/) 2026-01

**衛星 NTN**
- [Skylo Technologies Raises $37 Million](https://www.intelcapital.com/skylo-technologies-raises-37-million-from-intel-capital-innovation-endeavors-bmw-i-ventures-samsung-catalyst-next47-seraphim-space/) — Intel Capital, 2024-02-13 ／ [Skylo Raises $30M](https://www.skylo.tech/newsroom/skylo-raises-30m-in-oversubscribed-funding-round-to-scale-direct-to-device-satellite-service-worldwide) — Skylo, 2025-02-27
- [Sateliot Raises €100M to Scale 5G IoT Satellite Network](https://iotbusinessnews.com/2026/04/13/sateliot-raises-e100m-to-scale-5g-iot-satellite-network/) — IoT Business News, 2026-04-13 ／ [DCD(EUR 116M・公的共同出資)](https://www.datacenterdynamics.com/en/news/sateliot-launches-116-million-publicprivate-series-c-to-fund-its-constellation-deployment/) ／ [Computer Weekly](https://www.computerweekly.com/news/366641696/Sateliot-launches-100m-series-C-financing-round)
- [OQ Technology receives €25m in EIB funding](https://www.advanced-television.com/2026/02/26/oq-technology-receives-e25m-in-eib-funding/) — Advanced Television, 2026-02-26 ／ [Space Intel Report(Series B 計画)](https://www.spaceintelreport.com/satellite-iot-startup-oq-technology-13m-series-a-in-hand-series-b-planned-betting-on-open-5g-standards-over-proprietary-tech/) ／ [Via Satellite](https://www.satellitetoday.com/connectivity/2025/12/17/oq-technology-believes-semiconductor-iot-breakthrough-will-open-new-markets/) 2025-12-17
- [Starlink T-Satellite: Cost, Compatible Phones & Coverage (2026)](https://www.satelliteinternet.com/providers/starlink/starlink-direct-to-cell/) — SatelliteInternet.com ／ [Fierce Network(MWC 2026: Starlink Mobile V2)](https://www.fierce-network.com/wireless/mwc-starlink-mobile-unveils-plans-v2-satellites-and-more) 2026-03 ／ [5Gstore(T-Satellite V2)](https://5gstore.com/blog/2026/03/07/t-mobile-tsatellite-starlink-v2/) 2026-03-07 ／ [T-Mobile 公式](https://www.t-mobile.com/coverage/satellite-phone-service) ／ [TechCrunch(EchoStar USD 17B)](https://techcrunch.com/2025/09/08/spacex-strikes-17b-deal-to-buy-echostars-spectrum-for-starlinks-direct-to-phone-service/) 2025-09-08
- [AST SpaceMobile Provides Business Update and First Quarter 2026 Results](https://www.businesswire.com/news/home/20260511685431/en/AST-SpaceMobile-Provides-Business-Update-and-First-Quarter-2026-Results) — Business Wire, 2026-05-11 ／ [Light Reading](https://www.lightreading.com/satellite/ast-spacemobile-targets-intermittent-national-coverage-in-early-2026)

**市場構造・マルチプル参考**
- [The shifting sands of the IoT MVNO market landscape](https://transformainsights.com/blog/shifting-sands-iot-mvno-market-landscape) — Transforma Insights, 2024-06
- [IoT MVNOs: 290 Million Connections Managed in 2025](https://www.iotforall.com/iot-mvno-2025-report) — IoT For All, 2025
- [Current M&A Multiples Across Sectors: 2025-2026 Reference](https://ibinterviewquestions.com/guides/valuation-investment-banking/current-ma-multiples-across-sectors-2025-2026)(参考値・二次情報)
- [Digi International Acquires Particle](https://www.businesswire.com/news/home/20260127820853/en/Digi-International-Acquires-Particle-to-Accelerate-ARR-Growth-and-Strengthen-Digis-Embedded-as-a-Service-Offering) — Business Wire, 2026-01-27

> 注: 「未確認」「推定」「推測」「確認不能」と付した項目は一次情報での裏取りができていない。意思決定に用いる前に deal-desk / 外部アドバイザーでの追加検証を要する。
