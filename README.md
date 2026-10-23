# 🍽️ Bugün Yemekte Ne Var?

Yemekhanenin günlük menüsünü gösteren küçük bir site. Git & GitHub atölyesinde
**Arya** ve **Berk**'in birlikte geliştirdiği örnek proje.

🌐 **Canlı site:** https://ekinyuksel12.github.io/yemekhane/

Her `main` push'unda GitHub Actions siteyi otomatik olarak GitHub Pages'e yükler
([Actions sekmesi](https://github.com/ekinyuksel12/yemekhane/actions)).

---

## 📋 Komut özeti (kopya kâğıdı)

### Bir kere yapılır
| Komut | Ne işe yarar? |
|---|---|
| `git config --global user.name "Adın"` | Commit'lere atılacak isim |
| `git config --global user.email "e-posta@ornek.com"` | Commit'lere atılacak e-posta |
| `git config --global init.defaultBranch main` | Yeni projelerde ana dalın adı `main` olsun |
| `git config --global pull.rebase false` | `git pull` gerekirse birleştirsin (merge) |

### Tek başına çalışırken
| Komut | Ne işe yarar? |
|---|---|
| `git init` | Bu klasörü bir git deposuna çevir |
| `git status` | Şu an durum ne? (en çok kullanacağın komut) |
| `git add dosya` / `git add .` | Değişikliği bir sonraki commit'e ekle |
| `git commit -m "mesaj"` | Kayıt noktası (commit) oluştur |
| `git commit -am "mesaj"` | Değişen dosyaları ekle + commit'le |
| `git diff` | Neyi değiştirdim? |
| `git log --oneline` | Geçmişi kısa listele |
| `git restore dosya` | Kaydedilmemiş değişikliği geri al |
| `git checkout <hash>` | Geçmişteki bir commit'e bak (zaman yolculuğu) |
| `git switch main` | Ana dala geri dön |

### GitHub ile
| Komut | Ne işe yarar? |
|---|---|
| `git remote add origin <adres>` | Projeye GitHub adresini tanıt |
| `git push -u origin main` | İlk kez gönder (sonrasında sadece `git push`) |
| `git clone <adres>` | Projeyi bütün geçmişiyle indir |
| `git pull` | GitHub'daki yenilikleri al ve birleştir |
| `git push` | Commit'lerini GitHub'a gönder |

### Takım çalışması
| Komut | Ne işe yarar? |
|---|---|
| `git switch -c dal-adi` | Yeni bir dal (branch) aç ve ona geç |
| `git push -u origin dal-adi` | Dalı GitHub'a gönder → Pull Request aç |
| `git revert <hash>` | Hatalı commit'i, tersini yapan yeni bir commit'le geri al |
| `git log --oneline --graph` | Dalları ve birleşmeleri ağaç olarak gör |

---

## 🚀 Kendi projeni GitHub'a koymak için

1. [github.com/new](https://github.com/new) adresinden boş bir repo oluştur.
2. Projenin klasöründe:
   ```bash
   git init
   git add .
   git commit -m "İlk commit"
   git remote add origin https://github.com/KULLANICI-ADIN/PROJE-ADIN.git
   git push -u origin main
   ```
3. Bu kadar! Sayfayı yenile, kodun GitHub'da. 🎉

## 🔀 Çakışma (conflict) olursa

Git dosyaya şu işaretleri koyar:

```
<<<<<<< HEAD
senin halin
=======
gelen hali
>>>>>>> ...
```

Doğru hali bırak, işaretleri sil, sonra `git add dosya` ve `git commit`.
