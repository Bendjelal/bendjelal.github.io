---
layout: page
order: 1
---

<head>
    <meta charset="UTF-8">
    <meta name="photo" content="width=device-width, initial-scale=1.0">
    <style>
        .circular-photo {
            width: 250px; /* Ajustez la taille selon vos préférences */
            height: 250px; /* Ajustez la taille selon vos préférences */
            border-radius: 100%;
            overflow: hidden;
            display: block;
            margin-left: auto;
            margin-right: auto;
            margin-top: auto;
            margin-bottom: auto;
        }
    </style>
</head>



Médecin et chercheur, je viens de terminer le second cycle de mes études de Médecine.

En médecine, je m'intéresse à l'allergologie et à la chirurgie ORL.

En recherche, je m'intéresse à l'analyse de données à grande échelle et au machine learning, en particulier par le développement du machine learning interprétable pour la santé.

# Nouveautés

* **Juillet 2024** : Elu VP Informatique de l'Association Nationale des Doubles Cursus en Santé (ANDCS)
  
* **Juin 2024** : Nommé Président du Collectif Interfacultaire Représentant les Externes en Médecine (CIREM)
  
* **Mai 2024** : Fin du deuxième cycle des études médicales

# Formations

**2024 :** Diplôme de Formation Approfondies en Sciences Médicales, *Sorbonne Université*

**2021 :** Master en Chimie pour les Sciences du Vivant, *ENS Ulm - Université PSL*

**2020 :** Master en Informatique, *Sorbonne Université*

**2019 :** Troisième année du cycle ingénieur, *Ecole polytechnique*

# Contact

Pour une collaboration, vous pouvez me contacter via [Linkedin](https://www.linkedin.com/in/yanis-bendjelal/?locale=fr_FR).











<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carousel</title>
    <style>
        .carousel {
            position: relative;
            width: 500px;
            height: 500px;
            overflow: hidden;
            margin: auto;
        }

        .carousel-inner {
            display: flex;
            width: 100%;
            height: 100%;
            transition: transform 0.5s ease;
        }

        .carousel-item {
            min-width: 100%;
            height: 100%;
        }

        .carousel-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .carousel-controls {
            position: absolute;
            top: 50%;
            width: 100%;
            display: flex;
            justify-content: space-between;
            transform: translateY(-50%);
        }

        .carousel-controls button {
            background-color: rgba(0, 0, 0, 0.5);
            border: none;
            color: white;
            padding: 10px;
            cursor: pointer;
        }

        .carousel-indicators {
            position: absolute;
            bottom: 10px;
            width: 100%;
            display: flex;
            justify-content: center;
        }

        .carousel-indicators button {
            background-color: rgba(0, 0, 0, 0.5);
            border: none;
            color: white;
            padding: 5px;
            cursor: pointer;
            margin: 0 2px;
        }

        .carousel-indicators button.active {
            background-color: white;
            color: black;
        }
    </style>
</head>
<body>
    <div class="carousel">
        <div class="carousel-inner">
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1F05a3hE29wF0WNmbFvGRHGyZ2l3nMrXU/preview" title="Gradient 2.jpg" width="300" height="300"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1F05a3hE29wF0WNmbFvGRHGyZ2l3nMrXU/preview" title="Gradient 2.jpg" width="300" height="300"></iframe>
            </div>
        </div>
        <div class="carousel-controls">
            <button id="prev">❮</button>
            <button id="next">❯</button>
        </div>
        <div class="carousel-indicators">
            <button class="active" data-slide="0"></button>
            <button data-slide="1"></button>
        </div>
    </div>

    <script>
        const carouselInner = document.querySelector('.carousel-inner');
        const carouselItems = document.querySelectorAll('.carousel-item');
        const prevButton = document.getElementById('prev');
        const nextButton = document.getElementById('next');
        const indicators = document.querySelectorAll('.carousel-indicators button');

        let currentIndex = 0;

        function updateCarousel() {
            carouselInner.style.transform = `translateX(-${currentIndex * 100}%)`;
            indicators.forEach((indicator, index) => {
                if (index === currentIndex) {
                    indicator.classList.add('active');
                } else {
                    indicator.classList.remove('active');
                }
            });
        }

        prevButton.addEventListener('click', () => {
            currentIndex = (currentIndex > 0) ? currentIndex - 1 : carouselItems.length - 1;
            updateCarousel();
        });

        nextButton.addEventListener('click', () => {
            currentIndex = (currentIndex < carouselItems.length - 1) ? currentIndex + 1 : 0;
            updateCarousel();
        });

        indicators.forEach((indicator, index) => {
            indicator.addEventListener('click', () => {
                currentIndex = index;
                updateCarousel();
            });
        });
    </script>
</body>
</html>








<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carousel</title>
    <style>
        .carousel {
            position: relative;
            width: 500px;
            height: 500px;
            overflow: hidden;
            margin: auto;
        }

        .carousel-inner {
            display: flex;
            width: 100%;
            height: 100%;
            transition: transform 0.5s ease;
        }

        .carousel-item {
            min-width: 100%;
            height: 100%;
        }

        .carousel-item iframe {
            width: 100%;
            height: 100%;
        }

        .carousel-controls {
            position: absolute;
            top: 50%;
            width: 100%;
            display: flex;
            justify-content: space-between;
            transform: translateY(-50%);
        }

        .carousel-controls button {
            background-color: rgba(0, 0, 0, 0.5);
            border: none;
            color: white;
            padding: 10px;
            cursor: pointer;
        }

        .carousel-indicators {
            position: absolute;
            bottom: 10px;
            width: 100%;
            display: flex;
            justify-content: center;
        }

        .carousel-indicators button {
            background-color: rgba(0, 0, 0, 0.5);
            border: none;
            color: white;
            padding: 5px;
            cursor: pointer;
            margin: 0 2px;
        }

        .carousel-indicators button.active {
            background-color: white;
            color: black;
        }
    </style>
</head>
<body>
    <div class="carousel">
        <div class="carousel-inner">
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1Zkoowxd10KM7p9QVjdBBFsCnb6zv9PCL/preview" title="Baricade arc-en-ciel.heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1GBfhOWgN1oS_JyB0WrnfjyZocRtvcNYx/preview" title="Cardboard pull 11 (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1v-ZQ906S-UfL0ejklFhciv1Ov2Pm2I-G/preview" title="Cardboard pull 2 (CE 20 x 20).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/131BjXzLPFu2ioNz3Ys-jzU6BOxZvRFhL/preview" title="Cardboard pull 3 (CE 20 x 20).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1INsEnUjB3MEL1CYF0pwq3XgJki7mLYIi/preview" title="Cardboard pull 4 - Fluorescent (CE 21 x 30).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1fNgU0reOz7Cqd4yQIXkQBx1Vk2G_C0-R/preview" title="Cardboard pull 6.heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1Ae52NCcpynB29mIGXB7_uRpfS3U6MCdu/preview" title="Cardboard pull 8 (toile 40 x 50).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1bzcES1Lh90mDuexcZmCb0W0Bmsy3RI-X/preview" title="Cardboard pull 9 - Butterfly (toile 40 x 50).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1BNILMiH8bKWKX1WJdQh9U3A0m6qHQcjk/preview" title="Cardboard swipe 1 (CE 21 x 30).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1fNBxvhyV4XPppI9DPs2dzG6F-PpzUvdS/preview" title="Chaotic pour 2 (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1VM_O09YhvGyG7eX5B8Qag4uJkAjxhch2/preview" title="Chaotic pour 3 - Rose et mauve (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1wBXJjhOXYgoUXfGtH3IUrydU1K3QG0HP/preview" title="Chaotique pour 1 (toile 20 x 20).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/150hKglGTN3-R_7po5riJjCS6aFLQprx9/preview" title="Couteau 1 (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1LpOfI5D9pJ6IhEuQzEAC_4G6CvCrBptE/preview" title="Couteau 2 (CE 20 x 20).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1t9AM-XCmKHm8SxtNsngRn16aoz8QfikT/preview" title="Couteau 3 (CE 20 x 20).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1-4DbQ1XKqkdYG8jZVyq4dvT3q3F2BznW/preview" title="Diagonal pour 2 (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1cbmZg8CiEcJkUofapn-XFjClJm9cNNOh/preview" title="Diagonal pour 3 (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1GxBLbnp4YrCnfrymS29JCkk_wXRVsLld/preview" title="Flip cup 1 - Géode onirique (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1qKQHPkB85uvqHLa8oL8jrXXhDHViYq64/preview" title="Flip cup 2 - Oniroi (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1LX5HCV4psmm4xxKJYQf-MCDVP6uWEbnN/preview" title="Flower pour 1 (toile 20 x 20).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1G48JSfgraW_w59fN5rWFYfCg4EXx9W8V/preview" title="Flower pour 3 - Centrifugé (toile 20 x 20).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1G5gf2yEmV8pG8zWnKBfUBIFxk-yTRmch/preview" title="Flower pour 4 (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1zkXTTEShJ85LoZ8NorPH9_tzJZr_QBaZ/preview" title="Mix arc-en-ciel 1 (toile 20 x 20).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1Z4_TdhjxeW8v8zJTkuVNlw7lajZPN-8J/preview" title="Mix arc-en-ciel 3 (toile 20 x 20).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1Vy277BRddI0LgNKlpX2SllqdrHNgc2k_/preview" title="Mix arc-en-ciel 4 (toile 30 x 30).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1duI87n9ZxEGvqrdX-p1sZox4sH36aDwB/preview" title="Squeegee swipe 1 .heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1m5f7i8b6NI4zGvD8Tq6Q3z5ssfUbREad/preview" title="Squeegee swipe 3 (CE 20 x 20).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1T0eCzwR_cnggGhCI1Nyfvzv8lJtTYEhQ/preview" title="Squeegee swipe 3 (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1qzU4GJUEsXDQA7ZPyKa6WJJX2oC7iFrI/preview" title="Squeegee swipe 4 (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/11Ly-vJiB1BxAiS_l304TeShQR3uB3XFy/preview" title="Straight pour 1 - Ciel nuageux (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1-puIp4b8fzAI2uBovZ4szJzxmbPwimXk/preview" title="Straight pour 6 (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/186FZqYGxQQ6VSruiUmnNWGLH5wvbggoi/preview" title="Straight pour 7 (toile 40 x 40).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1E0-0tLQoG8ywRxCkT9my-07O-wzpfFLD/preview" title="Géométrique 2 (CE 20 x 20).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1jfwWYWx21eqiHQIsacpyGp24VWP6ORw-/preview" title="Puddle pour 1 - Colorful (toile 20 x 20).heic"></iframe>
            </div>
            <div class="carousel-item">
                <iframe src="https://drive.google.com/file/d/1_UVtOHtTDLjnFbCFae1dKi6kLpNzbYlu/preview" title="Puddle pour 2 (toile 40 x 40).heic"></iframe>
            </div>

        </div>
        <div class="carousel-controls">
            <button id="prev">❮</button>
            <button id="next">❯</button>
        </div>
        <div class="carousel-indicators">
            <button class="active" data-slide="0"></button>
            <button data-slide="1"></button>
            <button data-slide="2"></button>
            <button data-slide="3"></button>
            <button data-slide="4"></button>
            <button data-slide="5"></button>
            <button data-slide="6"></button>
            <button data-slide="7"></button>
            <button data-slide="8"></button>
            <button data-slide="9"></button>
            <button data-slide="10"></button>
            <button data-slide="11"></button>
            <button data-slide="12"></button>
            <button data-slide="13"></button>
            <button data-slide="14"></button>
            <button data-slide="15"></button>
            <button data-slide="16"></button>
            <button data-slide="17"></button>
            <button data-slide="18"></button>
            <button data-slide="19"></button>
            <button data-slide="20"></button>
            <button data-slide="21"></button>
            <button data-slide="22"></button>
            <button data-slide="23"></button>
            <button data-slide="24"></button>
            <button data-slide="25"></button>
            <button data-slide="26"></button>
            <button data-slide="27"></button>
            <button data-slide="28"></button>
            <button data-slide="29"></button>
            <button data-slide="30"></button>
            <button data-slide="31"></button>
            <button data-slide="32"></button>
            <button data-slide="33"></button>
            <button data-slide="34"></button>
            <button data-slide="35"></button>
            <button data-slide="36"></button>
        </div>
    </div>

    <script>
        const carouselInner = document.querySelector('.carousel-inner');
        const carouselItems = document.querySelectorAll('.carousel-item');
        const prevButton = document.getElementById('prev');
        const nextButton = document.getElementById('next');
        const indicators = document.querySelectorAll('.carousel-indicators button');

        let currentIndex = 0;

        function updateCarousel() {
            carouselInner.style.transform = `translateX(-${currentIndex * 100}%)`;
            indicators.forEach((indicator, index) => {
                if (index === currentIndex) {
                    indicator.classList.add('active');
                } else {
                    indicator.classList.remove('active');
                }
            });
        }

        prevButton.addEventListener('click', () => {
            currentIndex = (currentIndex > 0) ? currentIndex - 1 : carouselItems.length - 1;
            updateCarousel();
        });

        nextButton.addEventListener('click', () => {
            currentIndex = (currentIndex < carouselItems.length - 1) ? currentIndex + 1 : 0;
            updateCarousel();
        });

        indicators.forEach((indicator, index) => {
            indicator.addEventListener('click', () => {
                currentIndex = index;
                updateCarousel();
            });
        });
    </script>
</body>
</html>









<img src="photo.png" alt="Photo de moi" class="circular-photo">
