## Phase 0 手動部署

需求: 把專案手動部署到 EC2 Linux instance 上去
- 手動部署 example-web 專案
- 先不管 .env 檔案

## Phase 1 基本 Pipeline

需求: 自動化佈署至 EC2 Linux instance 上

- 手動已經做過了，所以 pipeline 中應該要有哪些 jobs?
- 什麼時候觸發 pipeline?
- 其他先不管，先可以成功自動部署
  - 假設環境只有一個 (production)
  - 不用 container
  - 不用測試、不用 lint…
- 使用 Phase 0 準備好的 infra 環境，不用自己建立

## Phase 2 加上 lint
需求: 加上 lint / Prettier...

- 在哪裡執行 lint?
- 成功或失敗？

## Phase 3 加上測試
需求: 執行測試

- 可以執行測試
- 測試失敗就停下來
- 把測試報告保留下來

## Phase 4 加上通知
需求: 測試跑失敗要通知相關人士

- 通知方式: email / slack / discord

## Phase 5 人工介入 approval
需求: 不再從頭到尾自動化了，要有人工介入

- 怎麼介入?
- 介入後怎麼繼續?
- 負責 approve 的人要怎麼知道有 pipeline 要他 approve?

## Phase 6 改成 containerize
需求: infra 改變，希望 containerize

- build Docker image & push to registry
- 怎麼部署到 EC2 上？

## Phase 7 多環境
需求: 有 dev / staging / production 三個環境
- pipeline 會怎麼調整？