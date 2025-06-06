# 🚀 GitHub Profil Metrics Kurulumu

Bu dosyalar, GitHub profilinizde profesyonel görselleştirmeler oluşturmak için [lowlighter/metrics](https://github.com/lowlighter/metrics) projesini kullanır.

## 📋 Kurulum Adımları

### 1. GitHub Token Oluşturma

1. GitHub'da **Settings** > **Developer settings** > **Personal access tokens** > **Tokens (classic)** bölümüne gidin
2. **Generate new token (classic)** butonuna tıklayın
3. Token için bir isim verin (örn: "Metrics Token")
4. Aşağıdaki izinleri seçin:
   - `public_repo` (public repository'ler için)
   - `read:user` (kullanıcı bilgileri için)
   - `read:org` (organizasyon bilgileri için - opsiyonel)
   - `read:packages` (paket bilgileri için - opsiyonel)
5. **Generate token** butonuna tıklayın
6. Token'ı kopyalayın (tekrar gösterilmeyecek!)

### 2. GitHub Repository Kurulumu

1. GitHub'da **username/username** adında bir repository oluşturun (örn: `ArslanKG/ArslanKG`)
2. Repository'yi public yapın
3. **Settings** > **Secrets and variables** > **Actions** bölümüne gidin
4. **New repository secret** butonuna tıklayın
5. **Name:** `METRICS_TOKEN`
6. **Secret:** Yukarıda oluşturduğunuz token'ı yapıştırın

### 3. GitHub Actions Workflow Ekleme

1. Repository'nizde `.github/workflows/` klasörünü oluşturun
2. `metrics-main.yml` dosyasını bu klasöre kopyalayın
3. Dosyayı commit ve push edin

### 4. Profil README'sini Güncelleme

Repository'nizin ana dizininde `README.md` dosyasını oluşturun veya güncelleyin:

```markdown
# Merhaba 👋, Ben Arslan!

## 📊 GitHub İstatistiklerim

<!-- Ana metrics -->
![Metrics](https://github.com/ArslanKG/ArslanKG/blob/main/metrics.svg)

<!-- Programlama dilleri -->
![Languages](https://github.com/ArslanKG/ArslanKG/blob/main/metrics-languages.svg)

<!-- Commit takvimi -->
![Calendar](https://github.com/ArslanKG/ArslanKG/blob/main/metrics-calendar.svg)

<!-- Kodlama alışkanlıkları -->
![Habits](https://github.com/ArslanKG/ArslanKG/blob/main/metrics-habits.svg)

<!-- GitHub başarıları -->
![Achievements](https://github.com/ArslanKG/ArslanKG/blob/main/metrics-achievements.svg)

<!-- Son aktiviteler -->
![Activity](https://github.com/ArslanKG/ArslanKG/blob/main/metrics-activity.svg)

<!-- Öne çıkan projeler -->
![Repositories](https://github.com/ArslanKG/ArslanKG/blob/main/metrics-repositories.svg)

<!-- İlgi alanları -->
![Topics](https://github.com/ArslanKG/ArslanKG/blob/main/metrics-topics.svg)

<!-- Topluluk -->
![People](https://github.com/ArslanKG/ArslanKG/blob/main/metrics-people.svg)
```

## 🎨 Özelleştirme Seçenekleri

### Tema Değişiklikleri

```yaml
# Koyu tema için
config_theme: dark

# Aydınlık tema için
config_theme: light

# Özel renkler için
config_theme: "@import url('https://themes.lecoq.io/github-dark.css')"
```

### Animasyonlar

```yaml
# Animasyonları aktif etmek için
config_animations: yes

# Animasyonları kapatmak için
config_animations: no
```

### Dil Filtrelemeleri

```yaml
# Belirli dilleri gizlemek için
plugin_languages_ignored: html, css, dockerfile

# Sadece belirli kategorileri göstermek için
plugin_languages_categories: programming
```

## 📱 Responsive Tasarım

Metrikler otomatik olarak farklı ekran boyutlarına uyum sağlar. Ayrıca gece modu ve aydınlık mod desteği vardır.

## 🔄 Güncelleme Sıklığı

- **Otomatik:** Her gün saat 00:00'da (UTC+3)
- **Manuel:** Repository'de herhangi bir değişiklik yaptığınızda
- **İsteğe bağlı:** Actions sekmesinden manuel olarak çalıştırabilirsiniz

## 🛠️ Sorun Giderme

### Metrikler görünmüyor
1. GitHub Actions'ın çalıştığını kontrol edin
2. METRICS_TOKEN'ın doğru ayarlandığını kontrol edin
3. Token'ın gerekli izinlere sahip olduğunu kontrol edin

### Token süresi doldu
1. Yeni bir token oluşturun
2. Repository secrets'ı güncelleyin

### Özel repository'ler görünmüyor
- Token'a `repo` iznini ekleyin (güvenlik riski!)

## 📚 Ek Kaynaklar

- [Metrics Dokümantasyonu](https://github.com/lowlighter/metrics#readme)
- [Tüm Plugin'ler](https://github.com/lowlighter/metrics#-plugins)
- [Örnekler Galerisi](https://github.com/lowlighter/metrics/tree/examples)

## ⚡ Hızlı Başlangıç

1. Bu repository'yi fork edin
2. Repository ismini `username/username` olarak değiştirin
3. METRICS_TOKEN secret'ını ekleyin
4. Actions'ın çalışmasını bekleyin
5. Profil README'nizde görüntülerin linklerini güncelleyin

---

🔧 **Özelleştirme:** Bu yapılandırma dosyaları tamamen özelleştirilebilir. İhtiyaçlarınıza göre plugin'leri ekleyip çıkarabilirsiniz.