---
title: Galerie
layout: collection
permalink: /galerie/
collection: galerie
entries_layout: grid
---


#### Carye de voeux

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carousel avec Lazy Loading</title>
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
                <iframe loading="lazy" src="https://drive.google.com/file/d/1-vCFRQoR9onBp0J2rUp0rjpGYpH9SM41/preview" title="Carte de voeux - Bloom.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1UuhXpWisJDKODkMApstSJ8zLsx1MQim_/preview" title="Carte de voeux - Bulles.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1T8EyrWqZZymELqD7psiCiwCzPHOjkMDr/preview" title="Carte de voeux - Décoration abstraite 1.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1SBew-9IEh1nxWztR56LNKUtTegq_BoAq/preview" title="Carte de voeux - Saint Valentin 1.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1j9jsn5UQMpgYDWfgH7Dmm2BeMXaHrJc8/preview" title="Carte de voeux - Saint Valentin 2.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1LUSAACMu5oYw8WmqL_kelDG5asj5XXNF/preview" title="Carte de voeux - Spring.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1Z08HKcKQsFRK66EIpYopJ1KCrPfYcXwo/preview" title="Carte de voeux - Tulipes.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1NG4zDro5iegGi1s6CXWUDWaWKfu7tWuU/preview" title="Faire-part 1.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1ryXCTwY3n2r6T5p8Sw12anP8JKAtyktV/preview" title="Faire-part 2.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1fHtTT62toOgzjhJJVOxJxTCn05-EoDQZ/preview" title="Faire-part 3.jpg"></iframe>
            </div>
        </div>
        <div class="carousel-controls">
            <button id="prev1">❮</button>
            <button id="next1">❯</button>
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
        </div>
    </div>

    <script>
        const carouselInner1 = document.querySelector('.carousel-inner');
        const carouselItems1 = document.querySelectorAll('.carousel-item');
        const prevButton1 = document.getElementById('prev1');
        const nextButton1 = document.getElementById('next1');
        const indicators1 = document.querySelectorAll('.carousel-indicators button');

        let currentIndex1 = 0;

        function updateCarousel1() {
            carouselInner1.style.transform = `translateX(-${currentIndex1 * 100}%)`;
            indicators1.forEach((indicator, index) => {
                if (index === currentIndex1) {
                    indicator.classList.add('active');
                } else {
                    indicator.classList.remove('active');
                }
            });
        }

        prevButton1.addEventListener('click', () => {
            currentIndex1 = (currentIndex1 > 0) ? currentIndex1 - 1 : carouselItems1.length - 1;
            updateCarousel1();
        });

        nextButton1.addEventListener('click', () => {
            currentIndex1 = (currentIndex1 < carouselItems1.length - 1) ? currentIndex1 + 1 : 0;
            updateCarousel1();
        });

        indicators1.forEach((indicator, index) => {
            indicator.addEventListener('click', () => {
                currentIndex1 = index;
                updateCarousel1();
            });
        });
    </script>
</body>
</html>

#### Motifs

<script>
        const carouselInner1 = document.querySelector('.carousel-inner');
        const carouselItems1 = document.querySelectorAll('.carousel-item');
        const prevButton1 = document.getElementById('prev1');
        const nextButton1 = document.getElementById('next1');
        const indicators1 = document.querySelectorAll('.carousel-indicators button');

        let currentIndex1 = 0;

        function updateCarousel1() {
            carouselInner1.style.transform = `translateX(-${currentIndex1 * 100}%)`;
            indicators1.forEach((indicator, index) => {
                if (index === currentIndex1) {
                    indicator.classList.add('active');
                } else {
                    indicator.classList.remove('active');
                }
            });
        }

        prevButton1.addEventListener('click', () => {
            currentIndex1 = (currentIndex1 > 0) ? currentIndex1 - 1 : carouselItems1.length - 1;
            updateCarousel1();
        });

        nextButton1.addEventListener('click', () => {
            currentIndex1 = (currentIndex1 < carouselItems1.length - 1) ? currentIndex1 + 1 : 0;
            updateCarousel1();
        });

        indicators1.forEach((indicator, index) => {
            indicator.addEventListener('click', () => {
                currentIndex1 = index;
                updateCarousel1();
            });
        });
    </script>

    <div class="carousel">
        <div class="carousel-inner">
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1UaFVqjFMDPqRNqWc7hR3glV160UXzAol/preview" title="Motif 1.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/15O3kWjAgc9Trv_S2Xh2dKW5VOM95cJTg/preview" title="Motif 10.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/18VYn5mpNe06pnT_zu27bEG7OE98lGWXD/preview" title="Motif 11.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/190Jt_L0EPVn85R4R12taZ0Y6_YjssovN/preview" title="Motif 12.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1FBVtQsLJzMWJzYsndbcp6nuEY8vomQGt/preview" title="Motif 14.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/17zmXI4jQq9T7kutljVhKsOQDNK6ljzLy/preview" title="Motif 2.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/16Mklxumh_ojzE5726PuO9iS-I-yykArM/preview" title="Motif 3.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1E6i_jM2yEpGrSUjxzJsqLKeV5IvSZbmE/preview" title="Motif 5 - 5 cm par seconde.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1PLdu6STpHXndAIDJFUhw18Etgx_XzpC6/preview" title="Motif 6 - Abondance de fleur.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1Ix30qlyZR47IQK05u0htU_N8wt3tMTdh/preview" title="Motif 7.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/13709QnmMA57f3x5NIPv2t7g_X1a2ljjH/preview" title="Motif 8.jpg"></iframe>
            </div>
            <div class="carousel-item">
                <iframe loading="lazy" src="https://drive.google.com/file/d/1hAuobVlfmzRVasjdFAzC1aUKaiTe2-qb/preview" title="Motif 9.jpg"></iframe>
            </div>
        </div>
        <div class="carousel-controls">
            <button id="prev2">❮</button>
            <button id="next2">❯</button>
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
        </div>
    </div>

    <script>
        const carouselInner2 = document.querySelector('.carousel-inner');
        const carouselItems2 = document.querySelectorAll('.carousel-item');
        const prevButton2 = document.getElementById('prev2');
        const nextButton2 = document.getElementById('next2');
        const indicators2 = document.querySelectorAll('.carousel-indicators button');

        let currentIndex2 = 0;

        function updateCarousel2() {
            carouselInner2.style.transform = `translateX(-${currentIndex2 * 100}%)`;
            indicators2.forEach((indicator, index) => {
                if (index === currentIndex2) {
                    indicator.classList.add('active');
                } else {
                    indicator.classList.remove('active');
                }
            });
        }

        prevButton2.addEventListener('click', () => {
            currentIndex2 = (currentIndex2 > 0) ? currentIndex2 - 1 : carouselItems2.length - 1;
            updateCarousel2();
        });

        nextButton2.addEventListener('click', () => {
            currentIndex2 = (currentIndex2 < carouselItems2.length - 1) ? currentIndex2 + 1 : 0;
            updateCarousel2();
        });

        indicators2.forEach((indicator, index) => {
            indicator.addEventListener('click', () => {
                currentIndex2 = index;
                updateCarousel2();
            });
        });
    </script>
</body>
</html>

