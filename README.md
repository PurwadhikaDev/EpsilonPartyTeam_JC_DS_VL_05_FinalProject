# EpsilonPartyTeam_JC_DS_VL_05_FinalProject
Ecommerce Customer - Churn Analysis

Dataset Source : https://www.kaggle.com/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction

Contents Flowchart Program :
1. Business Problem Understanding
2. Data Understanding / EDA
3. Data Preprocessing
4. Modeling
5. Conclusion
6. Recommendation

Problem Understanding :
Sebuah perusahaan e-commerce yang bergerak dalam bisnis jual beli barang secara online merupakan salah satu solusi dalam dunia digital yang mempermudah pelanggan dalam memenuhi kebutuhannya tanpa harus berkunjung secara langsung ke toko penjual. Online e-commerce menawarkan banyak kemudahan bagi pelanggan diantaranya pelanggan dapat membandingkan banyak produk sekaligus untuk mendapatkan produk dengan harga yang murah dan berkualitas, banyak tersedia berbagai macam barang dalam satu tampilan, menyediakan berbagai metode pembayaran dari pembayaran secara cash hingga cicil melalui kartu kredit atau financial partner, hingga terdapat banyak promo dari diskon hingga cashback yang ditawarkan kepada pelanggan. Dalam bisnis online e-commerce, pelanggan menjadi komponen penting dalam pendapatan perusahaan contohnya seperti pelanggan dapat memberikan pendapatan secara langsung ketika pelanggan tersebut melakukan transaksi melalui online platform perusahaan, atau tingkat keramaian atau trafic pelanggan dalam online platform perusahaan juga dapat menarik brand untuk bekerjasama ikut memasarkan produknya melalui online platform perusahaan. Oleh karena itu menjadi hal yang sangat penting untuk perusahaan agar dapat menjaga pelanggannya agar tetap setia / loyal tidak berpindah pada online platform perusahaan lain (Customer Churn). Kita dapat melihat pada kasus netflix yang merupakan online platform untuk menonton film, pada kuartal 1 tahun 2022 netflix kehilangan hingga 200.000 pelanggan yang tentunya dapat berpengaruh cukup signifikan terhadap pendapatan perusahaan.

Customer Churn atau yang dikenal juga dengan pindahnya pelanggan adalah pemutusan jasa suatu perusahaan oleh pelanggan karena pelanggan tersebut memilih menggunakan jasa layanan lain (Masarifoglu & Buyuklu, 2019). Dengan memprediksi churn perusahaan dapat mengidentifikasi churn lebih awal sehingga kerugian perusahaan akibat konsumen yang pindah dapat dihindari. Konsumen adalah aset utama perusahaan sehingga salah satu cara perusahaan mempertahankan konsumen adalah dengan mengenali pelanggan potensial dan harus mampu mempertahankan pelanggan potensial (customer retention) sehingga dapat mencegah pelanggan menghentikan pembelian dan berpindah ke perusahaan pesaing (churn).

Menurut Emmet C. Murphy dan Mark A. Murphy dalam buku Leading On The Edge of Chaos bahwa memperoleh pelanggan baru menghabiskan biaya lima kali lipat dari biaya untuk memuaskan dan mempertahankan pelanggan lama, sementara itu peningkatan sebanyak 2% dalam mempertahankan pelanggan (customer retention) punya dampak terhadap laba seperti memangkas biaya sebesar 10%. Dengan menerapkan churn prediction, perusahaan dapat melakukan identifikasi pelanggan churn dan menerapkan strategi pemasaran yang tepat terhadap pelanggan – pelanggan lama dengan harapan dapat meningkatkan pendapatan perusahaan.

Target :
0 : Pelanggan tetap menggunakan E-commerce/Loyal
1 : Pelanggan meninggalkan menggunakan E-commerce/Keluar


Problem Statement :
Salah satu permasalahan yang penting dalam bisnis jual beli online adalah bagaimana perusahaan dapat menjaga konsumennya agar tetap loyal dan tidak pindah ke online platform perusahaan lain. Konsumen adalah aset utama perusahaan sehingga salah satu cara perusahaan mempertahankan konsumen yaitu dengan melakukan prediksi pelanggan churn. Dengan melalukan prediksi, perusahaan mampu mengidentifikasi pelanggan potensial (customer retention) sehingga perusahaan dapat menerapkan strategi pemasaran yang tepat seperti memberikan promo diskon atau cashback kepada pelanggan yang berpotensi churn sehingga dapat mencegah pelanggan tersebut menghentikan pembelian dan berpindah ke perusahaan pesaing (churn).

Dengan adanya model prediksi pelanggan churn ini, perusahaan dapat meminimalkan kerugian akibat kehilangan sejumlah pelanggan karena perusahaan mampu mengidentifikasi pelanggan yang loyal dan tidak. Sehingga biaya yang keluar untuk menarik pelanggan baru dapat dihindari dengan mempertahankan pelanggan yang loyal dimana biaya untuk mempertahankan pelanggan yang sudah ada relatif lebih rendah dibanding dengan menarik pelanggan baru.


Goals :
Berdasarkan permasalahan tersebut, perusahaan harus memiliki tools yang dapat memprediksi pelanggan churn dan mengenali karakteristik pelanggan churn sehingga perusahaan dapat mengambil langkah - langkah antisipatif untuk menjaga pelanggan tersebut. Variabel - variabel yang berpengaruh dalam pelanggan churn diantaranya gender, tenure / masa lama pakai aplikasi, kemudahan dalam menggunakan aplikasi (user friendly), jumlah promo yang ada dalam aplikasi, jangka waktu pengiriman barang hingga respon dari customer service jika terdapat kendala selama bertransaksi.

Tujuan pemodelan dengan memprediksi pelanggan churn adalah mengetahui karakteristik pelanggan churn berdasarkan metode klasifikasi. Pemodelan ini diharapkan mampu mengidentifikasi pelanggan churn dan tidak sehingga perusahaan mampu menerapkan strategi customer retention dan costumer churn yang tepat. Dan juga perusahaan dapat mengetahui variable kostumer loyal atau tidak terhadap layanan.


Analytic Approach :
Yang perlu dilakukan yaitu menganalisis karakteristik pelanggan yang loyal dan tidak sehingga data tersebut dapat diproses untuk membangun model. selanjutnya akan dibangun model klasifikasi yang mampu memprediksi pelanggan yang loyal atau tidak sehingga perusahaan dapat menerapkan strategi yang tepat terhadap customer retention dan costumer churn.


Metric Evaluation :
True Positive (TP) : Pelanggan diprediksi churn, secara aktual memang churn
True Negative (TN) : Pelanggan diprediksi tidak churn, secara aktual memang tidak churn
False Positive (FP) : Pelanggan diprediksi churn, tapi secara aktual tidak churn
False Negative (FN) : Pelanggan diprediksi tidak churn, tapi secara aktual churn

Berdasarkan klasifikasi confusion matrix diatas, dapat diklasifikasikan 2 tipe error yang dimungkinkan terjadi yaitu:

Type 1 error : False Positive
Kondisi dan dampak : Dimana dalam kondisi ini pelanggan yang diprediksi churn oleh model, namun secara aktual / sebenarnya pelanggan tersebut tidak churn. Kegagalan prediksi pada kondisi ini tidak akan menyebabkan perusahaan kehilangan pelanggan karena pelanggan yang dipresdiksi salah tetap akan menggunakan online platform perusahaan. Untuk dampak atas langkah perusahaan dalam mengantisipasi pelanggan churn seperti pemberian promo kepada pelanggan justru terdapat potensi peningkatan aktifitas transaksi oleh pelanggan tersebut dan untuk karakteristik pelanggannya tetap dapat digunakan untuk improvement performance pelayanan.

Type 2 error : False Negative
Kondisi dan dampak : Dimana dalam kondisi ini pelanggan yang diprediksi tidak churn oleh model, namun secara aktual / sebenarnya pelanggan tersebut churn. Kegagalan prediksi pada kondisi ini menyebabkan perusahaan kehilangan pelanggan tanpa tau alasan dan tanpa langkah antisipatif untuk menjaga pelanggan tersebut. Dengan hilangnya seketika sejumlah pelanggan tersebut, terdapat 2 kerugian yang sangat penting untuk perusahaan yaitu perusahaan kehilangan pendapatan langsung dari pelanggan, dan perusahaan kehilangan kesempatan untuk memetakan langkah-langkah perbaikan agar pelanggan tidak churn.

Dari kedua tipe error tersebut, dengan menimbang dampak yang paling besar terhadap pendapatan perusahaan maka yang akan dilakukan adalah membuat model yang dapat menekan angka False Negative agar perusahaan tidak kehilangan pelanggan dan memiliki kesempatan dalam melakukan langkah-langkah perbaikan untuk improvement performance palayanannya. Jadi matriks utama yang akan ditingkatkan nilainya yaitu recall agar mencegah nilai false negative yang tinggi.


Data Preprocessing :
Pada tahap ini, akan dilakukan cleaning pada data untuk kebutuhan proses analisis selanjutnya. Beberapa hal yang perlu dilakukan adalah:
1. Melakukan pengecekan terhadap duplikat data, missing value, dan drop fitur yang tidak memiliki relevansi terhadap permasalahan yang sedang dihadapi.
2. Melakukan treatment terhadap missing value jika ada. Hal ini dilakukan dengan cara men-drop fiturnya jika memang tidak dibutuhkan, mendrop data duplikat, menyatukan fitur yang memiliki kemiripan nama, mengganti nama data menjadi nama yang lebih umum dipakai dan mengimputasi dengan nilai yang paling masuk akal berdasarkan kasusnya.

Metode missing value yang digunakan yaitu simple imputer dengan nilai median untuk fitur yang memiliki rentang antara nilai min dan maxnya kecil, sedangkan iterative imputer digunakan untuk fitur yang memiliki keterkaitan cukup tinggi dengan fitur lainnya dan memiliki rentang antara nilai min dan max yang besar.

Metode handling data outlier menggunakan metode mahalanobis distance. Mahalanobis adalah suatu metode untuk menangani beberapa data outlier sekaligus (multivariat outlier) dengan mengukur mahalanobis distance dari setiap data outlier. Dari output mahalanobis distance tersebut dilakukan pengujian chi squared test untuk mendapat pvalue dari data. Nilai pvalue < 0.001 lah yang nantinya dikategorikan sebagai outlier.

Metode scaling yang akan digunakan yaitu robust scaler. Robust scaler merupakan metode scaling yang kuat dengan data yang memiliki banyak outlier. Robust Scaler menggunakan rentang inter quartile secara default (rentang antara q1 dan q3). Transformer dengan robust scaler hanya digunakan untuk model logistic regression yang tidak menggunakan basis tree dalam algoritmanya.


Modeling and Evaluation :
Pada model and evaluation dibandingkan hasil performa model dengan menggunakan nilai recall sesuai dengan evaluasi metrics yang telah ditetapkan diawal dengan harapan mampu menekan sekecil mungkin nilai false negative dan mendapatkan nilai recall yang tinggi. Formula recall yaitu:

Recall = (TP) / (TP + FN)

Model yang akan dibandingkan yaitu terdapat 5 model yaitu:
1. Logistic regression
2. LightGBM
3. Decision Tree
4. Random Forest
5. XGBoost
Dari kelima model tersebut akan dipilih model terbaik yang memberikan nilai recall yang tinggi, stabil antara train dan testnya serta standar deviasi yang rendah.

Berdasarkan hasil prediksi pada train dan test set, XGBoost memberikan performa yang paling baik dengan score recall yang lebih tinggi dibanding model yang lain. Jika dibandingkan hasil uji performa yang ada, model tanpa handling outlier memberikan performa akhir yang lebih baik untuk nilai recall pada test setnya namun model dengan handling outlier memberikan performa yang lebih stabil antara train dan testnya, sehingga akan diambil model dengan handling outlier dengan hasil berikut:
1. Recall Score (Train) : 0.856563
2. Recall Score (Test) : 0.864198
3. Standard Deviasi : 0.027270

Selanjutnya dilakukan handling imbalance menggunakan oversampling dan undersampling dengan hasil didapatkan nilai recall terbaik dari metode undersampling. Maka selanjutnya akan dilakukan hyperparam tuning dengan menggunakan algoritma XGboost dan undersampling.

Dilakukan percobaan hyperameter tuning namun hasil yang didapatkan tidak dapat meningkatkan performa model, model mengalami penurunan performa setelah di hyperparameter tuning walaupun hanya sedikit dengan hasil :
1. Nilai recall menurun dari 94,4% menjadi 93,8%
2. Nilai false negative (FN) meningkat dari sebanyak 9 menjadi 10

Selanjutnya dilakukan feature importance dengan hasil dapat meningkatkan performa model serta diketahui fitur mana saja yang penting dan tidak penting untuk model:
1. Tenure menjadi fitur yang paling berpengaruh terhadap model
2. 'OrderCount','CouponUsed', 'MaritalStatus','PreferredPaymentMode','NumberOfDeviceRegistered' menjadi fitur yang paling kurang berpengaruh terhadap model
3. Setelah dilakukan drop untuk fitur yang kurang berpengaruh jika dibandingkan dengan hasil dari model setelah di hyperparam tuning, didapatkan nilai recall jadi meningkat dari 93,8% menjadi 95,06% dan nilai FN menurun dari 10 menjadi 8.
4. Serta jika dilihat dari model sebelum di hyperparam tuning yang lebih baik, didapatkan nilai recall meningkat juga dari 94,4% menjadi 95,06% dan nilai FN menurun dari 9 menjadi 8.


Conclusion :
Berdasarkan hasil classification report dari model yang memberikan kinerja recall dan FN rate terbaik yaitu model setelah dilakukan handling imbalance menggunakan undersampling namun tanpa dilakukan hyperparameter tuning maupun feature importance. Dapat disimpulkan bahwa untuk model yang digunakan untuk memprediksi pelanggan mana saja yang berpotensi untuk Churn ke aplikasi perusahaan lain, model yang terpilih dapat mengurangi 95% kandidat pelanggan yang akan benar - benar Churn karena sebelum pelanggan tersebut churn perusahaan dapat memberikan treatment untuk mencegah pelanggan tersebut Churn. Hal ini sangat berdampak positif bagi perusahaan karena dengan begitu model dapat digunakan untuk menjaga sumber pendapatan perusahaan (pelanggan) dengan cukup akurat sehingga perusahaan dapat meminimalkan biaya yang keluar untuk mencari pelanggan baru dan biaya yang dapat digunakan untuk fokus pada pelanggan yang telah ada agar dapat meningkatkan transaksinya.

Namun dari model didapatkan sejumlah FN sebanyak 8 pelanggan yang dapat berpotensi pada hilangnya pelanggan tersebut akibat Churn atau berpindah ke perusahaan lain. Untuk mengatasi hal tersebut perusahaan dapat melakukan langkah preventif kepada seluruh pelanggan tanpa memperhatikan hasil prediksi churn atau tidaknya terlebih dahulu dengan memperhatikan feature importance dari data. Seperti perusahaan dapat memberikan fokusnya kepada pelanggan dengan Tenure < 2 bulan dimana pada periode ini merupakan waktu kritis pelanggan banyak Churn. Bisa jadi memang selama ini perusahaan kurang memberikan perhatian untuk pelanggan dengan jangka waktu tersebut seperti hanya memberikan promo yang menarik untuk pelanggan baru yang pertama kali transaksi dan selanjutnya pelanggan baru akan mendapat promo yang menarik kembali setelah berlangganan dan bertransaksi cukup banyak terlebih dahulu.


Recommendation:
Hal-hal yang dapat dilakukan untuk mengembangkan model agar lebih baik lagi, seperti:
1. Melakukan pengecekan dan pengelompokkan atas fitur - fitur mana saja yang memberikan error yang tinggi terhadap target Churn sehingga kita dapat melakukan feature engineering yang lebih baik terlebih dahulu terhadap fitur tersebut agar dapat meningkatkan performa model.
2. Melakukan penambahan data dari yang ada saat ini sejumlah sekitar 5000 menjadi lebih banyak. Sehingga model mendapatkan banyak refrensi data yang dipelajari. Penambahan data dapat dilakukan dengan melakukan update data terbaru atau memperbaiki data mentah yang terdapat missing value dengan nilai sebenarnya.
3. Jika memungkinkan, penambahan fitur yang lebih korelatif dengan target ('Churn'), seperti sentimen analisis untuk feedback dari pelanggan, ataupun jumlah transaksi untuk setiap bulannya untuk melihat tren kenaikan atau penurunan yang terjadi dari transaksi pelanggan.
4. Jika ada penambahan banyak data, dapat dicoba dengan menggunakan model yang lebih kompleks, seperti recursive neural networks (RNN) ataupun support vector machine (SVM).
5. Selanjutnya kedepan dari model ini dapat dijadikan sebagai dasar pengembangan untuk model lainnya seperti model untuk mengklasifikasikan jenis pelanggan terhadap barang yang diminati dan jumlah transaksinya. Model tersebut bermanfaat sebagai dasar perencanaan biaya marketing strategy agar dapat optimal terhadap peningkatan pendapatan perusahaan dari transaksi oleh pelanggan.

Adapun sebagai upaya untuk menjaga agar pelanggan tidak Churn, strategi yang dapat dilakukan oleh perusahaan yaitu:
1. Memberikan promo diskon / cashback. Pemberian promo berupa diskon atau cashback mampu memberikan ketertarikan pelanggan agar terus berlangganan dan bertransaksi, namun langkah ini juga harus dianalisis lebih dalam untuk jumlah dan periode waktunya karena dapat berdampak buruk juga jika perusahaan terlalu berlebihan dalam melakukannya.
2. Meningkatkan dukungan konsumen. Ketika customer mendapatkan dukungan dan arahan penuh dari perusahaan, maka customer lebih mungkin untuk tidak melakukan churn. Misalnya seperti dukungan via telepon, text, video tutorial, in-app customer service, atau blog yang membantu. Dukungan ini memberikan kesan perlindungan lebih terhadap customer dari berpindah ke kompetitor.
3. Monitor Kompetitor. Analisis kompetitor dan lihat kembali layanan mana yang bisa ditingkatkan lebih baik dari kompetitor.
4. Memperhatikan feedback. Perhatikan feedback yang didapat dari customer baik yang positif maupun negatif.
5. Menambahkan layanan promosi via mobile phone. Pergunakan promosi via mobile phone karena customer yang churn maupun tidak lebih banyak login menggunakan mobile phone.
6. Meningkatkan Layanan Tambahan. 2 Bulan pertama merupakan masa paling krusial untuk menjaga customer tetap loyal. Hal ini karena pengguna cenderung churn pada 2 bulan pertama penggunaan. Sehingga untuk mengantisipasi hal tersebut, lebih baik customer diberikan layanan tambahan, seperti UX yang baik, hadiah untuk pembelian pertama, ataupun pemberian diskon eksklusif untuk pelanggan pertama.
7. Segmentasi pengguna. Kebutuhan customer perempuan dan laki-laki bisa jadi berbeda. Kebutuhan customer awal dan customer yang bertahan lebih lama tentu berbeda. Oleh karena itu bentuk segmentasi customer sehingga perusahaan dapat memberikan targeted ads khusus untuk pengguna sesuai segmentasinya. Berikan promosi menarik ketika pengguna meraih milestone tertentu, misal bertahan 10 bulan dapat diberikan hadiah gratis ongkos kirim barang.
8. Bangun Komunitas. Pada data diatas, pengguna Churn lebih banyak membeli mobile phone. Oleh karena itu lebih baik membuat komunitas di sosial media untuk saling terkoneksi dengan pelanggan lainnya yang membeli produk mobile phone di e-commerce. Hal ini akan mendorong testimonial, update terbaru tentang gadget, dan mendorong customer untuk tidak merasa sendiri. Bentuk lain dari membentuk komunitas mungkin dapat menggunakan membership.
