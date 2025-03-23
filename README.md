# bootcamp_akbank
# Sürücüsüz Metro Simülasyonu

## Proje Hakkında
Bu projede, metro ağında **en az aktarmalı** ve **en hızlı** rotayı bulmayı amaçladım. 
Bunu yaparken **BFS** ve **A*** algoritmalarını kullandım. Kullanıcılar başlangıç ve hedef istasyonlarını seçerek en uygun güzergahı öğrenebiliyor.

## Kullandığım Teknolojiler ve Kütüphaneler
- **Python**: Projenin geliştirme dili.
- **collections.deque**: BFS için kuyruk yapısı.
- **heapq**: A* algoritması için öncelik kuyruğu.
- **defaultdict**: Metro hatlarını düzenlemek için.
- **typing**: Kodun daha okunabilir olması için tip tanımlamaları.

## Algoritmaların Çalışma Mantığı

### **BFS – En Az Aktarma**
BFS, düğümleri katman katman keşfederek en kısa adımda hedefe ulaşmayı sağlar.
1. **Kuyruk (deque) kullanılır**, başlangıç istasyonu kuyruğa eklenir.
2. **Ziyaret edilen istasyonlar takip edilir**, böylece aynı noktaya dönmek önlenir.
3. **Komşular sırayla işlenir**, aktarmasız ilerleme önceliklidir.
4. **Hedefe ulaşıldığında güzergah döndürülür**.

### **A* – En Hızlı Rota**
A* algoritması, en kısa sürede hedefe varan yolu bulmak için öncelik kuyruğu kullanır.
1. **Toplam geçiş süreleri hesaplanır**.
2. **Öncelik kuyruğundaki en kısa süreli güzergah seçilir**.
3. **En hızlı rota bulunur ve süreyle birlikte döndürülür**.

### **Bu Algoritmaları Neden Seçtim?**
- **BFS**, en az hat değiştirerek ulaşmayı garanti ediyor.
- **A***, ağırlıklı grafikte en kısa sürede hedefe ulaşmak için en iyi seçenek.
- İkisini birleştirerek hem pratik hem de hızlı bir ulaşım modeli oluşturdum.

## Örnek Kullanım
Kod çalıştırıldığında aşağıdaki gibi kullanılabilir:

```python
python metro_simulation.py
```

Örnek çıktı:
```
En az aktarmalı rota:
Istasyon A -> Istasyon B -> Istasyon C

En hızlı rota:
12 dakika: Istasyon A -> Istasyon B -> Istasyon C
```

## Projeyi Nasıl Geliştirebilirim?
- **Görselleştirme eklemek**: Metro hattını grafik olarak çizdirmek.
- **Gerçek zamanlı trafik**: İstasyon yoğunluklarını hesaba katmak.
- **Farklı ulaşım türleri**: Otobüs, tramvay gibi diğer ulaşım araçlarıyla entegrasyon sağlamak.

