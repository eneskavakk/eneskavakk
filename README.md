<div align="center">

<img src="./assets/ot-hero.svg" width="100%" alt="Enes Kavak — Siber güvenlik ve OT güvenliği" />

<br>

<a href="https://www.eneskavak.com.tr"><img src="https://img.shields.io/badge/WEB-F25154?style=for-the-badge&logo=safari&logoColor=white" alt="Website" /></a>
<a href="https://www.linkedin.com/in/eneskavakk/"><img src="https://img.shields.io/badge/LINKEDIN-08090B?style=for-the-badge&logo=linkedin&logoColor=8B5CF6" alt="LinkedIn" /></a>
<a href="https://www.kaggle.com/eneskavakk"><img src="https://img.shields.io/badge/KAGGLE-08090B?style=for-the-badge&logo=kaggle&logoColor=62D5FF" alt="Kaggle" /></a>

<br><br>

![Cyber Security](https://img.shields.io/badge/CYBER_SECURITY-15161A?style=flat-square&logoColor=white)
![OT Security](https://img.shields.io/badge/OT_%2F_ICS_SECURITY-15161A?style=flat-square&logoColor=white)
![IEC 62443](https://img.shields.io/badge/IEC_62443-15161A?style=flat-square&logoColor=white)
![Network Defense](https://img.shields.io/badge/NETWORK_DEFENSE-15161A?style=flat-square&logoColor=white)
![Secure Coding](https://img.shields.io/badge/SECURE_CODING-15161A?style=flat-square&logoColor=white)

</div>

## FOCUS

Endüstriyel ortamları, yani fabrika ağlarını, PLC/CNC gibi sahadaki cihazları ve bunların IT ile kesiştiği noktaları **savunma** gözüyle inceliyorum. İlgi alanım siber güvenliğin geneli; en çok zaman verdiğim alan **OT güvenliği**.

| Alan | Neye bakıyorum |
| --- | --- |
| **OT / ICS güvenliği** | Envanter olmadan güvenlik olmaz: hangi cihaz, hangi portta, kim değiştirdi, hangi güvenlik bölgesinde |
| **IEC 62443** | SUC, **zone / conduit** modeli, **SL-T** (hedef) ve **SL-A** (mevcut) seviyelerinin ayrı kaydı, FR1–FR7 boşluk analizi |
| **Ağ savunması** | PCAP analizi, transport katmanı saldırıları (SYN/UDP flood), kural tabanlı ve ML destekli tespitin karşılaştırması |
| **Güvenli kodlama** | scrypt, oturum özeti saklama, CSRF, CSP, backend yetki kontrolü, optimistic locking, denetim izi |
| **Kriptografi ve parola güvenliği** | RSA'yı sıfırdan uygulama, k-anonymity ile sızıntı kontrolü, entropi analizi |

## SELECTED LABS · SECURITY

<a href="https://github.com/eneskavakk/portAtlas">
  <img src="./assets/project-portatlas.svg" width="100%" alt="PortAtlas: OT güvenliği ve bağlantı kaydı" />
</a>

**PortAtlas**, fabrika ağındaki cihaz–kablo–switch portu bağlantılarını gerekçeli ve geçmişli biçimde tutan, bunun üzerine OT güvenlik katmanı kuran bir web uygulamasıdır. IEC 62443 kavramlarını (zone, conduit, SL-A/SL-T) kayıt ve iş akışına çevirir:

- SL-A ve SL-T **ayrı revizyonlu kayıtlardır**; seviye otomatik atanmaz, tek bir "genel SL" veya uyum yüzdesi üretilmez, `null` ile `0` farklıdır.
- Zone üyeliği veya bağlantı değişince ilgili profil ve kontrol maddeleri **"gözden geçirme gerekli"** olur; eski kayıt silinmez.
- Bulgu akışında **görev ayrılığı**: yüksek öncelikte bulguyu uygulayan kişi doğrulayamaz; kanıt referansı zorunludur.
- Uygulamanın kendisi de sertleştirilmiştir: scrypt, `HttpOnly` + `SameSite=Strict` oturum, CSRF, sıkı CSP, CDN bağımlılığı yok.

`Python` `FastAPI` `SQLite` `vanilla JS` · 45 otomatik test · repo şu an özel (private)

<br>

<a href="https://github.com/eneskavakk/layer4-detector">
  <img src="./assets/project-layer4.svg" width="100%" alt="Layer 4 Defense Lab" />
</a>

<p align="center">
  <a href="https://github.com/eneskavakk/cybershield"><img src="./assets/project-cybershield.svg" width="49%" alt="CyberShield" /></a>
  <a href="https://github.com/eneskavakk/rsa-dashboard"><img src="./assets/project-rsa.svg" width="49%" alt="RSA Lab" /></a>
</p>

## HOW I THINK ABOUT OT SECURITY

```text
  Envanter  ──►  Segmentasyon  ──►  Hedef (SL-T)  ──►  Mevcut (SL-A)  ──►  Boşluk  ──►  Aksiyon  ──►  Doğrulama
  "ne var?"      zone / conduit      risk kararı         kanıtlı durum       FR bazında     sahipli,        farklı kişi,
                                                                             max(0, T−A)    tarihli         kanıtla
```

- Standardın kendisini değil **kararın izlenebilirliğini** modellemek: kim, neye dayanarak, ne zaman.
- Bilinmeyeni güvenli saymamak. "Belirlenmedi", "bilinmiyor" ve "uygulanamaz" ayrı durumlardır.
- Pasif ve kayıt odaklı başlamak: canlı ağ taramasından önce **doğru envanter**.
- Güvenlik aracı da saldırı yüzeyidir; araçların kendisi sertleştirilmeli.

## TOOLKIT

<div align="center">

![Python](https://img.shields.io/badge/PYTHON-08090B?style=for-the-badge&logo=python&logoColor=F25154)
![FastAPI](https://img.shields.io/badge/FASTAPI-08090B?style=for-the-badge&logo=fastapi&logoColor=62D5FF)
![SQLite](https://img.shields.io/badge/SQLITE-08090B?style=for-the-badge&logo=sqlite&logoColor=8B5CF6)
![Git](https://img.shields.io/badge/GIT-08090B?style=for-the-badge&logo=git&logoColor=8B5CF6)
![JavaScript](https://img.shields.io/badge/JAVASCRIPT-08090B?style=for-the-badge&logo=javascript&logoColor=F25154)
![Streamlit](https://img.shields.io/badge/STREAMLIT-08090B?style=for-the-badge&logo=streamlit&logoColor=62D5FF)

</div>

## ALSO

Güvenlik dışında makine öğrenmesi çalışmaları da yapıyorum; saldırı tespiti tarafında XGBoost ile kesiştiği yerler en çok ilgimi çeken kısım.
[AIHR](https://github.com/eneskavakk/AIHR) · [Heart-Attack-Prob](https://github.com/eneskavakk/Heart-Attack-Prob) · [diabetes-prediction-model-comparison](https://github.com/eneskavakk/diabetes-prediction-model-comparison) · [tüm projeler](https://www.eneskavak.com.tr/projeler)

---

<div align="center">

**KNOW YOUR ASSETS. SEGMENT YOUR NETWORK. VERIFY EVERYTHING.**

<a href="https://www.linkedin.com/in/eneskavakk/">LET'S CONNECT ↗</a>

</div>
