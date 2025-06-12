# 🧠 Soru-Cevap Chatbot Geliştirme (NLP + Sağlık)

Bu proje, **doğal dil işleme (NLP)** yöntemleri kullanarak **sağlık alanında** soru-cevap yeteneklerine sahip bir **chatbot** geliştirmeyi amaçlamaktadır. MedQuAD veri seti temel alınarak, **Flan-T5-small** ve **distilGPT-2** modelleri fine-tune edilmiştir. Sonuçlar hem istatistiksel metriklerle hem de örnek yanıtlarla değerlendirilmiştir.

---

## 📌 Proje Özellikleri

- 🔬 Sağlık verilerine dayalı soru-cevap üretimi
- 🤖 FLAN-T5 ve distilGPT-2 modelleriyle karşılaştırmalı modelleme
- ⚙️ Hugging Face Trainer API ile eğitim
- 📈 BLEU, ROUGE ve METEOR metrikleri ile değerlendirme
- 🖥️ Gradio ile etkileşimli chatbot arayüzü

---

## 📂 Kullanılan Teknolojiler

| Araç/Kütüphane         | Açıklama                                       |
|------------------------|------------------------------------------------|
| Python                 | Temel programlama dili                         |
| Hugging Face Transformers | Model eğitimi ve yükleme                      |
| Datasets               | MedQuAD veri seti işleme                       |
| Gradio                 | Web tabanlı chatbot arayüzü                    |
| Google Colab           | Eğitim ortamı (GPU destekli)                   |
| Evaluate               | Değerlendirme metrikleri (BLEU, ROUGE, METEOR)|

---

## 📊 Model Karşılaştırması

| Metrik     | T5 (Flan-T5-Small) | GPT-2 (distilgpt2) |
|------------|--------------------|---------------------|
| BLEU       | 0.0473             | **0.7935**          |
| ROUGE-1    | 0.2257             | **0.8661**          |
| ROUGE-2    | 0.0963             | **0.8645**          |
| ROUGE-L    | 0.1945             | **0.8662**          |
| METEOR     | -                  | **0.9112**          |

> distilGPT-2 modeli, daha yüksek puanlar ile daha doğal ve bağlama uygun yanıtlar üretebilmiştir.

---

## 🛠️ Kurulum

```bash
git clone https://github.com/kullaniciadi/soru-cevap-chatbot.git
cd soru-cevap-chatbot
pip install -r requirements.txt


🧪 Değerlendirme
Başarılı Örnek:
Soru: What causes Glaucoma?
distilGPT-2 Yanıtı: The most common cause of glaucoma is an inflammation of the glomeruli...

Başarısız Örnek:
Soru: What causes Diabetes?
T5 Yanıtı: Diabetes is a condition that affects the body's ability...

Açıklama: Cevap yapay ve tekrar eden cümlelerden oluşuyor, gerçek neden belirtilmiyor.

📉 Sınırlılıklar
Veri seti yalnızca İngilizce ve sınırlı örnek içeriyor

Cevaplar bazı durumlarda yüzeysel veya kısa kalabiliyor

Tıbbi doğruluk her zaman garanti edilemez

🔮 Gelecek Çalışmalar
🔁 Daha büyük modeller (Flan-T5-Base, GPT-J vb.)

🌍 Çok dilli destek (özellikle Türkçe)

✅ Gerçeklik kontrolü için bilgi tabanı entegrasyonu

🔀 Soru tipi sınıflandırması ve alt model yönlendirme
