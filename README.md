# waranalyze
戦争の分析

以下は `war.dot` の各要因カテゴリを個別に示した図です。図中のノードはクリックで元の参考ページ（主に Wikipedia）に遷移します。

## 技術的要因

```mermaid
graph LR
  E10_20["マンハッタン計画開始<br>1942.5.12"]
  E10_30["ナチスドイツの原爆懸念"]
  E10_40["ドイツ 核分裂発見 1938"]
  E10_00["原爆完成<br>1945.7.16"]

  E10_40 --> E10_30
  E10_30 --> E10_20
  E10_20 --> E10_00

  %% Links
  click E10_40 "https://ja.wikipedia.org/wiki/%E6%A0%B8%E5%88%86%E8%A3%82%E3%81%AE%E7%99%BA%E8%A6%8B" "核分裂発見（ドイツ）"
  click E10_20 "https://ja.wikipedia.org/wiki/%E3%83%9E%E3%83%B3%E3%83%8F%E3%83%83%E3%82%BF%E3%83%B3%E8%A8%88%E7%94%BB" "マンハッタン計画"
  click E10_00 "https://ja.wikipedia.org/wiki/%E3%83%9E%E3%83%B3%E3%83%8F%E3%83%83%E3%82%BF%E3%83%B3%E8%A8%88%E7%94%BB" "原爆完成（参照）"
  
  %% Visual: style nodes that have links
  classDef linkNode fill:#dff7e0,stroke:#2b7a0b,stroke-width:1px;
  class E10_40,E10_20,E10_00 linkNode
```

## 動機的要因（米国）

```mermaid
graph LR
  E20_20["ポツダム宣言を日本が無視<br>1945.07.26"]
  E20_30["日本に降伏を迫る特別な手段が必要"]
  E20_31["本土決戦は避けたい"]
  E20_31A["沖縄戦：米軍想定外の被害"]
  E20_40["圧倒的戦力差でも降伏しない日本"]
  E20_41["ミッドウェー海戦の損失"]
  E20_42["サイパン島陥落"]
  E20_43["多数の空襲 被害甚大"]
  E20_00["原爆投下の動機"]

  E20_20 --> E20_00
  E20_30 --> E20_00
  E20_31 --> E20_30
  E20_31A --> E20_31
  E20_40 --> E20_30
  E20_41 --> E20_40
  E20_42 --> E20_40
  E20_43 --> E20_40

  %% Links
  click E20_20 "https://ja.wikipedia.org/wiki/%E3%83%9D%E3%83%84%E3%83%80%E3%83%A0%E5%AE%A3%E8%A8%80" "ポツダム宣言"
  click E20_31A "https://ja.wikipedia.org/wiki/%E6%B2%96%E7%B8%84%E6%88%A6" "沖縄戦"
  click E20_41 "https://ja.wikipedia.org/wiki/%E3%83%9F%E3%83%83%E3%83%89%E3%82%A6%E3%82%A7%E3%83%BC%E6%B5%B7%E6%88%A6" "ミッドウェー海戦"
  click E20_43 "https://ja.wikipedia.org/wiki/%E6%97%A5%E6%9C%AC%E6%9C%AC%E5%9C%9F%E7%A9%BA%E8%A5%B2" "日本本土空襲"
  
  %% Visual: style nodes that have links
  classDef linkNode fill:#dff7e0,stroke:#2b7a0b,stroke-width:1px;
  class E20_20,E20_31A,E20_41,E20_43 linkNode
```

## 動機的要因（日本）

```mermaid
graph LR
  E30_00["原爆投下まで降伏しなかった"]
  E30_10["政治における軍の発言権が強い"]
  E30_11["憲法の問題（基本的人権・平和主義欠如等）"]
  E30_12["軍部大臣 現役武官制"]
  E30_13["政治の弱体化"]
  E30_20["戦陣訓の影響（玉砕推奨）"]
  E30_22["南京大虐殺（参照資料）"]
  E30_30["沖縄戦後の講和交渉の遅れ"]

  E30_10 --> E30_00
  E30_11 --> E30_10
  E30_12 --> E30_10
  E30_13 --> E30_10
  E30_20 --> E30_00
  E30_30 --> E30_00

  %% Links
  click E30_12 "https://ja.wikipedia.org/wiki/%E8%BB%8D%E9%83%A8%E5%A4%A7%E8%87%A3%E7%8F%BE%E5%BD%B9%E6%AD%A6%E5%AE%98%E5%88%B6" "軍部大臣 現役武官制"
  click E30_13 "https://ja.wikipedia.org/wiki/%E4%BA%94%E3%83%BB%E4%B8%80%E4%BA%94%E4%BA%8B%E4%BB%B6" "5.15事件（代表例）"
  click E30_20 "https://ja.wikipedia.org/wiki/%E6%88%A6%E9%99%A3%E8%A8%93#:~:text=%E6%88%A6%E9%99%A3%E3%81%A7%E3%81%AE%E8%A8%93%E6%88%92%E3%81%AE,%E8%A8%93%E4%B8%80%E5%8F%B7%EF%BC%89%E3%82%92%E6%8C%87%E3%81%99%E3%80%82" "戦陣訓"
  click E30_22 "https://seesaawiki.jp/w/nankingfaq/" "南京大虐殺（外部）"
  
  %% Visual: style nodes that have links
  classDef linkNode fill:#dff7e0,stroke:#2b7a0b,stroke-width:1px;
  class E30_12,E30_13,E30_20,E30_22 linkNode
```

## 機会的要因

```mermaid
graph LR
  E40_00["真珠湾攻撃 → 米国の参戦<br>1941.12.7"]
  E40_10["ハルノート 1941.11.26"]
  E40_20["対米戦争支持の世論の高まり"]
  E40_200["米国による石油輸出禁止 1941.8.1"]

  E40_10 --> E40_00
  E40_20 --> E40_00
  E40_200 --> E40_20

  %% Links
  click E40_00 "https://ja.wikipedia.org/wiki/%E7%9C%9F%E7%8F%A0%E6%B9%BE%E6%94%BB%E6%92%83" "真珠湾攻撃"
  click E40_10 "https://ja.wikipedia.org/wiki/%E3%83%8F%E3%83%AB%E3%83%BB%E3%83%8E%E3%83%BC%E3%83%88" "ハルノート"
  click E40_200 "https://www.jacar.go.jp/nichibei/popup/pop_13.html" "石油輸出禁止（資料）"
  
  %% Visual: style nodes that have links
  classDef linkNode fill:#dff7e0,stroke:#2b7a0b,stroke-width:1px;
  class E40_00,E40_10,E40_200 linkNode
```

---

必要なら各章のノードをさらに詳細化（全ノード・全URLを反映）します。
    click E20_31A "https://ja.wikipedia.org/wiki/%E6%B2%96%E7%B8%84%E6%88%A6" "沖縄戦"
    click E20_41 "https://ja.wikipedia.org/wiki/%E3%83%9F%E3%83%83%E3%83%89%E3%82%A6%E3%82%A7%E3%83%BC%E6%B5%B7%E6%88%A6" "ミッドウェー海戦"
    click E20_43 "https://ja.wikipedia.org/wiki/%E6%97%A5%E6%9C%AC%E6%9C%AC%E5%9C%9F%E7%A9%BA%E8%A5%B2" "日本本土空襲"
    click E30_12 "https://ja.wikipedia.org/wiki/%E8%BB%8D%E9%83%A8%E5%A4%A7%E8%87%A3%E7%8F%BE%E5%BD%B9%E6%AD%A6%E5%AE%98%E5%88%B6" "軍部大臣 現役武官制"
    click E30_13A "https://ja.wikipedia.org/wiki/%E4%BA%94%E3%83%BB%E4%B8%80%E4%BA%94%E4%BA%8B%E4%BB%B6" "5.15事件"
    click E30_13B "https://ja.wikipedia.org/wiki/%E4%BA%8C%E3%83%BB%E4%BA%8C%E5%85%AD%E4%BA%8B%E4%BB%B6" "2.26事件"
    click E30_20 "https://ja.wikipedia.org/wiki/%E6%88%A6%E9%99%A3%E8%A8%93#:~:text=%E6%88%A6%E9%99%A3%E3%81%A7%E3%81%AE%E8%A8%93%E6%88%92%E3%81%AE,%E8%A8%93%E4%B8%80%E5%8F%B7%EF%BC%89%E3%82%92%E6%8C%87%E3%81%99%E3%80%82" "戦陣訓"
    click E30_22 "https://seesaawiki.jp/w/nankingfaq/" "南京大虐殺（外部）"
    click E30_220 "https://ja.wikipedia.org/wiki/%E7%AC%AC%E4%BA%8C%E6%AC%A1%E4%B8%8A%E6%B5%B7%E4%BA%8B%E5%A4%89" "第二次上海事変"
    click E40_00 "https://ja.wikipedia.org/wiki/%E7%9C%9F%E7%8F%A0%E6%B9%BE%E6%94%BB%E6%92%83" "真珠湾攻撃／米国参戦"
    click E40_10 "https://ja.wikipedia.org/wiki/%E3%83%8F%E3%83%AB%E3%83%BB%E3%83%8E%E3%83%BC%E3%83%88" "ハルノート"
    click E40_200 "https://www.jacar.go.jp/nichibei/popup/pop_13.html" "米国による石油輸出禁止（資料）"
    click E40_2000 "https://ja.wikipedia.org/wiki/%E4%BB%8F%E5%8D%B0%E9%80%B2%E9%A7%90" "仏印進駐"
    click E40_20001 "https://ja.wikipedia.org/wiki/%E5%A4%A7%E6%9D%B1%E4%BA%9C%E5%85%B1%E6%A0%84%E5%9C%8F" "大東亜共栄圏"
    click E40_201A "https://ja.wikipedia.org/wiki/%E6%97%A5%E6%B8%85%E6%88%A6%E4%BA%89" "日清戦争"
    click E40_201B "https://ja.wikipedia.org/wiki/%E6%97%A5%E9%9C%B2%E6%88%A6%E4%BA%89" "日露戦争"
  ```

注: 元の `war.dot` に含まれる各ノードの詳細ラベルや外部URLは、Mermaid の簡潔さのため簡略化しています。必要ならすべてのノードと改行・URLを保持する完全変換も作成できます。


