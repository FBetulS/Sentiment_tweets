# Sentiment_tweets
# Sentiment140 Dataset with 1.6 Million Tweets

## 📖 Proje Açıklaması
Bu proje, Sentiment140 veri setini kullanarak duygu analizi gerçekleştirmeyi amaçlamaktadır. Veri seti, 1.6 milyon tweet içerir ve bu tweetler, iki duygu kategorisine (pozitif ve negatif) ayrılmıştır. Proje, metin işleme teknikleri ve LSTM (Uzun Kısa Süreli Bellek) modelini kullanarak bu tweetlerin duygu durumlarını sınıflandırmayı hedeflemektedir.

## 🔗 Veri Kümesi
Veri kümesi, [Sentiment140 dataset with 1.6 million tweets] adresinden alınmıştır. Bu veri seti, duygu analizi için yaygın olarak kullanılan önemli bir kaynaktır.

## 🛠️ Kullanılan Kütüphaneler
- `pandas`: Veri analizi ve manipülasyonu için.
- `numpy`: Sayısal işlemler için.
- `re`: Metin temizleme işlemleri için.
- `matplotlib` ve `seaborn`: Verilerin görselleştirilmesi için.
- `sklearn`: Model değerlendirme ve metrikler için.
- `tensorflow`: Derin öğrenme modelleri için.

## 📊 Veri Analizi ve Görselleştirme
### Veri Yükleme ve Ön İşleme
Veri, CSV dosyasından yüklenir ve gerekli sütunlar belirlenir:
```python
df = pd.read_csv("training.1600000.processed.noemoticon.csv", encoding='latin-1', header=None)
df.columns = ['target', 'ids', 'date', 'flag', 'user', 'text']
df['target'] = df['target'].replace({4: 1})
