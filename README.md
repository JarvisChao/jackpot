# **JACKPOT**

## **Table of Contents**

  * [Usage](#usage)
  * [Notice](#notice)
  * [License](#license)

## **Usage**

/database/config.json 設置
```json
{
  "title": "至尊柏青哥",
  "jackpotName": ["至尊JP1" ,"至尊JP2" ,"至尊JP3" ,"至尊招財" ,"至尊進寶"],
  "api": "http://jpct.aaforfun.com/api/jackpot_setting",
  "apiRecord": "http://jpct.aaforfun.com/api/jackpot_record"
}
```
## **Notice !**
Record API 沒有給 id，所以只能抓預設 name 值，如果替換新的 api 而 name 值不同將顯現空白
- Record API
```json
{
  "location": "足球小將翼15號 恭賀24597珠 B區皇室",
  "name": "至尊進寶",
  "score": 3700,
  "time": "2021-11-01 15:26:37"
}
```

- 目前 js 寫死抓到的預設 name 值
```js
const nameFilter = (val) => {
  const nameMap = {
    '至尊JP1': config.data.jackpotName[0],
    '至尊JP2': config.data.jackpotName[1],
    '至尊JP 3': config.data.jackpotName[2],
    '至尊招財': config.data.jackpotName[3],
    '至尊進寶': config.data.jackpotName[4]
  }
  return nameMap[val]
}
```


## **License**

Copyright (c) 2021 [JarvisChao](https://github.com/JarvisChao/)
