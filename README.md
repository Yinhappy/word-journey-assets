# 词途 (Word Journey) - 静态资源仓库

存放 **word-journey** 微信小程序所需的词库 JSON 文件。

通过 **jsDelivr CDN** 提供全球加速访问，**小程序端按需下载**，主包保持小巧。

## 文件说明

- `static/<id>.json` — 各词库数据
- `manifest.json` — 词库清单(可选,用于 app 端动态加载)

## 词库列表

| ID | 名称 | 词数 | 大小 |
|---|---|---|---|
| cet4 | CET4 真题核心词 | 1162 | 1.3 MB |
| cet6 | CET6 真题核心词 | 1228 | 1.2 MB |
| kaoyan | 考研必考词汇 | 1341 | 1.4 MB |
| gaozhong | 高考必备词汇 | 3668 | 3.7 MB |
| ielts | 雅思词汇 | 3427 | 3.1 MB |
| toefl | TOEFL 词汇(新东方精选) | 4264 | 3.9 MB |
| bec | BEC 商务英语 | 2753 | 2.8 MB |
| chuzhong | 中考必备词汇 | 1420 | 1.5 MB |
| xiaoxue | 小学英语(人教版,合并 8 分册) | 819 | 0.7 MB |

## CDN 访问

通过 jsDelivr 加速:
```
https://cdn.jsdelivr.net/gh/yhmmd2015/word-journey-assets@main/static/cet6.json
```

## 数据来源

词库数据来自开源仓库 [kajweb/dict](https://github.com/kajweb/dict),基于有道考神团队的真题词频整理。

## 词库数据格式

每个 JSON 文件是一个数组,每个元素结构如下:
```json
{
  "rank": 1,
  "word": "access",
  "phonetic": { "us": "'æksɛs", "uk": "'ækses" },
  "translations": [
    { "pos": "v", "meaning": "获取" },
    { "pos": "n", "meaning": "接近,入口" }
  ],
  "sentences": [
    { "en": "Users can access their voice mail remotely.", "cn": "用户可以远程获取语音邮件。" }
  ],
  "phrases": [{ "phrase": "have access to", "meaning": "使用" }],
  "synonyms": [],
  "related": [{ "pos": "adj", "word": "accessible", "meaning": "易接近的" }],
  "memory": "ac + cess(去) → 来去要走通道 → 通道",
  "image": "http://ydschool-online.nos.netease.com/CET4luan_1_1_access_xxx.png"
}
```

## 添加新词库

1. 准备清洗好的 JSON,放入 `static/<new_id>.json`
2. 更新本 README 的词库列表
3. (可选)更新 `manifest.json`
4. commit 并 push 到 Gitee
5. 小程序端无需任何代码改动,刷新缓存即可

## License

数据遵循 [kajweb/dict](https://github.com/kajweb/dict) 仓库的开源协议。
