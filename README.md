import streamlit as st

# Ganti dengan direct image URL kamu
background_url = "https://i.ibb.co.com/xqwsXfq8/IMG-0774.jpg"

st.markdown(
    f"""
    <style>
    .stApp {{
        background-image: url("{background_url}");
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        background-attachment: fixed;
    }}
    </style>
    """,
    unsafe_allow_html=True
)
# ---------- SESSION STATE UNTUK NAVIGASI ----------
if 'page' not in st.session_state:
    st.session_state.page = 0

# ---------- HALAMAN-HALAMAN ----------
def halaman_1():
    st.markdown(
        """
        <h1 style="
            font-weight: 1000;
            color: #1A1A1A;
            text-shadow: 1px 1px 3px rgba(255,255,255,0.6);
            background-color: rgba(255, 255, 255, 0.6);
            padding: 10px;
            border-radius: 10px;
            display: inline-block;
        ">
            🥦Helloooww welcome at VeggieBites guys!!
        </h1>
        """, 
        unsafe_allow_html=True
     )
    st.markdown("Cari tahu yukk tipe vegetarian kamu yang mana biar kita bisa bantu kasih menu sehat yang sesuai buat kamuu><")

    pilihan = st.radio(
        "Kamu termasuk tipe vegetarian yang mana nih?",
        [
            "Lacto-ovo (telur & susu masih aku makan sieh)",
            "Lacto (only susu, telur big no no)",
            "Ovo (telur oke sieh, tapi susu ga dulu deh)",
            "Vegan total (no hewani et all)"  ]
    )
    
    if st.button("Next"):
        st.session_state.page += 1
def halaman_2():
    st.title("BesBite Kasih Sedikit Penjelasan Yaaa!!!")
    st.subheader("Vegetarian Lacto-Ovo")
    st.markdown("Pada jenis diet vegetarian ini, kamu tidak boleh mengonsumsi daging atau ikan. Akan tetapi, kamu masih diizinkan mengonsumsi telur dan produk susu. Kata “lacto” mengacu pada susu sapi dan produk olahannya, sedangkan kata “ovo” berarti telur. Pola makan tersebut memperbolehkan kamu mengonsumsi susu dan olahan lain, seperti mentega, keju, krim, yoghurt, atau es krim.")
    st.subheader("Vegetarian Lacto")
    st.markdown("Berbeda dengan jenis diet vegetarian sebelumnya, diet vegetarian lacto masih memperbolehkan konsumsi susu dan produknya, seperti mentega, keju, yoghurt, krim, dan es krim. Namun, kamu harus menghindari jenis daging, seperti sapi, babi, ayam, dan ikan. Tak hanya itu, pelaku diet vegetarian lacto juga tidak mengonsumsi telur. Oleh karena itu, orang yang mengikuti pola makan ini hanya boleh mengonsumsi sayur, buah, protein nabati seperti tahu, tempe, dan kacang-kacangan, serta susu dan produk olahannya")
    st.subheader("Vegetarian Ovo")
    st.markdown("Diet vegetarian ovo adalah pola makan yang tidak memasukkan produk susu dan daging dalam daftar makanannya. Akan tetapi, pelaku jenis diet vegetarian ini masih boleh mengonsumsi telur. Dengan demikian, sumber protein dalam diet vegetarian ini masih cukup terjamin, yakni dari tahu, tempe, kacang, dan telur.")
    st.subheader("Vegan")
    st.markdown("Jenis diet vegetarian ini mengecualikan semua produk yang berasal dari hewan, termasuk daging, ikan, produk susu, dan telur. Beberapa orang yang menjalani diet ini juga tidak boleh mengonsumsi madu karena diproduksi oleh hewan lebah. Diet vegan hanya membolehkan makanan nabati, seperti buah, sayuran, biji-bijian, kacang-kacangan, tahu, dan tempe. Penganut vegan biasanya juga menghindari pembelian produk seperti kosmetik, pakaian, dan sepatu yang terbuat atau diujicobakan pada hewan. Meski memiliki manfaat tersendiri, diet vegan juga berisiko menyebabkan rendahnya asupan nutrisi. Ahli kesehatan menyarankan untuk mengonsumsi suplemen mengandung vitamin B12, zat besi, omega-3, zinc, dan lainnya yang biasanya didapat dari produk hewani.")
    if st.button("Next"):
        st.session_state.page += 1
    if st.button("Back"):
        st.session_state.page -= 1
def halaman_3():
    st.title("Kebutuhan Nutrisi Kamu")
    st.markdown("Sebagai vegetarian, kamu perlu perhatian khusus pada beberapa nutrisi ini loh:")
    st.markdown("""
    - Protein: Tempe, tahu, kacang-kacangan, Telur, Biji Chia, Quinoa, Bayam
    - Zat Besi: Bayam, Brokoli, Kacang Merah, Buncis, Lentil
    - Vitamin B12: Susu Kedelai Fortifikasi, suplemen, Serealia, Nori
    - Kalsium: Tahu, Almond, Sayur Hijau, Susu Kedelai
    - Omega-3: Flaxseed, Spirulina, Chlorella
    """)
    if st.button("Next"):
        st.session_state.page += 1
    if st.button("Back"):
        st.session_state.page -= 1
def halaman_4():
    st.title("Rekomendasi Menu Cemilan Vegetarian Buat Kamu")
    st.subheader("1. 💚Smoothie Green💚")
    st.markdown("Bahan: Bayam, pisang, susu almond, chia seed")
    st.subheader("2. 🫑Tofu Stir Fry🥕")
    st.markdown("Bahan: Tahu, paprika, wortel, kecap asin")
    st.subheader("3. 🍫Overnight Oat Choco-Berry🍓")
    st.markdown("Bahan: Oat, susu oat, kakao bubuk, stroberi")
    st.markdown("Cara buat: Campur bahan, simpan di kulkas semalam.")
    st.subheader("4. 🥜Salad Kacang🥜")
    st.markdown("Bahan: Kacang merah, jagung, tomat, alpukat")
    st.markdown("Cara buat: Campur semua bahan dengan dressing lemon & olive oil.")
    st.subheader("5. 🥬Veggie Wrap🥬")
    st.markdown("Bahan: Tortilla, selada, wortel, hummus, timun")
    st.markdown("Cara buat: Isi tortilla dengan semua bahan dan gulung.")
    if st.button("Next"):
        st.session_state.page += 1
    if st.button("Back"):
        st.session_state.page -= 1
def halaman_5():
    st.title("Ada Resep Makanan Vegetarian Tambahan Nih Buat Kamu + Cara Masaknya Lohhh!")
    st.subheader("1. 🍗Drumstick Vegetarian🍗")
    st.markdown("Bahan: 100 gram tempe, 3 sdm tepung tapioka, ½ sdt garam, ½ sdt kaldu jamur, ¼ sdt lada bubuk, 150 ml minyak goreng")
    st.markdown("Cara Membuat: Pertama, potong-potong tempe. Lalu, haluskan tempe dengan chopper. Campurkan tempe, tepung, garam, kaldu dan lada aduk rata. Bentuk adonan drumstick seperti paha ayam atau drumstick. Goreng sampai kecoklatan lalu angkat dan sajikan.")
    st.subheader("2. 🥖Mirukuhasu Vegetarian🥖")
    st.markdown("Bahan: 300 gr tepung cakra, 35 gr gula pasir, 125 ml air hangat, 4 rg ragi, 4 gr garam.")
    st.markdown("Cara Membuat: Campurkan air hangat dengan ragi dan gula, biarkan mengembang. Campurkan tepung dan garam. Tuang campuran air ke campuran tepung. Uleni hingga kalis dan halus. Biarkan sekitar 1 jam atau mengembang dua kali lipat. Kempiskan adonan lalu bagi beberapa bagian. Ambil adonan lalu giling dan bentuk sesuai selera. Tutup dengan lap biarkan mengembang. Setelah mengembang, taburi dengan tepung. Scoring dengan isi cutter atau pisau tajam, bentuk sesuai selera. Panggang pada suhu 180-190 derajat Celsius selama 40 menit atau hingga matang. Mirukuhasu siap disajikan.")
    st.subheader("3. 🫕Miso Soup🫕")
    st.markdown("Bahan: Tofu, potong dadu 200 gram, Dashi 2 sdm, Pasta miso 1,5 sdm, Daun bawang iris tipis 2 batang, Air 750ml.")
    st.markdown("Cara Membuat: Panaskan air, masukan dashi. Masak hingga mendidih. Setelah mendidih, kecilkan api. Masukan pasta miso dengan menggunakan saringan kecil di atas kuah sambal dilumatkan dengan sendok hingga pasta larut. Besarkan menjadi api sedang, aduk rata kuah. Masukan tofu dan daun bawang. Aduk perlahan hingga tofu matang, matikan api. Tuang dalam mangkuk, sup miso siap disajikan hangat.")
    st.subheader("4. 🍕Pizza Mozzarella Jamur🍕")
    st.markdown("Bahan: Terigu protein tinggi 125 gram, Ragi instan 3 gram, Air 90 ml, Olive oil 2 sdm, Garam 1/2 sdt")
    st.markdown("Topping: Jamur kancing iris tipis 100 gram, Saus tomat 4 sdm, Oregano 1/4 sdt, Paprika potong kecil 1/4 buah, Bawang bombay iris tipis 1/2 buah, Tomat potong bulat tipis 1 buah, Keju mozarella parut 100 gram, Parsley kering secukupnya")
    st.markdown("Cara Membuat: Adonan pizza: Campur terigu, ragi instan, air, olive oil, dan garam, uleni sampai kalis. Setelah kalis, bulatkan adonan. Tutup dengan serbet bersih supaya permukaan adonan tidak kering. Istirahatkan 30 menit sampai mengembang 2x lipat. Kempiskan adonan, taruh di loyang yang sudah dioles tipis dengan olive oil. Pipihkan sesuai bentuk loyang, tekan-tekan tepi adonan untuk membentuk pinggiran pizza. Tusuk-tusuk permukaannya dengan garpu. Kemudian, oles tipis dengan olive oil. Campur saus tomat dengan oregano, aduk rata kemudian oles di adonan pizza. Taburi dengan 1/2 bagian keju mozzarella, tata jamur kancing, paprika, tomat dan bawang bombay, taburi kembali dengan sisa mozzarella dan sedikit parsley kering. Panggang 180°C selama 30 menit, sampai matang. Potong-potong dan sajikan pizza mozzarella jamur.")
    st.subheader("5. 🍄Rendang Jamur🍄")
    st.markdown("Bahan: Jamur tiram suwir 300 gram, Bawang merah iris tipis 3 butir, Daun salam 1 lembar, Lengkuas 2 ruas jari, Gula merah 1/2 sdm, Santan 500 ml, Minyak untuk menumis 3 sdm, Bawang putih 2 siung, Bawang merah 3 butir, Cabai merah 6 buah, Ketumbar 1/2 sdt, Jinten 1/4 sdt, Garam 1 sdt")
    st.markdown("Cara Membuat: Panaskan minyak, tumis bawang merah hingga layu dan harum. Tambahkan bumbu halus, daun salam, lengkuas dan gula. Tumis hingga harum dan matang. Masukkan santan. Aduk terus hingga mendidih. Masak hingga santan menyusut dan mengental. Masukkan jamur tiram. Aduk rata dan masak hingga santan hampir habis dan mengeluarkan minyak. Angkat Siap disajikan.")
    if st.button("Next"):
        st.session_state.page += 1
    if st.button("Back"):
        st.session_state.page -= 1
def halaman_6():
    st.title("Butuh Pengganti Bahan?")
    st.markdown("Masukkan bahan yang ingin diganti, nanti kita bantu kasih alternatifnya!")
    st.markdown("Contoh: susu, telur, daging, keju, dll")

    # Simpan hasil di session_state
    if "hasil_pengganti" not in st.session_state:
        st.session_state.hasil_pengganti = ""
    if "bahan_input" not in st.session_state:
        st.session_state.bahan_input = ""
     # Input text biasa
    st.session_state.bahan_input = st.text_input("Masukkan nama bahan yang mau diganti:", value=st.session_state.bahan_input)

    # Tombol Search
    if st.button("Search"):
        bahan = st.session_state.bahan_input.lower()
        pengganti = {
            "susu": "susu almond / oat milk",
            "telur": "chia egg (chia + air)",
            "daging": "jamur, tempe, atau tofu",
            "keju": "keju vegan berbasis kacang",
            "daging sapi": "tempe, tahu, jamur tiram, jackfruit, seitan",
            "daging ayam": "tempe, tahu, jamur tiram, jackfruit, seitan",
            "daging giling": "kacang hitam, kacang merah, walnut cincang, tahu hancur",
            "susu sapi": "susu almond, susu kedelai, oat milk, coconut milk",
            "keju cheddar": "keju vegan, nutritional yeast",
            "parmesan": "nutritional yeast, kacang mete blend",
            "cream cheese": "tahu sutra + lemon + garam (di-blend)",
            "mentega": "minyak kelapa, margarin vegan, alpukat",
            "mayones": "mayones vegan, tofu + mustard + lemon",
        }
        hasil = pengganti.get(bahan, "Bahan yang kamu cari belum ada di daftar. Coba bahan lain yuk!")
        st.session_state.hasil_pengganti = f"Pengganti untuk {bahan}: {hasil}"

    # Tampilkan hasil kalau ada
    if st.session_state.hasil_pengganti:
        st.success(st.session_state.hasil_pengganti)

    # Navigasi tombol
    col1, col2 = st.columns(2)
    with col1:
        if st.button("Back", key="back4"):
            st.session_state.page -= 1
            st.session_state.hasil_pengganti = ""
    with col2:
        if st.button("Next", key="next4"):
            st.session_state.page += 1
            st.session_state.hasil_pengganti = ""
def halaman_7():
    st.title("Terima Kasih Telah Berkunjung!")
    st.markdown("Semoga VeggieBites bermanfaat untuk kamu!")
    if st.button("Back"):
        st.session_state.page -= 1

halaman_fungsi = [halaman_1, halaman_2, halaman_3, halaman_4, halaman_5, halaman_6, halaman_7]
halaman_fungsi[st.session_state.page]()
        
