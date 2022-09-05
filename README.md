# Capstone-Project-3
# Travel Insurance
Created by: Pratiwi Astuti

Created By: Pratiwi Astuti

## Business Problem Understanding
**Context** <br>
Perusahaan travel menawarkan paket asuransi kepada customernya. Perusahaan ingin tahu customer mana yang dapat meng-claim asuransi sesuai dengan history yang ada pada database. <br>
Asuransi diberikan kepada customer yang memenuhi kriteria perusahaan berdasarkan data yang sudah ada. Dalam hal ini kita akan membuat model untuk memprediksi customer mana yang lolos claim asuransinya.

**Target** <br>
0 : Claim accepted <br>
1 : Claim declined

## Data Understanding
Dataset source: https://www.kaggle.com/datasets/mhdzahier/travel-insurance 
### Atribute Information
| Attribute | Data Type, Length | Description |
| --- | --- | --- |
| Agency | Text | Name of agency |
| Agency Type | Text | Type of travel insurance agencies |
| Distribution Channel | Text | Distribution channel of travel insurance agencies |
| Product Name | Text | Name of the travel insurance products |
| Gender | Text | Gender of insured |
| Duration | Long | Duration of travel |
| Destination | Text | Destination of travel |
| Net Sales | Float | Amount of sales of travel insurance policies |
| Commision (in value) | Float | Commission received for travel insurance agency |
| Age | Long | Age of insured |
| Claim | Float | Claim status (0 : `not approved` dan 1 : `approved`) |

## Exploratory Data Analysis
Pada tahap ini kita melakukan pengecekan untuk tiap kolom, seperti typo, data type, missing value, dan korelasi antar data. Setelah melakukan pengecekan kita melakukan tindakan atas data-data yang tidak sesuai, seperti drop kolom Gender yang memiliki banyak missing value, replace data yang tidak sesuai seperti pada kolom Net Sales dan Commision.<br>
Selanjutnya kita akan mendapatkan data yang sudah bersih dan kita akan lakukan analisa pada data ini.
### Data Analysis
Dari analisa data, ditemukan ada data yang outlier dan imbalanced.
![imbalanced](https://user-images.githubusercontent.com/107948562/188425588-a341a96a-b71e-4d9c-8238-0434a28ee37c.png)
![outlier](https://user-images.githubusercontent.com/107948562/188425622-64b783f3-d448-4482-a067-ed5bdd3bc5b1.png)
## Data Preparation and Feature Engineering
### Data Preparation
Menyiapkan data yang sudah bersih untuk dilakukan proses feature engineering.
### Feature Engineering
Pada proses ini, akan dilakukan proses sbb:
- Encoding: Merubah data kategorik menjadi numerik agar dapat dibaca oleh Machhine Learning.
- Scaling: Proses scaling ini dilakukan karena ditemukan data outlier pada type data numerik.
- Handle imbalance data: Pada proses ini menggunakan teknik SMOTE.
- Splitting: Membagi data menjadi data training dan testing

## Model Building and Evaluation
Pada proses ini, kita akan coba 5 model klasifikasi, yaitu:
- Logistic Regression
- Random Forest
- Decision Tree
- KNN
- XGBoost
Dalam tahap ini, kita akan mencari model terbaik yang dapat menghasilkan prediksi dengan tingkat keakuratannya tinggi dilihat dari recall.

## Conclusion and Recomendation
**Conclusion**
Model terbaik yaitu XGBoost dengan nilai sbb:
<img width="344" alt="best model" src="https://user-images.githubusercontent.com/107948562/188428937-69deae21-b84a-4af5-a242-8a57d38aea61.png">
Model ini sudah di melalui teknik oversampling dan hasil prediksi yang didapat cukup baik yaitu dengan tingkat keakuratan nilai hingga 90%.

**Recomendation**
Berikut hal yang dapat dilakukan untuk mengembangkan project dan modelnya:
- Perusahaan membuat kebijakan agar customer dapat mengisi data dengan benar dan sesuai.
- Menambahkan fitur atau kolom baru yang berkaitan agar menghindari imbalance data dan data lebih bervariasi.




