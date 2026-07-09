# 戦場バーティカル調査: 現場カメラ / 車載 / ロボット / 遠隔到達性 — 2026-07-09

> 作成: market-scout ／ テーマ: コネクティビティ・ロードマップ議論 T5(バーティカル戦場)
> 位置づけ: `2026-07-09-connectivity-roadmap-briefing.md` の検証依頼(C 表 T5)への回答 + 最新動向。公開情報のみに基づく参考情報であり投資判断ではない。外部向け文書化の際は必ず人間レビューを要する。

## TL;DR(経営向け)

- ブリーフィング C 表の 4 主張は **全件「支持」**。ただし富士経済 5,729 億円は 2019 年調査・ファシリティ分野有償サービス限定の数字で、経営資料に使うなら注記必須。Ewon は直近 60 万マシン超に伸びており 50 万台は保守的。
- 現場カメラは「制度(遠隔臨場: 2022 年度から直轄土木で原則全工事)× レンタル商流」で立ち上がり済み。セーフィーは FY2025 に売上 190 億円・初の通期黒字・課金 35.4 万台に到達し、資本系列(ソニー NC・キヤノン MJ・NTT・セコム)で商流を固めている。参入余地は「自社ブランド化するレンタル会社」「i-PRO/Axis 等機器メーカーのクラウド化」側にある。
- 車載は OEM 系(トヨタ×KDDI GCP: 自動車 2,400 万台)が固く、回線選定権は「後付けドラレコ/デジタコ・保険(あいおい 200 万台等)・フリート SaaS」に分散して残る。J8 の「車載は選別受注」を裏付ける構図。
- ロボットは歩道走行(届出制)の実装が始まったが台数は小さく、中速・中型(車道 20km/h)は 2025-02 の経産省取りまとめで「3 年集中実証」段階 = 需要本格化は 2027 年以降。ドコモビジネスが ugo を再販するなどキャリアが RaaS 商流を先取りし始めた点が要警戒。
- 遠隔到達性は Ewon(HMS IDS 部門が Q4 2025 に有機成長 +28%)が「発呼型レトロフィット」の構造成長を実証。国内閉域型は KDDI CRG 8,470 円/月〜(0.5Mbps)が価格アンカーで、「数百円〜数千円のオンデマンド到達性」の空白帯が確認できた。

---

## 1. 主要ファインディング(出典付き)

### 1-1. クラウドカメラ / VSaaS 日本市場

- **市場規模**: 矢野経済研究所(2025-03 発表)は国内クラウドカメラサービスの累計稼働台数を 2023 年度 44 万台 → 2024 年度見込 54.75 万台 → **2029 年度 131 万台**と予測。監視カメラ/システム総市場は 2024 年度見込 2,252 億円 → 2029 年度 4,108 億円([OPTRONICS ONLINE, 2025-03-27](https://optronics-media.com/news/20250327/98883/))。最新の 2025-12-24 発表では総市場 2024 年度実績 2,254 億円 → **2030 年度 4,362 億円**に上方更新([矢野経済研究所, 2025-12-24](https://www.yano.co.jp/press/press.php/003982))。けん引役は VCA 画像解析とクラウドカメラサービス。
- **テクノ・システム・リサーチ(TSR)**: クラウド録画サービスの 2024 年カメラ登録台数は 528,150 台(前年比 +22%、2017 年 85,025 台比 621% 増)。ハイブリッドクラウド(GW/エッジ録画併用)で裾野拡大([セーフィー, 2025 発表](https://safie.co.jp/news/3989/))。矢野「稼働 54.75 万台(2024 年度)」と TSR「登録 52.8 万台(2024 年)」はオーダー整合。
- **セーフィー業績(FY2025・12 月期)**: 売上 190.29 億円(+26.4%)、ARR 145.23 億円(+21.7%)、リカーリング比率約 70%、課金カメラ 35.4 万台(+20.8%)、調整後営業利益 4.03 億円で**上場来初の通期黒字**([決算説明資料, 2026-02-13](https://safie.co.jp/ir/library/4748/))。
- **セーフィーの通信込みモデル**: LTE 搭載屋外カメラ「Safie GO」はレンタル月額 25,000 円(GO)/30,000 円(GO 360)/40,000 円(GO PTZ)+初期 15,000 円(税別)で、**LTE 通信費・30 日録画込み**。工事不要・電源のみで稼働([Safie GO 製品ページ](https://safie.jp/go/)、[キヤノン販売ページ](https://canon.jp/biz/product/camera/nvs/cloud-service/safie-go))。回線調達元は公開情報では**確認不能**。清水建設・アイダ設計が Safie GO 360 を全社標準導入([BUILT, 2024-02-14](https://built.itmedia.co.jp/bt/articles/2402/14/news095.html))。
- **セーフィーの資本・OEM 商流**: ソニーネットワークコミュニケーションズ、キヤノン MJ(2019-09 に 9.8 億円追加出資)、オリックス、NTT グループ、セコム、NEC キャピタル等が出資し、キヤノン MJ・セコム・NTT 東へ OEM 提供([沿革](https://safie.co.jp/company/history/)、[キヤノン, 2019-09](https://canon.jp/corporate/newsrelease/2019/2019-09/pr-safie-canon))。NTT 東「ギガらくカメラ クラウドプラン」(2018-11〜)はセーフィー提供([セーフィー, 2018-11](https://safie.co.jp/news/2582/))。→ **J9「通信選定権がエンドにない商流」を裏付け**。
- **ギガらくカメラ(NTT 東)**: 2016-04 提供開始、**累計約 14.5 万台販売(2025-03 時点)**。AI 異常検知「MIMAMORI AI」はカメラ 1 台月額 14,850 円([クラウド Watch, 2025-03-24](https://cloud.watch.impress.co.jp/docs/news/1671884.html))。
- **i-PRO**: 国内監視カメラメーカーシェア No.1 を標榜。クラウドは「みえますねっと」「i-PRO Remo.」を展開しつつ、クラウド録画はセーフィーと共同開発(第二弾 2024-02-13)([i-PRO](https://i-pro.com/products_and_solutions/ja/surveillance/newsroom/20240213))。→ 機器メーカー自身のクラウド内製は限定的で、外部プラットフォーム/回線の調達余地あり。
- **Axis**: 売上ベースで世界トップ級のネットワークカメラメーカー。アプリ基盤 ACAP をパートナーに開放([BUSINESS NETWORK](https://businessnetwork.jp/article/17928/)、[Axis](https://www.axis.com/ja-jp/about-axis))。日本ではディストリビューター/SIer 経由の箱売りが主で、通信はインテグレーター側の選定。
- **警備会社**: セコムはセーフィー出資+画像クラウド連携。ALSOK は自社「画像クラウドサービス」(最長 3 年保管、RTSP 対応で既設カメラ収容)を運用([ALSOK](https://www.alsok.co.jp/corporate/kanshi-camera/))。→ 警備系は自社閉域・自社クラウドで垂直統合。
- **建機レンタル商流**: アクティオは自社ブランドのクラウドカメラ「AktioEyes」(低遅延 0.3〜0.5 秒)や AI カメラをレンタル展開([アクティオ](https://www.aktio.co.jp/products/model/s/300449/))。カナモトは通信・計測機器レンタルでカメラを扱う([カナモト](https://www.kanamoto.co.jp/kenki/kenki16.html))。Safie GO はグリーンクロス・東電 PG 指定店等のレンタル網でも流通([Green Cross](https://products.green-cross.co.jp/rental/detail/11233/)、[東電 PG パートナーズナビ](https://www.tepco.co.jp/pg/consignment/partners/category-c/06-j.html))。→ レンタル商流は「①自社ブランド化(通信を自社調達)」「②セーフィー再販」の二形態で、**①が独立系コネクティビティの入口**。
- **遠隔臨場(国交省)**: 2022-04(令和 4 年度)から直轄土木工事で**原則全工事に本格実施**(通信環境が整わない現場は除く)。費用は技術管理費に積上げ計上 = 発注者側の予算措置あり([国交省報道発表, 2022-03-29](https://www.mlit.go.jp/report/press/content/001473363.pdf))。2024-03 には工事検査(監督・検査)向け要領も策定([国交省, 2024-03](https://www.mlit.go.jp/tec/content/001736205.pdf))。官庁営繕・自治体(茨城・埼玉・滋賀等)・下水道事業団へ横展開中。→ **仮設・屋外カメラ需要の制度ドライバーは継続**(J8 P1 戦場の前提を支持)。

### 1-2. 車載・テレマティクス

- **OEM 系(通信搭載)**: トヨタは 2018 年以降ほぼ全新型乗用車に DCM を標準搭載([Car Watch, 2018-06](https://car.watch.impress.co.jp/docs/news/1129671.html))。トヨタ×KDDI は 2016-06 に「つながるクルマ」グローバル通信プラットフォーム(GCP)を共同構築([KDDI, 2016-06-02](https://news.kddi.com/kddi/corporate/newsrelease/2016/06/02/1840.html))。KDDI の GCP は 83 の国と地域をカバーし、**KDDI のグローバル IoT 4,550 万台のうち 2,400 万台が自動車**。マツダもトヨタから DCM 供給を受け KDDI がグローバル通信を支援([KDDI Spark Journal(発行日不明)](https://tobira.kddi.com/to-global/article00075/)、[KDDI, 2020-07-14](https://news.kddi.com/kddi/corporate/newsrelease/2020/07/14/4552.html))。→ **OEM 回線はメーカー×キャリアの長期直契約で固定化**。参入は構造的に困難(J8 の「OEM ドラレコは捨てる」判断と整合)。
- **後付け(通信型ドラレコ・デジタコ)**: 矢野経済によると 2024 年度のトラック・バス向けデジタコ出荷は 78,800 台(貸切バスの装着義務化(2025-04 施行)前の駆け込み、通信型への移行進行)([矢野経済, 2025-10](https://www.yanoict.com/summary/show/id/786)、[プレス全文](https://www.dreamnews.jp/press/0000331399/))。JVC ケンウッドは通信型ドラレコを SDK 化しテレマ事業者へ供給、スマートドライブと法人向けプラットフォームで提携([JVCKENWOOD, 2020-09-14](https://www.jvckenwood.com/jp/press/2020/09/press_200914_2.html)、[提携リリース, 2021-06](https://prtimes.jp/main/html/rd/p/000000137.000045133.html))。→ **回線選定権はデバイスメーカー/サービス事業者側にあり、ここが独立系の入口**。
- **保険テレマティクス**: あいおいニッセイ同和のテレマ自動車保険は**契約 200 万台突破(2025-03-17)**([あいおい ND](https://www.aioinissaydowa.co.jp/corporate/about/news/pdf/2025/news_2025031701402.pdf))。東京海上日動「ドライブエージェント パーソナル」は法人・個人合計 100 万台超(2023-03)([東京海上](https://www.tokiomarine-nichido.co.jp/service/auto/total-assist/shohin/dap.html)、[コラム](https://www.lotascard.jp/column/future/19807/))。端末はデンソーテン等が供給し、内蔵通信のキャリアは非公表(**確認不能**)。→ 保険会社×端末ベンダーが回線をまとめて調達する「回線同梱」商流。
- **フリート管理 SaaS**: Cariot(フレクト、2016-04〜、Salesforce 基盤のリアルタイム車両管理)はシガーソケット型デバイス+回線同梱で提供([Cariot](https://www.cariot.jp/))。2024-07-26 にソラコムとフレクトが Cariot 事業の合弁会社化契約を公表(公開情報)([ニュースリリース, 2024-07-26](https://soracom.com/ja/news/20240726-1))。スマートドライブも同型。→ SaaS 事業者が回線選定権を持つ層は既に取り組み実績のある商流。
- **市場の外形**: 富士経済はコネクテッドカー世界台数を 2030 年 9,480 万台と予測、2035 年には新車販売の約 9 割がコネクテッド化([日本自動車会議所まとめ](https://www.aba-j.or.jp/info/industry/12853/))。国内商用テレマティクスは 2024 年 USD 1,681M → 2033 年 USD 6,128M(CAGR 15.5%)の外部予測([IMARC](https://www.imarcgroup.com/japan-commercial-telematics-market)、精度は要留意)。

### 1-3. ロボット

- **配送ロボ(歩道・小型低速)**: 改正道交法(2023-04-01 施行)で「遠隔操作型小型車」は届出制に。パナソニック HD が 2023-07〜08 に藤沢・丸の内で日本初の届出制運用を開始([Panasonic, 2023-08-01](https://news.panasonic.com/jp/press/jn230801-1))、2025-01-23 には日本初の「1 オペレーター・複数地域・合計 10 台同時運行」の道路使用許可を取得([Panasonic, 2025-01-23](https://prtimes.jp/main/html/rd/p/000006117.000003442.html))。Uber Eats は東京(2024-03〜)に続き大阪市のローソン店舗でも Cartken 製ロボ(時速 5.4km、夜間走行許可含む)で展開([Uber Newsroom](https://uber.com/ja-JP/newsroom/osaka-robot-2024))。→ 実装は進むが 1 オペレーター多台数化がようやく始まった段階で、**回線数の増分は当面小さい**。
- **中速・中型(車道走行)**: 経産省/NEDO の検討 WG が 2025-02-26 に「自動配送ロボットの将来像」を公表。軽自動車より小型・最高 20km/h・車道左側通行の仮説で、**直近 3 年を集中実証期間**とし関係省庁と協議するロードマップ([METI, 2025-02-26](https://www.meti.go.jp/press/2024/02/20250226002/20250226002.html))。経済効果は年約 6,600 億円と試算([自動運転ラボ, 2025](https://jidounten-lab.com/u_53325))。→ **制度化・需要本格化は 2027 年以降**。J8 の「ロボは条件付き増分」と整合。仕込みは今。
- **警備・点検ロボ**: ugo は 2025-05-27 にサンケイビル・ダイワ通信・トヨタ紡織・パーソル系等から第三者割当増資(金額非公表。2024-01 には 8.5 億円調達)([ugo, 2025-05-27](https://ugo.plus/information/press-release/2025/05/27/corpinfo/)、[創業手帳, 2024-01-31](https://sogyotecho.jp/news/20240131ugo/))。クラウドの「ugo Platform」で遠隔操作・多台数管理。**NTT ドコモビジネスが ugo を法人向けに販売**しており、キャリアが RaaS 商流(回線込み)を取りに来ている([ドコモビジネス](https://www.nttdocomo.co.jp/biz/service/ugo/))。SEQSENSE は 2023-08 に 17.9 億円調達、オフィスビル警備で稼働([創業手帳, 2023-08-21](https://sogyotecho.jp/news/20230821seqsense/))。
- **清掃・搬送ロボ**: ソフトバンクロボティクスの Whiz シリーズは 2025 年国内新規導入 3,800 台・メーカーシェア 42.2% で 1 位(富士経済「2026 年版 国内自律走行ロボット市場分析」)。新機種は Gausium ベースの OEM([SoftBank Robotics, 2026-03-23](https://www.softbankrobotics.com/jp/news/press/20260323a/))。→ 単一施設内は Wi-Fi 完結が多く(J8 の「捨てる」領域)、セルラーの出番は多拠点管理・屋外搬送に限られる。
- **家庭用ロボ**: GROOVE X「LOVOT」は本体+**月額サービス(ソフトウェア・クラウド込み、スタンダードで月 1.4 万円前後)**が必須のモデル([LOVOT 料金](https://lovot.life/pricing))。接続は無線 LAN 前提で、LTE 内蔵の有無は公開情報で**確認不能**([FAQ](https://www.pa-solution.net/as/scope3/groove-x/lovot/jp/detail.aspx?id=166))。→ 「接続がないと製品が成立しない」サブスク一体型の参考モデル。ヒューマノイド監視(J8 P4)にも同型の課金構造が予想される。

### 1-4. 遠隔到達性・産業リモートアクセス

- **HMS Networks / Ewon**: Ewon は **178 カ国・50 万台超のゲートウェイ・年間 700 万セキュア VPN 接続・接続マシン 60 万台超**を公称([HMS Industrial Remote Access](https://www.hms-networks.com/industrial-remote-access)、[ewon.biz](https://www.ewon.biz/))。Talk2M は顧客 25,000 社・45 万デバイス([HMS Talk2M](https://www.hms-networks.com/talk2m))。HMS 全社は FY2025 売上 SEK 3,577M(+17%、オーガニック +3%)・調整後 EBIT SEK 911M(利益率 25.5%)([Year-end report, 2026-01-27](https://www.globenewswire.com/news-release/2026/01/27/3226079/0/en/Year-end-report-2025-January-December.html))。Ewon を含む Industrial Data Solutions 部門は Q4 2025 売上 SEK 481M(+22%、**オーガニック +28%**、マージン約 29%)([TipRanks 決算まとめ, 2026-01](https://www.tipranks.com/news/company-announcements/hms-networks-delivers-record-2025-profit-and-bolsters-industrial-communications-portfolio))。→ レトロフィット型の発呼式遠隔保守は高収益で構造成長中。J7 テーゼを実証する存在。
- **TeamViewer**: Tensor(エンタープライズ)を OT/組込機器(Tensor Embedded)へ拡張。2025 年上期売上 €364.4M(+12%)、Enterprise は +48% YoY(1E 買収込みプロフォーマ、二次ソース)([TeamViewer Tensor](https://www.teamviewer.com/en-us/products/tensor/)、[事業まとめ(二次)](https://matrixbcg.com/blogs/how-it-works/teamviewer))。→ IT リモートの巨人が OT へ降りてくる動き。
- **remote.it**: ゼロトラスト・ポート開放不要の到達性サービス。有償プランは **USD 10/月〜(5 デバイス込み)**の低価格 SaaS 型([remote.it Pricing](https://www.remote.it/pricing))。資金調達状況は**確認不能**。
- **Tosibox / Secomea / 産業 VPN ルーター勢**: Tosibox は ISO 27001・P2P VPN 型、Secomea は IEC 62443・ゼロトラスト型で工場向け。ほか INSYS icom、MB connect line、IXON、Welotec、Moxa 等が林立し、価格は個別見積が主流([routerstore 比較, 2025](https://routerstore.com/secure-ot-remote-access-sim-antenna-connectivity/)、[Secomea](https://secomea.com/))。
- **国内閉域リモート保守の価格アンカー**: KDDI「クローズド リモート ゲートウェイ」は基本料 **月 8,470 円(0.5Mbps、税込)**〜、1Mbps 63,800 円、ドメイン使用料は 6 ドメイン目から 3,300 円/月([KDDI 料金ページ](https://biz.kddi.com/service/crg/charge/))。→ ブリーフィング J7 の「セキュア閉域型 1 万円級/月」の価格帯を公開情報で確認。数百円/台の監視型との間に**中間価格帯の空白**がある。
- **発呼型(アウトバウンド)の標準化**: Ewon Talk2M はデバイス側からのアウトバウンド VPN でファイアウォールを透過する設計([Ewon ホワイトペーパー](https://media.hms-networks.com/image/upload/v1655128538/Documents/Whitepapers/Ewon_Whitepaper_Get-started-with-Industrial-Remote-Access_EN.pdf))。Secomea・remote.it もゼロトラスト/アウトバウンド型で、**主要ベンダーの実装は発呼型が事実上の標準**。着信(固定 IP/ポート開放)型は経過需要化している。
- **市場規模の参照値**: 富士経済「リモートモニタリング有償サービス(ファシリティ分野)」2030 年予測 5,729 億円は 2019-07-09 発表の調査([富士経済](https://www.fuji-keizai.co.jp/press/detail.html?cid=20068&view_type=1&la=ja&la=en)、[日経掲載, 2019-07](https://www.nikkei.com/article/DGXLRSP514033_Z00C19A7000000/))。**7 年前の予測であり、現在値の根拠には更新調査が必要**。

## 2. 競合・プレイヤー動向(通信の選定権の所在)

| 領域 | プレイヤー | 通信の選定・供給者 | 独立系の参入余地 |
|---|---|---|---|
| クラウドカメラ | セーフィー(シェア 55.3%) | セーフィー自身が LTE 同梱(調達元非公開) | 低(垂直統合済み)。競合プラン供給の相見積り先にはなり得る |
| 〃 OEM 網 | ギガらくカメラ(14.5 万台)・セコム・キヤノン MJ | NTT 東/セコムが自社網・自社調達 | ほぼ無し(J9 のとおり構造的に困難) |
| 〃 機器メーカー | i-PRO(国内 No.1)・Axis・パナソニック コネクト | SIer・レンタル会社・ユーザー側で選定 | **中〜高(クラウド化・LTE 化の外部調達余地)** |
| 〃 レンタル | アクティオ(AktioEyes 自社ブランド)・カナモト・グリーンクロス等 | 自社ブランド機は自社調達、Safie GO 再販は Safie 同梱 | **高(自社ブランド化する会社が入口)** |
| 車載 OEM | トヨタ×KDDI GCP(車 2,400 万台)、マツダも供給網内 | メーカー×キャリア直契約 | ほぼ無し(捨てる判断を支持) |
| 後付け・保険 | JVC ケンウッド、デンソーテン、あいおい ND(200 万台)、東京海上(100 万台) | 端末メーカー/保険会社が同梱調達 | **中(端末・SaaS ベンダー経由の選別受注)** |
| フリート SaaS | Cariot、スマートドライブ等 | SaaS 事業者が同梱 | 実績ある商流(Cariot は JV 化を公表済み) |
| 配送ロボ | パナソニック HD、Uber Eats×Cartken、楽天等 | ロボ事業者が調達(遠隔監視に上り+マルチキャリア要件) | **高(制度ドリブン、台数は 2027 年以降)** |
| 警備・点検ロボ | ugo(ドコモビジネスが再販)、SEQSENSE | ロボメーカー or 再販キャリア | 中(キャリア先行に注意) |
| 産業リモートアクセス | HMS/Ewon(60 万マシン)、TeamViewer、Secomea、Tosibox、remote.it | 機械メーカー(OEM)が SIM+GW を同梱 | **高(国内は閉域 SIer 型が高価格で空白帯あり)** |

## 3. ブリーフィング主張の裏取り結果(C 表 T5 担当分)

| # | 主張 | 判定 | 根拠 |
|---|---|---|---|
| 1 | クラウドカメラ国内 131 万台(2029・矢野経済) | **支持** | 矢野経済 2025-03 発表調査: 累計稼働台数 2029 年度 131 万台(2023 年度実績 44 万台)。[OPTRONICS ONLINE, 2025-03-27](https://optronics-media.com/news/20250327/98883/)。注: 「年度」ベース。最新 2025-12-24 版リリースは台数非開示のため、更新値の有無は原本レポート([矢野 C67114700](https://www.yano.co.jp/market_reports/C67114700))で要確認 |
| 2 | セーフィーのクラウドカメラシェア 55.3%(2024・TSR) | **支持** | TSR「ネットワークカメラのクラウド録画サービス市場調査(2024)」でシェア 55.3%・8 年連続 No.1。[セーフィー公式](https://safie.co.jp/news/3989/)。注: 分母は「クラウド録画サービスのカメラ登録台数 528,150 台(2024 年)」であり、監視カメラ全体のシェアではない |
| 3 | Ewon 50 万台/178 カ国 | **支持(保守的)** | 公式サイトが「178 カ国・50 万台超ゲートウェイ・年 700 万 VPN 接続」を明記。[HMS](https://www.hms-networks.com/industrial-remote-access)。直近は「接続マシン 60 万台超」([ewon.biz](https://www.ewon.biz/))まで拡大しており 50 万台は控えめな引用 |
| 4 | 富士経済リモートモニタリング関連市場 5,729 億円(2030) | **支持(要注記)** | 2019-07-09 発表「ファシリティ分野のリモートモニタリング有償サービス」2030 年予測 5,729 億円(法人向け機械警備・空調がけん引)。[富士経済](https://www.fuji-keizai.co.jp/press/detail.html?cid=20068&view_type=1&la=ja&la=en)。**2019 年調査かつファシリティ分野限定**。全産業のリモート到達性市場の代理変数としては過小/過大の両リスクあり |
| 5 | (関連)遠隔臨場の制度 | **支持** | 2022 年度から直轄土木工事で原則全工事に本格実施、費用は技術管理費計上。[国交省, 2022-03-29](https://www.mlit.go.jp/report/press/content/001473363.pdf) |
| 6 | (関連)配送ロボ規制 | **支持** | 改正道交法 2023-04-01 施行・遠隔操作型小型車は届出制。パナソニックが届出制第 1 号運用。[Panasonic, 2023-08-01](https://news.panasonic.com/jp/press/jn230801-1) |
| 7 | (関連)J7 の「KDDI CRG 8,470 円/月〜」 | **支持** | 公式料金ページで基本料 0.5Mbps 8,470 円/月(税込)を確認。[KDDI](https://biz.kddi.com/service/crg/charge/) |
| 8 | (関連)J6 の「IIJ→セーフィー大口卸」 | **確認不能** | 公開情報では両社の回線供給関係を確認できず。セーフィー LTE 製品の回線調達元は非公表 |

## 4. SORACOM への戦略的含意

1. **現場カメラ(J8 P1)は「制度×レンタル×自社ブランド化」の三点で攻める**。遠隔臨場の発注者予算措置は継続しており需要は制度で下支えされている。セーフィー本体・OEM 網(NTT 東/セコム/キヤノン MJ)は閉じているが、(a) 自社ブランド化したいレンタル会社(アクティオ型)、(b) クラウド内製が薄い機器メーカー(i-PRO は Safie 依存、Axis は箱売り)、(c) 中堅 SIer が「SIM+クラウド+固定 IP 不要の到達性」をまとめて外部調達し得る層。大容量プランの相対提案先リスト化はこの 3 層で行うべき。
2. **車載は「選定権が残る層」だけに絞る J8 方針が正しい**。OEM(KDDI GCP 2,400 万台)は構造的にロック済み。一方、通信型ドラレコ/デジタコの端末メーカー(JVC ケンウッド SDK 供給網、デンソーテン)、保険会社の裏側、フリート SaaS は回線同梱・多数キャリア比較の商流であり、J10-①の「実名リスト」はこの層(端末メーカー×保険×SaaS)から作れる。デジタコは義務化駆け込み(2024 年度 78,800 台)の反動減に注意。
3. **ロボは「制度開放前の 2 年」が仕込み期**。歩道ロボの回線数は当面小さく、中速・中型の制度協議(3 年集中実証)が本丸。1 オペレーター多台数運行(パナ 10 台同時)は「上り映像常時+低遅延遠隔介入+閉域」という接続要件を標準化するフェーズで、ここに参照アーキテクチャを持ち込めるかが勝負。ドコモビジネス×ugo のように**キャリアが RaaS 再販で回線込み商流を先取りしている**ため、ロボメーカーとの直接の技術標準化(開発キット・帯域プラン)を急ぐ必要。
4. **到達性は「Ewon の下・KDDI CRG の下」の空白帯を取る**。Ewon は 60 万マシンで高成長・高マージン(IDS 部門オーガニック +28%)を実証したが、GW ハード前提・工場 OEM 中心。国内閉域は 8,470 円/月〜の帯域課金で中小現場には過剰。発呼型が実装標準になった今、「1 回線から・工事なし・オンデマンド」の中間価格帯(数百〜数千円/月)はグローバルでも国内でも構造的な空白であり、J7 の二枚看板(オンデマンド管理型到達性+安全な固定 IP)の妥当性を裏付ける。
5. **数字の取り扱い**: 経営資料で富士経済 5,729 億円(2030)を使う場合は「2019 年調査・ファシリティ分野有償サービス」の注記が必須。矢野 131 万台は 2025-03 調査で確度が高いが、2025-12 の更新調査で総市場が上方修正(2030 年度 4,362 億円)されており、台数予測も更新版の購読確認を推奨。

## 5. インオーガニック(M&A・出資・提携)の含意

前提: `pipeline/pipeline.yaml` は現在サンプルのみ、`research/targets/` にも既存プロファイルなし(重複なし)。以下は deal-desk への提案であり、本レポートでは追加登録しない。

| 会社/対象 | 地域 | 分野 | 注目理由 | 該当ピラー | 推奨アクション |
|---|---|---|---|---|---|
| remote.it | 米国 | ゼロトラスト到達性(SaaS、$10/月〜) | 発呼型・ポート開放不要の到達性を SaaS 化した希少な独立系。小規模で技術・チーム獲得レンジの可能性。Napter/到達性二枚看板の補完 | P2 / P5 | 規模・資本状況の初期調査(00_sourcing 提案) |
| Secomea | デンマーク | 産業リモートアクセス(IEC 62443) | 工場 OT 到達性の欧州中堅。GW ハード+クラウドの型は Ewon 型レトロフィット需要の受け皿。買収は重くても提携で欧州 OEM 商流に接続 | P2 / P4 | 提携(Partner)起点で評価 |
| ugo | 日本 | 警備・点検 RaaS | 制度ドリブンのロボ戦場(J8 P2)の中核。事業会社からの調達直後で、キャリア(ドコモ)再販が始まった今が接続レイヤーで組む最終盤の窓 | P2 / P3 | 提携(接続標準化・開発キット)+少額出資の検討 |
| SEQSENSE | 日本 | 自律警備ロボ | ビル警備での稼働実績。接続要件(上り映像・閉域)が当社の武器と合致 | P2 | モニタリング(提携打診の優先度は ugo 次点) |
| スマートドライブ | 日本 | フリート管理 SaaS/データ基盤 | JVC ケンウッド等ハード陣営と組み後付け車載の回線選定権を持つ層。Cariot 型 JV の再現可能性 | P3 | 提携可能性の整理(Build/Partner 比較) |
| 建機レンタル大手(アクティオ/カナモト等)の IoT 子会社・機器部門 | 日本 | 現場 IoT レンタル商流 | 「自社ブランド化」の通信・クラウド裏方需要。買収対象というよりチャネル提携の本命 | P3 / P4 | チャネル提携提案(plan 系商材の卸) |

- **バリュエーション相場観**: 今回の対象領域で公表マルチプルのある新規ディールは確認できず(セーフィーは上場: FY2025 売上 190 億円・時価総額は市況で変動、参照可能)。HMS の高マージン(調整後 EBIT 率 25.5%)は「到達性資産」が高収益で取引される根拠として記録。
- **セーフィーそのものは対象外扱いを推奨**: 資本系列(ソニー NC・キヤノン MJ・NTT・セコム)が濃く、ガードレール(規模・独立性)に照らして M&A 対象とせず「競合兼相見積り相手」として扱うのが妥当。

## 6. 未解決の問い

1. セーフィー LTE 製品(Safie GO)の回線調達元と契約構造 — 公開情報で確認不能。相対提案の余地判断に必要(J6 の検証課題)。
2. 矢野「131 万台(2029 年度)」の 2025-12 更新調査版での台数予測値 — レポート購読での確認を推奨。
3. 中速・中型配送ロボの法制化時期(車両区分・保安基準・免許/届出の枠組み)— 3 年実証後の省庁協議スケジュールが未確定。
4. 保険テレマ(あいおい 200 万台等)の通信契約構造 — 保険会社直契約か端末ベンダー(デンソーテン等)経由か非公表。攻略単位の特定に必要。
5. Ewon/Talk2M の国内実装台数と国内代理店経済圏 — 国別開示なし。国内レトロフィット市場の実在規模の推定材料。
6. ギガらくカメラの Safie OEM 範囲(クラウドプランのみか、LTE 版含むか)と NTT 東の回線内製度合い。

## 情報源一覧

**カメラ/VSaaS**
- [監視カメラ市場、画像解析システムが市場をけん引](https://optronics-media.com/news/20250327/98883/) — OPTRONICS ONLINE, 2025-03-27
- [監視カメラ/システム国内市場に関する調査(2025 年)](https://www.yano.co.jp/press/press.php/003982) — 矢野経済研究所, 2025-12-24 ／ [調査サマリー](https://www.yanoict.com/summary/show/id/796)
- [セーフィー「クラウド録画サービス」シェア 55.3% 獲得](https://safie.co.jp/news/3989/) — セーフィー, 2025
- [セーフィー 2025 年 12 月期 通期決算説明資料](https://safie.co.jp/ir/library/4748/) — セーフィー IR, 2026-02-13
- [Safie GO 製品ページ](https://safie.jp/go/) ／ [キヤノン Safie GO 販売ページ](https://canon.jp/biz/product/camera/nvs/cloud-service/safie-go)
- [セーフィー沿革](https://safie.co.jp/company/history/) ／ [キヤノン MJ 9.8 億円追加出資](https://canon.jp/corporate/newsrelease/2019/2019-09/pr-safie-canon) — 2019-09
- [ギガらくカメラ クラウドプラン提供(セーフィー)](https://safie.co.jp/news/2582/) — 2018-11
- [NTT 東日本 MIMAMORI AI(累計約 14.5 万台の記載)](https://cloud.watch.impress.co.jp/docs/news/1671884.html) — クラウド Watch, 2025-03-24
- [i-PRO×セーフィー共同開発第二弾](https://i-pro.com/products_and_solutions/ja/surveillance/newsroom/20240213) — i-PRO, 2024-02-13 ／ [みえますねっと](https://miemasu.i-pro.com/)
- [Axis について](https://www.axis.com/ja-jp/about-axis) ／ [BUSINESS NETWORK インタビュー](https://businessnetwork.jp/article/17928/)
- [ALSOK 防犯カメラ・画像クラウド](https://www.alsok.co.jp/corporate/kanshi-camera/)
- [アクティオ AktioEyes](https://www.aktio.co.jp/products/model/s/300449/) ／ [アクティオ クラウドカメラ](https://www.aktio.co.jp/products/model/s/50120/) ／ [カナモト 通信・計測機器レンタル](https://www.kanamoto.co.jp/kenki/kenki16.html) ／ [グリーンクロス Safie GO PTZ レンタル](https://products.green-cross.co.jp/rental/detail/11233/) ／ [東電 PG パートナーズナビ](https://www.tepco.co.jp/pg/consignment/partners/category-c/06-j.html)
- [清水建設・アイダ設計が Safie GO 360 全社標準導入](https://built.itmedia.co.jp/bt/articles/2402/14/news095.html) — BUILT, 2024-02-14
- [「遠隔臨場」を本格的に実施します](https://www.mlit.go.jp/report/press/content/001473363.pdf) — 国土交通省, 2022-03-29 ／ [遠隔臨場による工事検査 実施要領(案)](https://www.mlit.go.jp/tec/content/001736205.pdf) — 2024-03 ／ [実施要領(案) R5](https://www.mlit.go.jp/tec/content/001594449.pdf)

**車載・テレマティクス**
- [トヨタ×KDDI グローバル通信プラットフォーム](https://news.kddi.com/kddi/corporate/newsrelease/2016/06/02/1840.html) — KDDI, 2016-06-02 ／ [KDDI Spark Journal(GCP 83 カ国・車 2,400 万台)](https://tobira.kddi.com/to-global/article00075/) — 発行日不明 ／ [マツダ支援](https://news.kddi.com/kddi/corporate/newsrelease/2020/07/14/4552.html) — 2020-07-14
- [トヨタ DCM 標準搭載](https://car.watch.impress.co.jp/docs/news/1129671.html) — Car Watch, 2018-06
- [業務用車両向けテレマティクス調査(2025 年)](https://www.yanoict.com/summary/show/id/786) — 矢野経済研究所, 2025-10 ／ [プレス全文(デジタコ 78,800 台)](https://www.dreamnews.jp/press/0000331399/)
- [あいおい ND テレマ保険 200 万台突破](https://www.aioinissaydowa.co.jp/corporate/about/news/pdf/2025/news_2025031701402.pdf) — 2025-03-17
- [東京海上日動 DAP](https://www.tokiomarine-nichido.co.jp/service/auto/total-assist/shohin/dap.html) ／ [DAP 100 万台コラム](https://www.lotascard.jp/column/future/19807/)
- [JVCKENWOOD 通信型ドラレコ開発](https://www.jvckenwood.com/jp/press/2020/09/press_200914_2.html) — 2020-09-14 ／ [スマートドライブ提携](https://prtimes.jp/main/html/rd/p/000000137.000045133.html) — 2021-06
- [Cariot](https://www.cariot.jp/) ／ [Cariot 事業の合弁会社化(公開リリース)](https://soracom.com/ja/news/20240726-1) — 2024-07-26
- [コネクテッドカー普及(富士経済予測の引用)](https://www.aba-j.or.jp/info/industry/12853/) — 日本自動車会議所 ／ [IMARC Japan Commercial Telematics](https://www.imarcgroup.com/japan-commercial-telematics-market)

**ロボット**
- [届出制に基づく自動配送ロボット運用開始](https://news.panasonic.com/jp/press/jn230801-1) — Panasonic, 2023-08-01 ／ [10 台同時運行](https://prtimes.jp/main/html/rd/p/000006117.000003442.html) — 2025-01-23
- [Uber Eats 大阪ロボットデリバリー](https://uber.com/ja-JP/newsroom/osaka-robot-2024) — Uber Newsroom
- [自動配送ロボットの将来像とりまとめ](https://www.meti.go.jp/press/2024/02/20250226002/20250226002.html) — 経済産業省, 2025-02-26 ／ [経済効果 6,600 億円試算](https://jidounten-lab.com/u_53325) — 自動運転ラボ
- [ugo 第三者割当増資](https://ugo.plus/information/press-release/2025/05/27/corpinfo/) — 2025-05-27 ／ [ugo 8.5 億円調達](https://sogyotecho.jp/news/20240131ugo/) — 2024-01-31 ／ [ドコモビジネス ugo 販売ページ](https://www.nttdocomo.co.jp/biz/service/ugo/)
- [SEQSENSE 17.9 億円調達](https://sogyotecho.jp/news/20230821seqsense/) — 2023-08-21
- [ソフトバンクロボティクス 清掃ロボ国内シェア 1 位(富士経済調べ)](https://www.softbankrobotics.com/jp/news/press/20260323a/) — 2026-03-23
- [LOVOT 価格](https://lovot.life/pricing) ／ [LOVOT 接続 FAQ](https://www.pa-solution.net/as/scope3/groove-x/lovot/jp/detail.aspx?id=166)

**遠隔到達性**
- [HMS Industrial Remote Access(178 カ国・50 万 GW・年 700 万 VPN)](https://www.hms-networks.com/industrial-remote-access) ／ [ewon.biz(60 万マシン)](https://www.ewon.biz/) ／ [Talk2M(顧客 2.5 万社・45 万台)](https://www.hms-networks.com/talk2m)
- [HMS Year-end report 2025](https://www.globenewswire.com/news-release/2026/01/27/3226079/0/en/Year-end-report-2025-January-December.html) — 2026-01-27 ／ [IDS 部門 Q4 SEK 481M(+28% 有機成長)](https://www.tipranks.com/news/company-announcements/hms-networks-delivers-record-2025-profit-and-bolsters-industrial-communications-portfolio) — TipRanks, 2026-01
- [TeamViewer Tensor](https://www.teamviewer.com/en-us/products/tensor/) ／ [TeamViewer 事業まとめ(二次ソース)](https://matrixbcg.com/blogs/how-it-works/teamviewer)
- [remote.it Pricing](https://www.remote.it/pricing) ／ [Secomea](https://secomea.com/) ／ [OT リモートアクセス比較](https://routerstore.com/secure-ot-remote-access-sim-antenna-connectivity/)
- [KDDI クローズド リモート ゲートウェイ 料金](https://biz.kddi.com/service/crg/charge/)
- [Ewon Whitepaper: Get started with industrial remote access(アウトバウンド VPN)](https://media.hms-networks.com/image/upload/v1655128538/Documents/Whitepapers/Ewon_Whitepaper_Get-started-with-Industrial-Remote-Access_EN.pdf)
- [富士経済 リモートモニタリングサービス国内市場調査](https://www.fuji-keizai.co.jp/press/detail.html?cid=20068&view_type=1&la=ja&la=en) — 2019-07-09 ／ [日経掲載](https://www.nikkei.com/article/DGXLRSP514033_Z00C19A7000000/) — 2019-07

> 注: 本レポートは公開情報のみに基づく。「確認不能」と付した項目は一次情報での裏取りができていない。内容はインサイダー情報になりうるため社外持ち出し禁止。
