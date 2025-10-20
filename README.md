## クロスドメイン推薦
 **<details><summary>A privacy-preserving framework with multi-modal data for cross-domain recommendation(2024)**</summary><div>  
  マルチモーダル情報を活用して既存手法より情報量の多いドメイン共通及び固有の埋め込みを分離・抽出するエンコーダと、知識転移中のユーザのプライバシー保護のためローカル差分プライバシーによる難読化を行う。加えて、難読化された分離表現の整合性と差異性を保証するため、コントラスト学習に基づいたドメイン間およびドメイン内損失を組み込んだ。

  [[link]](https://www.sciencedirect.com/science/article/pii/S0950705124011638)
  [[code]](https://github.com/Lili1013/P2M2-CDR)
</details>

 **<details><summary>Joint Similarity Item Exploration and Overlapped User Guidance for Multi-Modal Cross-Domain Recommendation(2025)**</summary><div>  
 類似度グラフにペアワイズグラフ・ハイパーグラフの2つを導入し、局所的な類似性と広範囲な類似性を捉える。また、重複ユーザをガイドとし、ドメイン間で嗜好が似ている非重複ユーザをマッチングし、クロスドメイン推薦を実現。


  [[link]](https://dl.acm.org/doi/10.1145/3696410.3714860)
  [[code]]()
</details>

**<details><summary>Enhancing Transferability and Consistency in Cross-Domain
Recommendations via Supervised Disentanglement(2025)**</summary><div>  
 GNNで抽出した特徴量をアンカーとして設定し，教師あり対照学習の枠組みで特徴の分離．具体的には、ドメイン間で変換した共有情報，GNNの特徴，固有情報とアンカーとの類似度を計算し、共有情報> GNNの特徴>固有特徴という関係が成立するように損失を設計．アイテム埋め込みも活用し、ドメインAの固有嗜好とドメインAのアイテムの埋め込みを近づけ、ドメインBのアイテム埋め込みと遠ざける。（ドメインBでも同様）


  [[link]](https://dl.acm.org/doi/10.1145/3705328.3748044)
  [[code]](https://github.com/WangYuhan-0520/DGCDR)
</details>

## 因果推論と推薦システム
**<details><summary>Instrumental Variables in Causal Inference and Machine Learning: A Survey(2022)**</summary><div>  
  交絡因子を特定できないとき場合に使える、因果効果の測定法の1つである操作変数法に関するサーベイ論文。

  [[link]](https://arxiv.org/abs/2212.05778)
  [[code]]()
</details>


 **<details><summary>A Model-Agnostic Causal Learning Framework for Recommendation using Search Data(2022)**</summary><div>  
  ユーザの検索行動を操作変数とみなし、処置変数を操作変数で回帰することで、クリックに重要な因果的要素と人気バイアスなどの非因果的要素を分離。

  [[link]](https://dl.acm.org/doi/10.1145/3485447.3511951)
  [[code]](https://github.com/Ethan00Si/Instrumental-variables-for-recommendation)
</details>

## マルチモーダル推薦
### マルチモーダル推薦のためのオープンソースフレームワーク

[[link]](https://dl.acm.org/doi/10.1145/3611380.3628561)
  [[code]](https://github.com/enoche/MMRec)

### アイテム-アイテムグラフ構築
 **<details><summary>Mining Latent Structures for Multimedia Recommendation(2021)**</summary><div>  
 各モダリティ内でコサイン類似度を計算し、上位k個のアイテム間にエッジを結ぶことでグラフを構築。モダリティ間のグラフを融合する際、重要度パラメータαを掛け合わせて加算。このグラフは学習プロセス中に動的に変化する。最終的に、この構築したグラフとインタラクショングラフを用いてスコアを算出する。

 [[link]](https://dl.acm.org/doi/abs/10.1145/3474085.3475259)
  [[code]](https://github.com/CRIPAC-DIG/LATTICE)
</details>

 **<details><summary>Freezing and Denoising Graph Structures for Multimodal Recommendation(2023)**</summary><div>  
 LATTICEのグラフ動的学習が不要であると主張し、事前にマルチモーダル特徴の類似度からグラフを構築し、モデル学習時には固定する。また、次数の多いノード（インタラクションが多いユーザ・人気アイテム）ほどノイズの影響を受けやすいため、DropEdgeによって一定の割合のエッジをランダムに削除。ノードの次数を分母にした確率により、次数の高いエッジを枝刈りの対象にしやすくする。LATTICEと比較してメモリ使用量を最大6分の1、訓練時間を4分の1にまで短縮した。

 [[link]](https://dl.acm.org/doi/abs/10.1145/3581783.3611943)
  [[code]](https://github.com/enoche/FREEDOM)
</details>

 **<details><summary>Multi-View Graph Convolutional Network for Multimedia Recommendation(2023)**</summary><div>  
ユーザの行動情報を手掛かりに、モダリティ特徴から不要なノイズを除去し、ユーザとアイテムの関係、アイテム間の類似度に基づくグラフを構築。さらに、ユーザがどのモダリティを重視する傾向があるかを学習し、重要度を調整。

 [[link]](https://dl.acm.org/doi/abs/10.1145/3581783.3613915)
  [[code]](https://github.com/demonph10/MGCN)
</details>

 **<details><summary>Improving Multi-modal Recommender Systems by Denoising and Aligning Multi-modal Content and User Feedback(2024)**</summary><div>  
各モダリティごとにアイテム間の類似度を算出し、グラフを作成。ただし、全アイテムの平均類似度よりも低いスコアのエッジは削除する。モダリティ間のグラフの融合の際、両方のモダリティでエッジが結ばれている場合のみ残し、それ以外は削除する。また、類似度グラフに加えてアイテム間の共起行列に基づく行動グラフも構築。

 [[link]](https://dl.acm.org/doi/10.1145/3637528.3671703)
  [[code]](https://github.com/XMUDM/DA-MRS)
</details>

 **<details><summary>Seeing Beyond Noise: Joint Graph Structure Evaluation and Denoising for Multimodal Recommendation(2025)**</summary><div>  
各モダリティの類似度に基づくグラフとアイテムの共起行列による行動グラフの構築。損失関数を各アイテム表現で偏微分し、アイテム表現のモデルに対する貢献度を算出。損失が大きいほど貢献度が高いとみなし、これとノードの次数に基づく確率値を計算し、枝刈りするエッジを決定。さらに、ノイズありのインタラクショングラフと枝刈り後のインタラクショングラフのユーザ表現を近づけ、一貫性を保つために対照学習を導入。ノイズ除去後のアイテムグラフ、ユーザ・アイテムグラフのアイテム表現を同じ潜在空間に整合するための対照学習も導入。

 [[link]](https://ojs.aaai.org/index.php/AAAI/article/view/33358)
  [[code]]()
</details>

 **<details><summary>Beyond Graph Convolution: Multimodal Recommendation with Topology-aware MLPs(2025)**</summary><div>  
各モダリティ内で類似度に基づくアイテムグラフを構築。ただし、GCNの代わりにMLPを使用。2つのノードが共通の近傍ノードを多く持つなら位相的に類似しているという仮定により、ノード間の位相的類似度を計算。位相類似度が高い上位K個のノードとの接続のみ残して後は枝刈りする。MLPにグラフ構造を認識させるため、ノード表現と文脈的近傍との間の相互情報量を最大化し、モーダル内の相関を捉える。これによって意味的に類似するように整列させる。

 [[link]](https://arxiv.org/abs/2412.11747)
  [[code]](https://github.com/jessicahuang0163/TMLP?tab=readme-ov-file)
</details>

 **<details><summary>Multimodal Recommendation System Based on Cross Self-Attention Fusion(2025)**</summary><div>  
あるモダリティの情報から、別のモダリティのどこに注目すべきかの重みを計算することで、相互に関連する情報を伝播。モダリティ内でも、どの特徴が重要であるか判断し、重みづけを行う。

 [[link]](https://www.mdpi.com/2079-8954/13/1/57)
  [[code]]()
</details>
