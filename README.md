# 如何跑起來:
#### 1. 創建專案資料夾，並初始化環境
> 設定 github pages 並軟連結至 public_html 中，
> 接著建立 package.json, 並安裝 yarn


#### 2. 創建一個 src 資料夾
> src 資料夾裡放 index.pug, aboutus.sass, aboutus.js
> origin 資料夾中放的是原版的 index.html, aboutus.css


#### 3. aboutus.pug 連結 aboutus.css 和 aboutus.js
> link(href="./dist/aboutus.css", rel="stylesheet")
> script(src="./dist/aboutus.js")


#### 4. preprocess
> 執行以下指令將./src中的 pug, sass 檔分別轉譯成 html, css檔，並儲存在 ./dist 中
> ./node_modules/.bin/pug3 ./src/index.pug -o ./dist
> ./node_modules/.bin/node-sass ./src/aboutus.sass -o ./dist


#### 5. alternative way
> 利用tmux執行以下指令監聽，存檔時會自動將./src中的 pug, sass轉譯成 html, css檔，並儲存在 ./dist 中
> ./node_modules/.bin/pug3 ./src/index.pug -o ./dist --watch
> ./node_modules/.bin/node-sass ./src/aboutus.sass -o ./dist --watch


#### 6. 網站網址
> https://luffy.ee.ncku.edu.tw/~e24094025/AboutUs_preprocessor/dist/index.html
