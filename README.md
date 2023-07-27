PublicFeature
===
共用的功能模組，模組化一些共用的大眾需求，希望讓工程師不再重工。

## 專案架構
現在可能專案內不是長這樣，但朝向這個規劃前進。目前的 api 與 impl 分別對應 usecase 的介面與實作層，且含有可以拆成 feature 的功能。模組分為功能模組與共用模組。
![](./doc/blueprint.png)
- app
  - 使用專案內各個 feature 或 usecase 的 sample
- feature
  - 功能模組，目標是包成該功能的 Library，讓專案能直接從 gradle 引用並使用
- ui-common
  - ui 共用模組
- usecase-api
  - usecase 介面
- usecase-impl
  - usecase 介面的實作
  - feature 模組不直接引用 impl 模組
- common
  - usecase 實作共通的使用案例
