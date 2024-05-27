<h2 align="center">
    Cloud-DevOps
</h2>

## [LaTeX](/https://zh.wikipedia.org/zh-tw/LaTeX)
LaTex為一種程式語言，支援標準庫和外部程式庫，不過與一般程式語言不同的是，它可以直接表述Tex排版結構，類似於PHP之於HTML的概念，但是直接撰寫LaTex仍較複雜，因此可以藉由Markdown或其他輕量的標註式語言先行完成文章，再交由LaTex排版。

LaTeX可用於創建高質量的文件，例如論文、書籍和報告，它是一種功能強大的工具，但學習和使用難度較高。


## [Releases](/https://github.com/kuanhaolin/Cloud-DevOps/releases)
由Github Action中的workflow將Tex檔案轉換成PDF文件，並且發佈版號可以至releases查看。

觸發條件:
1. push pdf或main分之且更新latex文件夾
2. pull pdf分支
3. 手動更新
```
on:
  push:
    branches:
      - pdf
      - main
    paths:
      - 'latex/**'
  pull_request:
      branches: [ pdf ]
  workflow_dispatch:
  ```
