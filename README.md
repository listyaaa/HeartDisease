Dataset yang digunakan adalah dataset Heart. Dataset ini terdiri dari 919 data dan 12 kolom. Dataset ini berisi informasi tentang ciri fisik seseorang untuk tujuan diagnosis penyakit jantung.
Dataset ini saya pilih karena saya pernah mencoba melakukan model prodeksi regresi logistik.

Proses Pembuatan dan Evaluasi Model Decision Tree:
Model Decision Tree dibuat dengan menggunakan library Scikit-learn. Proses pembuatan model ini meliputi:
1. Import data
2. Preprosesing data: Import library, memisahkan fitur dan target, membagi data menjadi data pelatihan dan data test.
3. Mencari parameter yang terbaik
5. Melatih model dan membuat pohon keputusan
6. Evaluasi Model

Hasil yang di dapatkan:
Classification Report:
               precision    recall  f1-score   support

           0       0.84      0.86      0.85        77
           1       0.90      0.88      0.89       107

    accuracy                           0.87       184
   macro avg       0.87      0.87      0.87       184
weighted avg       0.87      0.87      0.87       184

![image](https://github.com/user-attachments/assets/45bb26d3-0f96-4f0c-8a9a-503c4495563c)

Pohon Keputusan:
![image](https://github.com/user-attachments/assets/b8c4a0b1-1681-4373-baad-64179fe33253)

Kesimpulan:
Model Decision Tree tanpa scaling memiliki performa yang cukup baik dengan akurasi 86,96%, presisi 89,52%, dan recall 87,85%.
Dari diagram confusion matrix terlihat bahwa model lebih baik dalam memprediksi kelas "Disease" dibandingkan kelas "No Disease". 
Hal ini ditunjukkan oleh nilai recall yang lebih tinggi pada kelas "Disease". Namun, nilai recall pada kelas "No Disease" juga cukup baik (86%), sehingga model dapat dikatakan seimbang dalam memprediksi kedua kelas. Secara keseluruhan, model Decision Tree tanpa scaling dapat dikatakan memiliki performa yang cukup baik.

Rekomendasi berdasarkan confusion matrix:
Dari confusion matrix yang diberikan, terlihat bahwa model Decision Tree tanpa scaling memiliki performa yang baik dengan akurasi yang tinggi. Model ini mampu mengklasifikasikan dengan baik kasus penyakit dan non-penyakit.
Namun, terdapat beberapa hal yang perlu diperhatikan:
- False Positives: Terdapat 11 kasus yang diklasifikasikan sebagai penyakit (disease) padahal sebenarnya bukan. Hal ini berarti model memiliki kecenderungan untuk "overpredict" penyakit.
- False Negatives: Terdapat 13 kasus yang diklasifikasikan sebagai non-penyakit (no disease) padahal sebenarnya penyakit. Hal ini menunjukkan bahwa model mungkin kehilangan beberapa kasus penyakit yang penting untuk dideteksi.
