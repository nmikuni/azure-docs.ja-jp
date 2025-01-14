---
title: Azure Cosmos DB Gremlin API の概要
description: Azure Cosmos DB を使用し、Apache TinkerPop の Gremlin グラフ クエリ言語を使って待ち時間の短い大規模なグラフの格納、クエリの実行、トラバースを行う方法について説明します。
author: LuisBosquez
ms.service: cosmos-db
ms.subservice: cosmosdb-graph
ms.topic: overview
ms.date: 06/25/2019
ms.author: lbosq
ms.openlocfilehash: 126c825106b7844a5fc8a5a3cdbcc7aa6c273b5b
ms.sourcegitcommit: 837dfd2c84a810c75b009d5813ecb67237aaf6b8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "67502800"
---
# <a name="introduction-to-azure-cosmos-db-gremlin-api"></a>Azure Cosmos DB の概要: Gremlin API

[Azure Cosmos DB](introduction.md) は、ミッション クリティカルなアプリケーション向けの、Microsoft のグローバル分散マルチモデル データベース サービスです。 これはマルチモデル データベースであり、ドキュメント、キー値、グラフ、および列指向データ モデルをサポートします。 Azure Cosmos DB Gremlin API は、あらゆる規模のフル マネージド データベース環境でのグラフ データの格納および操作に使用されます。  

![Azure Cosmos DB グラフ アーキテクチャ](./media/graph-introduction/cosmosdb-graph-architecture.png)

この記事では、Azure Cosmos DB Gremlin API の概要と、これを使用して何十億もの頂点と辺のある大規模なグラフを保存する方法について説明します。 ミリ秒の待機時間でグラフを照会したり、グラフ構造を簡単に改善したりできます。 Azure Cosmos DB の Gremlin API は [Apache TinkerPop](https://tinkerpop.apache.org)  グラフ データベース標準に基づいており、Gremlin クエリ言語を使用します。 

Azure Cosmos DB の Gremlin API は、グラフ データベース アルゴリズムの機能を非常にスケーラブルなマネージド インフラストラクチャと結合して、柔軟性の不足に関連する最も一般的なデータの問題への一意で柔軟な解決策と、リレーショナル アプローチを提供します。 

## <a name="features-of-azure-cosmos-db-graph-database"></a>Azure Cosmos DB グラフ データベースの機能
 
Azure Cosmos DB は、グローバル配布、ストレージとスループットのエラスティック スケーリング、自動インデックス作成とクエリ、調整可能な整合性レベルを提供し、TinkerPop 標準をサポートする、完全に管理されたグラフ データベースです。 

Azure Cosmos DB Gremlin API で提供される差別化された機能は、次のとおりです。

* **弾力的にスケーラブルなスループットとストレージ**

  実際のグラフは、1 つのサーバーの容量を超えてスケールする必要があります。 Azure Cosmos DB では、スループットの観点で実質的に無制限のサイズとプロビジョニングされたスループットを持つことができる、水平方向にスケーラブルなグラフ データベースがサポートされています。 グラフ データベースのスケールが大きくなるにつれて、データは[グラフのパーティション分割](https://docs.microsoft.com/azure/cosmos-db/graph-partitioning)を使用して自動的に分散されます。

* **複数リージョンのレプリケーション**

  Azure Cosmos DB では、任意の Azure リージョンにグラフ データを自動的にレプリケートできます。 レプリケーションを使用すると、データへのグローバル アクセスを必要とするアプリケーションの開発を簡素化できます。 Azure Cosmos DB は、読み取り待機時間を最小化するだけでなく、リージョン内でサービスが中断するまれなケースにおいて、アプリケーションの継続性を確保できるリージョン内フェールオーバー メカニズムを提供します。 

* **最も広く採用されているグラフ クエリ標準を使用した高速なクエリとトラバーサル**

  異種の頂点と辺を格納し、使い慣れた Gremlin 構文を使用してこれらのドキュメントを照会できます。 Gremlin は、一般的なグラフ アルゴリズムを実装するために豊富なインターフェイスを提供する命令型で関数型のクエリ言語です。 
  
  Azure Cosmos DB では、スキーマのヒント、セカンダリ インデックス、またはビューを指定しなくても、豊富なリアルタイム クエリとトラバーサルが可能です。 詳細については、[Gremlin を使用したグラフの照会](gremlin-support.md)に関する記事を参照してください。

* **フル マネージドのグラフ データベース**

  Azure Cosmos DB を使用すると、データベースやコンピューター リソースを管理する手間がかかりません。 ほとんどの既存のグラフ データベース プラットフォームは、そのインフラストラクチャの制限事項に縛られ、多くの場合、その運用を確実に行うために高度なメンテナンスが必要になります。 
  
  フル マネージドの Microsoft Azure サービスとして、仮想マシンの管理、ランタイム ソフトウェアの更新、シャーディングやレプリケーションの管理、複雑なデータ層のアップグレードの操作を行う必要はありません。 すべてのグラフが自動的にバックアップされ、リージョンの障害から保護されます。 このような保証により、開発者はデータベースの運用と管理ではなく、アプリケーションの価値の提供に専念できます。 

* **インデックスの自動作成**

  既定では、Azure Cosmos DB はグラフのノードおよび辺内のすべてのプロパティのインデックスを自動的に作成するため、スキーマや、セカンダリ インデックスの作成は不要です。 詳細については、[Azure Cosmos DB のインデックス作成](https://docs.microsoft.com/azure/cosmos-db/index-overview)に関する記事をご覧ください。 

* **Apache TinkerPop との互換性**

  Azure Cosmos DB では、[オープン ソースの Apache TinkerPop 標準](http://tinkerpop.apache.org/)がサポートされています。 Tinkerpop 標準には、Azure Cosmos DB の Gremlin API と簡単に統合できるアプリケーションおよびライブラリの豊富なエコシステムがあります。 

* **調整可能な整合性レベル**

  整合性とパフォーマンスの最適なトレードオフを実現するために、明確に定義された 5 つの整合性レベルの中から選択できます。 Azure Cosmos DB では、クエリと読み取り操作に関して、強固、有界整合性制約、セッション、一貫性のあるプレフィックス、最終的の 5 種類の整合性レベルを提供します。 明確に定義されたきめ細かな整合性レベルにより、整合性、可用性、待機時間の適切なトレードオフを行うことができます。 詳しくは、「[Azure Cosmos DB の調整可能なデータの一貫性レベル](consistency-levels.md)」をご覧ください。

## <a name="scenarios-that-can-use-gremlin-api"></a>Gremlin API を使用できるシナリオ
Azure Cosmos DB のグラフ サポートを使用できるシナリオを以下に示します。

* ソーシャル ネットワーク

  顧客に関するデータと顧客による他のユーザーとのやり取りに関するデータを組み合わせることで、パーソナライズされたエクスペリエンスを開発したり、顧客の行動を予測したりできます。また、ユーザーを同じような興味を持つ他のユーザーと結び付けることもできます。 Azure Cosmos DB を使用して、ソーシャル ネットワークを管理し、顧客の嗜好やデータを追跡できます。

* 推奨エンジン

  このシナリオは、小売業界で一般的に使用されます。 製品、ユーザー、ユーザー インタラクション (商品の購入、閲覧、評価など) に関する情報を組み合わせることで、カスタマイズされたレコメンデーションを構築できます。 低待機時間、エラスティック スケール、グラフのネイティブ サポートを実現する Azure Cosmos DB は、これらのインタラクションのモデル化に最適です。

* GeoSpatial

  通信、物流、旅行プランニングの各分野の多くのアプリケーションでは、エリア内で対象となる場所を見つけたり、2 つの場所間の最短ルートや最適ルートを見つけたりする必要があります。 Azure Cosmos DB はこれらの問題に自然に適合します。

* モノのインターネット (IoT)

  ネットワークと、グラフとしてモデル化された IoT デバイス間の接続により、デバイスと資産の状態について理解を深めることができます。 さらに、ネットワークのある部分の変更が別の部分に及ぼす可能性のある影響についても学習できます。

## <a name="introduction-to-graph-databases"></a>グラフ データベースの概要
実世界で出現するデータは、自然に結び付けられています。 従来のデータ モデリングでは、エンティティを個別に定義して、実行時にそれらのリレーションシップを計算することに焦点が当てられています。 このモデルにはその利点がありますが、緊密に接続されたデータをその制約の下で管理するのは困難な場合があります。  

グラフ データベース アプローチは、代わりに、ストレージ層でリレーションシップを持続することに依存します。これで、グラフ取得の操作が非常に効率的になります。 Azure Cosmos DB の Gremlin API では、[プロパティ グラフ モデル](https://tinkerpop.apache.org/docs/current/reference/#intro)がサポートされています。

### <a name="property-graph-objects"></a>プロパティ グラフのオブジェクト

プロパティ [グラフ](http://mathworld.wolfram.com/Graph.html)とは、[頂点](http://mathworld.wolfram.com/GraphVertex.html)と[辺](http://mathworld.wolfram.com/GraphEdge.html)で構成された構造です。 両方のオブジェクトで、プロパティとして任意の数のキーと値のペアを持つことができます。 

* **頂点** - 頂点は、人、場所、イベントなどの個々のエンティティを表します。

* **辺** - 辺は、頂点間のリレーションシップを表します。 たとえば、あるユーザーは、別のユーザーと知り合いで、あるイベントに関連があり、ある場所に最近行ったような場合です。 

* **プロパティ** - プロパティは頂点と辺に関する情報を表します。 頂点または辺のいずれかに任意の数のプロパティが存在する可能性があり、それらをクエリ内のオブジェクトの記述やフィルター処理に使用できます。 プロパティの例には、名前と年齢を持つ頂点、タイムスタンプや重みを持つことができる辺などがあります。 

グラフ データベースは、スキーマまたは制約付きデータ モデルへの依存関係がないため、多くの場合 NoSQL (非リレーショナル) データベース カテゴリ内に含まれています。 このようにスキーマが無いことにより、接続されている構造体を自然かつ効率的にモデリングして格納できます。 

### <a name="gremlin-by-example"></a>Gremlin の例
サンプル グラフを使用して、Gremlin でクエリを表現する方法を理解しましょう。 次の図は、ユーザー、関心事、デバイスに関するデータを管理するビジネス アプリケーションをグラフの形で示しています。  

![ユーザー、デバイス、関心事を示すサンプル データベース](./media/gremlin-support/sample-graph.png) 

このグラフには、次の頂点の種類 (Gremlin では "ラベル" と呼ばれます) が含まれています。

- ユーザー: このグラフには、Robin、Thomas、Ben の 3 人のユーザーが含まれています。
- 関心: 各ユーザーの関心事。この例では、フットボールの試合です。
- デバイス:ユーザーが使用しているデバイスです。
- オペレーティング システム: 各デバイスが実行されているオペレーティング システムです。

次の辺の種類/ラベルによって、これらのエンティティの関係を表しています。

- 知り合い: たとえば、"Thomas は Robin を知っている" ことが示されています。
- 関心あり: このグラフの各ユーザーの関心事を表します。たとえば、"Ben はフットボールに関心がある" ことが示されています。
- RunsOS: ノート PC で Windows OS が実行されています。
- 使用: ユーザーが使用しているデバイスを表します。 たとえば、Robin はシリアル番号が 77 の Motorola Phone を使用しています。

[Gremlin コンソール](https://tinkerpop.apache.org/docs/3.3.2/reference/#gremlin-console)を使用して、このグラフに対していくつかの操作を実行しましょう。 これらの操作は、任意のプラットフォーム (Java、Node.js、Python、または .NET) で Gremlin ドライバーを使用して実行することもできます。  Azure Cosmos DB でサポートされているものを確認する前に、構文に慣れるために例をいくつか見てみましょう。

まず、CRUD を見てみます。 次の Gremlin ステートメントでは、グラフに "Thomas" 頂点を挿入します。

```java
:> g.addV('person').property('id', 'thomas.1').property('firstName', 'Thomas').property('lastName', 'Andersen').property('age', 44)
```

次の Gremlin ステートメントでは、Thomas と Robin の間に "knows" 辺を挿入します。

```java
:> g.V('thomas.1').addE('knows').to(g.V('robin.1'))
```

次のクエリは、ユーザーの姓の降順で "person" 頂点を返します。
```java
:> g.V().hasLabel('person').order().by('firstName', decr)
```

グラフが強調表示されている場合、"Thomas の友人が使用しているオペレーティング システムは何か" というような質問に答える必要があります。 次の Gremlin トラバーサルを実行することで、グラフからこの情報を取得できます。

```java
:> g.V('thomas.1').out('knows').out('uses').out('runsos').group().by('name').by(count())
```
次に、Azure Cosmos DB が Gremlin 開発者に提供するものを見ていきましょう。

## <a name="next-steps"></a>次の手順
Azure Cosmos DB のグラフ サポートの詳細については、以下をご覧ください。

* [Azure Cosmos DB グラフ チュートリアル](create-graph-dotnet.md)を開始する
* [Gremlin を使用して Azure Cosmos DB のグラフを照会する](gremlin-support.md)方法を確認する。
