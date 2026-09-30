# Otonom Araçlar İçin Dur Tabelası Tespiti (YOLOv8)

Bu proje, otonom sistemlerde gerçek zamanlı nesne tespiti yapabilmek amacıyla YOLOv8 mimarisi kullanılarak geliştirilmiştir. Model, Roboflow üzerinden alınan bir 'Stop Sign' veri seti üzerinde eğitilmiş ve farklı koşullardaki test verileriyle doğrulanmıştır.

## Kullanılan Eğitim Parametreleri
* **Model:** YOLOv8n (Pre-trained)
* **Epoch:** 25
* **Batch Size:** 16
* **Image Size:** 640
* **Optimizer:** AdamW

## Nasıl Çalıştırılır?
1. `stop_sign_detection.ipynb` dosyasını Google Colab ortamında açın.
2. Gerekli kütüphaneleri kurmak için hücreye `!pip install ultralytics` yazıp çalıştırın.
3. Projedeki eğitilmiş en iyi model ağırlıklarını (`best.pt`) kullanarak test işlemi yapmak için aşağıdaki kodu kullanın:
```python
test_model.predict(source='/content/stop_sign_data_set/', conf=0.5, save=True)
