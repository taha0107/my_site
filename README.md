# my_site<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Silinemez İçerik Sayfası</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #333;
            color: white;
            padding: 20px;
            text-align: center;
        }

        main {
            padding: 20px;
            text-align: center;
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            width: 100%;
            bottom: 0;
        }

        .content {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
            font-size: 1.2em;
        }

        /* İçeriği düzenlemeyi zorlaştıran stil */
        .content div {
            pointer-events: none; /* Tıklanmasını engeller */
            user-select: none;    /* Seçilmesini engeller */
        }

        /* Silinemez içerik için özel stil */
        .content div.silinemez {
            background-color: #eaeaea;
            border: 2px dashed #888;
        }
    </style>
</head>
<body>
    <header>
        <h1>Web Sitenize Hoş Geldiniz!</h1>
    </header>

    <main>
        <div class="content">
            <div class="silinemez">
                <h2>Silinemez İçeriğiniz</h2>
                <p>Bu içerik, sayfa kaynağından düzenlenmeye çalışılsa da, kolayca silinemez. Ancak, içerik üzerinde değişiklik yapılabilir. Bu bir güvenlik önlemi değildir, sadece düzenlemeyi zorlaştırmak içindir.</p>
                <p>İstediğiniz metni buraya yazabilirsiniz. Bu alan, kullanıcıların yanlışlıkla veya kasıtlı olarak silmesini engellemek için tasarlanmıştır.</p>
            </div>
        </div>
    </main>

    <footer>
        <p>© 2025 - Silinemez İçerik Sayfası</p>
    </footer>

    <script>
        // JavaScript ile içerik düzenlemesini engellemek için ek önlemler
        document.querySelector('.silinemez').addEventListener('contextmenu', function(event) {
            event.preventDefault(); // Sağ tıklamayı engeller
            alert("İçerik düzenlenemez!");
        });

        // Kullanıcının içerik üzerinde değişiklik yapmasını engelleyen ek kod
        document.querySelector('.silinemez').contentEditable = 'false'; // İçerik düzenlemesini engeller
    </script>
</body>
</html>
