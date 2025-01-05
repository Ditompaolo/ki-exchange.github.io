<!DOCTYPE html>
<html lang="de">
<head>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-rbsA2VBKQhggwzxH7pPCaAqO46MgnOM80zW1RWuH61DGLwZJEdK2Kadq2F9CUG65" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.15.1/devicon.min.css">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Markdown Anzeige</title>
    <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <title>KI-exchange, KI/AI Austauschforum</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        </nav>
        <nav class="navbar navbar-dark navbar-expand-lg bg-dark ">
    <div class="container-fluid">
        <div class="mx-4">
            <img src="KIexchange_01.png" alt="Logo" >
        </div>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
            data-bs-target="#navbarTogglerDemo02" aria-controls="navbarTogglerDemo02" aria-expanded="false"
            aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li class="nav-item"> 
                    <a class="nav-link" href="goform_kontaktdaten.html">Google-Umfrage</a>
                </li>
            </ul>
        </div>
    </div>
    </nav>
    </header>
    <main>
    </nav>
    <div class="container my-4 ">
        <div class="row justify-content-center">
            <div class="col-lg mx-2 align-self-center">
                <div class="my-3">
                    <script>
                        const files = ['beschreibung.md', 'tuchschmidhuus.md'];
                
                        function loadMarkdown(file) {
                            return $.ajax({
                                url: file,
                                dataType: 'text'
                            });
                        }
                                        Promise.all(files.map(loadMarkdown))
                            .then(contents => {
                                const html = contents.map(content => marked.parse(content)).join('<hr>');
                                $('#content').html(html);
                                })
                                .catch(error => console.error('Fehler beim Laden der Markdown-Dateien:', error));
                    </script> 
                        <img src="im-beschr/20240914_Tuchschmidhuus.png" alt="tuchschmidhuus" width="300" height="200">
                        <script>
                            // Funktion zum Laden und Anzeigen des Markdown-Inhalts
                            function loadMarkdown() {
                            fetch('tuchschmidhuus.md')
                                    .then(response => response.text())
                                    .then(text => {
                                    document.getElementById('content').innerHTML = marked.parse(text);
                                    })
                                    .catch(error => console.error('Fehler beim Laden der Markdown-Datei:', error));
                            }
                                            // Laden Sie den Markdown-Inhalt, wenn die Seite geladen ist
                            window.onload = loadMarkdown;
                    </script> 
                </div>
            </div> 
        <div id="content"></div>
    </nav>
    <div class="container my-4 ">
        <div class="row justify-content-center">
            <div class="col-lg mx-2 align-self-center">
            <p>Ihre Meinung ist mir wichtig! Daher bitte ich Sie höflich mir Ihr Feedback mittels Umfrage zu geben.</p>
            <p>Klicken Sie dafür auf den Button "Umfrage öffnen":</p>
                <button onclick="window.open('https://docs.google.com/forms/d/13a-3H141T2XXf3bOBnJJApaeMSSuped4WbY1ginzJA0/edit', '_blank')">
                    Umfrage öffnen
                </button>
            <br><br>
            <p>Für mehr Informationen schreiben Sie eine Mail an:</p><address><a href="mailto:info@di-tommaso.site">info@di-tommaso.site</a><br /></address>
            </div>
        </div> 
    <footer>
        <div class="container my-4 ">
            <div class="row justify-content-center">
                <div class="col-lg mx-2 align-self-center">
                    <div class="my-3">
                        <p>&copy; 2024 KI-Exchange</p>
                            <nav
                            <ul>
                            <a href="Impressum.md">Impressum</a>
                            </ul>
                            </nav>
                    </div>
                </div>    
        </footer>
    <script src="js/script.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-kenU1KFdBIe4zVF0s0G1M5b4hcpxyD9F7jL+jjXkk+Q2h455rYXK/7HAuoJl+0I4" crossorigin="anonymous"></script>
</body>
</html>  