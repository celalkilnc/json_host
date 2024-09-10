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
        {
            "image": "https://celalkilnc.github.io/json_host/media/grey.jpg",
            "tag": "Kadın Okuryazarlığı",
            "text": "Kadın okuryazarlığı, toplumun ilerlemesi için temel bir güçtür.",
            "id": "1"
        },
        {
            "image": "https://celalkilnc.github.io/json_host/",
            "tag": "test",
            "text": "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
            "id": "2"
        }
    ]
}
```
 
### Modül içeriği

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
<h2>Döküman Modülü Dosyası</h2>
Döküman dosyaları için "Döküman içerikli mdül örneği" alanındaki örnekte belirtilen 'documentName' alanıyla aynı olacak şekilde ayrı JSON dosyaları oluşturulur.
Tanımlanan JSON içeriğinde dosyanın ismi ve liste tanımlanır. Liste, 'text' isminde olmalıdır ve listenin her bir öğesi dökümanın her bir paragrafına eşdeğerdir.

Aşağıda 'egitimde-cinsiyet-esitligi' dosyası örnek olarak verilmiştir

```json
{
    "documentName": "Eğitimde cinsiyet eşitliği",
    "text": [
        "Eğitimde cinsiyet eşitliği, bireylerin cinsiyeti ne olursa olsun eşit fırsatlara sahip olması anlamına gelir. Bu, hem erkekler hem de kadınlar için eğitimde fırsat eşitliğini sağlamak ve cinsiyet tabanlı ayrımcılığı ortadan kaldırmak amacıyla atılacak adımları içerir. Eğitimde cinsiyet eşitliği sağlamak, bireylerin potansiyellerini en üst düzeye çıkarmalarını ve toplumsal eşitliği teşvik etmelerini destekler. İşte eğitimde cinsiyet eşitliği ile ilgili bazı önemli noktalar:",
        "Erişim ve Katılım: Eğitimde cinsiyet eşitliği, hem kız hem de erkek çocukların eğitim fırsatlarına eşit erişimlerini sağlamayı içerir. Bu, tüm çocukların, cinsiyeti ne olursa olsun, eğitim sistemine dahil olmalarını ve eğitimden yararlanmalarını güvence altına alır.",
        "Müfredat ve Öğretim: Cinsiyet eşitliğini destekleyen bir müfredat, hem erkeklerin hem de kadınların başarılarını ve katkılarını vurgular. Öğretim materyallerinin cinsiyet kalıpyargılarını içermemesi ve çeşitli cinsiyet rollerini teşvik etmeyen bir dil kullanılması önemlidir.",
        "Rol Modeli ve Mentorluk: Öğrencilere güçlü rol modeller sunmak, özellikle kadın öğrenciler için önemlidir. Kadın öğretmenler ve yöneticiler, kız çocuklarının eğitim ve kariyer hedeflerine ulaşmalarını teşvik edebilir. Aynı şekilde, erkek çocuklar için de olumlu rol modeller sunulmalıdır.",
        "Ayrımcılığın Önlenmesi: Eğitim kurumları, cinsiyet temelli ayrımcılığı engellemek için politika ve uygulamalar geliştirmelidir. Ayrımcılığın önlenmesi, cinsiyete dayalı şiddet ve tacizle mücadele, adil ve eşit bir eğitim ortamının oluşturulmasında kritik rol oynar.",
        "Eğitim Politikalarda Cinsiyet Eşitliği: Eğitim politikaları ve düzenlemeleri, cinsiyet eşitliğini teşvik etmek ve cinsiyete dayalı engelleri ortadan kaldırmak için tasarlanmalıdır. Bu, burs ve destek programları, cinsiyet eşitliği eğitimi ve cinsiyet dengesizliğini azaltma stratejilerini içerebilir."
    ]
}
```

<h2>Günlük Söz</h2>
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
