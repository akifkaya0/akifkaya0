# M. Akif Kaya

## Kronset

Kronset, HIIT, Tabata ve koşu aralıkları gibi süreli antrenmanlar için bir aralık sayacı. Her antrenman çalışma, dinlenme ve iç içe kurulabilen tekrar adımlarından oluşur. Başlatıldığında süreleri uygulama tutar ve adım değiştikçe sesle uyarır; antrenman boyunca telefona bakmak gerekmez. Türkçe ve İngilizce dahil 11 dilde kullanılabilir; hesap, reklam ve takip içermez.

[kronset.com](https://kronset.com)

<!-- Uygulama App Store'da görününce aç: [App Store'da indir](https://apps.apple.com/app/id6824268800) -->
<!-- Uygulama Google Play'de görününce aç: [Google Play'den indir](https://play.google.com/store/apps/details?id=com.kronset.app) -->

<p>
  <img src="kronset/1-list.png" width="180" alt="Antrenman listesi">
  <img src="kronset/2-run-work.png" width="180" alt="Çalışma adımı">
  <img src="kronset/3-run-rest.png" width="180" alt="Dinlenme adımı">
  <img src="kronset/4-editor.png" width="180" alt="Düzenleyici">
</p>

React 19 · TypeScript · Tailwind CSS 4 · Capacitor 8 · Swift

## Tasky

Tasky, gün içinde not almaya ve hangi işe ne kadar zaman harcandığını kaydetmeye yarayan bir masaüstü uygulaması. Sistem tepsisinde çalışır; simgeye tıklayınca açılan küçük pencereden not yazılır ya da bir görev başlatılıp bitirilir. Çalışılan süreler haftalık takvimde kayıt olarak görünür ve orada düzenlenir. Bir çalışma sürerken tepsi simgesi alev gibi yanar, her saat dolduğunda da bildirim gelir; böylece bitirilmesi unutulan bir çalışma gözden kaçmaz.

<p>
  <img src="tasky/takvim.png" width="732" alt="Takvim ve haftalık özet">
</p>
<p>
  <img src="tasky/hizli-not.png" width="240" alt="Hızlı not">
  <img src="tasky/gorevler.png" width="240" alt="Görev listesi">
  <img src="tasky/calisiyor.png" width="240" alt="Süren çalışma">
</p>

Görevler bir iş takip aracı gibi başka bir sistemden gelir; takvimdeki süreler de aynı ya da başka bir sisteme aktarılır. Bu bağlantılar uygulamaya gömülü değildir; her sistem için tek bir JavaScript dosyası (bağlayıcı) yazılıp bir klasöre konur. Hesap gerektiren sistemlerde kullanıcı sağlayıcının kendi sayfasında giriş yapar; şifre uygulamaya uğramaz, oturum ve gizli ayarlar bilgisayarda şifrelenerek saklanır.

Electron 44 · React 19 · TypeScript · Tailwind CSS 4 · HeroUI · NeDB

## Trace Tail

Trace Tail, IntelliJ IDEA'dan çalıştırılan Java uygulamalarının loglarını canlı olarak ve ait oldukları isteğe göre gruplayarak gösteren bir eklenti. Loglar tek bir uzun akış olarak değil, istek başına bir satır olarak listelenir. Bir istek seçilince satırları, hangi adımın hangisini başlattığına göre iç içe görünür. Aynı istek, uygulamalar ve sınıflar arasında kimin kimi çağırdığını gösteren bir sequence diyagramı olarak da çizilir. Böylece birden fazla uygulamadan geçen bir isteğin hangi adımlardan oluştuğu ve nerede hata verdiği tek bakışta görülür.

[GitHub](https://github.com/akifkaya0/trace-tail) · [JetBrains Marketplace](https://plugins.jetbrains.com/plugin/34886)

<p>
  <img src="https://raw.githubusercontent.com/akifkaya0/trace-tail/main/docs/images/tree-steps.png" width="732" alt="İstek listesi ve seçili isteğin adımları">
</p>
<p>
  <img src="https://raw.githubusercontent.com/akifkaya0/trace-tail/main/docs/images/tree-sequence.png" width="732" alt="Seçili isteğin sequence diyagramı">
</p>

Uygulamanın kendisinde değişiklik gerekmez. Eklenti, IDE'den başlatılan her Java uygulamasına kendi Java agent'ını ekler; agent çalışma anında uygulamanın Logback ya da Log4j2'sine bağlanır ve her log satırını ECS JSON olarak IDE'nin yalnızca bu bilgisayardan erişilebilen bir portuna gönderir. Eklenti satırları `trace.id`, `span.id` ve `parent.id` alanlarına göre isteklere ve adımlara ayırır.

Kotlin · IntelliJ Platform · Java (agent) · Gradle
