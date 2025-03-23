# MetroSimulation
# Metro Simülasyonu

Bu proje, bir metro ağındaki istasyonlar arasında en az aktarmalı ve en hızlı rotaları bulmak için geliştirilmiş bir simülasyondur. 

## Özellikler

- **İstasyon Ekleme**: Metro ağına yeni istasyonlar eklenebilir.
- **Bağlantı Ekleme**: İstasyonlar arasında bağlantılar (hatlar) tanımlanabilir.
- **En Az Aktarmalı Rota Bulma**: İki istasyon arasında en az aktarmalı rotayı bulur.
- **En Hızlı Rota Bulma**: İki istasyon arasında en kısa sürede ulaşım sağlayan rotayı bulur.

## Nasıl Çalışır?

Proje, iki ana sınıf üzerine kuruludur:

1. **Istasyon**: Her bir istasyonun kimliği (`idx`), adı (`ad`) ve bağlı olduğu hat (`hat`) bilgilerini içerir. Ayrıca, komşu istasyonlar ve bu istasyonlara ulaşım süreleri de bu sınıfta saklanır.
2. **MetroAgi**: Metro ağını temsil eder. İstasyonlar ve bağlantılar bu sınıf tarafından yönetilir. Ayrıca, en az aktarmalı ve en hızlı rotaları bulmak için gerekli algoritmalar bu sınıfta yer alır.

### Algoritmalar

- **En Az Aktarmalı Rota Bulma (BFS)**: Breadth-First Search (BFS) algoritması kullanılarak, iki istasyon arasında en az aktarmalı rota bulunur.
- **En Hızlı Rota Bulma (A*)**: A* algoritması kullanılarak, iki istasyon arasında en kısa sürede ulaşım sağlayan rota bulunur.

## Kurulum ve Kullanım

1. **Gereksinimler**: Bu proje, Python 3.x ile çalışmaktadır. 

2. **Kodu Çalıştırma**:
   - Proje dosyasını (`ElifnazGür_MetroSimulation.py`) indirin veya kopyalayın.
   
3. **Test Senaryoları**:
   - Kod içinde örnek bir metro ağı tanımlanmıştır ve bu ağ üzerinde üç test senaryosu çalıştırılır:
     1. **AŞTİ'den OSB'ye**: AŞTİ istasyonundan OSB istasyonuna en az aktarmalı ve en hızlı rotalar bulunur.
     2. **Batıkent'ten Keçiören'e**: Batıkent istasyonundan Keçiören istasyonuna en az aktarmalı ve en hızlı rotalar bulunur.
     3. **Keçiören'den AŞTİ'ye**: Keçiören istasyonundan AŞTİ istasyonuna en az aktarmalı ve en hızlı rotalar bulunur.

   - Her senaryo için, en az aktarmalı rota ve en hızlı rota bilgileri ekrana yazdırılır.

## Örnek Çıktı

=== Test Senaryoları ===

1. AŞTİ'den OSB'ye:
En az aktarmalı rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB
En hızlı rota (24 dakika): AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB

2. Batıkent'ten Keçiören'e:
En az aktarmalı rota: Batıkent -> Demetevler -> Gar -> Keçiören
En hızlı rota (21 dakika): Batıkent -> Demetevler -> Gar -> Keçiören

3. Keçiören'den AŞTİ'ye:
En az aktarmalı rota: Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ
En hızlı rota (14 dakika): Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ
