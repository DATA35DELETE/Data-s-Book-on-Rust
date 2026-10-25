# Data's Book on Rust
 
## Rust
 
### Ön Söz
- Ben kimim?
- Bu Data's Book on Rust nedir?
- Bu dokümantasyon ne öğretecek?
 
---
 
### Rust : Giriş
- **Yazılım Nedir?**
  - **Donanım Nedir?**
  - **Low-Level ve High-Level**
  - **Yazılım Dilleri**
- **Rust Nedir?**
  - **Kısa Tarihçesi**: Mozilla, 2010, 1.0 Sürümü (2015).
  - **C/C++ ile Farkı**: Bellek Güvenliği. Garbage Collector Yok. Ownership Modeli.
  - **Nasıl Kullanılır?**
  - **Kullanım Alanları**: Sistem Programlama. WebAssembly. CLI Araçları. Embedded.
  - **Rust'ın Temel Felsefesi**: Güvenlik. Hız. Eş Zamanlılık (Fearless Concurrency).
- **Rust'ı Kurma**
  - **rustup Kurulumu**: rustup Nedir? Nasıl Kurulur? Toolchain Yönetimi.
  - **IDE Seçimi**: VS Code + rust-analyzer. RustRover.
  - **İlk Proje**: `cargo new`. Proje Yapısı.
- **İlk Kod**: println! ve Giriş Alma
  - **println! Makrosu**: Tanım. Formatlama (`{}`, `{:?}`, `{:#?}`). Örnek.
  - **Kullanıcıdan Girdi Alma**: `std::io::stdin`. `read_line`. Örnek.
  - **C/C++'dan Farkı**: printf vs println!. scanf vs stdin. Örnek.
  - **Parametreli Programlar Yazma**: `std::env::args`. Tanım. Örnek.
- **Derleme Süreci**: Tanım. Neden Önemli?
  - **Cargo**: Tanım. `cargo build`. `cargo run`. `cargo check`. Örnek.
  - **rustc**: Doğrudan Derleme. Örnek.
  - **Derleme Hedefleri (Targets)**: `--target`. Cross Compilation. Örnek.
  - **Rust Editions**: 2015, 2018, 2021, 2024. `edition` Alanı. Farklar.
 
---
 
### Rust : Değişkenler
- **Değişkenler Nedir?**: Tanımı. Kullanım Senaryoları.
- **let ve Değişmezlik (Immutability)**: Tanım. `let` vs `let mut`. Örnek.
- **Sayısal Değişkenler**
  - **i8 / i16 / i32 / i64 / i128**: Tanım. İşaretli Tam Sayılar. Örnek.
  - **u8 / u16 / u32 / u64 / u128**: Tanım. İşaretsiz Tam Sayılar. Örnek.
  - **isize / usize**: Tanım. Platform Bağımlı. Örnek.
  - **f32 / f64**: Tanım. Kayan Nokta. Örnek.
- **İsimlendirme Kuralları**: snake_case. Tablo Halinde.
- **char**: Tanım. Unicode Skalar Değer. 4 Byte. Örnek.
- **bool**: Tanım. true/false. Örnek.
- **Tür Çıkarımı (Type Inference)**: Tanım. Derleyicinin Tür Belirlemesi. Örnek.
- **Tür Dönüşümü (Type Casting)**: `as` Anahtar Kelimesi. Tanım. Örnek.
  - **i32 → f64**: Örnek.
  - **f64 → i32**: Örnek.
- **Sabitler**: `const`. `static`. Farkları. Örnek.
- **Shadowing**: Tanım. `let` ile Yeniden Tanımlama. `mut` ile Farkı. Örnek.
- **Tür Takma Adları (Type Aliases)**: `type` Anahtar Kelimesi. Tanım. Örnek.
 
---
 
### Rust : Operatörler
- **Operatörler Nedir?**: Tanımı. Kullanım Senaryoları.
- **Atama Operatörü**: Tanım. Örnek.
- **Aritmetik Operatörler**
  - **+**: Tanım. Örnek.
  - **-**: Tanım. Örnek.
  - **\***: Tanım. Örnek.
  - **/**: Tanım. Tamsayı Bölme Davranışı. Örnek.
  - **%**: Tanım. Örnek.
  - **Bileşik Atama Operatörleri**: +=, -=, \*=, /=. Örnek.
- **Yorum Satırı**: // ve /* */. `///` Dokümantasyon Yorumu. `//!` Modül Yorumu. Örnek.
- **Karşılaştırma Operatörleri**
  - **<, >, <=, >=, ==, !=**: Tanım. `PartialEq` ve `PartialOrd` Trait'leri. Örnek.
- **Mantıksal Operatörler**
  - **!**: Tanım. Örnek.
  - **&&**: Tanım. Kısa Devre Değerlendirme. Örnek.
  - **||**: Tanım. Kısa Devre Değerlendirme. Örnek.
- **Bitwise Operatörler**: &, |, ^, !, <<, >>. Tanım. Örnek.
- **Aralık Operatörleri**: `..` ve `..=`. Tanım. Örnek.
- **std::mem::size_of**: Tanım. `size_of_val`. Örnek.

---
 
### Rust : Karar Yapıları
- **Karar Yapısı Nedir?**: Tanım. Program Akışı. Örnek.
- **if-else if-else**: Tanım. İfade Olarak Kullanımı (Expression). Örnek.
- **match**: Tanım. Pattern Matching. Exhaustiveness. Örnek.
  - **Guard Koşulları**: `if` ile match kolu. Örnek.
  - **Binding**: `@` Operatörü. Örnek.
- **if let**: Tanım. Tek Patern Eşleştirme. Örnek.
- **while let**: Tanım. Döngüsel Patern Eşleştirme. Örnek.
 
---
 
### Rust : Döngü Yapıları
- **Döngü Nedir?**: Tanım. Örnek.
- **loop**: Tanım. Sonsuz Döngü. `break` ile Değer Döndürme. Örnek.
- **while**: Tanım. Örnek.
- **for**: Tanım. Iterator Tabanlı. Örnek.
  - **Range ile for**: `0..10`, `0..=10`. Örnek.
  - **Koleksiyon ile for**: `iter()`, `iter_mut()`, `into_iter()`. Örnek.
- **break ve continue**: Tanım. Etiketli Döngüler (`'label`). Örnek.
 
---
 
### Rust : Ownership ve Borrowing
- **Ownership Nedir?**: Tanım. Rust'ın Temel Kuralı. Üç Kural.
  - **Kural 1**: Her Değerin Tek Bir Sahibi Vardır.
  - **Kural 2**: Aynı Anda Yalnızca Bir Sahip Olabilir.
  - **Kural 3**: Sahip Scope Dışına Çıkınca Değer Drop Edilir.
- **Move Semantiği**: Tanım. Stack vs Heap Davranışı. Örnek.
- **Clone ve Copy**: `Clone` Trait'i. `Copy` Trait'i. Farkları. Örnek.
- **Borrowing (Ödünç Alma)**: Tanım. `&` Referans. Örnek.
  - **Immutable Borrowing**: `&T`. Birden Fazla Olabilir. Örnek.
  - **Mutable Borrowing**: `&mut T`. Aynı Anda Yalnızca Bir Tane. Örnek.
  - **Borrowing Kuralları**: Tanım. Derleyici Kontrolü. Örnek.
- **Dangling References**: Tanım. Rust'ın Önleme Mekanizması. Örnek.
- **Slice'lar**: `&[T]`. `&str`. Tanım. Örnek.
 
---
 
### Rust : Lifetimes (Yaşam Süreleri)
- **Lifetime Nedir?**: Tanım. Neden Gerekli? Derleyici Perspektifi.
- **Lifetime Annotasyonu**: `'a` Sözdizimi. Tanım. Örnek.
- **Fonksiyonlarda Lifetime**: Tanım. Birden Fazla Referans. Örnek.
- **Struct'larda Lifetime**: Tanım. Referans İçeren Struct. Örnek.
- **Lifetime Elision Kuralları**: Tanım. Üç Kural. Derleyicinin Otomatik Çıkarımı.
- **'static Lifetime**: Tanım. String Literal. Kullanım Senaryoları. Örnek.
 
---
 
### Rust : String Yapısı
- **String Tipleri**: `String` vs `&str`. Tanım. Farkları. Örnek.
- **String Oluşturma**: `String::new()`. `String::from()`. `.to_string()`. Örnek.
- **String Fonksiyonları**: `len`, `push`, `push_str`, `contains`, `replace`, `trim`, `split`. Örnek.
  > Metodları
- **String Dilimi (&str)**: Tanım. Kullanım Senaryosu. Örnek.
- **String Formatlama**: `format!` Makrosu. Tanım. Örnek.
- **String ve Ownership**: Tanım. Borrowing ile Kullanım. Örnek.
- **Karakter İterasyonu**: `chars()`. `bytes()`. Örnek.
 
---
 
### Rust : Koleksiyonlar
- **Koleksiyon Nedir?**: Tanım. Heap Üzerinde Depolama. Kullanım Senaryoları.
- **Vec<T> (Vektör)**: Tanım. Dinamik Dizi. Örnek.
  > Metodları
- **VecDeque<T>**: Tanım. Çift Uçlu Kuyruk. Örnek.
  > Metodları
- **HashMap<K, V>**: Tanım. Anahtar-Değer. Örnek.
  > Metodları
- **BTreeMap<K, V>**: Tanım. Sıralı Map. HashMap ile Farkı. Örnek.
- **HashSet<T>**: Tanım. Küme İşlemleri. Örnek.
  > Metodları
- **BTreeSet<T>**: Tanım. Sıralı Küme. Örnek.
- **LinkedList<T>**: Tanım. Doubly Linked List. Örnek.
- **BinaryHeap<T>**: Tanım. Öncelikli Kuyruk. Örnek.
 
---
 
### Rust : Struct, Enum ve Pattern Matching
- **Struct Nedir?**: Tanım. C Struct ile Karşılaştırma.
- **Struct Tanımlama ve Kullanma**: Tanım. Örnek.
- **Tuple Struct**: Tanım. Örnek.
- **Unit Struct**: Tanım. Kullanım Senaryosu. Örnek.
- **impl Bloğu**: Tanım. Metod Tanımlama. `self`, `&self`, `&mut self`. Örnek.
- **Associated Functions**: Tanım. `Self`. Constructor Paterni. Örnek.
- **Enum Nedir?**: Tanım. C enum ile Farkı. Veri Taşıyan Enum.
- **Enum Tanımlama**: Tanım. Varyantlar. Veri İçeren Varyantlar. Örnek.
- **Option<T>**: Tanım. `Some(T)` ve `None`. Null Güvenliği. Örnek.
- **Result<T, E>**: Tanım. `Ok(T)` ve `Err(E)`. Hata Yönetimi. Örnek.
- **Pattern Matching Detaylı**: Tanım. Destructuring. Nested Pattern. Örnek.
- **if let ve while let**: Tanım. match Kısayolu. Örnek.
- **let-else**: Tanım. Erken Çıkış Paterni. Örnek.
 
---
 
### Rust : Hata Yönetimi
- **Hata Yönetimi Nedir?**: Tanım. Rust Yaklaşımı. Panik vs Kurtarılabilir Hata.
- **panic! Makrosu**: Tanım. Kullanım Senaryoları. Örnek.
  - **RUST_BACKTRACE**: Tanım. Hata İzleme. Örnek.
- **Result<T, E>**: Tanım. Kullanım. Örnek.
  - **unwrap()**: Tanım. Tehlikesi. Örnek.
  - **expect()**: Tanım. Mesajlı Panik. Örnek.
  - **match ile Hata Yönetimi**: Tanım. Örnek.
  - **? Operatörü**: Tanım. Hata Yayılımı (Propagation). Örnek.
- **Özel Hata Tipleri**: Tanım. `std::fmt::Display`. `std::error::Error`. Örnek.
- **thiserror Crate'i**: Tanım. Derive Makrosu. Örnek.
- **anyhow Crate'i**: Tanım. Dinamik Hata. Kullanım Senaryosu. Örnek.
 
---
 
### Rust : Fonksiyonlar ve Closure'lar
- **Fonksiyon Nedir?**: Tanım. `fn` Anahtar Kelimesi. main Fonksiyonu.
- **Parametreli Fonksiyonlar**: Tanım. Tür Belirtme Zorunluluğu. Örnek.
- **Dönüş Değeri**: Tanım. `->` Sözdizimi. İfade ile Dönüş. Örnek.
- **Çoklu Dönüş (Tuple)**: Tanım. Örnek.
- **Fonksiyon Overloading Yoktur**: Tanım. Alternatifler (Trait, Generic).
- **Özyinelemeli Fonksiyonlar (Recursion)**: Tanım. Örnek.
- **Higher-Order Fonksiyonlar**: Tanım. Fonksiyon Parametre Olarak. Örnek.
- **Closure (Anonim Fonksiyon)**: Tanım. `||` Sözdizimi. Örnek.
  - **Closure ve Ortam Yakalama**: `Fn`, `FnMut`, `FnOnce`. Tanım. Farkları. Örnek.
  - **move Closure**: Tanım. Ownership Devri. Örnek.
- **Fonksiyon Pointer'ları**: `fn` Tipi. Tanım. Closure ile Farkı. Örnek.
 
---
 
### Rust : Trait'ler ve Generics
- **Trait Nedir?**: Tanım. Interface Benzeri Yapı. Kullanım Senaryoları.
- **Trait Tanımlama**: Tanım. Sözdizimi. Örnek.
- **Trait Implementasyonu**: `impl Trait for Type`. Tanım. Örnek.
- **Varsayılan Metod**: Tanım. Override. Örnek.
- **Derived Trait'ler**: `#[derive()]`. `Debug`, `Clone`, `Copy`, `PartialEq`, `Eq`, `Hash`. Örnek.
- **Trait Bound**: `T: Trait`. `where` Clause. Tanım. Örnek.
- **impl Trait Sözdizimi**: Parametrede ve Dönüş Tipinde. Tanım. Örnek.
- **Trait Objesi (dyn Trait)**: Tanım. Dynamic Dispatch. `Box<dyn Trait>`. Örnek.
- **Supertraits**: Tanım. Trait Kalıtımı. Örnek.
- **Generics Nedir?**: Tanım. Fonksiyonda. Struct'ta. Enum'da. Örnek.
- **Generic Fonksiyonlar**: Tanım. Monomorphization. Örnek.
- **Generic Struct ve Enum**: Tanım. Örnek.
- **Turbofish Sözdizimi**: `::<>`. Tanım. Örnek.
- **Yaygın Standart Trait'ler**: `Display`, `Debug`, `Default`, `From`, `Into`, `Iterator`, `Drop`. Tablo Halinde.
 
---
 
### Rust : İteratörler
- **Iterator Trait'i**: Tanım. `next()` Metodu. `Item` Associated Type. Örnek.
- **iter(), iter_mut(), into_iter()**: Farkları. Tablo Halinde. Örnek.
- **Iterator Adaptörleri (Lazy)**:
  - **map()**: Tanım. Örnek.
  - **filter()**: Tanım. Örnek.
  - **enumerate()**: Tanım. Örnek.
  - **zip()**: Tanım. Örnek.
  - **take() ve skip()**: Tanım. Örnek.
  - **chain()**: Tanım. Örnek.
  - **flat_map()**: Tanım. Örnek.
  - **peekable()**: Tanım. Örnek.
- **Tüketiciler (Consumers)**:
  - **collect()**: Tanım. Turbofish. Örnek.
  - **for_each()**: Tanım. Örnek.
  - **fold()**: Tanım. Örnek.
  - **sum() ve product()**: Tanım. Örnek.
  - **count()**: Tanım. Örnek.
  - **any() ve all()**: Tanım. Örnek.
  - **find()**: Tanım. Örnek.
  - **min() ve max()**: Tanım. Örnek.
- **Özel Iterator Yazma**: `impl Iterator for`. Tanım. Örnek.
 
---
 
### Rust : Akıllı Pointer'lar
- **Akıllı Pointer Nedir?**: Tanım. C++ ile Karşılaştırma. Kullanım Senaryoları.
- **Box<T>**: Tanım. Heap Allocation. Recursive Tipler. Örnek.
- **Rc<T>**: Tanım. Referans Sayımı (Reference Counting). Tek Thread. Örnek.
- **Arc<T>**: Tanım. Atomik Referans Sayımı. Multi-Thread. Örnek.
- **RefCell<T>**: Tanım. İç Değişkenlik (Interior Mutability). Çalışma Zamanı Borrowing. Örnek.
- **Cell<T>**: Tanım. Copy Tipler için İç Değişkenlik. Örnek.
- **Mutex<T>**: Tanım. Thread-Safe İç Değişkenlik. Örnek.
- **RwLock<T>**: Tanım. Çoklu Okuyucu, Tek Yazıcı. Örnek.
- **Cow<'a, B>**: Tanım. Clone on Write. Kullanım Senaryosu. Örnek.
- **Weak<T>**: Tanım. Döngüsel Referans Çözümü. Rc/Arc ile Kullanım. Örnek.
- **Deref ve DerefMut Trait'leri**: Tanım. Deref Coercion. Örnek.
- **Drop Trait'i**: Tanım. Kaynak Temizleme. RAII. Örnek.
 
---
 
### Rust : Bellek Yönetimi
- **Bellek Yönetimi Nedir?**: Stack vs Heap. Tanım. GC Olmadan Yönetim.
- **Memory Layout**: Programın RAM'deki Yapısı. Görselleştirme.
  - **Text Segment**: Kod. Salt Okunur. Tanım.
  - **Data Segment**: Static ve Const Değişkenler. Tanım.
  - **Stack**: Otomatik Ömürlü Değişkenler. Sabit Boyut. Tanım.
  - **Heap**: Dinamik Bellek. `Box`, `Vec`, `String`. Tanım.
- **Ownership ile Otomatik Bellek Yönetimi**: Tanım. Drop Mekanizması. Örnek.
- **std::mem Fonksiyonları**: `size_of`, `align_of`, `swap`, `replace`, `take`. Örnek.
- **ManuallyDrop**: Tanım. Drop Kontrolü. Örnek.
- **Pin ve Unpin**: Tanım. Self-Referential Struct. Async ile İlişkisi. Örnek.
- **Bellek Hataları Rust'ta Olmaz**: Dangling Pointer. Buffer Overflow. Use After Free. Derleyici Garantisi.
- **unsafe ile Bellek Yönetimi**: `unsafe` Bloğu. Ham Pointer (`*const T`, `*mut T`). Örnek.
 
---
 
### Rust : Modül Sistemi ve Crate'ler
- **Modül Sistemi Nedir?**: Tanım. Kod Organizasyonu. Kullanım Senaryoları.
- **mod Anahtar Kelimesi**: Tanım. Inline Modül. Dosya Modülü. Örnek.
- **Dosya Hiyerarşisi**: `mod.rs` vs `dosya_adi.rs`. 2018 Edition Değişikliği. Örnek.
- **pub Anahtar Kelimesi**: Tanım. Görünürlük. `pub(crate)`. `pub(super)`. Örnek.
- **use Anahtar Kelimesi**: Tanım. Yeniden İsimlendirme (`as`). Glob Import (`*`). Örnek.
- **Crate Nedir?**: Tanım. Binary vs Library Crate. Örnek.
- **Cargo.toml**: Tanım. [dependencies]. [dev-dependencies]. [features]. Örnek.
- **crates.io**: Tanım. Crate Yayınlama. Bağımlılık Yönetimi. Örnek.
- **Workspace**: Tanım. Çoklu Crate Projesi. Örnek.
- **Prelude**: Tanım. Otomatik İçe Aktarılan Tipler. Örnek.
 
---
 
### Rust : Dosya İşlemleri
- **Dosya İşlemleri Nedir?**
- **std::fs Modülü**: Tanım. Temel Fonksiyonlar. Örnek.
- **Dosya Okuma**: `fs::read_to_string`. `File::open`. `BufReader`. Örnek.
  > Metodları
- **Dosya Yazma**: `fs::write`. `File::create`. `BufWriter`. Örnek.
  > Metodları
- **Dosya Ekleme (Append)**: `OpenOptions`. Modlar. Örnek.
- **Satır Satır Okuma**: `BufRead`. `lines()`. Örnek.
- **Dosya Varlık Kontrolü**: `Path::exists()`. `metadata()`. Örnek.
- **Klasör İşlemleri**: `fs::create_dir_all`. `fs::remove_dir_all`. `fs::read_dir`. Örnek.
- **Dosya Kopyalama/Taşıma**: `fs::copy`. `fs::rename`. Örnek.
- **Path ve PathBuf**: Tanım. Platform Bağımsız Yol. `join()`. `extension()`. Örnek.
- **Geçici Dosyalar**: `tempfile` Crate'i. Tanım. Örnek.
- **JSON Dosyası**: JSON Nedir?
  - **JSON Mantığı**: Tanım. Yapısı.
  - **serde ve serde_json Crate'leri**: Tanım. Kurulum. `#[derive(Serialize, Deserialize)]`. Örnek.
  - **JSON Oluşturma**: Örnek.
  - **JSON Yazma**: Örnek.
  - **JSON Okuma**: Örnek.
- **TOML Dosyası**: TOML Nedir?
  - **TOML Mantığı**: Tanım. Yapısı. JSON ile Farkı.
  - **toml Crate'i**: Tanım. Kurulum. Örnek.
  - **TOML Okuma ve Yazma**: Örnek.
- **XML Dosyası**: XML Nedir?
  - **XML Mantığı**: Tanım. Yapısı.
  - **quick-xml Crate'i**: Tanım. Kurulum. Örnek.
  - **XML Okuma ve Yazma**: Örnek.
- **CSV Dosyası**: CSV Nedir?
  - **csv Crate'i**: Tanım. Kurulum. Örnek.
  - **CSV Okuma ve Yazma**: serde Entegrasyonu. Örnek.
- **Zstandard ile Sıkıştırılmış Dosyalar**: Tanım. Kullanım Senaryoları.
  - **Zstandard Nedir?**: zstd Crate'i. Kurulum. Örnek.
  - **Kompresyon**: `zstd::encode_all`. Sıkıştırma Seviyeleri (1-22). Örnek.
  - **Dekompresyon**: `zstd::decode_all`. Örnek.
  - **Streaming Kompresyon**: `zstd::stream::Encoder`. Büyük Dosyalar. Örnek.
  - **Streaming Dekompresyon**: `zstd::stream::Decoder`. Örnek.
  - **Dosyaya Sıkıştırarak Yazma**: `File` + `Encoder`. Örnek.
  - **Sıkıştırılmış Dosyayı Okuma**: `File` + `Decoder`. Örnek.
  - **Dictionary Kullanımı**: Tanım. Eğitim. `zstd::dict`. Örnek.
  - **.zst Formatı**: Tanım. CLI ile Uyumluluk. Örnek.
 
---
 
### Rust : Makrolar
- **Makro Nedir?**: Tanım. Fonksiyon ile Farkı. Metaprogramlama.
- **Declarative Makrolar (macro_rules!)**: Tanım. Pattern Matching. Örnek.
  - **Tekrarlama ($(...)\*)**: Tanım. Örnek.
  - **Fragment Specifier'lar**: `expr`, `ident`, `ty`, `tt`, `block`, `stmt`. Tablo Halinde.
- **Procedural Makrolar**: Tanım. Türleri. Kullanım Senaryoları.
  - **Derive Makroları**: `#[derive()]`. Tanım. Örnek.
  - **Attribute Makroları**: `#[...]`. Tanım. Örnek.
  - **Function-like Makroları**: Tanım. Örnek.
- **Yaygın Standart Makrolar**: `println!`, `vec!`, `format!`, `todo!`, `unimplemented!`, `dbg!`, `assert!`, `cfg!`. Tablo Halinde.
 
---
 
### Rust : Trait Objesi ve Dinamik Dispatch
- **Statik vs Dinamik Dispatch**: Tanım. Performans Farkı. Kullanım Senaryoları.
- **Monomorphization**: Tanım. Derleme Zamanı Kod Üretimi. Örnek.
- **dyn Trait**: Tanım. `Box<dyn Trait>`. `&dyn Trait`. vtable. Örnek.
- **Object Safety**: Tanım. Kurallar. Self: Sized. Örnek.
- **Trait Objesi vs Generic**: Karşılaştırma. Ne Zaman Hangisi? Tablo Halinde.
 
---
 
### Rust : Asenkron Programlama
- **Asenkron Nedir?**: Tanım. Senkron vs Asenkron. Kullanım Senaryoları.
- **Thread Nedir?**: Tanım. `std::thread::spawn`. `join()`. Örnek.
  - **Thread ile Veri Paylaşımı**: `Arc<Mutex<T>>`. `mpsc` Channel. Örnek.
  - **Mutex ve Deadlock**: Tanım. Örnek.
  - **std::sync::mpsc**: Tanım. `Sender`. `Receiver`. Örnek.
  - **crossbeam Channel**: Tanım. mpsc ile Farkı. Örnek.
- **Rayon Crate'i**: Tanım. Paralel İteratör. `par_iter()`. Örnek.
- **async/await**: Tanım. Future Trait'i. Örnek.
  - **async fn**: Tanım. Örnek.
  - **await**: Tanım. Örnek.
  - **.await Sözdizimi**: Tanım. Zincirleme. Örnek.
- **Tokio Runtime**: Tanım. Kurulum. `#[tokio::main]`. Örnek.
  - **tokio::spawn**: Tanım. Task Oluşturma. Örnek.
  - **tokio::select!**: Tanım. Çoklu Future Bekleme. Örnek.
  - **tokio::sync**: `Mutex`, `RwLock`, `Semaphore`, `Notify`. Örnek.
  - **tokio::time**: `sleep`, `interval`, `timeout`. Örnek.
  - **tokio::fs**: Asenkron Dosya İşlemleri. Örnek.
- **async-std**: Tanım. Tokio ile Karşılaştırma. Örnek.
- **Stream Trait'i**: Tanım. Asenkron İteratör. Örnek.
 
---
 
### Rust : Güvenlik ve Şifreleme
- **Güvenlik Nedir?**: Tanım. Rust'ın Bellek Güvenliği Garantisi.
- **unsafe Rust**: Tanım. Ne Zaman Gerekli? Beş unsafe Süper Güç. Örnek.
  - **Ham Pointer Dereference**: Tanım. Örnek.
  - **unsafe Fonksiyon Çağırma**: Tanım. Örnek.
  - **static mut Değişkene Erişim**: Tanım. Örnek.
  - **unsafe Trait Implementasyonu**: Tanım. `Send` ve `Sync`. Örnek.
- **FFI (Foreign Function Interface)**: Tanım. C ile Etkileşim. `extern "C"`. Örnek.
- **ring Crate'i**: Tanım. Kurulum. Örnek.
  - **Hashing**: SHA-256. SHA-512. Örnek.
  - **HMAC**: Tanım. Örnek.
  - **AES-GCM Şifreleme**: Tanım. Örnek.
- **rust-argon2 / bcrypt**: Parola Hashing. Tanım. Örnek.
- **rand Crate'i**: Rastgele Sayı Üretme. `thread_rng()`. `gen_range()`. Örnek.
 
---
 
### Rust : Log Sistemi
- **Loglama Nedir?**: Tanım. Kullanım Senaryoları.
- **log Crate'i**: Tanım. Facade Paterni. Örnek.
- **Log Seviyeleri**: `error!`, `warn!`, `info!`, `debug!`, `trace!`. Tanım.
- **env_logger Crate'i**: Tanım. `RUST_LOG` Ortam Değişkeni. Kurulum. Örnek.
- **tracing Crate'i**: Tanım. Yapısal Loglama. Span. Örnek.
  - **tracing-subscriber**: Tanım. Katmanlı Yapı. Örnek.
- **Dosyaya Loglama**: Tanım. `tracing-appender`. Örnek.
- **Basit Logger Yazma**: Tanım. `log::Log` Trait'i. Örnek.
 
---
 
### Rust : Veritabanı İşlemleri
- **Veritabanı Nedir?**: Tanım. Kullanım Senaryoları.
- **SQLite ile rusqlite**: Tanım. Kurulum. Örnek.
  - **Bağlantı Kurma**: `Connection::open`. Örnek.
  - **Tablo Oluşturma**: `execute`. Örnek.
  - **Veri Ekleme (INSERT)**: Tanım. Parametreli Sorgu. Örnek.
  - **Veri Sorgulama (SELECT)**: `query_map`. Örnek.
  - **Veri Güncelleme (UPDATE)**: Tanım. Örnek.
  - **Veri Silme (DELETE)**: Tanım. Örnek.
- **Diesel ORM**: Tanım. Kurulum. Migration. Örnek.
  - **Schema Tanımlama**: `table!` Makrosu. Örnek.
  - **CRUD İşlemleri**: Tanım. Örnek.
- **SQLx**: Tanım. Async Veritabanı. Compile-Time Query Doğrulama. Örnek.
- **PostgreSQL Bağlantısı**: `tokio-postgres`. Tanım. Örnek.
 
---
 
### Rust : HTTP ve Web
- **HTTP Nedir?**: Tanım. Kullanım Senaryoları.
- **reqwest Crate'i (Client)**: Tanım. Kurulum. Örnek.
  - **GET İsteği**: Tanım. `blocking` vs `async`. Örnek.
  - **POST İsteği**: Tanım. JSON Gönderme. Örnek.
  - **Header Yönetimi**: Tanım. Örnek.
  - **Timeout ve Retry**: Tanım. Örnek.
- **actix-web (Server)**: Tanım. Kurulum. Örnek.
  - **Route Tanımlama**: `#[get]`, `#[post]`. Örnek.
  - **JSON Yanıt**: Tanım. serde Entegrasyonu. Örnek.
  - **Middleware**: Tanım. Örnek.
- **axum (Server)**: Tanım. Tower Ekosistemi. Tokio Tabanlı. Örnek.
  - **Router**: Tanım. Örnek.
  - **Handler Fonksiyonlar**: Tanım. Extractor. Örnek.
  - **State Paylaşımı**: `Extension`. `State`. Örnek.
- **warp (Server)**: Tanım. Filter Tabanlı. Örnek.
 
---
 
### Rust : Ağ (Network) Programlama
- **Socket Nedir?**: Tanım. Kullanım Senaryoları.
- **TCP vs UDP**: Farkları. Tablo Halinde.
- **std::net ile TCP**:
  - **TcpListener**: Tanım. `bind`. `incoming`. Örnek.
  - **TcpStream**: Tanım. `connect`. `read`. `write`. Örnek.
- **std::net ile UDP**:
  - **UdpSocket**: Tanım. `send_to`. `recv_from`. Örnek.
- **tokio::net**: Asenkron TCP/UDP. Tanım. Örnek.
- **Çok İstemcili Server**: Thread veya Async ile. Örnek.
- **WebSocket**: `tungstenite` Crate'i. `tokio-tungstenite`. Örnek.
 
---
 
### Rust : Test Sistemi
- **Test Nedir?**: Tanım. Önemi. Kullanım Senaryoları.
- **Unit Test**: `#[test]` Attribute. `#[cfg(test)]` Modülü. Örnek.
- **assert Makroları**: `assert!`, `assert_eq!`, `assert_ne!`. Örnek.
- **should_panic**: `#[should_panic]` Attribute. Tanım. Örnek.
- **Result Döndüren Testler**: `Result<(), Box<dyn Error>>`. Örnek.
- **Integration Test**: `tests/` Klasörü. Tanım. Örnek.
- **Doc Test**: `///` İçindeki Kod Blokları. Tanım. Örnek.
- **cargo test**: Tanım. Filtreleme. `--nocapture`. `--test-threads`. Örnek.
- **Test Organizasyonu**: Yardımcı Fonksiyonlar. `mod common`. Örnek.
- **Benchmark**: `criterion` Crate'i. Tanım. Örnek.
- **Mocking**: `mockall` Crate'i. Tanım. Örnek.
 
---
 
### Rust : Cargo ve Build Sistemi
- **Cargo Nedir?**: Tanım. Paket Yöneticisi ve Build Aracı. Kullanım Senaryoları.
- **Cargo Komutları**: `new`, `build`, `run`, `test`, `check`, `doc`, `publish`, `update`. Tablo Halinde.
- **Cargo.toml Detaylı**: [package]. [dependencies]. [features]. [profile]. Örnek.
- **Feature Flag'ler**: Tanım. Koşullu Derleme. `#[cfg(feature = "...")]`. Örnek.
- **Build Script (build.rs)**: Tanım. Derleme Öncesi Kod Çalıştırma. Örnek.
- **cargo clippy**: Tanım. Lint Kuralları. Örnek.
- **cargo fmt**: Tanım. Kod Formatlama. rustfmt.toml. Örnek.
- **cargo doc**: Tanım. Dokümantasyon Üretme. Örnek.
- **Cross Compilation**: Tanım. Target Ekleme. Örnek.
 
---
 
## Ratatui (Terminal UI)
 
### Ratatui : Giriş
- **Ratatui Nedir?**: Tanım. Terminal Tabanlı UI. Kullanım Alanları. Neden Ratatui?
  - **TUI vs GUI**: Farkları. Avantajlar. Kullanım Senaryoları.
  - **tui-rs ile İlişkisi**: Tarihçe. Fork. Aktif Geliştirme.
  - **Diğer TUI Kütüphaneleri ile Karşılaştırma**: cursive, termion. Tablo Halinde.
  - **Lisanslama**: MIT.
- **Ratatui Kurulumu**:
  - **Cargo.toml Yapılandırması**: `ratatui`. `crossterm` Backend. Örnek.
  - **Backend Seçimi**: crossterm vs termion vs termwiz. Farkları. Tablo Halinde.
  - **İlk Ratatui Projesi**: Terminal Başlatma. Çerçeve Çizme. Temizleme. Örnek.
- **Ratatui Temel Yapısı**: `Terminal`. `Frame`. `Widget` Trait'i. Render Döngüsü. Örnek.
- **Uygulama Yaşam Döngüsü**: `setup()`. `run()`. `restore()`. Panic Handler. Örnek.

---

### Ratatui : Terminal ve Backend
- **crossterm Backend**: Tanım. Platform Bağımsız. Kurulum. Örnek.
  - **Terminal Başlatma**: `enable_raw_mode()`. `EnterAlternateScreen`. Örnek.
  - **Terminal Kapatma**: `disable_raw_mode()`. `LeaveAlternateScreen`. Örnek.
  - **Raw Mode Nedir?**: Tanım. Normal Mode ile Farkı. Örnek.
- **Alternate Screen**: Tanım. Ana Ekranı Koruma. Örnek.
- **Terminal Boyutu**: `terminal.size()`. Dinamik Boyut Algılama. Örnek.
- **Mouse Desteği**: `EnableMouseCapture`. `DisableMouseCapture`. Örnek.

---

### Ratatui : Temel Widget'lar
- **Widget Trait'i**: Tanım. `render()` Metodu. `Rect`. Örnek.
- **Block**: Tanım. Kenarlık. Başlık. `Borders`. `BorderType`. Örnek.
  > Metodları
- **Paragraph**: Tanım. Metin Gösterme. Sarmalama (Wrap). Kaydırma (Scroll). Örnek.
  > Metodları
- **List**: Tanım. `ListItem`. Seçilebilir Liste. `ListState`. Örnek.
  > Metodları
- **Table**: Tanım. Sütunlar. Satırlar. `Row`. `Cell`. `TableState`. Örnek.
  > Metodları
- **Tabs**: Tanım. Sekme Navigasyonu. `Tabs::new()`. Örnek.
  > Metodları
- **Gauge**: Tanım. İlerleme Çubuğu. Yüzde. `Gauge::default()`. Örnek.
  > Metodları
- **LineGauge**: Tanım. Satır İçi İlerleme. Örnek.
- **Sparkline**: Tanım. Mini Grafik. Veri Görselleştirme. Örnek.
- **BarChart**: Tanım. Çubuk Grafik. `Bar`. `BarGroup`. Örnek.
  > Metodları
- **Chart**: Tanım. Çizgi Grafik. `Dataset`. `Axis`. Örnek.
  > Metodları
- **Canvas**: Tanım. Serbest Çizim Alanı. Şekiller. `Painter`. Örnek.
- **Clear**: Tanım. Alan Temizleme. Örnek.
- **Scrollbar**: Tanım. `ScrollbarState`. Dikey/Yatay. Örnek.
  > Metodları

---

### Ratatui : Layout Yönetimi
- **Layout Nedir?**: Tanım. Terminal'de Alan Bölme.
- **Layout::default()**: Tanım. Yön Belirleme. Kısıtlar. Örnek.
- **Direction**: `Direction::Horizontal`. `Direction::Vertical`. Örnek.
- **Constraint Tipleri**: Tanım. Esnek Boyutlandırma.
  - **Constraint::Percentage()**: Yüzde Tabanlı. Örnek.
  - **Constraint::Length()**: Sabit Uzunluk. Örnek.
  - **Constraint::Min() / Max()**: Minimum/Maksimum. Örnek.
  - **Constraint::Ratio()**: Oran Tabanlı. Örnek.
  - **Constraint::Fill()**: Kalan Alanı Doldurma. Örnek.
- **İç İçe Layout**: Tanım. Karmaşık Düzenler. Örnek.
- **Rect**: Tanım. Alan Tanımı. `x`, `y`, `width`, `height`. Örnek.
- **Margin**: Tanım. `inner()`. Kenar Boşlukları. Örnek.
- **Flex**: Tanım. `Flex::Start`. `Flex::Center`. `Flex::End`. `Flex::SpaceBetween`. Örnek.

---

### Ratatui : Stil ve Renklendirme
- **Style**: Tanım. `Style::default()`. Zincirleme. Örnek.
- **Renk (Color)**: Tanım. `Color::Red`. `Color::Rgb()`. `Color::Indexed()`. ANSI 256. Örnek.
- **Foreground ve Background**: `.fg()`. `.bg()`. Örnek.
- **Modifier'lar**: `Modifier::BOLD`. `ITALIC`. `UNDERLINED`. `REVERSED`. `DIM`. `CROSSED_OUT`. Örnek.
- **Span**: Tanım. Stillendirilmiş Metin Parçası. Örnek.
- **Line**: Tanım. Birden Fazla Span. Birleştirme. Örnek.
- **Text**: Tanım. Birden Fazla Line. Çok Satırlı Metin. Örnek.
- **Styled Widget'lar**: `.style()`. `.highlight_style()`. Seçili Eleman Stili. Örnek.
- **Tema Sistemi Yazma**: Tanım. Renk Paleti Struct'ı. Özel Tema. Örnek.

---

### Ratatui : Olay Yönetimi (Event Handling)
- **crossterm Event Sistemi**: Tanım. `event::read()`. `event::poll()`. Örnek.
- **KeyEvent**: Tanım. `KeyCode`. `KeyModifiers`. Tuş Algılama. Örnek.
  - **Karakter Tuşları**: `KeyCode::Char('q')`. Örnek.
  - **Özel Tuşlar**: `KeyCode::Enter`. `Esc`. `Tab`. `Backspace`. Örnek.
  - **Modifier ile Kombinasyon**: `Ctrl+C`. `Alt+Tab`. Örnek.
- **MouseEvent**: Tanım. `MouseEventKind`. Tıklama. Kaydırma. Örnek.
- **Resize Event**: Tanım. Terminal Boyut Değişikliği. Örnek.
- **Event Loop Paterni**: Tanım. Polling vs Blocking. `Duration`. Örnek.
- **Olay Tabanlı Mimari**: Tanım. Mesaj Kuyruğu. `mpsc` ile Event Channel. Örnek.

---

### Ratatui : Uygulama Mimarisi
- **App Struct Paterni**: Tanım. Uygulama Durumu. `App` Struct'ı. Örnek.
- **MVC / Elm Mimarisi**: Tanım. Model-View-Update. Ratatui'de Uygulama. Örnek.
- **State Yönetimi**: Tanım. Uygulama Modu. Sayfa Geçişi. Örnek.
  - **ListState**: Tanım. Seçili İndeks. Navigasyon. Örnek.
  - **TableState**: Tanım. Satır Seçimi. Sıralama. Örnek.
  - **ScrollbarState**: Tanım. Kaydırma Konumu. Örnek.
- **Component Paterni**: Tanım. Widget'ı Struct'a Sarma. `render()` ve `handle_event()`. Örnek.
- **Action / Message Paterni**: Tanım. Enum ile Aksiyonlar. `update()`. Örnek.
- **Popup ve Modal Diyalog**: Tanım. Katmanlı Render. `Clear` Widget. Örnek.
- **Async Entegrasyonu**: Tanım. Tokio ile Event Loop. Arka Plan Görevleri. Örnek.

---

### Ratatui : Gelişmiş Özellikler
- **Stateful Widget**: `StatefulWidget` Trait'i. Tanım. Kendi Widget'ını Yazma. Örnek.
- **Özel Widget Oluşturma**: `impl Widget for`. Render Mantığı. `Buffer`. Örnek.
- **Buffer Manipülasyonu**: `Buffer::empty()`. `set_string()`. `get_mut()`. Örnek.
- **Animasyon**: Tanım. Frame Sayacı. Zamanlayıcı ile Güncelleme. Örnek.
- **Renkli Loglar Gösterme**: `tui-logger` Crate'i. Tanım. Örnek.
- **Dosya Gezgini Yapma**: Tanım. `std::fs` ile Dosya Listesi. Navigasyon. Örnek.
- **Metin Editörü Yapma**: Tanım. `tui-textarea` Crate'i. Cursor Yönetimi. Örnek.
- **Üçüncü Parti Widget'lar**: `tui-input`. `tui-tree-widget`. `tui-big-text`. Tablo Halinde.
 
---
 
## Axum (Web Framework)
 
### Axum : Giriş
- **Axum Nedir?**: Tanım. Tokio Ekosistemi. Tower Tabanlı. Neden Axum?
  - **Kısa Tarihçesi**: Tokio Takımı. İlk Sürüm.
  - **Diğer Rust Web Framework'leri ile Karşılaştırma**: actix-web, warp, rocket. Tablo Halinde.
  - **Lisanslama**: MIT.
- **Axum Kurulumu**:
  - **Cargo.toml Yapılandırması**: `axum`, `tokio`, `serde`. Örnek.
  - **İlk Axum Projesi**: `Router::new()`. `axum::serve`. `#[tokio::main]`. Örnek.
- **Axum Proje Yapısı**: Modüler Mimari. Klasör Düzeni. Örnek.
- **Tokio ile İlişkisi**: Tanım. async Runtime Gereksinimi. Örnek.

---

### Axum : Router ve Route Tanımlama
- **Router Nedir?**: Tanım. `Router::new()`. Örnek.
- **Route Tanımlama**: `.route()`. Yol Desenleri. Örnek.
- **HTTP Metod Fonksiyonları**: `get()`, `post()`, `put()`, `patch()`, `delete()`. Örnek.
- **Dinamik Route Parametreleri**: `Path<T>`. `/users/:id`. Örnek.
- **Query Parametreleri**: `Query<T>`. `?key=value`. Örnek.
- **Wildcard ve Catch-All**: `/*path`. Tanım. Örnek.
- **Route Gruplama**: `.nest()`. Prefix ile Alt Router. Örnek.
- **Route Birleştirme**: `.merge()`. Modüler Router. Örnek.
- **Fallback Handler**: `.fallback()`. 404 Sayfası. Örnek.
- **Method Routing**: `method_router`. `on()`. Birden Fazla Metod. Örnek.

---

### Axum : Handler Fonksiyonlar
- **Handler Nedir?**: Tanım. async Fonksiyon. Örnek.
- **Response Dönüş Tipleri**: `String`. `Html`. `Json<T>`. `StatusCode`. `impl IntoResponse`. Örnek.
- **IntoResponse Trait'i**: Tanım. Özel Response. Tuple ile Durum Kodu. Örnek.
- **Hata Döndürme**: `Result<T, E>`. Hata Tipi Tasarımı. Örnek.
- **Handler Fonksiyonlarda Kısıtlar**: Tanım. `Send` + `'static`. Örnek.

---

### Axum : Extractor'lar
- **Extractor Nedir?**: Tanım. Request'ten Veri Çıkarma. Kullanım Senaryoları.
- **Path Extractor**: `Path<(String, u32)>`. Tanım. Örnek.
- **Query Extractor**: `Query<Params>`. Tanım. serde ile. Örnek.
- **Json Extractor**: `Json<T>`. Request Body. serde ile. Örnek.
- **Form Extractor**: `Form<T>`. URL-Encoded Body. Örnek.
- **Header Extractor**: `TypedHeader`. `HeaderMap`. Örnek.
- **State Extractor**: `State<T>`. Uygulama Durumu. Örnek.
- **Extension Extractor**: `Extension<T>`. Middleware'den Veri. Örnek.
- **Body Extractor**: `Bytes`. `String`. Ham Body Okuma. Örnek.
- **Multipart Extractor**: `Multipart`. Dosya Yükleme. Örnek.
- **Özel Extractor Yazma**: `#[async_trait]`. `FromRequestParts`. `FromRequest`. Örnek.
- **Extractor Sıralaması**: Tanım. Body Tüketen Extractor Son Olmalı. Kural.

---

### Axum : Middleware
- **Middleware Nedir?**: Tanım. Request/Response Pipeline. Kullanım Senaryoları.
- **Tower Katmanları (Layer)**:
  - **Tower Nedir?**: Tanım. `Service` Trait'i. Axum ile Entegrasyonu.
  - **CorsLayer**: CORS Ayarları. `tower-http`. Örnek.
  - **TraceLayer**: İstek Loglama. `tower-http`. `tracing` ile. Örnek.
  - **CompressionLayer**: Gzip/Brotli/Zstd Sıkıştırma. Örnek.
  - **TimeoutLayer**: İstek Zaman Aşımı. Örnek.
  - **RateLimitLayer**: Hız Sınırlama. Örnek.
- **axum::middleware::from_fn**: Tanım. Fonksiyon Tabanlı Middleware. `next.run(request)`. Örnek.
- **axum::middleware::map_request**: Tanım. İstek Dönüşümü. Örnek.
- **axum::middleware::map_response**: Tanım. Yanıt Dönüşümü. Örnek.
- **Route Bazlı Middleware**: `.route_layer()`. Belirli Route'lara Uygulama. Örnek.
- **Özel Middleware Yazma**: Tower `Service` Implementasyonu. Örnek.
- **Middleware Sırası**: Tanım. Uygulama Sırası. Yığın (Stack) Modeli. Örnek.

---

### Axum : State Yönetimi
- **Application State Nedir?**: Tanım. Paylaşımlı Veri. Kullanım Senaryoları.
- **State ile Paylaşım**: `Router::with_state()`. `State<T>`. `Clone` Gereksinimi. Örnek.
- **Arc ile State**: `Arc<AppState>`. Thread-Safe Paylaşım. Örnek.
- **Arc<Mutex<T>> ile Değiştirilebilir State**: Tanım. Dikkat Edilecekler. Örnek.
- **Veritabanı Havuzu (Connection Pool)**: `sqlx::Pool`. `deadpool`. State Olarak. Örnek.
- **Birden Fazla State**: Tanım. Alt State. `FromRef` Derive. Örnek.
- **Extension ile State**: `.layer(Extension(...))`. Eski Yöntem. Örnek.

---

### Axum : JSON API Geliştirme
- **RESTful API Nedir?**: Tanım. Prensipleri. Kaynak Yapısı.
- **CRUD Endpoint'leri**: Create. Read. Update. Delete. Tam Örnek.
- **Request Doğrulama (Validation)**: `validator` Crate'i. `#[validate]`. Örnek.
- **Hata Yönetimi**: Özel Error Tipi. `IntoResponse`. HTTP Durum Kodları. Örnek.
  - **anyhow ile Entegrasyon**: Tanım. Örnek.
  - **thiserror ile Entegrasyon**: Tanım. Hata Dönüştürme. Örnek.
- **Pagination**: Tanım. `Query` ile Sayfa/Limit. Örnek.
- **Seri Hale Getirme/Çözme**: serde. `#[serde(rename_all)]`. `#[serde(skip)]`. Örnek.
- **API Versiyonlama**: `/api/v1/`. Nest ile. Örnek.
- **Response Envelope**: Tanım. Standart JSON Yapısı. `ApiResponse<T>`. Örnek.

---

### Axum : Kimlik Doğrulama ve Yetkilendirme
- **Authentication Nedir?**: Tanım. Kullanım Senaryoları.
- **JWT (JSON Web Token)**:
  - **JWT Nedir?**: Tanım. Header. Payload. Signature.
  - **jsonwebtoken Crate'i**: Tanım. Kurulum. Örnek.
  - **Token Oluşturma**: `encode()`. Claims Struct. Expire. Örnek.
  - **Token Doğrulama**: `decode()`. Middleware ile. Örnek.
  - **Auth Middleware**: Tanım. `Authorization` Header. Bearer Token. Örnek.
- **Session Tabanlı Auth**: `tower-sessions`. Tanım. Örnek.
- **OAuth2**: `oauth2` Crate'i. Tanım. Akış. Örnek.
- **Password Hashing**: `argon2`. `bcrypt`. Kayıt ve Giriş. Örnek.
- **Role-Based Access Control (RBAC)**: Tanım. Middleware ile. Örnek.

---

### Axum : Veritabanı Entegrasyonu
- **SQLx ile Axum**: Tanım. Async. Compile-Time Doğrulama. Örnek.
  - **Connection Pool**: `sqlx::PgPool`. `SqlitePool`. State Olarak. Örnek.
  - **Migration**: `sqlx::migrate!`. Tanım. Örnek.
  - **CRUD İşlemleri**: `query_as!`. `query!`. Örnek.
- **Diesel ile Axum**: Tanım. Senkron ORM. `r2d2` Pool. Örnek.
- **SeaORM ile Axum**: Tanım. Async ORM. Entity. Örnek.
- **Redis Entegrasyonu**: `redis` Crate'i. Cache. Session Store. Örnek.

---

### Axum : Statik Dosya ve Template
- **Statik Dosya Sunma**: `tower-http::ServeDir`. Public Klasörü. Örnek.
- **ServeFile**: Tek Dosya Sunma. `index.html`. Örnek.
- **Template Engine'ler**:
  - **Askama**: Tanım. Derleme Zamanı Template. `#[derive(Template)]`. Örnek.
  - **Tera**: Tanım. Jinja2 Benzeri. Dinamik Template. Örnek.
  - **Minijinja**: Tanım. Hafif Template. Örnek.
- **HTML Response**: Tanım. `Html<String>`. Örnek.
- **SPA (Single Page Application) Desteği**: Tanım. Fallback ile. React/Vue. Örnek.

---

### Axum : WebSocket
- **WebSocket Nedir?**: Tanım. HTTP ile Farkı. Kullanım Senaryoları.
- **Axum WebSocket Desteği**: `axum::extract::ws`. Tanım. Örnek.
- **WebSocket Upgrade**: `WebSocketUpgrade`. `on_upgrade`. Örnek.
- **Mesaj Gönderme ve Alma**: `Message::Text`. `Message::Binary`. `send()`. `recv()`. Örnek.
- **Broadcast**: Tanım. `tokio::sync::broadcast`. Tüm Bağlantılara Yayın. Örnek.
- **Chat Uygulaması**: Tanım. Tam Örnek. Paylaşımlı State. Örnek.
- **Ping/Pong**: Tanım. Bağlantı Canlılığı. Örnek.

---

### Axum : SSE (Server-Sent Events)
- **SSE Nedir?**: Tanım. WebSocket ile Farkı. Tek Yönlü Akış.
- **Sse Response**: `axum::response::Sse`. Tanım. Örnek.
- **Event Stream**: `Event::default()`. `.data()`. `.event()`. `.id()`. Örnek.
- **Tokio Channel ile SSE**: `broadcast::Receiver`. Gerçek Zamanlı Güncelleme. Örnek.
- **Keep-Alive**: Tanım. Bağlantı Düşmesini Önleme. Örnek.

---

### Axum : Test Sistemi
- **Axum Test Nedir?**: Tanım. Entegrasyon Testi. Kullanım Senaryoları.
- **axum::test**: `TestClient`. Tanım. Örnek.
- **tower::ServiceExt**: `oneshot()`. `ready()`. Direkt Service Testi. Örnek.
- **Request Oluşturma**: `Request::builder()`. Body. Header. Örnek.
- **Response Doğrulama**: `StatusCode`. Body Okuma. JSON Parse. Örnek.
- **Mock Veritabanı**: Tanım. Test için In-Memory DB. Örnek.
- **Test Yardımcıları**: Ortak Setup. `TestApp` Struct'ı. Örnek.

---

### Axum : Performans ve Dağıtım
- **Graceful Shutdown**: `tokio::signal`. `Ctrl+C`. Tanım. Örnek.
- **Konfigürasyon Yönetimi**: `config` Crate'i. `.env`. Ortam Değişkenleri. Örnek.
- **Loglama ve İzleme**: `tracing`. `tracing-subscriber`. Yapısal Log. Örnek.
- **Health Check Endpoint**: `/health`. Veritabanı Kontrolü. Örnek.
- **Docker ile Dağıtım**: `Dockerfile`. Multi-Stage Build. Optimizasyon. Örnek.
- **HTTPS / TLS**: `axum-server`. `rustls`. Sertifika. Örnek.
- **Rate Limiting**: `tower-governor`. Tanım. Örnek.
- **CORS Yapılandırması**: `CorsLayer`. Detaylı Ayarlar. Örnek.
- **Reverse Proxy Arkasında**: `X-Forwarded-For`. Proxy Header. Örnek.
- **Benchmark**: `wrk`. `hey`. Performans Testi. Örnek.

---

### Sonsöz
- **Bu Dokümantasyonda Ne Öğrendik**
- **İlerki Projeler**
- **Diğer Data's Books Dökümantasyonları**
- **Özel Teşekkürler**

---
