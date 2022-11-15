# api-doc


## Poem import for none-original poem
1. Get access token from /api/v1/user/login
```cmd
curl --location --request POST 'https://poemwiki.org/api/v1/user/login' \
--header 'Accept: application/json' \
--header 'Content-Type: application/json' \
--data-raw '{"email": "****@*.com", "password": "1234****"}'
```

2. Post poem data to api/v1/poem/import
```cmd
curl --location --request POST 'https://poemwiki.org/api/v1/poem/import' \
--header 'Accept: application/json' \
--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGc......' \
--header 'Content-Type: application/json' \
--data-raw '{
    "poems": [
        {
            "title": "红花草",
            "poet": "阿斐",
            "poem": "冬天了，广州并不冷\n在铸山村，我的家乡",
            "language_id": 1
        },
        {
            "title": "和谁对饮",
            "poet": "阿斐",
            "poem": "是一个陌生人\n还是老相识\n已不重要",
            "language_id": 1
        }
    ]
}'
```
All fields are required. `language_id` must be in [supported language list](#supported-languages)

3. Check recent contributions at https://poemwiki.org/contribution


## Supported Languages
|id |name                                   |name_cn|locale|
|---|---------------------------------------|-------|------|
|1  |简体中文                                   |简体中文   |zh-CN |
|2  |English                                |英语     |en    |
|3  |Deutsch                                |德语     |de    |
|4  |français                               |法语     |fr    |
|5  |Italiano                               |意大利语   |it    |
|6  |Español                                |西班牙语   |es    |
|7  |にほんご                                   |日语     |ja    |
|8  |조선말                                    |朝鲜语    |kr    |
|9  |Ελληνικά                               |希腊语    |el    |
|10 |ру́сский язы́к                         |俄语     |ru    |
|11 |Português                              |葡萄牙语   |pt    |
|12 |Polski                                 |波兰语    |pl    |
|13 |svenska                                |瑞典语    |sv    |
|14 |हिन्दी                                 |印度语    |hi    |
|15 |اَلْعَرَبِيَّةُ‎                       |阿拉伯语   |ar    |
|16 |עִבְרִית                               |希伯来语   |he    |
|46 |अवधी                                   |阿瓦德语   |awa   |
|103|čeština                                |捷克语    |cs    |
|108|dansk                                  |丹麦语    |da    |
|128|eesti keel                             |爱沙尼亚语  |et    |
|132|زبان فارسی                             |波斯語    |fa    |
|160|Galego                                 |加利西亚语  |gl    |
|178|hrvatski jezik                         |克罗地亚语  |hr    |
|229|Latine                                 |拉丁语    |la    |
|263|македонски јазик                       |马其顿语   |mk    |
|292|Nederlands                             |荷兰语    |nl    |
|294|norsk                                  |挪威语    |no    |
|367|Sängö                                  |桑戈语    |sg    |
|381|slovenščina                            |斯洛文尼亚语 |sl    |
|391|Gjuha shqipe                           |阿尔巴尼亚语 |sq    |
|421|Türkçe                                 |土耳其语   |tr    |
|436|Українська мова                        |乌克兰语   |uk    |
|487|ئەرەب ھەرپلىرى ئاساسىدىكى ئۇيغۇر يېزىقى|传统维文   |ug-arab|
|491|繁體中文                                   |繁体中文   |zh-hant|
