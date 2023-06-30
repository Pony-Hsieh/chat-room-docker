# 決定基底映像檔
FROM node:20-alpine

# 設定環境變數
ENV DIR=/backend

# 創建資料夾
RUN mkdir -p ${DIR}

# 設定工作目錄
WORKDIR ${DIR}

# 將整個資料夾複製到工作目錄
COPY . ${DIR}

# 安裝 dependencies
RUN npm install
# 清除 npm 快取後再安裝
# RUN npm cache clean --force && npm install

EXPOSE 7654

CMD ["node", "server.js"]