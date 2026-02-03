```mermaid
graph LR
Milk["生乳"]
%% === ルート1: チーズ製造（生乳を使用） ===
Milk --> CheeseProcess["菌・酵素(レンネット)"]
CheeseProcess --> Cheese["ナチュラルチーズ"]
CheeseProcess --> SweetWhey["<b>チーズホエイ</b>"]
SweetWhey --> MainPro["<b>ホエイプロテイン (メイン)</b>"]
%% === ルート2: 分離・脱脂（脱脂乳を使用） ===
Milk --> Separator["遠心分離"]
%% --- クリーム側の流れ ---
Separator --> Cream["乳脂肪"]
Cream --> Creamy["生クリーム"]
Cream --> ButterProcess["撹拌"]
ButterProcess --> Butter["バター"]
%% --- 脱脂乳側の流れ ---
Separator --> SkimMilk["<b>脱脂乳 (副産物)</b>"]
%% そのまま加工
SkimMilk --> Calpis["乳酸菌飲料"]
SkimMilk --> Powder["脱脂粉乳"]
%% 発酵プロセスへ（酸で固める）
SkimMilk --> Ferment["<b>発酵・酸凝固 (ヨーグルト製造)</b>"]
%% 固形分（カゼイン）
Ferment --> Oikos["<b>高タンパク脂質ゼロヨーグルト</b>"]
%% 液体（ホエイ）
Ferment --> AcidWhey["<b>アシッドホエイ<b>"]
AcidWhey --> main["中和・排水処理"]
AcidWhey --> sub["バイオガス"]
AcidWhey --> limit["肥料・飼料"]
AcidWhey --> RarePro["<b>ホエイプロテイン(明治)</b>"]
```
```mermaid
graph LR
%% ノードの定義
Intro[<b>1. INTRODUCTION (導入)</b><br>プラスミドの概要と本総説の目的]
    
subgraph Molecular_Mechanisms [分子メカニズムの解明]
direction LR
Init[<b>2. PLASMID REPLICATION INITIATION<br>AT ORIGINS OF REPLICATION</b><br>複製起点での開始<br><small>ori構造、Repタンパク質の役割</small>]
Mech[<b>3. MECHANISMS OF PLASMID REPLICATION</b><br>複製のメカニズム<br><small>シータ型複製、DnaA/PriA依存経路</small>]
end

subgraph System_Regulation [分類と制御システム]
direction LR
Class[<b>4. SEQUENCE-BASED CLASSIFICATION<br>OF PLASMID REPLICONS</b><br>配列に基づくレプリコンの分類<br><small>類似性によるグループ化</small>]
Reg[<b>5. REGULATION OF PLASMID REPLICATION</b><br>複製の制御<br><small>コピー数制御、アンチセンスRNA、イテロン</small>]
end

subgraph Eco_Evo_Context [生物学的・進化的文脈]
 direction LR
Host[<b>6. BROADER BIOLOGICAL CONTEXT:<br>HOST RANGE</b><br>宿主域<br><small>広宿主域 vs 狭宿主域、適応コスト</small>]
        Maint[<b>7. BROADER BIOLOGICAL CONTEXT:<br>PLASMID MAINTENANCE</b><br>プラスミドの維持<br><small>分配システム(Par)、トキシン-アンチトキシン系</small>]
        Cluster[<b>8. CLUSTERING OF<br>PLASMID MAINTENANCE ELEMENTS</b><br>維持エレメントのクラスター化<br><small>複製・維持遺伝子の物理的近接と共進化</small>]
end

Concl[<b>9. CONCLUDING REMARKS (結論)</b><br>総括と今後の展望]

%% フローの接続
Intro --> Init
Init --> Mech
Mech --> Class
Class --> Reg
Reg --> Host
Host --> Maint
Maint --> Cluster
Cluster --> Concl

%% スタイル調整
style Intro fill:#f9f9f9,stroke:#333,stroke-width:2px
style Concl fill:#f9f9f9,stroke:#333,stroke-width:2px
style Molecular_Mechanisms fill:#e1f5fe,stroke:#01579b
style System_Regulation fill:#fff9c4,stroke:#fbc02d
style Eco_Evo_Context fill:#e8f5e9,stroke:#2e7d32
```







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
    Cream --> Butter["バター/生クリーム"]
    %% 脱脂乳側
    Separator --> SkimMilk["<b>脱脂乳</b>"]
    %% 脱脂乳の活用
    SkimMilk --> Calpis["カルピス/脱脂粉乳"]
    %% オイコス（ヨーグルト）
    SkimMilk --> YogurtProcess["<b>発酵・酸凝固</b><br>(ヨーグルト製造)"]
    YogurtProcess --> Oikos["<b>🥣 オイコス</b><br>(脂肪ゼロ・高タンパク)"]
    YogurtProcess --> AcidWhey["<b>アシッドホエイ</b><br>(酸性ホエイ)"]
    AcidWhey --> AcidPro["アシッドホエイプロテイン<br>(※加工難易度が高い)"]
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
