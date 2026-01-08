FROM debian:stable
WORKDIR /app
#COPY ./TomatoNovelDownloader* /app/

#在线下载默认amd64如需arm64修改下载链接
RUN apt-get update && apt-get install -y curl
RUN curl -L -o ./TomatoNovelDownloader \
    "https://github.com/zhongbai2333/Tomato-Novel-Downloader/releases/download/v2.1.1/TomatoNovelDownloader-Linux_amd64-v2.1.1" \
    && chmod +x ./TomatoNovelDownloader

EXPOSE 18423
ENV TOMATO_WEB_ADDR=0.0.0.0:18423
CMD ./TomatoNovelDownloader* --server --data-dir ./config
