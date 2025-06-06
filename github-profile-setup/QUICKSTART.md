# ⚡ Hızlı Başlangıç Kılavuzu

## 🎯 5 Dakikada GitHub Profil Kurulumu

### Adım 1: Repository Oluştur
```bash
# GitHub'da yeni repository oluştur
Repository name: ArslanKG  # (kendi kullanıcı adınız)
Description: GitHub Profile
Public: ✅
Add README: ✅
```

### Adım 2: Token Oluştur
1. GitHub → Settings → Developer settings → Personal access tokens
2. Generate new token (classic)
3. İzinleri seç:
   - ✅ `public_repo`
   - ✅ `read:user`
   - ✅ `read:org`
4. Token'ı kopyala

### Adım 3: Secret Ekle
1. Repository → Settings → Secrets and variables → Actions
2. New repository secret
3. Name: `METRICS_TOKEN`
4. Value: Token'ı yapıştır

### Adım 4: Dosyaları Yükle
```bash
git clone https://github.com/ArslanKG/ArslanKG.git
cd ArslanKG

# .github/workflows klasörü oluştur
mkdir -p .github/workflows

# Ana workflow dosyasını kopyala
cp metrics-main.yml .github/workflows/

# Snake animasyonu için (opsiyonel)
cp snake-animation.yml .github/workflows/

# README.md dosyasını güncelle
cp profile-README-example.md README.md

# Değişiklikleri commit et
git add .
git commit -m "Add GitHub metrics setup"
git push
```

### Adım 5: Actions'ı Çalıştır
1. Repository → Actions sekmesi
2. "GitHub Profile Metrics" workflow'u seç
3. "Run workflow" butonuna tıkla
4. 2-3 dakika bekle

### ✅ Tamamlandı!
Profiliniz şimdi şu adreste görünecek: `https://github.com/ArslanKG`

---

## 🎨 Özelleştirme

### Kullanıcı Adını Değiştir
`metrics-main.yml` dosyasında:
```yaml
user: ArslanKG  # Buraya kendi kullanıcı adınızı yazın
```

### Tema Değiştir
```yaml
config_theme: dark     # Koyu tema
config_theme: light    # Açık tema
```

### Dil Filtreleme
```yaml
plugin_languages_ignored: html, css, dockerfile
plugin_languages_limit: 6  # Gösterilecek dil sayısı
```

---

## 🔧 Sorun Giderme

### ❌ Actions çalışmıyor
- Token'ın doğru ayarlandığını kontrol edin
- Repository'nin public olduğunu kontrol edin

### ❌ Görseller görünmüyor
- Actions'ın başarıyla tamamlandığını kontrol edin
- Dosya isimlerinin README'de doğru yazdığını kontrol edin

### ❌ Permission hatası
- Token izinlerini kontrol edin
- Repository settings → Actions → General → Workflow permissions → Read and write permissions

---

## 🎁 Bonus İpuçları

### GitHub Stats Ekleme
```markdown
![Stats](https://github-readme-stats.vercel.app/api?username=ArslanKG&show_icons=true&theme=dark)
```

### Ziyaretçi Sayacı
```markdown
![Profile views](https://komarev.com/ghpvc/?username=ArslanKG)
```

### Typing Animation
```markdown
[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%2336BCF7&lines=Full+Stack+Developer;Technology+Enthusiast;Always+Learning)](https://git.io/typing-svg)
```

---

## 📱 Responsive README Şablonu

```markdown
<div align="center">
  
# 👋 Hi, I'm Arslan!

[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=F75C7E&width=435&lines=Full+Stack+Developer;React+%26+Node.js+Expert;Always+Learning+New+Things)](https://git.io/typing-svg)

</div>

![Metrics](https://github.com/ArslanKG/ArslanKG/blob/main/metrics.svg)

<details>
<summary>📊 More Stats</summary>

![Languages](https://github.com/ArslanKG/ArslanKG/blob/main/metrics-languages.svg)
![Calendar](https://github.com/ArslanKG/ArslanKG/blob/main/metrics-calendar.svg)

</details>
```

---

## 🌟 Pro İpuçları

1. **Düzenli Güncelleme:** Actions'ı günlük çalışacak şekilde ayarlayın
2. **Mobile Friendly:** README'nizde responsive tasarım kullanın
3. **SEO Optimizasyonu:** Açıklayıcı alt textler ekleyin
4. **Brand Consistency:** Tutarlı renkler ve fontlar kullanın
5. **Loading Optimization:** Görselleri optimize edin

**🚀 Başarılar! GitHub profiliniz artık profesyonel görünüyor!**