# Submission : Meningkatkan Klasifikasi Gambar dengan Model Neural Network pada Dataset Kategori Alam

Username dicoding: mzfuadi97

| | Deskripsi |
| ----------- | ----------- |
| Dataset | [Image Classification](https://www.kaggle.com/datasets/puneet6060/intel-image-classification) |
| Masalah | Dalam dataset ini, terdapat 25.000 gambar berukuran 150x150 yang didistribusikan dalam 6 kategori berbeda, yaitu 'buildings', 'forest', 'glacier', 'mountain', 'sea', dan 'street'. Data ini dibagi menjadi tiga bagian: data latihan (Train) yang berisi sekitar 14.000 gambar, data pengujian (Test) yang berisi sekitar 3.000 gambar, dan data prediksi (Prediction) yang berisi sekitar 7.000 gambar. |
| Solusi machine learning | Untuk meningkatkan akurasi klasifikasi gambar, terapkan preprocessing dengan normalisasi dan augmentasi data, gunakan arsitektur CNN yang kompleks, sertakan regularisasi seperti dropout dan batch normalization, aktifkan fungsi aktivasi ReLU, gunakan penjadwalan learning rate dengan optimizer Adam, evaluasi dengan akurasi dan matriks konfusi, pertimbangkan fine-tuning model transfer learning, terapkan early stopping, dan eksplorasi ensemble learning untuk kombinasi model yang lebih baik. |
| Metode pengolahan |data gambar diolah menggunakan augmentasi data seperti rotasi dan zoom dengan bantuan ImageDataGenerator, serta diubah ukurannya menjadi 128x128 piksel. |
| Arsitektur model |Arsitektur model yang digunakan dalam kode adalah Convolutional Neural Network (CNN) dengan banyak lapisan konvolusi dan pengurangan dimensi menggunakan MaxPooling. Setelah lapisan konvolusi, diterapkan lapisan dropout untuk menghindari overfitting. Model ini memiliki total 12 lapisan konvolusi dengan pertumbuhan kompleksitas dari lapisan ke lapisan. Setelah lapisan konvolusi, data diubah menjadi vektor dengan lapisan flatten, diikuti oleh dua lapisan dense. Lapisan akhir menggunakan fungsi aktivasi softmax untuk menghasilkan probabilitas kategori. |
| Metrik evaluasi | metrik evaluasinya adalah akurasi (accuracy), yang mengukur persentase jumlah prediksi yang benar dari total prediksi, serta categorical cross-entropy loss, yang mengukur kesesuaian prediksi model dengan label kategori yang sebenarnya. Model dikompilasi dengan optimizer Adam dan loss function 'categorical_crossentropy', dan selama pelatihan, kinerja model diukur dengan akurasi pada data pelatihan dan validasi. Pelatihan model berhenti jika akurasi di atas 80% pada kedua dataset, sesuai dengan callback yang telah diimplementasikan. |
| Performa model | Model mengalami peningkatan performa seiring berjalannya pelatihan dengan meningkatnya jumlah epoch. Terlihat bahwa loss semakin menurun dan akurasi semakin meningkat pada data pelatihan dan validasi. Pada epoch ke-6, akurasi pada data validasi mencapai 80.01%, sesuai dengan kondisi yang ditetapkan dalam callback, yang mengakibatkan penghentian pelatihan. Hasil ini mengindikasikan bahwa model dapat memahami pola-pola dalam data dan berhasil mengklasifikasikan gambar-gambar dengan akurasi yang sesuai dengan ambang batas yang ditargetkan. |
| Opsi deployment | Tahap ini melibatkan konversi model Keras yang sudah dilatih menjadi format TFLite, yang lebih cocok untuk perangkat seluler atau sumber daya terbatas. Konversi dilakukan menggunakan objek konverter TFLite, dan model yang dihasilkan disimpan dalam file 'RPS_model.tflite', yang dapat digunakan untuk inferensi di perangkat terbatas seperti ponsel. |

### Dataset

### Metric_Evaluation

### Validation-Vis
