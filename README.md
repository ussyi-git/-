``mermaid
graph LR
Milk["生乳 (Raw Milk)"]-->Separator["遠心分離"]
%% --- クリーム側の流れ ---
Separator-->Cream["クリーム層"]
Cream-->ButterProcess["撹拌・チャーニング"]
ButterProcess-->Butter["🧈 バター"]
ButterProcess-->Buttermilk["💧 バターミルク<br>(欧米ではパンケーキや菓子の材料に)"]
%% --- 脱脂乳側の流れ ---
Separator-->SkimMilk["脱脂乳 (Skim Milk)"]
%% そのまま加工
SkimMilk-->Powder["脱脂粉乳"]
SkimMilk-->Calpis["🥤 カルピス<br>(脱脂乳の救世主)"]
%% 発酵プロセスへ
SkimMilk-->Ferment["発酵・凝固"]
%% 固形分（カゼイン）の行方
Ferment-->Curd["固形分 (カゼイン)"]
Curd-->Oikos["🥣 ギリシャヨーグルト<br>(オイコス等・脂肪ゼロ)"]
Curd-->Cheese["🧀 チーズ<br>(プロセス/ナチュラル)"]
%% 液体（ホエイ）の行方
Ferment-->Whey["💧 ホエイ (乳清)"]
Whey-->WPC_WPI["💪 ホエイプロテイン<br>(WPC/WPI)"]
Whey-->Lactose["💊 乳糖<br>(薬の錠剤・甘味料)"]
Whey-->Cooking["🍳 調理・飼料<br>(肉を柔らかくする/豚の餌)"]
```
