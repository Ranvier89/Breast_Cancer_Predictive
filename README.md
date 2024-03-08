# ✨ Breast Cancer : Predictive Analysis ✨ <br>

Dataset ini hasil dari 213 observasi pasien dari registrasi kanker Rumah Sakit Pengajaran Universitas Calabar selama 24 bulan (Januari 2019–Agustus 2021). <br>
Tujuan klasifikasi ini adalah untuk memprediksi pasien terkena kanker payudara atau tidak. <br>
Link untuk dataset : https://www.kaggle.com/datasets/fatemehmehrparvar/breast-cancer-prediction <br>
Proyek ini adalah Tugas Akhir dari dibimbing.id , Bootcamp Data Science yang saya ikuti. <br>


## Tujuan <br>
Kanker payudara adalah kanker yang terbentuk di jaringan payudara. Kanker payudara terjadi ketika sel-sel pada jaringan di payudara tumbuh secara tidak terkendali dan mengambil alih jaringan payudara yang sehat dan sekitarnya. <br>
Pada 2022, terdapat sekitar 2,4 juta kasus baru kanker payudara, atau 11,6 persen dari total kasus kanker baru. <br>
Kendati demikian, kanker payudara merupakan jenis kanker yang paling banyak diidap oleh wanita. <br>
Kanker ini juga menyebabkan sekitar 670 ribu kematian, atau 6,9 persen dari total kasus kematian akibat kanker.<br>

Studi ini menghipotesiskan bahwa terdapat hubungan signifikan antara karakteristik diagnostik pasien, termasuk usia, status menopause, ukuran tumor, keberadaan nodus invasif, payudara yang terkena, status metastasis, kuartan payudara, riwayat kondisi payudara, dan hasil diagnosis kanker payudara mereka.<br>
Dalam pemeriksaan awal, data menunjukkan variasi hasil diagnosis pada berbagai fitur pasien. <br>
Tren yang mencolok adalah prevalensi lebih tinggi pada hasil ganas di antara pasien dengan ukuran tumor yang lebih besar dan keberadaan nodus invasif. Selain itu, wanita pasca menopause tampaknya memiliki tingkat diagnosis ganas yang lebih tinggi

### Tujuan Bisnis <br>
Berdasarkan pernyataan sebelumnya, kita akan melatih Machine Learning untuk menentukan kekuatan dan signifikansi hubungan antara karakteristik pasien dan diagnosis kanker payudara.<br>
Hal ini dapat berkontribusi pada pemodelan prediktif untuk deteksi dini dan diagnosis kanker payudara.<br>
Namun, interpretasi harus mempertimbangkan potensi keterbatasan, karena data ini mencerminkan pasien dari satu rumah sakit, sehingga bisa membatasi generalisabilitas temuan ini pada populasi yang lebih luas. <br>
Data ini dapat berharga bagi profesional kesehatan, peneliti, atau pembuat kebijakan yang tertarik memahami faktor diagnosis kanker payudara dan meningkatkan strategi perawatan kesehatan untuk kanker payudara. <br>
Hal ini juga dapat digunakan dalam pendidikan pasien tentang faktor risiko yang terkait dengan kanker payudara. <br>

## Library
Library seperti [pandas](https://pandas.pydata.org/), [numpy](https://numpy.org/), [matplotlib](https://matplotlib.org/), dan [seaborn](https://seaborn.pydata.org/) adalah yang sangat umum digunakan dalam analisis. <br>
Namun , saya juga menggunakan library [sklearn](https://scikit-learn.org/stable/) untuk membuat prediksi analisis dengan berbagai model klasifikasi <br>

```
import pandas as pd
import numpy as np

import matplotlib.pyplot as plt
import seaborn as sns
from plotly.subplots import make_subplots
import plotly.graph_objects as go
import plotly.express as px
import matplotlib.patches as  mpatches

from sklearn.preprocessing import OneHotEncoder
from sklearn.model_selection import train_test_split
from statsmodels.tools.tools import add_constant
from statsmodels.stats.outliers_influence import variance_inflation_factor as vif
from sklearn.neighbors import KNeighborsClassifier
from sklearn.ensemble import RandomForestClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.tree import DecisionTreeClassifier
```
<br>

## Hasil Training <br>
Karena yang kita prediksi adalah suatu penyakit. Dan yang kita hindari adalah pasien yang di prediksi sehat tapi aktualnya sakit Kanker __(False Negative)__, maka kita akan fokus menggunakan **Sensitivitas** atau **Recall**. <br>


![image](https://github.com/Ranvier89/Breast_Cancer_Predictive/assets/153417873/5b0a86ea-0c91-4223-9233-de0cb0b2d831)

Model yang terbaik berdasarkan Scoring : **Recall** adalah **KNN Model**.Dengan Recall sebesar 0.84! <br>

Setelah mendapatkan prediksi yang spesifik berdasarkan Scoring Recall. Besar harapan kita bisa mendeteksi sedini mungkin gejala Kanker di setiap pasien.<br>
Sehingga semua para penderita Kanker bisa mendapatkan penanganan yang lebih baik.

