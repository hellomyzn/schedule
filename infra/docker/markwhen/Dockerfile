FROM node:18-alpine

WORKDIR /app

# 必要なパッケージのみインストール
RUN apk add --no-cache bash && \
    npm install -g @markwhen/mw nodemon

# nodemon を使って habit.mw の変更を監視
CMD ["nodemon", "--ext", "mw", "--exec", "mw serve /app/schedule.mw"]