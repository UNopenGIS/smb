# Smart Maps Walking Tour: Concept Note
## What are the challenges
United Nations Vector Tile Toolkit (UNVT) has been successful in enabling base map provision in a cloud-optimized way. By enabling easy sharing, access, and processing of vector geospatial data, we can save time and costs needed to utilize geospatial information. Additionally, the cloud optimization allows for easier integration with different applications, making it commonly accessible to more people, who can then utilize geospatial information to make better decisions. This approach is also forward-looking and inclusive, ensuring that everyone can benefit from the power of open geospatial information.

<details>
<summary>ja</summary>
国連ベクトルタイルツールキットを通じ、我々はベクトル形式のベースマップ情報をクラウド最適化することに成功しました。
ベクトル形式の地理空間情報を容易に共有、アクセス、処理できるようにすることで、
地理空間情報を活用するために必要な時間やコストを節約することができます。
また、クラウド最適化により、より簡単に使えて、多くのアプリケーションに結合できる用になるので、
より多くの人々が地理空間情報を活用し、より良い意思決定をすることができます。
</details>

Acquiring and configuring servers in deploying UNVT was a bit of a headache. With cloud-optimized geospatial information, the server-side processing is not as complex. If we can also provision cost-effective, high-capacity, and flexible storage on-demand, we can share even more timely geospatial information. This will enable us to further enhance the accessibility and utilization of geospatial information for everyone.

<details>
<summary>ja</summary>
国連ベクトルタイルツールキットを配備するに当たっても、サーバーの取得と設定は頭痛の種でした。
クラウド最適化された地理空間情報の場合、サーバー側の動的処理は複雑ではありませんが、
安価で大容量で柔軟なストレージを機動的に用意することができれば、さらにタイムリーな地理空間情報を
共有することができるようになります。
</details>

Furthermore, access to geospatial information is expanding to include data from UAVs, LiDAR, 3D point clouds, and 3D city models related to facility management and smart cities. These datasets are significantly larger than vector-based base map information, and without innovative storage technologies, server issues could hinder the utilization of geospatial information.

<details>
<sumary>ja</summary>
加えて、UAVやLiDARによる写真や三次元点群データ、施設管理やスマートシティに関連する三次元都市モデルが
次々にアクセス可能になりつつあります。これらのデータはベクトル形式のベースマップ情報よりもはるかに大きく、
より革新的なストレージ技術を用いなければサーバーの問題が地理空間情報の活用を阻害することになりかねません。
</details>

## Introduction of the basic idea, pros and cons
The idea of a decentralized web is gaining new implementations under the keyword of Web3. The InterPlanetary File System (IPFS) is a relatively fast, stable, and secure implementation of a decentralized web. The idea of sharing cloud-optimized geospatial information using IPFS was born out of the encounter with this technology.

<details>
<summary>ja</summary>
分散ウェブのアイディアは、Web3というキーワードとともに、新たな実装を得ています。
惑星間ファイルシステムは、比較的安定して高速で、またセキュリティにも考慮された分散ウェブの実装です。
クラウド最適化した地理空間情報を惑星間ファイルシステムを用いて共有するというアイディアは、
惑星間ファイルシステムとの出会いから始まりました。
</details>

The basic idea behind Smart Maps Bazaar is to store cloud-optimized geospatial information on IPFS and share it with applications through gateways that provide open access.

In implementation, an IPFS gateway for open access to cloud-optimized file sharing is called Smart Maps Bazaar.

To list cloud-optimized geospatial information on Smart Maps Bazaar, one simply needs to add the geospatial information to their IPFS node and share the resulting content identifier with the application.

<details>
<summary>ja</summary>
Smart Maps Bazaar は、クラウド最適化された地理空間情報を惑星間ファイルシステムに記録し、
オープンにアクセス可能なように設置したゲートウェイを通じてアプリケーションに共有するという基本的アイディアです。

実装においては、オープンにアクセス可能にしたクラウド最適化可能なファイル共有のための
惑星間ファイルシステムゲートウェイを、Smart Maps Bazaar と呼んでいます。

Smart Maps Bazaar にクラウド最適化した地理空間情報を出品したい時には、
地理空間情報を自分の惑星間ファイルシステムノードに追加して、得られたコンテンツ識別子を
アプリケーションと共有すれば良いのです。
</details>

One of the pros for this idea is that it allows for IPFS nodes necessary for information sharing to be made much more affordable. As the amount of geospatial data to be shared grows, there may be cases where the demand for access speed for individual geospatial data decreases. This may make it possible to allocate reasonably priced storage for data with low access speed requirements.

Moreover, the concept of "pinning" is present in IPFS. By pinning data to one's own node, it may be possible to carry the data offline. This feature could also potentially work as a cache to enhance access speed at devices or sites.

One challenge of this idea is the lack of established methods to implement access restrictions. For the time being, it may be best to limit the Smart Maps Bazaar idea to existing open data or unclassified data. However, unclassified data is often massive in scale, and applying this idea to unclassified data alone could still lead to cost reductions.

<details>
<summary>ja</summary>
このアイディアの利点は、情報共有のために必要なノードを必要なだけ安価にすることができることです。
共有する地理空間情報が莫大になればなるほど、個別の地理空間情報に対するアクセス速度の要求が低くなる
場合があります。アクセス速度の要求が低いデータに対して相応の安価なストレージを割り当てることができる可能性が
あります。

また、惑星間ファイルシステムには pin の概念があります。自分のノードに pin しておけば、
データを手元に持っておくことになるので、オフラインでの持ち運びが実現できる可能性があります。
これは、端末や拠点においてアクセスを高速にするためのキャッシュとしても働く可能性があります。

このアイディアの課題は、アクセス制限の概念を実装する確立された方法がまだないことです。
当面、Smart Maps Bazaar のアイディアは、既存のオープンデータか、unclassified のデータに
対して適用するにとどめた方が良いでしょう。他方で、そういった unclassified のデータは
膨大であることも多く、unclassified のデータに適用するだけでも、コスト低減を実現できる可能性はあります。
</details>

## Demos (point cloud, city models, vector tiles, and imagery) with a little bit more technical details.
This seminar is called Walking Tour, and just like in the actual Bazaar where people can enjoy shopping, we also have a Walking Tour section in this seminar where participants can actually consume geospatial information.

During the tour, we will provide technical details specific to each data format.

We believe that this hands-on approach will help participants better understand the potential of Smart Maps Bazaar and the benefits of a decentralized web. This inclusive and interactive experience is open to everyone, regardless of technical expertise, and we welcome anyone who is interested in learning more about the future of spatial data sharing.

<details>
<summary>ja</summary>
このセミナーは、Walking Tour という名前を持っています。実際の Bazaar でもそこで買い物を楽しむ
Walking Tour が開かれていることがあるように、このセミナーでも、実際に地理空間情報を消費していただく
Walking Tour のパートを用意します。

Tour の中で、個別のデータ形式に依存した技術的詳細についても説明します。
</details>

## Possible practical scenarios.
In DWG 7, Smart Maps Bazaar is realized using Raspberry Pi 4B. One of the possible practical scenarios includes placing nodes within a site. These nodes within a site can be used to share site-specific data or cache common data supplied from the global service center. Since IPFS is a content-addressed system, data duplication is automatically eliminated.

<details>
<summary>ja</summary>
DWG 7 でも、Smart Maps Bazaar を Raspberry Pi 4B を用いて実現しています。
可能な実用的シナリオには、拠点内部にノードを置くことを含みます。
拠点内部のノードは、拠点固有のデータを共有することに使われるかもしれませんし、
グローバルサービスセンターから供給される共通データをキャッシュすることに使われるかも
しれません。惑星間ファイルシステムはコンテンツアドレッシングシステムなので、データの重複は自動的に排除されます。
</details>

## What is the advantage of using Smart Maps Bazaar?
The benefits of using Smart Maps Bazaar include:

- Higher flexibility for server environment and storage requirements
- Utilization of content-addressable system to avoid information duplication and promote caching
- Standardized interface for system configuration simplification and unification
- Standardized interface for both internal organizational use and external public access, leading to improved user experience for internal users and enhanced partnership opportunities.

<details>
<summary>ja</summary>
Smart Maps Bazaar を利用することの利点は次のものを含むでしょう。

- サーバー環境やストレージ要求に対する柔軟性の導入
- コンテンツアドレッシングシステムの活用による情報の重複回避とキャッシュ促進
- 統一的なインタフェースの使用によるシステム構成の共通化と単純化
- 組織内利用と対外公開のインタフェースの共通化
  - 組織内利用のユーザエクスペリエンスの向上
  - パートナーシップの活性化
</details>

## Next steps
Smart Maps Bazaar is an experimental system to share vast amounts of open geospatial information in a cloud-optimized manner. Bringing together the efforts of those who stand to benefit from such a system can accelerate the development of this technology to the next level.

<details>
<summary>ja</summary>
Smart Maps Bazaar は、まだ実験的なソフトウェアである惑星間ファイルシステムを使って、オープンであるが
膨大な地理空間情報をクラウド最適化した方法で共有する仕組みです。

このような仕組みを活用することにメリットがある人々の努力を結集し、この技術の開発を加速することに繋げることが、
次のステップになります。
</details>

## Invitation
As members of DWG 7, we would like to propose an open and constructive discussion with UN staff members who participate in the UN Open GIS Initiative and UN Geospatial Network, as well as contributors who share our vision for the Smart Maps Bazaar. Our goal is to introduce the concept of the Smart Maps Bazaar and showcase a working web map to inspire collective efforts towards this concept. Let's have an open and honest conversation about how we can come together to make this vision a reality.

<details>
<summary>ja</summary>
我々 DWG 7 メンバーは、UN Open GIS Initiative や UN Geospatial Network に参加する国連スタッフや、
Smart Maps Bazaar のコンセプトに共感する貢献者にに対し、
Smart Maps Bazaar のコンセプトを紹介し、実際に動作する具体的なウェブ地図を見せることで、
このコンセプトのために努力を結集する方法について率直で建設的な議論を行うことを提案します。
</details>
