<header>
  <h1 align="center">Fundamental Information Technology Engineer Examination Note</h1>
</header>

- [1. コンピュータ構成要素［科目A］](#1-コンピュータ構成要素科目a)
  - [1.1. 情報の表現](#11-情報の表現)
  - [1.2. コンピュータの構成](#12-コンピュータの構成)
  - [1.3. CPU](#13-cpu)
  - [1.4. CPUの動作原理](#14-cpuの動作原理)
  - [1.5. CPUの高速化技術](#15-cpuの高速化技術)
  - [1.6. 半導体メモリ](#16-半導体メモリ)
  - [1.7. 補助記憶装置](#17-補助記憶装置)
  - [1.8. 入出力装置](#18-入出力装置)
  - [1.9. 入出力インタフェース](#19-入出力インタフェース)
- [2. ソフトウェアとマルチメディア　［科目A］](#2-ソフトウェアとマルチメディア科目a)
  - [2.1. ソフトウェア](#21-ソフトウェア)
  - [2.2. ジョブ管理とタスク管理](#22-ジョブ管理とタスク管理)
  - [2.3. 記憶管理](#23-記憶管理)
  - [2.4. ファイル管理](#24-ファイル管理)
  - [2.5. マルチメディア](#25-マルチメディア)
- [3. 基礎理論　［科目A］](#3-基礎理論科目a)
  - [3.1. 基数変換](#31-基数変換)
  - [3.2. 補数と固定小数点](#32-補数と固定小数点)
  - [3.3. 浮動小数点](#33-浮動小数点)
  - [3.4. 誤差](#34-誤差)
  - [3.5. シフト演算](#35-シフト演算)
  - [3.6. 論理演算](#36-論理演算)
  - [3.7. 半加算器と全加算器](#37-半加算器と全加算器)
  - [3.8. 計測と制御](#38-計測と制御)
  - [3.9. オートマトン](#39-オートマトン)
  - [3.10. AI](#310-ai)
  - [3.11. 線形代数](#311-線形代数)
  - [3.12. 確率と統計](#312-確率と統計)
- [4.アルゴリズムとプログラミング　［科目A・B］](#4アルゴリズムとプログラミング科目ab)
  - [4.1. アルゴリズム](#41-アルゴリズム)
  - [4.2. 配列](#42-配列)
  - [4.3. リスト](#43-リスト)
  - [4.4. キューとスタック](#44-キューとスタック)
  - [4.5. 木構造](#45-木構造)
  - [4.6. データの整列](#46-データの整列)
  - [4.7. データの探索](#47-データの探索)
  - [4.8. アルゴリズムの計算量](#48-アルゴリズムの計算量)
  - [4.9. プログラムの属性](#49-プログラムの属性)
  - [4.10. プログラム言語とマークアップ言語](#410-プログラム言語とマークアップ言語)
- [5. システム構成要素　［科目A］](#5-システム構成要素科目a)
  - [5.1. システム構成](#51-システム構成)
  - [5.2. クライアントサーバ](#52-クライアントサーバ)
  - [5.3. RAIDと信頼性設計](#53-raidと信頼性設計)
  - [5.4. システムの性能評価](#54-システムの性能評価)

## 1. コンピュータ構成要素［科目A］
### 1.1. 情報の表現
- 最小の情報量単位bit,8bitは1byteです
- pico(10<sup>-12</sup>) < nano(10<sup>-9</sup>) < micro(10<sup>-6</sup>) < mili(10<sup>-3</sup>) < kilo(10<sup>3</sup>) < Mega(10<sup>6</sup>) < Giga(10<sup>9</sup>) < Tera(10<sup>12</sup>)
- ASCII（米国標準符号、英数字・記号・制御文字）、JIS（ASCIIコード＋漢字・仮名の日本語）、EUC（UNIXやLinuxで使用、漢字・日本語）、Unicode（世界の文字の多くを一つの体系にしたもの）

### 1.2. コンピュータの構成
- コンピュータ構成： 
  - **CPU**（制御装置：記憶装置から命令を取り出し各装置に指示、演算装置：四則演算や理論演算）
  - **記憶装置**：データやプログラムの記憶
  - **入力装置**
  - **出力装置**
- プログラム記憶方式：CPUが順に取り出し、読解・実行する方式です。CPUから直接アクセス、メモリと呼ぶ

### 1.3. CPU
- プロセッサとも呼ぶ
- 性能はクロック周波数とバス幅で表現（高いほど処理能力が高い）
- **クロック周波数**：クロック信号の高低のサイクルが１秒間に繰り返される回数、単位はHz
- **バス**：コンピュータ内部でデータをやり取りするための伝送路

### 1.4. CPUの動作原理
- **レジスタ**:CPUに内蔵されている高速な記憶装置
- 命令レジスタ、命令アドレスレジスタ、指標レジスタ、基底レジスタ、アキュムレーター、汎用レジスタ
- 命令語:命令部とアドレス部で構成
- **命令実行サイクル**:命令取り出しー＞命令読解ー＞実効アドレス計算ー＞オペランド取り出しー＞命令実行ー＞演算結果格納
- **アドレス指定方法**:命令アドレス部の値から処理対象のデータが格納されている有効アドレスを求める方式
- 即値アドレス指定方式、直接アドレス指定方式、間接アドレス指定方式、相対アドレス指定方式、指標アドレス指定方式、基底アドレス指定方式

### 1.5. CPUの高速化技術 
- **逐次制御方式**:1命令ずつ順番に繰り返し実行する方式。非効率
- **パイプライン方式**:複数の命令を1ステージずつずらしながら並行処理。高速化
- **スーパーパイプライン方式**:パイプラインの細分化
- **スーパースカラ方式**:複数のパイプラインを使用して、同時に複数の命令を実行する
- **CSIC**:1回の命令で複雑な処理できる
- **RISC**:均等な命令の実行時間、パイプラインで効率よく処理
- **マルチプロセッサ**:一つのCPU内に複数のcoreがある。消費電力を抑えることと高速化の処理
- **GPU**:行列演算を持ちて3Dの画像処理を高速に実行する画像処理装置

### 1.6. 半導体メモリ
- RAM(Random Access Memory)：読み書きできるメモリ。電源切ると記憶が消える（揮発性）
  - DRAM(Dynamic RAM)：コンデンサに電荷を備えた状態か否かによって１ビットを表現。SRAMより大容量で安価。自然放電で記憶が消える。主記憶に使用
  - SRAM(Static RAM)：フリップフロップ回路で構成され高速、構造が伏在。DRAMより小容量で高価。電源供給があれば記憶が保持。キャッシュメモリに使用
  - フリップフロップ回路：二つの安定した状態を持ち、１ビットの情報を記録する回路
- ROM(Read Only Memory)：読み出し専用のメモリ。電源切っても記憶が消えない（不揮発性）
  - PROM(Programmable ROM)：書き込めるROM
  - UV-EPROM：紫外線照射で全消去
  - EEPROM：電圧をかけて部分消去
  - フラッシュメモリ：電圧で全消去・部分消去
- キャッシュメモリ：主記憶よりも高速で、CPUと主記憶の間に配置するメモリ。
  - 実効アクセス時間：キャッシュメモリのアクセス時間ｘヒット率＋主記憶のアクセス時間ｘ（１－ヒット率）
    - ヒット率：アクセスするデータがキャッシュメモリに存在する確率。その逆の場合はNFP(Not Found Probability)
  - 1次キャッシュと2次キャッシュ（Ｌ１、Ｌ２）：主記憶のアクセス時間とＣＰＵの処理時間の差が大きい場合は多レベルのキャッシュ構成する
  - ライトスルー方式：キャッシュメモリと主記憶の両方を書き込む方式。
  - ライトバック方式：キャッシュメモリだけ書き込み、主記憶にはデータがキャッシュメモリから追い出されるときに書き込む方式
- メモリインタリーブ：主記憶装置を複数の区画に分け、連続するアドレスの内容を並列アクセスすることで、高速化を図る方式
- アクセス速度・容量の順番：レジスタ＜L1＜L2＜主記憶＜SSD＜HDD

### 1.7. 補助記憶装置
- **主記憶装置と補助記憶装置の違い**：主記憶装置は高速で小容量、補助記憶装置は低速で大容量、不揮発性。「主記憶を補う」という意味で補助記憶装置と呼ばれる
- **磁気ディスク装置（HDD:Hard Disk Drive）**：磁性体を塗った円盤状のディスクにデータが記録され、磁気ヘッドを移動させながらデータをよみかきする装置です。
  - 構造：セクタ、トラック、シリンダ、ヘッド
  - アクセス時間：CPUがデータの読み書きを要求してから、データが読み書きできるまでの時間（シーク時間＋回転遅延時間＋データ転送時間）
  - フラグメンテーション：データの追加・削除を繰り返すと、データが断片化してしまう現象（逆の場合はデフラグメンテーション）
- **フラッシュメモリ**：電気的にデータを消去・書き込みできる半導体メモリ。消費電力が少なく、耐久性が高い。SSD（Solid State Drive）に使用(SDHC:32GB、SDXC:2TB)
- **SSD（Solid State Drive）**：フラッシュメモリを使用した補助記憶装置。HDDより高速、消費電力が少ない、耐久性が高い
- **光ディスク**：レーザ光を使ってデータを読み書きする装置。(CD:700MB、DVD:17.08GB、BD:100GB)

### 1.8. 入出力装置
- **入力装置**：音声や画像のデータをコンピュータに入力したり、コンピュータに指示を与えたりする装置
  - バーコードリーダ：商品などに印字されたバーコードを読み取る装置
  - POSシステム：バーコードを使って商品の情報を読み取り、売上情報を管理するシステム
  - RFID：極小のICチップとアンテナを組み合わせたタグを使って、物品の識別や位置情報の取得を行う技術
- **出力装置**：コンピュータの処理結果を人間が理解できる形で出力する装置
- **ディスプレイ**:
  - 液晶ディスプレイ：液晶パネルを光源の裏に配置し、液晶パネルの前面に光を透過させて表示する方式
  - 有機ELディスプレイ：有機材料を用いて発光するディスプレイ、バックライトが不要で薄型化が可能
    - 解像度：画面の表示能力を表す指標。画面の横方向と縦方向のドット数で表現。このどっとは画素やピクセルとも呼ばれる
    - VRAM：ビデオメモリ。ディスプレイに表示するためのデータを一時的に保存するメモリ。
- **プリンタ**:
  - ドットインパクトプリンタ：プリンタヘッドにピンを打ち込んで紙にインクを飛ばす方式
  - レーザプリンタ：トナーを使って紙に文字や図形を印刷する方式
  - ドットインクジェットプリンタ：インクを紙に吹き付けて印刷する方式

### 1.9. 入出力インタフェース
- USB(Universal Serial Bus)：コンピュータと周辺機器を接続する標準的なシリアルインタフェース。最大127台の機器を接続可能
  - USB1.1：12Mbps、USB2.0：480Mbps、USB3.0：5Gbps、USB3.1：10Gbps,USB3.2：20Gbps
  - ホットプラグ：電源を入れた状態で周辺機器を接続・取り外しできる機能
  - バスパワー：USBケーブルを通じて電力を供給する機能
  - HDMI：映像と音声をデジタル信号で伝送するインタフェース 
  - Bluetooth：免許不要の2.4GHz帯の無線通信規格。半径１００ｍ程度の範囲で最大速度は２４Mbps
  - BLE（Bluetooth Low Energy）：消費電力が少ないBluetoothの規格
  - ZigBee：免許不要の2.4GHz帯の無線通信規格。最大速度は250kbps、低コスト、低消費電力、短距離通信
  
## 2. ソフトウェアとマルチメディア　［科目A］
### 2.1. ソフトウェア
- **OS**:ハードウェアやアプリケーションソフトウェアを管理・制御するソフトウェアです
  - **制御プログラム**:ハードウェア資源状態を常に監視、コンピュータの効率的な利用を実現するソフトウェア群
  - 主な機能：ジョブ管理、タスク管理、記憶管理、ファイル管理、入出力管理、ユーザインタフェース
  - ハードウェア→OS→ミドルウェア→アプリケーションソフトウェア
  - API(Application Programming Interface)：OSが提供する機能をアプリケーションソフトウェアが利用するためのインタフェース
- OSS(Open Source Software)：ソースコードが公開されているソフトウェア
  - 最低条件：頒布先となる個人やグループや利用部やを制限しない、再頒布で追加ライセンスを要求しない、特定製品に限定したライセンスにしない
  - ディストリビュータ：OSSを配布する組織
  - OSSのライセンス：GPL（GNU General Public License）、BSD（Berkeley Software Distribution）、Apache License、MIT License
  - BSDライセンス：無保証で、改変後の再頒布の際に元のソフトウェアの著作権表示部分やライセンス条文は残すこと
  - GPLライセンス：ソフトウェアの再頒布時に、ソースコードを公開することを義務付けるライセンス、コピーレフトの制約がある

### 2.2. ジョブ管理とタスク管理
- **ジョブとタスク**：利用者から見た仕事の単位、タスクはOSから見た仕事の単位
- **ジョブ管理**:複数のジョブを効率よく処理するための管理
  - ジョブスケジューリング：ジョブの実行順序を決定すること
  - バッチ処理：一定量のデータをまとめて処理する方式
  - ジョブキュー：ジョブの実行順序を決定するための待ち行列
  - スプーリング：ジョブの出力結果を一時的に保存しておくこと
- **タスク管理**:実行可能状態（Ready）、実行状態（Running）、待機状態（Waiting）状態を持つ
  - タスクの状態遷移：タスク生成→実行可能状態→実行状態→待ち状態→終了状態
  - タスクスケジューリング：到着順、処理時間順、優先度順、ラウンドロビン方式がある
  - マルチタスク：複数のタスクにCPUの処理時間を順番に割り当てるで、タスクが同時に実行されているように見せる技術
  - 割り込み処理：CPUが実行中のタスクを中断して、別のタスクを実行すること
    - 内部割り込み：CPU内部で発生する割り内部割り込み、例：ゼロ除算、オーバーフロー
    - 外部割り込み：CPU外部で発生する割り込み、例：キーボード入力、マウス操作

### 2.3. 記憶管理
- **プログラム記憶方式**:プログラムを主記憶に読み込んで置き、CPUが順次読み出し実行する方式
- **実記憶管理**：
  - 区画方式：主記憶を幾つかの区画に分割し、プログラムに割り当てる方式
  - 固定区画方式：あらかじめ決まった大きさの区画に分割する方式。効率悪いが処理速度が一定
  - 可変区画方式：プログラムの大きさに応じて区画の大きさを変える方式。効率が良いが処理速度が一定でない
  - フラグメンテーション：OSが主記憶の領域の獲得と解放を繰り返して、領域が断片化する現象
  - メモリコンパクション：未使用領域を連続した一つの領域にまとめること
  - スワッピング方式：主記憶の一部を補助記憶装置に移動する方式。主記憶容量不足時に使用不足
  - オーバレイ方式：あらかじめプログラムを同時に実行しない排他的な部分に分割し、必要な部分だけを主記憶に読み込む方式
- **仮想記憶方式**:プログラムを仮想記憶空間に格納しておき、実行時に必要なプログラムやデータを動的に配置して実行する方式
  - 動的アドレス変換機構：プログラムが実行される際に、仮想アドレスを物理アドレスに変換する機構 
  - ページング方式：主記憶と補助記憶をページと呼ばれる固定長のブロックに分割し、プログラムをページ単位で管理する方式
  - ページフォルト：プログラムが必要なページが主記憶にない場合、補助記憶から主記憶に読み込む割り込むが発生する現象
  - スラッシング：ページフォルトが多発すると、処理効率が急激に低下する現象が発生すること
  - ページ置き換えアルゴリズム：
    - FIFO方式：最も古いページを置き換える方式
    - LRU方式：最後に参照されてから最も経過時間が長いページを置き換える
    - LFU方式：最も参照回数が少ないページを置き換える
    - 
### 2.4. ファイル管理
- **ディレクトリ**:ファイルを管理するためのデータ構造
  - パス指定：
    - 絶対パス：ファイルやディレクトリの位置を、ルートディレクトリからの位置で指定する方法
    - 相対パス：現在のディレクトリを基準にして、ファイルやディレクトリの位置を指定する方法
- **データのバックアップ**：
  - フルバックアップ：全てのデータをバックアップする方法
  - 差分バックアップ：前回のフルバックアップ以降に変更されたデータだけをバックアップする方法
  - 増分バックアップ：前回のバックアップ以降に変更されたデータだけをバックアップする方法

### 2.5. マルチメディア
- **静止画・動画**
    - 圧縮：データサイズを小さくする
    - 解凍：圧縮されたデータを元に戻す
    - 静止画：
      - ＢＭＰ：Windows標準。圧縮されないためファイルサイズが大きい
      - ＧＩＦ：256色までの色を使うことができる。アニメーション表示が可能
      - PNG：256とフルカラーの両方の色を使うことができる。部分透過処理が可能。可逆圧縮
      - ＪＰＥＧ：フルカラーの色を使うことができる。国際標準規格。不可逆圧縮
    - 動画：
      - MPEG：国際標準規格。不可逆圧縮
- **マルチメディアの応用**
  - CG:コンピュータを使って画像を処理・生成する技術、またその画像のこと
  - アンチエイリアシング：曲線などギザギザをなくす処理
  - テクスチャマッピング：表面に柄や模様を貼り付ける技術
  - シャーディング：影つけ、立体感を出す
  - レイトレーシング：光の反射、屈折を計算してリアルな画像を生成する技衧
  - クリッピング：画面外の部分を切り取る処理
  - モーフィング：滑らかに変形させる処理
  - レンダリング：情報を計算によって映像化
  - ポリゴン：立体の形状を表現するための基本要素
  - モーションキャプチャ：センサーを使って人間の動きをデータ化する技術
  - ソリッドモデル：物体の内部の詰まった部分を表現するためのモデル
  - ワイヤーフレーム：物体の外形を線で表現するモデル
  - サーフェスモデル：面や曲面で物体を表現するモデル
  - 隠線消去：隠れている線を消す処理
  - メタボール：複数の物体を一つの物体に見せる処理
  - ラジオシティ：相互反射を考慮し物体の明るさを計算する処理
  - バーチャルリアリティ：仮想の空間に入れ込んだような効果を生み出す技術
  - AR（Augmented Reality）：現実世界にコンピュータで生成した情報を重ね合わせる技術

## 3. 基礎理論　［科目A］
### 3.1. 基数変換
- **進数**:
  - **２進数**：0と1の２つの数字を使って数を表現する方法
  - **８進数**：0から7までの８つの数字を使って数を表現する方法。1,2,3,4,5,6,7,10,11,12,13,14,15,16,17,20
  - **１６進数**：0から９までの数字とAからFまでの６つのアルファベットを使って数を表現する方法。1,2,3,4,5,6,7,8,9,A,B,C,D,E,F,10,11,12,13,14,15,16,17,18,19,1A,1B,1C,1D,1E,1F,20
- 基数と重み対応表
  - 基数とは各桁の重み付けの基本となる数です
  - ... N<sup>2</sup>, N<sup>1</sup>, N<sup>0</sup>, N<sup>-1</sup>, N<sup>-2</sup>, N<sup>-3</sup>...
- N進数から10進数への基数変換
  - 例：(101.101)<sub>2</sub> = 1x2<sup>2</sup> + 0x2<sup>1</sup> + 1x2<sup>0</sup> + 1x2<sup>-1</sup> + 0x2<sup>-2</sup> + 1x2<sup>-3</sup> = 5.625
- 10進数からN進数への基数変換
  - 例：(13)<sub>10</sub>: 13/2 = 6 余り1, 6/2 = 3 余り0, 3/2 = 1 余り1, 1/2 = 0 余り1 → (1101)<sub>2</sub>
  - 例：(0.375)<sub>10</sub>: 0.375x2 = 0.75, 0.75x2 = 1.5, 0.5x2 = 1.0 → (0.011)<sub>2</sub>
- 2進数と８進数・１６進数の変換
  - ２進数３桁を８進数１桁に変換する場合、２進数を３桁ずつ区切り、それぞれを８進数に変換する
  - ２進数４桁を１６進数１桁に変換する場合、２進数を４桁ずつ区切り、それぞれを１６進数に変換する

### 3.2. 補数と固定小数点
- **補数**:
  - コンピュータ内部で負数を表現するための方法
  - ２の補数：符号ビットを反転させ、１を加える
- **固定小数点**:小数点の位置を決められた場所に固定して表現する形式

### 3.3. 浮動小数点
- **浮動小数点**:実数（小数点の付いた数）を扱う場合に使用する形式
  - 例：(1.101x2<sup>3</sup>)<sub>2</sub> = 1.101x2<sup>3</sup> = 1101.0 = 13.0
  - 指数部の値によって、小数点の位置が移動する
- 浮動小数点の形式：
  - **固定小数点形式**：小数点の位置が固定されている形式
  - **浮動小数点形式**：指数部と仮数部に分けて表現する形式
  - **IEEE754形式**：浮動小数点数を表現するための標準規格
    - 32ビット：符号部1ビット、指数部8ビット、仮数部23ビット
    - 64ビット：符号部1ビット、指数部11ビット、仮数部52ビット
    - 80ビット：符号部1ビット、指数部15ビット、仮数部64ビット
  - バイアス：実際の数値に一定の数値を加えることで、実際の数を127足して表現する方法

### 3.4. 誤差
- **誤差**:真の値と表現する値との間に差が発生
  - 桁あふれ誤差：演算結果がコンピュータの表現できる範囲を超えることで発生する誤差（オーバフロー）
  - アンダフロー：０に近い値を表現する際に、表現できる範囲を超えることで発生する誤差
  - 丸め誤差：指定された桁数で演算結果を表すために、切り捨て、切り上げ、四捨五入などを行うことで発生する誤差
  - 桁落ち誤差：絶対値がほぼ等しい数値の間に、同符号の減算や異符号の加算をしたときに、有効桁数が減ることで発生する誤差（有効桁数が減少することで発生する誤差）
    - 例：(1.23456789 - 1.23456788) = 0.00000001 → 0.00000000
  - 情報落ち誤差：絶対値の差が非常に大きい数値の間で加減算を行ったときに、絶対値の小さい数値が計算結果に反映されないことで発生する誤差（小さな数値が計算結果に反映されないことで発生する誤差）
    - 例：(1000000000 + 0.00000001) - 1000000000 = 0.00000000
  - 打切り誤差：浮動小数点数の計算処理の打切りを、指定した規則で行うことによって発生する誤差

### 3.5. シフト演算
- **シフト演算**:２進数の場合、左右にビットをずらして、乗算や除算の演算を行うこと
  - nビット左シフト：2<sup>n</sup>倍
  - nビット右シフト：2<sup>-n</sup>倍
- **論理シフト**:符号を考慮しないシフト演算
  - あふれたビットは捨てる、空いたビットは０で埋める
- **算術シフト**:符号を考慮したシフト演算
  - 算術左シフト：符号ビットはそのままの位置に、あふれビットは捨てられ、空いたビットには０が入れる
  - 符号ビットはそのまま
  - あふれたビットは捨てられる
  - 空いたビットは０で埋められる

### 3.6. 論理演算
- **論理演算**:
  - 論理和OR[+]、論理積AND[・]、否定NOT[-]
- **論理演算の組合せ**:
  - 排他的論理和XOR、否定論理積和NAND、否定論理和積NOR
- **ビット演算**
  - ビット列の取出し：特定のビットを取り出すには、取り出したいビットと１で論理積をとる
  - ビットの反転：反転させたいビットと１で排他的論理和をとる

### 3.7. 半加算器と全加算器
- **加算器**:２進数の加算を行う回路
  - **半加算器**:二つの２進数を加算して、同桁の値（S）と桁上がり（C）を出力する加算器
    - 排他的論理和（C）と論理積（S）の組合せで実現
  - **全加算器**:下位桁からの桁上がりと上位桁への桁上がりを考慮した加算器
    - ２つの半加算器と論理和回路を組み合わせ論理和

### 3.8. 計測と制御
- **アナログとデジタル**:
  - **アナログ**:連続的に変化する情報
  - **デジタル**:連続するアナログデータを細か区切って０，１に置き換えた不連続な情報
  - **A/D変換**:アナログデータをデジタルデータに変換すること
    - アナログデータより、加工、編集、検索しやすくノイズに強い
- PCM伝送方式：アナログの音声信号をデジタル符号に変換する方式。標本化→量子化→符号化
  - 標本化：時間的に連続したアナログ信号の波形を、一定の時間間隔で測定すること。サンプリングとも呼ばれる。
    - サンプリング周波数Hz：1秒間に行う標本化の回数
  - 量子化：測定した信号をあらかじめ決められた一定の間隔に対応した整数の近似値に変換すること
  - 符号化：量子化された値を２進数のデジタル符号に変換すること
- **制御技術**
  - フィードバック制御：環境など外部の作用の影響をセンサで検知し、コンピュータが半出して修正動作を行う制御
  - フィードフォワード制御：外乱があらかじめ予測できる場合、前もって必要な修正動作を行う制御
  - シーケンス制御：あらかじめ定められた順序または条件に従って、制御の各段階を逐次進めて行く制御
  - PWM制御：モータの回転速度やLEDの明るさなどをデジタル信号で制御する方式
- **クロック信号**：デジタル回路やコンピュータシステムにおいて、定期的に変化する信号を指します。この信号は通常、矩形波で表現され、高いレベル（High）と低いレベル（Low）を交互に繰り返します。クロック信号は、システム内の動作やデータの同期に使用されます。たとえば、CPUの動作を制御したり、データの読み書きのタイミングを決定したりするために使用されます
- **電力量**はワット時間（Wh）

### 3.9. オートマトン
- **オートマトン**: 現在の状態と入力によって、出力が決定される機械をモデル化したもの。最終的に終了状態になるものを有限オートマトン。オートマトンの状態の遷移を図にしたものが状態遷移図、表は状態遷移表

### 3.10. AI
- **AI**：(Artificial Intelligence) 人が行うような学習や認識、予測、判断などの知識的な活動を、コンピュータにさせる取り組みやその技術のこと
- **機械学習**：大量のデータをコンピュータに解析させ、コンピュータが予測や判断などができるように学習させること
  - 教師あり学習：あらかじめ万代と正解をコンピュータに提示、誤りを指摘したりすることで、コンピュータがそれらの特徴を楽手する
  - 教師なし学習：コンピュータ自らが、統計的性質やある種の条件に従い、データのグループ分けや、情報の集約を行うこと
  - 強化学習：試行錯誤を通して、報酬が最も多く得られるこうな方策を学習すること
- **ディープラーニング**：人の脳神経回路を模倣したモデルで解析し、AI自らがデータを判別するための特徴を探し出すこと

### 3.11. 線形代数

### 3.12. 確率と統計
- **確率**：ある事象が起こる可能性の度合い
  確率＝（事象の数）/（全事象の数）
- **順列**: n個の中からr個を取り出す場合の並べ方
  nPr = n! / (n-r)!
- **組み合わせ**: n個の中からr個を取り出す場合の組み合わせ
  nCr = nPr / r! = n! / r!(n-r)!
- **統計**
  - メジアン（中央値）
  - モード（最頻値）
  - レンジ（範囲）
  - 分散：平均値からのばらつきを表し、偏差（平均値との差）の2乗の総和の平均値
  - 標準偏差：分散の平方根
- 正規分布：平均値を中心に左右対称の釣鐘型の分布

## 4.アルゴリズムとプログラミング　［科目A・B］
### 4.1. アルゴリズム
- **アルゴリズム**：何らかの問題を有限の時間で解くための手順や方法
- **変数**:データを格納するためのメモリ領域
- **フローチェーとと疑似言語**:アルゴリズムを図や文章で表現したもの
  - 端子：処理の開始と終了を表す
  - 処理：データの加工や計算を行う
  - 判断：条件によって処理を分岐する
  - ループ：同じ処理を繰り返す
  - 線：処理の流れを表す
  - **アルゴリズムの制御構造**：
    - 順次処理：上から下に処理を行う
    - 分岐処理：条件によって処理を分岐する（双分岐、多双分岐、多分岐）
    - 繰り返し処理：同じ処理を繰り返す（前判定、後判定）
  - 疑似言語
    - 〇関数名
    - 型名：変数名
    - /* 注釈 */
    - 変数名←式
    - if （条件式）処理１
      elseif (条件式)　処理２
      else　処理３
      endif
    - while (条件式)　処理
      endwhile
    - for （制御記述）　処理
      endfor

### 4.2. 配列
- **データ構造**:データを効率よく管理するための方法。リスト、配列、スタック、キュー、木構造など
- **配列**:同じデータ型のデータをまとめて格納するためのデータ構造
  - 一次元配列：データを一列に並べたもの（T（要素番号））
  - 二次元配列：データを行と列に並べたもの（T（行、列））

### 4.3. リスト
- **リスト**:データを記録するデータ部とデータの格納一を示すポインタ部で構成されるデータ構造
  - リスト構造の種類：単方向リスト、双方向リスト、循環リスト
  - 配列とリスト構造の比較：
    - 配列：連続格納領域に順番通りに格納、総データ数が先に決定、挿入削除は後ろのデータもずらす必要がある、要素番号ですぐにアクセスできる
    - リスト：非連続格納領域に格納、データ数が後から追加可能柔軟に変更可能、前後のポインタのみ修正するので勝利時間小、要素番号ではなくポインタでアクセス

### 4.4. キューとスタック
- **キュー**:格納した順序でデータを取り出すことができるデータ構造（FIFO）
  - キューの操作：エンキュー（データの追加）、デキュー（データの取り出し）
- **スタック**:買う脳した順序とは逆の順序でデータを取り出すことができるデータ構造（LIFO）
  - スタックの操作：プッシュ（データの追加）、ポップ（データの取り出し）

### 4.5. 木構造
- **木構造**:階層の上位から下位に節点をたどることによって、データを取り出すことができるデータ構造
- ２分木の種類：すべての枝の分岐が二つ以下である木構造
  - 完全二分木：根から葉までの深さがすべて等しい２分木
  - 二分探索木：各節において、左の子＜親＜右ノ子お関係を持つ２分木
  - ヒープ：各節において、親＜子、または、親＞子という関係を持った完全２分木
  - 逆ポーランド記法：数式の記述方法の一つで、演算子を被演算子の後に記述する表記法

### 4.6. データの整列
- **整列**:ある規則に従ってデータを並べ替えること（ソート）
- **体表的な整列法**:
  - 基本交換法（バブルソート）：隣り合うデータを比較して、大小関係が逆なら交換する
    - 基本交換法の比較回数：n(n-1)/2
  - 基本選択法（選択ソート）：最小値を選んで、最初のデータと交換する
    - 比較回数：n(n-1)/2
  - 基本挿入法（挿入ソート）：未整列のデータを整列済みのデータに挿入する
    - 比較回数：n(n-1)/2
- **そのほかの整列法**:
  - シェルソート：データを一定間隔でグループ分けし、それぞれのグループを整列する
  - クイックソート：データを基準値を使って分割し、それぞれのグループを整列する
  - マージソート：データを分割し、それぞれのグループを整列し、結合する
  - ヒープソート：データをヒープ構造に整列し、整列済みのデータを取り出す
  - バケットソート：データを複数のバケットに分け、それぞれのバケットを整列する
  - カウントソート：データの最大値を求め、それを基準にデータを整列する

### 4.7. データの探索
- **探索**:配列などを使って目的のデータを探し出すこと
  - 線形探索：配列の先頭から順番にデータを比較して探す方法
  - 番兵法：探索したい目的のデータを配列の最後尾に追加する方法
    - 線形探索法の探索回数：平均（n+1）/2
  - ２分探索法：探索範囲を半分に絞り込みながら目的のデータを探索する方法
    - 探索回数：平均log<sub>2</sub>n
  - ハッシュ探索法：目的のデータの格納先のアドレスを、ハッシュ関数を用いて算出して探索方法
    - 格納先のアドレスが衝突してしまうことをシノニムという
    - 探索回数：１回

### 4.8. アルゴリズムの計算量
- **計算量（オーダー）**:データ量の増加に対して、アルゴリズムの実行時間がどれくらい増加するかを割合で表した指標
- **オーダー表記**
  - O(1)：定数オーダー（ハッシュ探索法）
  - O(n)：線形オーダー(線形探索法)
  - O(n<sup>2</sup>)：二重線形オーダー
  - 基本交換法、基本選択法、基本挿入法：O(n<sup>2</sup>)
  - O(log<sub>2</sub>n)：対数オーダー（２分探索法）

### 4.9. プログラムの属性
|再配置可能（Relocatable）|主記憶上のどのアドレスに配置しても、実行できる|
|:-|:-|
|再入可能（Reentrant）|複数のプログラムから同時に呼び出しても、問題なく実行できる|
|再使用可能（Reusable）|一度実行した後、ロードし直さずに再び実行を繰り返しても、正しい結果が得られる|
|再帰的（Recursive）|自分自身を呼び出すことができる|

### 4.10. プログラム言語とマークアップ言語
- **プログラム言語**:コンピュータが理解しやすい機械語またはそれに近い形式で記述した低水準言語と、人間が理解しやすい自然言語に近い形式で記述した高水準言語とがある
  - 低水準言語：機械語、アセンブリ言語
  - 高水準言語：C言語、Java、Python
- **言語プロセッサ**:人が理解できるプログラム言語で記述した原始プログラムを、コンピュータが理解できる機械語に翻訳するためのプログラム
  - アセンブラ：アセンブリ言語を機械語に翻訳する
  - コンパイラ：高水準言語を機械語に一括して目的プログラムに翻訳する
  - インタプリタ：高水準言語を機械語に逐次翻訳して実行する
- **プログラムの実行手順**：原始プログラム→コンパイラ→目的プログラム→リンカ→ロードモジュール実行プログラム
  - コンパイル：原始プログラムから目的プロクラムを生成する
  - 字句解析→構文解析→意味解析→最適化→コード生成
  - リンク：リンか（リンケージエディタ）を用いて、複数の目的プログラムなどから、一つのロードモジュールを生成する
  - ロード：ローダ（ローダプログラム）を用いて、ロードモジュールを主記憶に読み込み、実行する
- **形式言語**
  - BNF（Backus-Naur Form）：プログラム言語の文法を定義するための形式言語
- **マークアップ言語**:文書の構造や意味を記述するための言語
  - SGML（Standard Generalized Markup Language）：電子文書の管理。HTMLやXMLの元となった言語
  - HTML（HyperText Markup Language）：Webページの構造を記述するための言語
  - XML（eXtensible Markup Language）：利用者独自のタグを定義できる言語


## 5. システム構成要素　［科目A］
### 5.1. システム構成
- ミッションクリティカルシステム：システムが停止すると、重大な事故や損失が発生するシステム
- デュプレックスシステム：現用系と待機系の２つのシステムを用意し、現用系が故障した場合に待機系に切り替えるシステム
  - ホットスタンバイHot stanby：待機系をいつでも動作できる状態で待機させ、障害発生時にはすぐに切り替える。同じシステム同時に起動している
  - コールドスタンバイCold standby：待機系を停止状態で待機させ、障害発生時には起動して切り替える。同じシステムを別々に起動している
  - バッチ処理：一定の単位でまとめて処理を行う方式
- デュアルシステム：二つのシステムで構成され、同じ処理を同時に行い、結果を比較して正常なものを採用するシステム
- クラスタシステム：複数のサーバをクラスタとしてまとめ、負荷分散や冗長化を行うシステム
  - HAクラスタ：可用性を高めることで、高信頼化を目的とするシステム構成
  - HPCクラスタ：高性能かを目的とするシステム構成
- グリッドコンピューティング：ネットワークを介して複数のコンピュータを連携させることで、仮想的に１台の巨大で高性能なコンピュータをつくる技術

### 5.2. クライアントサーバ 
- **集中処理と分散処理**:集中処理は、一つのコンピュータで全ての処理を行う方式。分散処理は、複数のコンピュータで処理を分担して行う方式
- **クライアントサーバシステム**：クライアントとサーバという役割を分担して処理を行う方式
  - 3層クライアントサーバ：理論的にプレゼンテーション層、ファンクション層、データベース層の３層構造に分離したアーキテクチャ。APサーバをWebサーバに加えると４層クライアントサーバとなる
    - ストアドプロシージャ：利用頻度の高い命令群をあらかじめサーバ上に用意しておくことで、ネットワーク負荷を軽減できる
- **サーバの仮想化**：１台の物理サーバを複数の仮想サーバを動作させたり、複数の物理的なマシンを一つのサーバとして扱ったりするための技術
  - 仮想化の形態：ホスト型、ハイパーバイザ型、コンテナ型
- **シンクライアントシステム**：サーバ上でアプリケーションやデータを集中管理することで、クライアント端末には必要最低限の機能しかもたせないシステム
  - VDI（Virtual Desktop Infrastructure）：クライアント端末のデスクトップ環境を仮想化されたサーバ上に集約して、サーバ上で稼働させる仕組み

### 5.3. RAIDと信頼性設計
- **RAID**:複数の磁気ディスクを組合せ、１台の仮想的な磁気ディスクとして扱うことで、アクセスの高速化や信頼性を実現する技術
  - RAID0：データを分割して複数のディスクに書き込む方式。高速化が図れるが信頼性は低い（ストライピング）
  - RAID1：磁気ディスク２台に同じデータを書き込む。信頼性が高いが、容量効率が悪い（ミラーリング）
  - RAID3：データをビット/バイト単位に複数の磁気ディスクに分散して書き込む。（データを分散、パリティは１台に固定）
  - RAID5：データをブロック単位に複数の磁気ディスクに分散して書き込む。（データ・パリティとも分散）
- **信頼性設計**:
  - フォールトアボイダンス（故障回避）：構成要素の信頼性を高め、故障を回避する設計
  - フォールトトレランス（故障許容）：構成要素を冗長化し、故障が発生しても必要な機能は維持する設計
  - フェールセーフ（故障安全）：システムの一部が故障しても、危険が生じないような構造や仕組みを導入する設計。故障した時は、安全重視
  - フェールソフト（故障軟化）：故障が発生した場合、一部のサービスレベルを低下させても、稼働を継続する設計。故障しても、サービスを継続重視
  - フールプルーフ（誤操作防止）：誤操作が発生しないように、設計や仕組みを工夫する設計

### 5.4. システムの性能評価
- **性能指標**　
  - スループット：単位時間あたりに処理できるデータ量
  - ターンアラウンドタイム：利用者が処理を依頼してから、結果の出力が終了するまでの時間。
  - レスポンスタイム：利用者が処理を依頼してから、端末に処理結果が表示されるまでの時間
  - ベンチマークテスト：システムの使用目的に合った標準的なプログラムを実行させ、その測定数値から処理性能を相対的に評価する方法（基準）
- MIPS（Million Instructions Per Second）：１秒間に百万回の命令を実行できる性能を表す指標
  