<h1>WoMoM için bilgilendirme</h1>
 
<h2>JSON içerisinde tanımlanması gereken module tipleri:</h2>

| Module Tipi     | Sayı Karşılığı  | 
|-----------------|-----------------|
| Video           | 1       | 
| Döküman        | 2        | 
| Anket        | 3       | 
 
<h2>Örnek JSON Formatları</h2>

#### Her bir module için örnek JSON dosyası
 
```json
 {
    "tag": "Kadın Okuryazarlığı",
    "modules": [
        {
            "type": 1,
            "label": "Education Video",
            "url": "https://youtu.be/RTj7_HMCBeI?si=vsBJ6F_-cqkhfYHC",
            "description": "Kadın okuryazarlığı, kadınların eğitim ve bilgiye erişimini artırarak toplumsal eşitliği destekler."
        },
        {
            "type": 2,
            "label": "Documents",
            "documents": [
                {
                    "documentName":"egitimde-cinsiyet-esitligi",
                    "tag": "Eğitimde Cinsiyet Eşitliği"
                },
                {
                    "documentName":"kadınlar-ve-egitim-erisimi",
                    "tag": "Kadınlar ve Eğitim Erişimi"
                }
            ]
        },
        {
            "type": 1,
            "label":"Extra Education Video",
            "url": "https://youtu.be/imwmmv9r1oE?si=swWlSquIdEnI0yRW",
            "description": "Kadın okuryazarlığı, kadınların eğitim ve bilgiye erişimini artırarak toplumsal eşitliği destekler."
        },
        {
            "type":3,
            "label":"Survey Questions"
        }
    ]
}
```
