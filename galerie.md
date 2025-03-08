---
title: Galerie
layout: collection
permalink: /galerie/
collection: galerie 
entries_layout: grid
---

Je me plais à peindre sur mes heures perdues. Ici quelques créations que j'aime particulièrement. XXXXBBv

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carousel avec Lazy Loading</title>
    <style>
        .carousel {
            position: relative;
            width: 750px;
            height: 750px;
            overflow: hidden;
            margin: auto;
        }
        .carousel-inner {
            display: flex;
            transition: transform 0.5s ease;
            width: auto;
            white-space: nowrap;
        }
        .carousel-item {
            flex: 0 0 100%;
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
            <!-- Génération dynamique des items du carrousel -->
        </div>
        <div class="carousel-controls">
            <button id="prev">❮</button>
            <button id="next">❯</button>
        </div>
        <div class="carousel-indicators"></div>
    </div>

    <script>
        // Liste des URLs des images (mettre ici toutes tes URLs)
        const items = [
            "https://drive.google.com/file/d/1qzU4GJUEsXDQA7ZPyKa6WJJX2oC7iFrI/preview",
            "https://drive.google.com/file/d/1fgIqy1jRvxTpoCXN3wH5SuQJcLS7-HlR/preview",
            "https://drive.google.com/file/d/1udqgpjZKfTq5f7EUYEzyA-sFx13YebQV/preview",
            "https://drive.google.com/file/d/1cNLveEmEDr0elVbS4JxG1CTXAHq4RGnC/preview",
            "https://drive.google.com/file/d/1USEljVwcWTb1FYSNcoLCZbsqCgtL76hA/preview",
            "https://drive.google.com/file/d/1fNBxvhyV4XPppI9DPs2dzG6F-PpzUvdS/preview",
            "https://drive.google.com/file/d/150hKglGTN3-R_7po5riJjCS6aFLQprx9/preview",
            "https://drive.google.com/file/d/1LpOfI5D9pJ6IhEuQzEAC_4G6CvCrBptE/preview",
            "https://drive.google.com/file/d/1t9AM-XCmKHm8SxtNsngRn16aoz8QfikT/preview",
            "https://drive.google.com/file/d/154lOeXsuTq3ITvtOgI2gAv1W-4wlsZ9B/preview",
            "https://drive.google.com/file/d/1F8qsLRtuy91Yk6fZkqTVHxr_LsCinSlp/preview",
            "https://drive.google.com/file/d/1GxBLbnp4YrCnfrymS29JCkk_wXRVsLld/preview",
            "https://drive.google.com/file/d/1zkXTTEShJ85LoZ8NorPH9_tzJZr_QBaZ/preview",
            "https://drive.google.com/file/d/1m5f7i8b6NI4zGvD8Tq6Q3z5ssfUbREad/preview",
            "https://drive.google.com/file/d/1T0eCzwR_cnggGhCI1Nyfvzv8lJtTYEhQ/preview",
            "https://drive.google.com/file/d/11Ly-vJiB1BxAiS_l304TeShQR3uB3XFy/preview",
            "https://drive.google.com/file/d/1kzIoW4W0dapeRpknbBwmMKtjFLr-Ke6y/preview",
            "https://drive.google.com/file/d/1jfwWYWx21eqiHQIsacpyGp24VWP6ORw-/preview",
            "https://drive.google.com/file/d/1_UVtOHtTDLjnFbCFae1dKi6kLpNzbYlu/preview",
            "https://drive.google.com/file/d/1KKPpbET0LZGFh0c76Lho7F2oUDou2iPZ/preview",
            "https://drive.google.com/file/d/1KKPpbET0LZGFh0c76Lho7F2oUDou2iPZ/preview",
            "https://drive.google.com/file/d/1gDs4tg9bXbGWh1QFxVTtDyknBxXTg6JW/preview",
            "https://drive.google.com/file/d/1Y7xQBQyjZEOBS9uezkTjPGE2tXfr-IUG/preview",
            "https://drive.google.com/file/d/1zQiqZj41gz01YjikocEesDTKKcZwrM21/preview",
            "https://drive.google.com/file/d/1fQrQqPQBzFBAvJXOhuVg7MBSIByBn6Ww/preview",
            "https://drive.google.com/file/d/1IwvJ74ULtGGAipEjkI1JrVMDEYVijRjN/preview",
            "https://drive.google.com/file/d/1-VFpdxP1uy5VOzrRTRyos2-zynGtDb66/preview",
            "https://drive.google.com/file/d/1jxbNjmmxGQ3HRt4Po7KX_f7JjgfdzguL/preview",
            "https://drive.google.com/file/d/1p0jnZpn6kxpfhRxc_zs9d6WaWxuBfq3r/preview"
        ];


        const carouselInner = document.querySelector('.carousel-inner');
        const carouselIndicators = document.querySelector('.carousel-indicators');
        const prevButton = document.getElementById('prev');
        const nextButton = document.getElementById('next');

        let currentIndex = 0;

        // Générer dynamiquement les éléments
        items.forEach((url, index) => {
            const item = document.createElement('div');
            item.classList.add('carousel-item');
            if (index === 0) item.classList.add('active');

            const iframe = document.createElement('iframe');
            iframe.setAttribute('loading', 'lazy');
            iframe.setAttribute('src', url);
            item.appendChild(iframe);

            carouselInner.appendChild(item);

            // Ajouter les indicateurs
            const indicator = document.createElement('button');
            indicator.setAttribute('data-slide', index);
            if (index === 0) indicator.classList.add('active');
            carouselIndicators.appendChild(indicator);
        });

        const carouselItems = document.querySelectorAll('.carousel-item');
        const indicatorsContainer = document.querySelector('.carousel-indicators');

            // Générer les indicateurs en fonction du nombre d'éléments
            carouselItems.forEach((item, index) => {
            const indicator = document.createElement('button');
            indicator.setAttribute('data-slide', index);
            if (index === 0) {
                indicator.classList.add('active');
            }
            indicatorsContainer.appendChild(indicator);

            indicator.addEventListener('click', () => {
                currentIndex = index;
                updateCarousel();
            });
            });
        const indicators = document.querySelectorAll('.carousel-indicators button');

        function updateCarousel() {
            const translateValue = -(currentIndex * 100);
            carouselInner.style.transform = `translateX(${translateValue}%)`;

            indicators.forEach((indicator, index) => {
                indicator.classList.toggle('active', index === currentIndex);
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

        // Appliquer directement la bonne position au chargement
        updateCarousel();
    </script>
</body>
</html>


