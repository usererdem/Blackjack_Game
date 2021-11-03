Creating a blackjack card game -->

Possible Variables --> 
highestMoney = 1000
currentMoney = 1000
roundsWon = 0
cardsLeft = 104

Possible eventlisteners --> 
blackChip veya chip100
redChip veya chip50
greenChip veya chip20
Play veya Deal button
Hit button
Doublex2 button
Split button 
Stand button 
End the game button 

Game Rules --> 
x2 deste --> 104 kart her karttan 2 tane var
 

kac para ile bahse gireceğini seçersin :  --> gsap ile yapmayı deneyebilirsin

Ekranda solda total paran yazar
Hemen altında tüm paranı yatırma butonu
Altında 20 50 100 lük çipler görsel olarak
Görsele tıkladığında bahis o miktarda artar.

Ortada nekadarlık bahis ile oyuna gireceğin yazar,
Hemen altında yatırdığın çiplerin görseli,
Çiplere tıklarsan yatıracağın para miktarını 0'a kadar azaltabilirsin

Sağda Deal veya Play butonu ile oyuna başlayabilirsin.

Create two seperate objects for 1,2,3,4,5,King etc. and Spades,hearts etc.

Game will generate random number to generate a random ace to king value
Game will generate random number to generate a random Spades etc. value
(use to value to find the matching value in object)

ace to king value kartın değerlerinin belirleneceği kısım,
2 = 2 puan gibi object üzerinden değerler belirlenecek
ace = 1 veya 11 duruma göre bunun implemente edeceksin,
21 puanı geçerse oyun ace varmı kontrol edecek ve eğer varsa,
ace değeri 11 yerine 1 olacak

spades etc. yardımı ile ekrana konulacak görsel belirlenecek.

Desteden random 2 kart verilir açık şekilde
kasa da 2 kart alır kartlardan biri kapalı olarak durur.
kart miktarı güncellenir (yani oyun başı 4 kart dağıtılacak 100cards left)
 ve oynanan kartlar desteden gider,

destedeki kart miktarı sürekli olarak check edilir --> 
ör: kart sayısı 55'in altına düşerse yeni bahise başlanırken,
deste tekrardan x2 deste 104 kart olarak 0'lanır.

if 
  kart değerlerin aynı ise split seçeneği de olan bir menü çıkar
  if 
    splite basarsan kartlar ayrılır ve 2 farklı el oynarsın
else
  if 
    hit butonuna tıklarsan 1 kart eklenir
  else if 
    double x2 butonuna tıklarsan başta yatırdığın bahis 2ye katlanır,
    bir kart verilir ve el sonlanıp sonuçlara bakılır
  else if 
    stand butonuna bastıgında el sonlanıp sonuclara bakılır

el sonunda yatırdığın para miktarı kadar para kazandıysan total parana eklenir,
kazanılan el sayısı +1
kaybettiysen total parandan düşülür, berabere bittiyse değişmez

Güncellenmiş paran ile birlikte Yeni el için bahis ekranı gelir
if --> highest money < current money --> current money = highest money

Fonksiyonlar --> 

dealerCardReveal fonksiyonu
  dealerın kapalı olan kartı açılır,
  Natours projesindeki kart çevirme animasyonunu buraya uygulayabilirsin

dealerCardDraw fonksiyonu
  dealer deger 17 veya 17den büyük olana kadar dealera yeni kart çeker,

resultCheck fonksiyonu 
  senin elin mi yoksa dealırın eli mi kazanıyor kontrol edilir,
  21 kazanan el, 21'den küçük ise 21'e yakın olan el, 21'den büyük rakam batar
  Değerler eşit gelirse push olur - berabere biter
  Player ve Dealer yanında yazacak olan rakamlar üzerinden yapılabilir

currentPoint fonksiyonu
  çağrıldığında 2 değer alıp toplayıp
  o değeri return eder 
  ilk başta 2 kartın toplamı için sonrasında kart çekersen,
  2 kart toplam değeri tek değer olacak, yeni eklenen kart ile toplanacak
  (return edilen değer Player ve Dealer yanındaki puanları güncellemek için kullanılacak)

Sol üstte oyunu bitir butonu olacak -->
Tıkladığında 

Oyun sonu paran --> 1200 dolar
Kaç el kazandığın --> 5
En çok oyun süresince kaç paraya ulaştığın --> 1400 dolar
Income --> Profit / Loss --> Oyun sonu paran - 1000





