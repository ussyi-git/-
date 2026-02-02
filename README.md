```mermaid
graph LR
Milk["生乳"]-->Separator["遠心分離"]
%% --- クリーム側の流れ ---
Separator-->Cream["乳脂肪"]
Cream-->ButterProcess["撹拌"]
  Cream-->creamyProcess["生クリーム"]
ButterProcess-->Butter["バター"]
%% --- 脱脂乳側の流れ ---
Separator-->SkimMilk["<b>脱脂乳 (副産物)</b>"]
%% 発酵プロセスへ
SkimMilk-->Ferment["<b>発酵・凝固</b>"]
%% そのまま加工
SkimMilk-->Calpis["乳酸菌飲料"]
SkimMilk-->Powder["脱脂粉乳"]
%% 固形分（カゼイン）の行方
Ferment-->Curd["<b>カゼイン</b>"]
Curd-->Oikos["<b>高タンパク脂質ゼロ<br>のヨーグルト</b>"]
%% 液体（ホエイ）の行方
Ferment-->Whey["<b>ホエイ</b>"]
Whey-->WPC_WPI["<b>ホエイプロテイン</b>"]
```
#Whey-->Lactose["乳糖(薬の錠剤・甘味料)"]
#Whey-->Cooking["飼料(豚の餌)"]
<b></b>

```mermaid
graph LR
    Milk["<b>生乳</b>"]

    %% === ルート1: チーズ製造（全乳を使うメインルート） ===
    Milk -->|脂肪を抜かずに| CheeseProcess["<b>① チーズ製造</b><br>(酵素・レンネット)"]
    CheeseProcess --> Cheese["<b>🧀 ナチュラルチーズ</b><br>(チェダー・ゴーダ等)"]
    CheeseProcess --> SweetWhey["<b>チーズホエイ</b><br>(スイートホエイ)"]
    SweetWhey --> SweetPro["<b>🏆 チーズホエイプロテイン</b><br>(WPC/WPIの主流)"]

    %% === ルート2: 分離・脱脂（バター・脱脂乳ルート） ===
    Milk -->|遠心分離| Separator["<b>② 分離機</b>"]
    
    %% クリーム側
    Separator --> Cream["乳脂肪"]
    Cream --> Butter["<b>🧈 バター/生クリーム</b>"]
    
    %% 脱脂乳側
    Separator --> SkimMilk["<b>脱脂乳</b>"]
    
    %% 脱脂乳の活用
    SkimMilk --> Calpis["カルピス/脱脂粉乳"]
    
    %% オイコス（ヨーグルト）
    SkimMilk --> YogurtProcess["<b>発酵・酸凝固</b><br>(ヨーグルト製造)"]
    YogurtProcess --> Oikos["<b>🥣 オイコス</b><br>(脂肪ゼロ・高タンパク)"]
    YogurtProcess --> AcidWhey["<b>アシッドホエイ</b><br>(酸性ホエイ)"]
    AcidWhey --> AcidPro["アシッドホエイプロテイン<br>(※加工難易度が高い)"]

    %% スタイル調整
    linkStyle 2,3,4 stroke-width:4px,fill:none,stroke:orange;
    linkStyle 11,12,13 stroke-width:4px,fill:none,stroke:cyan;
```

```mermaid
graph LR
Milk["生乳 (Raw Milk)"]-->Separator["遠心分離"]
%% --- 脂肪分（クリーム層）の流れ ---
Separator-->Cream["クリーム層 (乳脂肪)"]
Cream-->FreshCream["<b>🍰 生クリーム</b><br>(そのまま製品化)"]
Cream-->ButterProcess["撹拌・チャーニング"]
ButterProcess-->Butter["<b>🧈 バター</b>"]
ButterProcess-->Buttermilk["💧 バターミルク<br>(パン・菓子の原料)"]
%% --- 脱脂分（脱脂乳）の流れ ---
Separator-->SkimMilk["脱脂乳 (Skim Milk)"]
SkimMilk-->Powder["<b>🥛 脱脂粉乳</b>"]
SkimMilk-->Calpis["<b>🥤 カルピス/乳酸菌飲料</b>"]
%% 発酵・凝固
SkimMilk-->Ferment["発酵・凝固"]
%% 固形分
Ferment-->Curd["固形分 (カゼイン)"]
Curd-->Oikos["<b>🥣 オイコス</b><br>(水切り・濃縮)"]
Curd-->Cottage["<b>🥗 カッテージチーズ</b>"]
Curd-->IndCasein["💊 カゼイン原料<br>(プロテイン等)"]
%% 液体
Ferment-->Whey["💧 ホエイ (乳清)"]
Whey-->WPC_WPI["<b>💪 ホエイプロテイン</b>"]
Whey-->Lactose["💊 乳糖 (錠剤の形を作る成分)"]
Whey-->Cooking["🍳 調理・飼料"]
```
