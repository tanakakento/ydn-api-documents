# ConditionSet
FeedSetオブジェクトは、商品セット情報の条件を保持します。

### Service
+ [FeedSetService](../../services/FeedSetService.md)

### Namespace
[FeedSetService#Namespace](../../services/FeedSetService.md#namespace)

| Field | Type | Description | response | add | remove 
|---|---|---|---|---|---|
| type | [ConditionType](./ConditionType.md)| 条件種別 | ○ | Requirement | Ignore
| orConditions[0..10] | [Condition](./Condition.md)| 商品セットのOR条件 | ○ | Requirement | Ignore

<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>
