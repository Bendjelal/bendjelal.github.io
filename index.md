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
            width: 300px;
            height: 300px;
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
                <img src="images/Gradient1.jpg" alt="Gradient 1">
            </div>
            <div class="carousel-item">
                <img src="images/Gradient2.jpg" alt="Gradient 2">
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













<img src="photo.png" alt="Photo de moi" class="circular-photo">
