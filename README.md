# api-doc


## Poem import for none-original poem
1. Get access token from /api/v1/user/login
```cmd
curl --location --request POST 'https://poemwiki-dev.com/api/v1/user/login' \
--header 'Accept: application/json' \
--header 'Content-Type: application/json' \
--data-raw '{"email": "****@*.com", "password": "1234****"}'
```

2. Post poem data to api/v1/poem/import
```cmd
curl --location --request POST 'https://poemwiki-dev.com/api/v1/poem/import' \
--header 'Accept: application/json' \
--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGc......' \
--header 'Content-Type: application/json' \
--data-raw '{
    "poems": [
        {
            "title": "红花草",
            "poet": "阿斐",
            "poem": "冬天了，广州并不冷\n在铸山村，我的家乡"
        },
        {
            "title": "和谁对饮",
            "poet": "阿斐",
            "poem": "是一个陌生人\n还是老相识\n已不重要"
        }
    ]
}'
```

3. Check recent contributions at https://poemwiki-dev.com/contribution
