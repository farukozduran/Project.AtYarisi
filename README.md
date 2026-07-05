# Project.AtYarisi API 🐎

At yarışları ile ilgili verilerin yönetilmesini sağlayan, ASP.NET Core Web API kullanılarak geliştirilmiş bir RESTful API projesidir. Sistem; atlar, jokeyler, hipodromlar ve sponsorlar gibi temel at yarışı unsurlarının yönetimini (CRUD işlemleri) sağlar.

## 🚀 Özellikler

*   **At Yönetimi (Horses):** Sisteme at ekleme, listeleme, güncelleme ve silme.
*   **Jokey Yönetimi (Jockeys):** Jokey bilgilerinin kaydedilmesi ve yönetimi.
*   **Hipodrom Yönetimi (Racecourses):** Yarışların yapıldığı hipodromların sisteme tanımlanması.
*   **Sponsor Yönetimi (Sponsors):** Yarışlara veya atlara sponsor olan kurum/kişilerin yönetimi.
*   Entity Framework Core ile Code-First yaklaşımı kullanılarak veritabanı yönetimi.
*   REST standartlarına uygun mimari.

## 🛠 Kullanılan Teknolojiler

*   **Backend Framework:** ASP.NET Core Web API (.NET)
*   **ORM:** Entity Framework Core
*   **Programlama Dili:** C#

## 📂 Proje Yapısı

*   `Controllers/`: API isteklerini karşılayan yönlendirici sınıflar (Horses, Jockeys, Racecourses, Sponsors).
*   `Models/`: Veritabanı tablolarına karşılık gelen varlık (entity) sınıfları.
*   `Data/`: Entity Framework Core veritabanı bağlamı (`ApplicationDbContext`).
*   `Migrations/`: Veritabanı şema güncellemeleri.

## ⚙️ Kurulum ve Çalıştırma

Projeyi yerel ortamınızda çalıştırmak için aşağıdaki adımları izleyebilirsiniz:

1.  **Depoyu Klonlayın:**
    ```bash
    git clone <repo-url>
    cd Project.AtYarisi/Project.AtYarisi.API
    ```

2.  **Veritabanı Bağlantı Dizesini Ayarlayın:**
    `appsettings.json` veya `appsettings.Development.json` dosyası içerisindeki `ConnectionStrings` ayarını kendi SQL Server (veya kullandığınız veritabanı) bilgilerinize göre güncelleyin.

3.  **Migration İşlemlerini Uygulayın:**
    Veritabanını oluşturmak için Package Manager Console (PMC) veya .NET CLI üzerinden aşağıdaki komutu çalıştırın:
    ```bash
    dotnet ef database update
    ```
    *(Not: Eğer `ef` aracı yüklü değilse öncelikle `dotnet tool install --global dotnet-ef` komutu ile yükleyebilirsiniz.)*

4.  **Projeyi Çalıştırın:**
    ```bash
    dotnet run
    ```
    Uygulama çalıştıktan sonra tarayıcınızdan `https://localhost:<port>/swagger` (Swagger yapılandırılmışsa) adresine giderek API uç noktalarını inceleyebilir ve test edebilirsiniz.

## 🌐 Temel API Uç Noktaları

Uygulama genel olarak aşağıdaki rotalara (route) sahiptir (HTTP GET, POST, PUT, DELETE metodları desteklenmektedir):

*   `/api/Horses`
*   `/api/Jockeys`
*   `/api/Racecourses`
*   `/api/Sponsors`

## 🤝 Katkıda Bulunma

Geliştirmelere destek olmak isterseniz pull request gönderebilir veya issue açabilirsiniz.
