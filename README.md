<h1>WoMoM</h1>
 
<h2>JSON içerisinde tanımlanması gereken module tipleri:</h2>

| Module Tipi     | Sayı Karşılığı  | 
|-----------------|-----------------|
| Video | 1 | 
| Döküman | 2 | 
| Anket | 3 | 
 
<h2>Örnek JSON Formatları</h2>

### Modüller
Moduller sayfasında kullanıcıyı içeriğe yönlendirmek için listelenen modülleri 'moduleDetail.json' dosyası içerisinde aşağıdaki formatta eklemek gerekmektedir.
Her bir modül içerisine, yönlendirileceği detay sayfasının dosya ismi Id olarak tanımlanmalıdır. Daha sonra burada tanımlanan id ile '.json' uzantılı bir dosya oluşturulmalıdır.

```json
{
    "modules": [
        { "image": "https://celalkilnc.github.io/json_host/media/grey.jpg", "tag": "Kadın Okuryazarlığı", "text": "Kadın okuryazarlığı, toplumun ilerlemesi için temel bir güçtür.", "id": "1" },
        { "image": "https://celalkilnc.github.io/json_host/", "tag": "test", "text": "Lorem ipsum dolor sit amet, consectetur adipisicing elit.", "id": "2" }, 
    ]
}
```
 
#### Modül içeriği

'moduleDetail.json' içerisinde tanımlanan her bir modülün id'si ile oluşan örnek JSON dosyası aşağıdaki gibidir. Modüllün türüne göre yukarıda belirtilen 'type' değeri verilmelidir.
Sayfada modül sınırı yoktur listeye gerektiği kadar eklenebilir.
 
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
            "type":3,
            "label":"Survey Questions"
        }
    ]
}
```
#### Video içerikli mödül örneği
```json
{
    "type": 1,
    "label": "Education Video",
    "url": "https://youtu.be/RTj7_HMCBeI?si=vsBJ6F_-cqkhfYHC",
    "description": "Kadın okuryazarlığı, kadınların eğitim ve bilgiye erişimini artırarak toplumsal eşitliği destekler."
}
```

#### Döküman içerikli mödül örneği
```json
{
    "type": 2,
    "label": "Documents",
    "documents": [
        {
            "documentName": "egitimde-cinsiyet-esitligi",
            "tag": "Eğitimde Cinsiyet Eşitliği"
        },
        {
            "documentName": "kadınlar-ve-egitim-erisimi",
            "tag": "Kadınlar ve Eğitim Erişimi"
        }
    ]
}
```
<h3>Günlük Söz</h3>
Ana sayfada her gün farklı bir söz tanımlamak için 'quoteOfDay.json' adındaki dosyaya 'Quotes' listesinde sözlerin tanımlanması gerekmektedir.
Listeyi baştan sona gezerek her gün yeni bir söz gösterilecektir ve liste bittiğinde başa dönecektir.


```json
{
  "Quotes":[
    "Bir annenin karnında yeşeren her hayat, dünyanın en büyük mucizesidir.",
    "Bir annenin karnında yeşeren her hayat, dünyanın en büyük mucizesidir.2",
    "Bir annenin karnında yeşeren her hayat, dünyanın en büyük mucizesidir.3"
  ]
}
```
