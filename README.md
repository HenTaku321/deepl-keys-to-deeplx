## 介绍
使多个DeepL Free/Pro API可以通过DeepLX调用, 调用顺序为随机

更新: 现已支持混合其他DeepLX API

当你拥有很多个DeepL Free/Pro API或DeepLX API时, 这个程序就很有用

## 注意
只适用于DeeplX调用而不是DeepL

在部署前请编辑apis.txt, 一行填入一个DeepL Free/Pro API或DeepLX API

## 部署

### Docker部署
```
sudo docker run -d -v ./apis.txt:/apis.txt -p 9000:9000 hentaku/deepl-keys-to-deeplx
```
### 本机部署
```
go build main.go && nohup ./main &
```

## 使用
和DeepLX一致

请求localhost:9000/check-alive可重新测活一次
