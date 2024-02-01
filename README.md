# AlphaGroup_JC_DS_OL_11_FinalProject
This project was carried out by Alpha's Team:
1. Akmal Azaki
2. Ahmad Baihaqi
3. Athian Istafa Yahya


![datset](https://github.com/PurwadhikaDev/AlphaGroup_JC_DS_OL_11_FinalProject/blob/main/img/hubungan%20tiap%20dataset%20olist.png)
## **Business Problem Understanding**
#### **Context**
Olist merupakan salah satu perusahaan marketplace terbesar terletak di Brazil yang bergerak di segmen e-Commerce. Olist menghubungkan penjual e-commerce dengan customers secara mudah menggunakan single contract. Dengan demikian, para penjual dapat menjual produk mereka dan mengirimkan produk tersebut kepada customer melalui Olist logistics partners.
Setelah customer membeli produk melalui Olist store, para penjual mendapatkan notifikasi untuk memenuhi pesanan tersebut. Setelah customer menerima produk atau estimasi pengiriman sudah tersedia, customer mendapatkan survey kepuasan dimana para customers dapat memberikan review baik secara tulisan dan juga rating.
Sebagai data scientist, dataset yang tersedia pada Olist dapat dianalisa untuk mengetahui permasalahan yang sedang dihadapi Olist. Menurut ([Statista, 2023](https://www.statista.com/topics/4697/e-commerce-in-brazil/#topicOverview)), segmen e-commerce menghasilkan national total revenue sebesar 170 billion Brazilian reals di tahun 2022, meningkat 2 kali lipat dibandingkan 2019 dan naik sebesar 12% dari tahun 2021. Olist dapat memanfaatkan dataset yang dimiliki. Sehingga, analisis data tersebut menghasilkan kesimpulan dan rekomendasi yang terukur. Hal ini menjadi penting untuk dilakukan bagi Olist untuk mengambil kesempatan pada market yang berkembang pesat dan dapat memiliki competitive advantage diantara kompetitornya dengan cara meningkatkan performansi Olist.

#### **Problem Statement**
Berdasarkan Cohort analysis yang kita lakukan, terdapat suatu permasalahan dimana mayoritas setiap customer hanya melakukan frekuensi pembelian satu kali. Maka dari itu dibutuhkan solusi untuk meningkatkan frekuensi pembelian dalam E-commerce ini. Salah satu strategi yang dapat dilakukan yaitu melakukan Strategi pemasaran.
Aktivitas pemasaran dapat memakan waktu dan sumber daya yang berlebihan jika perusahaan tidak melakukan segmentasi pelanggan terlebih dahulu. Perusahaan ingin meningkatkan efektivitas dan efisiensi pemasaran dengan mengetahui pengelompokan dari setiap pelanggan sehingga perusahaan dapat memberikan metode pemasaran yang tepat untuk setiap pelanggannya.
Dan jika pemarasan yang diberikan tidak sesuai ataupun kurang optimal dengan jenis pelanggan, maka perusahaan beresiko kehilangan beberapa pelanggan, bahkan tidak dapat mengoptimalkan pelanggan potensial menjadi pelanggan tetap, dan tidak dapat mempertahankan pelanggan tetap.
Pada data e-commerce Olist, angka rata - rata cohort analisis dari customer Olist hanyalah sebesar 0.046%. Sehingga, Olist memiliki customer yang memiliki sifat engagement rendah terhadap pembelian pada Olist atau repeat order dari customer dapat dikatakan masih sangat rendah. Oleh karena itu, perlu dilakukan strategi marketing agar customer melakukan pembelian ulang pada Olist.
Namun, strategi marketing secara general untuk seluruh customer tidak akan efektif. Strategi marketing yang hendak dilakukan haruslah spesifik berdasarkan kebutuhan dan juga behaviour dari tiap customer Olist. Menurut [Temnjanovski dan Arsova, 2019](https://eprints.ugd.edu.mk/21568/), menyusun sebuah marketing strategi untuk segmentasi customer yang tepat penting untuk menghemat resources dan waktu. Oleh karena itu, terhadap data Olist, akan dilakukan segmentasi customer agar strategi marketing yang dilakukan sesuai dengan kebutuhkan tiap customer segment dari Olist.

#### **Goals**
Maka, berdasarkan probelm statement diatas. Goals dari project ini adalah sebagai berikut:
- Mengatahui customer behaviour seberapa sering customer melakukan pembelian di Olist melalui cohort analysis
- Melakukan cluster modelling untuk memprediksi segmentasi customer
- Memahami kebutuhan setiap customer segment dengan cara melakukan Exploratory Data Analysis terhadap hasil segmentasi
- Menentukan strategi marketing yang tepat untuk setiap segmentasi customer

#### **Analytic Approach**
Dalam project ini, kami menggunakan RFM Analysis dan K-Means Clustering dalam menentukan segmentasi pelanggan. RFM analysis membagi kebiasaaan pelanggan berdasarkan :
1. Recency: jumlah hari terakhir pelanggan melakukan transaksi
2. Frequency: frekuensi pembelian pelanggan
3. Monetary: nominal transaksi pelanggan

Untuk penentuan jumlah cluster menggunakan algoritma K-Means, kami menggunakan:
1. Silhouette Score: Silhouette Score mengukur seberapa baik setiap titik data ditempatkan dalam klasternya sendiri dibandingkan dengan klaster sekitarnya. Score ini berkisar antara -1 hingga 1, dan nilai yang lebih tinggi menunjukkan bahwa titik data tersebut ditempatkan dengan baik dalam klasternya dan berjauhan dari klaster lainnya. Jika Silhouette Score mendekati 1, itu menunjukkan bahwa klasternya sesuai.
Jika mendekati -1, itu menunjukkan bahwa titik data mungkin lebih baik ditempatkan dalam klaster lain. Nilai mendekati 0 menunjukkan tumpang tindih antar klaster.
2. Elbow Method berfokus pada varian intra-klaster sebagai fungsi dari jumlah klaster. Fungsi objektif yang diukur adalah jumlah kuadrat jarak antara setiap titik data dengan pusat klasternya. Jumlah klaster optimal dipilih di titik "siku" (elbow) di grafik, di mana penurunan varian mulai melambat.
3. Domain Knowledge untuk penyesuaian dan tujuan bisnis.

## **RFM Result**
![RFM](https://github.com/PurwadhikaDev/AlphaGroup_JC_DS_OL_11_FinalProject/blob/main/img/RFM%20Result.png)

**Customer Segmentation menggunakan RFM dibagi berdasarkan** :

1. **VVIP - Can't Loose Them** : 
Pelanggan yang sebelumnya sering melakukan pembelian secara terus menerus dan mengeluarkan sejumlah besar uang, namun belakangan ini mereka sudah lama tidak melakukan pembelian. Penting untuk meraih kembali minat dari kelompok pelanggan ini di perusahaan. Grup ini mencerminkan sebagian pelanggan yang seiring waktu kehilangan minat terhadap perusahaan. Oleh karena itu, perusahaan perlu melakukan upaya untuk mendapatkan kembali perhatian dari kelompok pelanggan ini.
2. **Loyal Customers** : 
Melakukan pembelian dalam waktu dekat, terus menerus, dan mengeluarkan banyak uang, Mereka adalah top custemer yang mendukung perusahaan. Hubungan baik antar Olist dan kelompok customer ini perlu dijaga agar tetap terjalin dengan baik.
3. **Need Attention** : 
Melakukan pembelian dengan frekuensi kecil, namun masih memiliki potensi untuk menjadi loyal customers, menghabiskan uang dengan nominal tidak terlalu besar. Kelompok ini membutuhkan tindakan agar mereka dapat merasakan bahwa perusahaan (Olist) dapat menawarkan kondisi terbaik dan memenuhi kebutuhan mereka.
4. **Hibernating - Almost Lost** : 
Customer yang memiliki nilai rfm terkecil, dan berpotensi menjadi customer yang churn.

## **Clustering with K-Means Result**
![K-Means](https://github.com/PurwadhikaDev/AlphaGroup_JC_DS_OL_11_FinalProject/blob/main/img/K-Means%20Result.png)
- Cluster 0: pelanggan yang membeli produk dengan harga mahal, berat, dan besar. Pelanggan golongan ini juga membayar dengan jumlah angsuran paling tinggi yaitu 5-6 kali, namun tingkat frekuensi pembeliannya rendah yaitu hanya sekitar 1 kali. kami menyebut kelompok ini sebagai Big Spenders.
- Cluster 1: pelanggan yang membeli produk murah, ringan, dan kecil. Pelanggan golongan ini juga membayar dengan jumlah angsuran pembayaran yang sedang yaitu 2-3 kali, serta memiliki tingkat frekuensi pembelian yang rendah yaitu hanya sekitar 1 kali. Namun pelanggan tipe ini memiliki jumlah yang sangat besar sehingga kami menyebutnya sebagai Need Attention.
- Cluster 2:  Pelanggan yang membeli produk dengan harga sedang, dimensi produk juga sedang. Pelanggan tipe ini melakukan pembayaran tanpa cicilan namun menggunakan beberapa metode pembayaran dan pelanggan tipe ini juga memiliki frekuensi pembelian yang tinggi yaitu sekitar 7-8 kali, sehingga kami menyebutnya sebagai Loyal Customers.
- Cluster 3: mirip seperti cluster 1, pelanggan tipe ini juga membeli produk murah, ringan, dan kecil serta membayar dengan jumlah angsuran yang sedang yaitu 2-3 kali. Bedanya kelompok ini memiliki tingkat frekuensi pembelian rata-rata 2 kali sehingga berpotensi menjadi loyal customers sehingga kami menyebut kelompok ini sebagai Potential Loyalist.
  
## **Conclusion**
Berdasarkan problem statement yang kami sampaikan diawal, permasalahan utama yang dihadapi oleh perusahaan adalah 99% pelanggan tidak melakukan pembelian ulang setelah melakukan transaksi pertamanya di e-commerce olist dimana angka tersebut kami dapat dari cohort analysis. Untuk mengetahui lebih lanjut dan memecahkan permasalah tersebut, kami melakukan segmentasi pelanggan dengan menggunakan RFM Analysis dan melakukan modelling dengan menggunakan K-Means Clustering. Adapun hasil yang kami temukan adalah sebagai berikut:

#### RFM Analysis

RFM Analysis yang kami buat telah menghasilkan segmentasi yang cukup beragam dimana terdiri dari 4 cluster. Namun, meskipun interpretasi setiap kluster sudah cukup memuaskan, penentuan setiap segmennya terlalu subjektif karena tidak didasarkan pada hasil algoritma, melainkan ditentukan berdasarkan pengetahuan domain. Oleh karena itu, kami tidak dapat memvalidasi hasil segmentasi tersebut. Alasan utama kenapa kami tetap menggunakan RFM Analysis adalah sebagai perbandingan dari segmentasi yang kami buat dengan menggunakan algoritma K-Means.

#### K-Means Clustering

Customer segmentation yang kami buat dengan menggunakan metode algoritma K-Means terlihat lebih baik dan mudah diinterpretasikan. Berdasarkan hasil segmentasi tersebut, ada 4 cluster yang terbentuk dengan nilai silhoutte score mencapai 0,70. Pemilihan model ini dilakukan karena pembagian klusternya telah memberikan hasil yang diinginkan, dimana karakteristik setiap clusternya tampak berbeda cukup signifikan. Dengan adanya cluster ini, kami dapat menentukan target segmen yang diutamakan untuk mengatasi permasalahan yang dihadapi oleh perusahaan.

Dari hasil segmentasi tersebut, pelanggan dengan cluster 1 atau kami menyebutnya kelompok Need Attention adalah kelompok yang paling mendominasi, yaitu sekitar 86,85% dari seluruh pelanggan yang ada. Artinya kelompok ini memiliki potensi yang sangat besar jika perusahaan berhasil menarik minat mereka untuk kembali melakukan pembelian ulang di e-commerce olist. Menurut artikel dari [www.moengage.com](https://www.moengage.com/blog/how-to-drive-repeat-purchases-ecommerce-customers/) mendatangkan pelanggan baru sepuluh kali lebih mahal dibanding mempertahankan pelanggan yang ada. Adapun beberapa hal yang menyebabkan pelanggan tidak melakukan pembelian ulang menurut riset yang kami lakukan diantaranya adalah pertama karena pelanggan merasa kecewa, baik itu karena durasi pengiriman yang lama, kualitas produk yang tidak sesuai dengan harga, dan juga pelayanan yang buruk. Menurut artikel [getrepeat.io](https://blog.getrepeat.io/increase-repeat-purchase-rate/) sebagian besar pelanggan Amerika percaya bahwa tiga hari adalah waktu tunggu yang dapat diterima untuk pesanan online. Dari hasil EDA yang kami lakukan, sebesar 48,2% pelanggan akan memberikan bintang 1 jika pesanan mereka tiba lebih lama dari estimasi pengiriman. Selain itu, rata-rata estimasi pengiriman di e-commerce olist jika transaksi terjadi dalam negara bagian adalah 14 hari dan rata-rata estimasi pengiriman jika antar negara bagian adalah 23 hari. Dari hasil EDA juga menunjukkan bahwa sebesar 6,5% pengiriman lebih lama dari estimasi pengiriman. Selain hal-hal tersebut diatas, menurut [startuptalky.com](https://startuptalky.com/understanding-repeat-purchases-online/#:~:text=Some%20major%20factors%20that%20influence%20the%20frequent%20buying,security%2C%20time%2C%20after-sale%20service%2C%20return%2C%20and%20discounted%20products.) pemasaran 4P (produk, harga, tempat, dan promosi) tidak cukup untuk mempertahankan pelanggan di pasar digital, perusahaan juga perlu memastikan kualitas pelayanan yang diberikan. 

## **Recommendation**
**Rekomendasi Terkait Peningkatan Kualitas layanan:**
Berdasarkan conclusion diatas, kami merekomendasikan agar perusahaan melakukan perbaikan terkait permasalahan diatas seperti:
1. Peningkatan Jasa Pengiriman dan Penambahan Mitra Pengiriman Berkualitas:
- Evaluasi dan tingkatkan kualitas layanan pengiriman yang ada.
- Identifikasi mitra pengiriman potensial yang memiliki jangkauan dan reputasi yang lebih baik.
- Pastikan kerja sama dengan mitra pengiriman yang dapat memberikan pengalaman pengiriman yang lebih cepat dan handal.
2. Memperbanyak jumlah seller dan ketersediaan produk di negara bagian lainnya. Dari hasil EDA, sebesar 70% seller berada di Sao Paulo dan sebesar 64,1% transaksi terjadi pada antar negara bagian. Dengan pemerataan jumlah seller dan memastikan ketersediaan produk diberbagai negara bagian, hal tersebut memungkinkan durasi pengiriman lebih cepat dan tentunya biaya ongkos kirim akan menjadi lebih murah.
**Rekomendasi terkait tindakan pada masing-masing cluster:**
#### Big Spenders (Cluster 0):
1. Berikan lebih banyak rekomendasi dan iklan terkait produk Office Furniture, Housewares, Furniture Decor, Health Beauty dan Bed Bath Table.
2. Kolaborasi dengan penyedia kartu kredit lokal atau internasional untuk memberikan angsuran bunga nol.
3. Bermitra dengan perusahaan logistik yang secara khusus hebat dalam mengangkut barang-barang besar.
4. Program Loyalty Premium: Tawarkan program loyalitas yang memberikan insentif tambahan kepada Big Spenders, seperti diskon eksklusif, akses ke penawaran khusus, atau hadiah lainnya.
5. Paket Bundling Premium: Kembangkan paket produk eksklusif atau bundel yang sesuai dengan preferensi mereka, dan tawarkan dengan harga spesial untuk meningkatkan nilai pembelian.
6. Promosi Terbatas: Berikan promosi khusus untuk produk-produk yang sering mereka beli, dengan batas waktu tertentu untuk mendorong pembelian lebih lanjut.
7. Komunikasi Eksklusif: Kirimkan informasi produk baru atau penawaran eksklusif kepada mereka terlebih dahulu sebagai anggota kelompok Big Spenders.
#### Need Attention (Cluster 1):
1. Berikan lebih banyak rekomendasi dan iklan terkait produk Bed Bath Table, Health Beauty, Sports Leisure, Computers Accessoris dan Furniture Decor.
2. Pemberian Diskon untuk Pembelian Kedua: Fokus terhadap customer Need Attention dengan memberikan diskon tersebut jika melakukan pembelian sebanyak 2 kali dengan begitu dapat memperbesar kesempatan customer tersebut dalam meningkatkan repeat order.
3. Diskon Pembelian Massal: Tawarkan diskon khusus untuk pembelian dalam jumlah besar seperti buy 2 get 1, mendorong pelanggan Need Attention untuk meningkatkan frekuensi pembelian mereka.
4. Program Referral: Implementasikan program referensi untuk mendorong pelanggan untuk memperkenalkan teman atau keluarga, dengan imbalan yang menarik untuk setiap referensi yang berhasil.
5. Educational Content: Sediakan konten pendidikan atau tips penggunaan produk melalui email atau media sosial untuk meningkatkan keterlibatan dan pemahaman produk.
6. Event Promosi: Selenggarakan acara promosi atau penjualan khusus yang hanya terbuka bagi pelanggan Need Attention.
#### Loyal Customers (Cluster 2):
1. Berikan lebih banyak rekomendasi dan iklan terkait produk Bed Bath Table, Furniture Decor, Housewares, Health Beauty dan Garden Tools
2. Program Rewards Tertinggi: Tingkatkan program loyalitas untuk memberikan poin atau hadiah yang lebih besar kepada Loyal Customers, memberikan dorongan tambahan untuk setiap pembelian.
3. Feedback Eksklusif: Minta masukan eksklusif dari Loyal Customers untuk meningkatkan produk atau layanan dan berikan apresiasi melalui diskon khusus atau keuntungan lainnya.
4. Unggah Produk Baru Terlebih Dahulu: Berikan akses awal kepada produk baru atau penawaran khusus kepada Loyal Customers untuk meningkatkan keterlibatan mereka.
5. Event Khusus Pelanggan Loyal: Selenggarakan acara khusus atau pre-sale untuk pelanggan Loyal sebagai bentuk penghargaan atas kesetiaan mereka.
#### Potential Loyalist (Cluster 3):
1. Berikan lebih banyak rekomendasi dan iklan terkait produk Bed Bath Table, Furniture Decor, Health Beauty, Sports Leisure dan Computers Accessoris.
2. Program Loyalitas Awal: Tarik perhatian Potential Loyalist dengan program loyalitas awal yang menawarkan keuntungan khusus untuk pembelian berulang.
3. Follow-Up Personalisasi: Kirimkan email personalisasi atau pesan terkait produk berdasarkan sejarah pembelian mereka untuk menunjukkan perhatian dan membantu memandu keputusan pembelian.
4. Diskon Masa Depan: Berikan kupon atau diskon untuk penggunaan di pembelian berikutnya sebagai insentif tambahan untuk tetap menjadi pelanggan setia.
5. Konten Edukasi: Berikan konten edukatif atau panduan penggunaan produk untuk membantu mereka memahami nilai tambah dari produk yang mereka beli.



Link Tableau :
[Tableau](https://public.tableau.com/app/profile/ahmad.baihaqi/viz/AlphasTeamOlisteCommerceDashboard/DashboardEDA?publish=yes)
