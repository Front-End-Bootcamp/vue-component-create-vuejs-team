[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=8837419&assignment_repo_type=AssignmentRepo)

## Aşağıdaki case’lerden en az birini yapınız:

### Autocomplete
- Search
- Complete
- Optional Request

İnput’a kelime yazdıkça compontent’e gönderilen kelimeler arasında arama yapması ve kelime yazılan alanın altında önermelerin çıkıyor olması gerekiyor.

Örneğin;

Şehir listesi gönderildiğinde İst yazıldığında İstanbul, Isparta önermelerinin listelenmesi gerekiyor. Önermelere tıklayınca ise kelimenin otomatik tamamlanması gerekiyor. Önerme listesi uygun formata göre farklı listeler ile çalışması lazım. Örneğin şehir listesi yerine film isimleri gönderdiğimizde yine aynı şekilde çalışıyor olması gerekiyor.

### Popup

- Video
- Image
- Title +Text
- Accept / Close

Popup component’i açıldığında hem video hem görsel gösterme seçeneği olması gerekiyor. Bazı kullanımlarda Başlık ve Video olabilir veya Sadece Başlık ve Metinden oluşabilir. Aynı zamanda popup üzerinde button seçeneğinin dinamik olması gerekiyor. Örneğin popup kapatılması için isteğe bağlı kapat veya onaylıyorum yazabilir. Bazı durumlarda ise Onayla ve Iptal şeklinde 2 seçenek ekleme imkanıda olması gerekiyor.

### Cookie

- Title
- Text
- Accept / Reject

Çerez componentinde içerik özelleştirilebilir olması dışında arayüzden Kabul et buttonuna bastığında component sayfa yenilendiğinde görüntülenmemesi gerekmekte. Aynı şekilde Reddet seçtiğinde ise her seferinde tekrar açılır olması gerekiyor. İsteğe bağlı sadece Kabul et buttonun görüntülenebilmesi seçeneği de olması gerekiyor.

### Notification

- New Notification Push
- Icon Change
- Color Change

Bildirim için sayfa üzerinde herhangi bir buttona basıldığında isteğe bağlı ekranın herhangi bir köşesinde bildirimin en üstte görüntülenmesi gerekiyor. Bildirimin pozisyonu dışında rengini ve iconunu da değiştirebilme imkanı olması gerekiyor mutlaka. Hiçbir şey yapılmadığında mesajın 10 saniye içinde kaybolması aynı anda 1’den fazla bildirim gönderildiğinde ise ekranda alt alt veya üst üste görüntülenmesi gerekiyor.

## Vue 3 + Vite

This template should help get you started developing with Vue 3 in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar)
