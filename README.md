# Magic Wormhole 檔案傳輸解決方案

方便且安全地將檔案自一地傳輸到另一地，由 Brian Warner 所開發用於推廣 PAKE(Password-authenticated key agreement) 金鑰產生演算法

![「檢查專案中的潛在問題」GitHub Actions 作業流程狀態標章](https://github.com/libre-knowledge/magic-wormhole/actions/workflows/check-potential-problems.yml/badge.svg "本專案使用 GitHub Actions 自動化檢查專案中的潛在問題") [![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white "本專案使用 pre-commit 檢查專案中的潛在問題")](https://github.com/pre-commit/pre-commit) [![REUSE 規範遵從狀態標章](https://api.reuse.software/badge/github.com/libre-knowledge/magic-wormhole "本專案遵從 REUSE 規範降低軟體授權合規成本")](https://api.reuse.software/info/github.com/libre-knowledge/magic-wormhole)

## 基本概念說明

以下說明與 Magic Workhole 有關的一些概念：

### PAKE(Password-authenticated key agreement) 金鑰產生演算法

將簡短的資訊轉換程強密碼的演算法

於 Magic Wormhole 的應用中為將一個傳送、接收者雙方共同知道，簡短易讀由 1 數字與二英文字組成的字串轉換為實際用來加密傳輸之資料的作業階段金鑰(session key)的邏輯

### 客戶端

終端使用者所使用的軟體組件，Python 包索引(PyPI)識別名稱為 `magic-wormhole`

### 會合服務器<br>Rendezvous Server

用於客戶端間傳遞初始訊息與產生作業階段金鑰(session key)的服務，不用於實際的資料傳輸

### 轉發中繼服務器<br>Data/Transit Relay Server

當客戶端間無法直接建立連接時負責將二客戶端與其的連接接在一起以轉發*加密後的*客戶端資料的服務，由上游開發者或是下游軟體散佈者所提供，也可以自行架設

## 解決方案<br>Solutions

* [The Magic Wormhole Transit Relay Server Ansible Role](https://github.com/brlin-tw/ansible-role-magic-wormhole-transit-relay)  
  Swiftly and precisely deploy the Magic Wormhole Transit Relay service on multiple servers

## 參考資料

* [magic-wormhole/magic-wormhole: get things from one computer to another, safely](https://github.com/magic-wormhole/magic-wormhole)  
  官方專案網站
* [Magic-Wormhole documentation](https://magic-wormhole.readthedocs.io/)  
  官方說明文件
* [PyCon 2016 官方介紹簡報](https://www.lothar.com/%7Ewarner/MagicWormhole-PyCon2016.pdf)（[錄影](https://www.youtube.com/watch?v=oFrTqQw0_3c)）  
  說明解決方案的理念與實現細節
* [magic-wormhole/magic-wormhole-transit-relay: Transit Relay server for Magic-Wormhole](https://github.com/magic-wormhole/magic-wormhole-transit-relay)  
  官方中繼轉發服務實現
* [magic-wormhole · PyPI](https://pypi.org/project/magic-wormhole/)  
  客戶端的 Python 包索引頁

---

本主題為[自由知識協作平台](https://libre-knowledge.github.io/)的一部分，除部份特別標註之經合理使用(fair use)原則使用的內容外允許公眾於授權範圍內自由使用

如有任何問題，歡迎於本主題的[議題追蹤系統](https://github.com/libre-knowledge/magic-wormhole/issues)創建新議題反饋
