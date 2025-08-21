<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sagesse Anima - Redécouvrez votre essence. Grandissez en sagesse.</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --noir: #1A1A1A;
            --blanc: #F8F5F0;
            --accent: #B35437;
            --texte: #333333;
            --gris-clair: #E5E2DD;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            color: var(--texte);
            background-color: var(--blanc);
            line-height: 1.6;
        }
        
        h1, h2, h3, h4 {
            font-family: 'Cormorant Garamond', serif;
            font-weight: 600;
            margin-bottom: 1rem;
            color: var(--noir);
        }
        
        h1 {
            font-size: 2.8rem;
            line-height: 1.2;
        }
        
        h2 {
            font-size: 2.2rem;
            position: relative;
            margin-bottom: 2rem;
        }
        
        h2:after {
            content: '';
            display: block;
            width: 60px;
            height: 2px;
            background-color: var(--accent);
            margin-top: 0.5rem;
        }
        
        p {
            margin-bottom: 1.5rem;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }
        
        /* Header */
        header {
            padding: 1.5rem 0;
            background-color: var(--blanc);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.8rem;
            font-weight: 600;
            color: var(--noir);
            text-decoration: none;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav li {
            margin-left: 2rem;
        }
        
        nav a {
            color: var(--noir);
            text-decoration: none;
            font-size: 1rem;
            transition: color 0.3s;
        }
        
        nav a:hover {
            color: var(--accent);
        }
        
        .panier-icon {
            font-size: 1.2rem;
        }
        
        /* Hero Section */
        .hero {
            background-image: linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%23F8F5F0"/><path d="M0 50 L100 50" stroke="%23E5E2DD" stroke-width="1"/><path d="M50 0 L50 100" stroke="%23E5E2DD" stroke-width="1"/></svg>');
            background-size: cover;
            padding: 6rem 0;
            text-align: center;
            color: var(--noir);
            margin-bottom: 4rem;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            margin-bottom: 1.5rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2.5rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 1rem 2rem;
            border: none;
            border-radius: 2px;
            font-size: 1rem;
            cursor: pointer;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #9a4630;
        }
        
        .confiance {
            margin-top: 2rem;
            font-size: 0.9rem;
            color: var(--noir);
        }
        
        /* Section Bénéfices */
        .benefits {
            padding: 4rem 0;
            text-align: center;
        }
        
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .benefit-card {
            padding: 2rem;
            background-color: white;
            border-radius: 4px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .benefit-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: var(--accent);
        }
        
        /* Section Produits */
        .featured-products {
            padding: 4rem 0;
            background-color: white;
            text-align: center;
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .product-card {
            background-color: var(--blanc);
            border-radius: 4px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
        }
        
        .product-image {
            height: 200px;
            background-color: var(--gris-clair);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--noir);
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.5rem;
            text-align: center;
            padding: 1rem;
        }
        
        .product-info {
            padding: 1.5rem;
        }
        
        .product-title {
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
        }
        
        .product-price {
            font-weight: 500;
            color: var(--accent);
            margin-bottom: 1rem;
        }
        
        /* Section Témoignages */
        .testimonials {
            padding: 4rem 0;
            text-align: center;
        }
        
        .testimonial-slider {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .testimonial {
            background-color: white;
            padding: 2rem;
            border-radius: 4px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin: 0 1rem;
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 1.5rem;
        }
        
        .testimonial-author {
            font-weight: 500;
            color: var(--accent);
        }
        
        /* CTA Section */
        .cta {
            padding: 5rem 0;
            text-align: center;
            background-color: var(--noir);
            color: var(--blanc);
        }
        
        .cta h2 {
            color: var(--blanc);
        }
        
        .cta h2:after {
            background-color: var(--accent);
            margin: 0.5rem auto 0 auto;
        }
        
        .cta p {
            max-width: 600px;
            margin: 0 auto 2rem auto;
        }
        
        /* Footer */
        footer {
            background-color: var(--noir);
            color: var(--blanc);
            padding: 4rem 0 2rem 0;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }
        
        .footer-logo {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: var(--blanc);
        }
        
        .footer-links h3 {
            color: var(--blanc);
            margin-bottom: 1.5rem;
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.5rem;
        }
        
        .footer-links a {
            color: var(--blanc);
            text-decoration: none;
            opacity: 0.8;
            transition: opacity 0.3s;
        }
        
        .footer-links a:hover {
            opacity: 1;
        }
        
        .newsletter input {
            padding: 0.8rem;
            width: 100%;
            margin-bottom: 1rem;
            border: none;
            border-radius: 2px;
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            opacity: 0.7;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .header-container {
                flex-direction: column;
            }
            
            nav ul {
                margin-top: 1.5rem;
                justify-content: center;
            }
            
            nav li {
                margin-left: 1rem;
                margin-right: 1rem;
            }
            
            .hero {
                padding: 4rem 0;
            }
            
            .benefits-grid, .products-grid, .footer-content {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <a href="#" class="logo">Sagesse Anima</a>
            <nav>
                <ul>
                    <li><a href="#">Accueil</a></li>
                    <li><a href="#">Boutique</a></li>
                    <li><a href="#">Notre Essence</a></li>
                    <li><a href="#">Vos Questions</a></li>
                    <li><a href="#" class="panier-icon">Panier (0)</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container hero-content">
            <h1>Votre voyage vers plus de clarté et de sérénité commence ici.</h1>
            <p>Sagesse Anima vous guide à travers des ebooks numériques d'exception, où la science rencontre les enseignements intemporels pour transformer votre quotidien.</p>
            <a href="#" class="btn">Explorer la Collection</a>
            <p class="confiance">Livraison immédiate ∙ Paiement 100% sécurisé ∙ Satisfaction garantie 30 jours</p>
        </div>
    </section>

    <!-- Benefits Section -->
    <section class="benefits container">
        <h2>Une bibliothèque de transformation à portée de clic</h2>
        <div class="benefits-grid">
            <div class="benefit-card">
                <div class="benefit-icon">📘</div>
                <h3>Sagesse Applicable</h3>
                <p>Des concepts profonds traduits en exercices et routines concrètes pour des résultats tangibles.</p>
            </div>
            <div class="benefit-card">
                <div class="benefit-icon">👑</div>
                <h3>Exigence Qualitative</h3>
                <p>Chaque ebook est le fruit de mois de recherche, structuré avec soin et design pour une expérience de lecture immersive.</p>
            </div>
            <div class="benefit-card">
                <div class="benefit-icon">🛡️</div>
                <h3>Confiance Absolue</h3>
                <p>Votre satisfaction est notre priorité. Téléchargez, lisez, et si vous n'êtes pas convaincu, nous vous remboursons.</p>
            </div>
        </div>
    </section>

    <!-- Featured Products -->
    <section class="featured-products container">
        <h2>Nos guides les plus recherchés</h2>
        <div class="products-grid">
            <div class="product-card">
                <div class="product-image">Le Code du Discipline</div>
                <div class="product-info">
                    <h3 class="product-title">Le Code du Discipline</h3>
                    <p class="product-description">Puisez dans la sagesse stoïcienne pour forger une volonté inflexible et une tranquillité d'esprit inébranlable.</p>
                    <p class="product-price">29 €</p>
                    <a href="#" class="btn">Découvrir</a>
                </div>
            </div>
            <div class="product-card">
                <div class="product-image">L'Art du Silence Intérieur</div>
                <div class="product-info">
                    <h3 class="product-title">L'Art du Silence Intérieur</h3>
                    <p class="product-description">Maîtrisez l'art de calmer votre mental et cultivez une présence profonde au monde, où que vous soyez.</p>
                    <p class="product-price">27 €</p>
                    <a href="#" class="btn">Découvrir</a>
                </div>
            </div>
            <div class="product-card">
                <div class="product-image">Ikigai Numérique</div>
                <div class="product-info">
                    <h3 class="product-title">Ikigai Numérique</h3>
                    <p class="product-description">Trouvez votre raison d'être à l'ère digitale. Combinez passion, mission, vocation et profession.</p>
                    <p class="product-price">31 €</p>
                    <a href="#" class="btn">Découvrir</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials container">
        <h2>Ils ont transformé leur quotidien</h2>
        <div class="testimonial-slider">
            <div class="testimonial">
                <p class="testimonial-text">"Enfin un livre sur le stoïcisme qui n'est pas que de la théorie. Les exercices du 'Code du Discipline' ont changé ma façon de réagir au stress."</p>
                <p class="testimonial-author">Marc, 34 ans</p>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section class="cta">
        <div class="container">
            <h2>Prêt à investir dans la version la plus importante de vous-même ?</h2>
            <p>Votre aventure vous attend. Rejoignez notre communauté de lecteurs engagés sur le chemin du développement personnel.</p>
            <a href="#" class="btn">Commencez Votre Lecture dès Maintenant</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-info">
                    <div class="footer-logo">Sagesse Anima</div>
                    <p>Redécouvrez votre essence. Grandissez en sagesse.</p>
                </div>
                <div class="footer-links">
                    <h3>Navigation</h3>
                    <ul>
                        <li><a href="#">Accueil</a></li>
                        <li><a href="#">Boutique</a></li>
                        <li><a href="#">Notre Essence</a></li>
                        <li><a href="#">Vos Questions</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h3>Informations</h3>
                    <ul>
                        <li><a href="#">Politique de confidentialité</a></li>
                        <li><a href="#">Conditions générales</a></li>
                        <li><a href="#">Mentions légales</a></li>
                    </ul>
                </div>
                <div class="newsletter">
                    <h3>Rejoignez notre cercle</h3>
                    <p>Inscrivez-vous pour recevoir des conseils exclusifs et être informé de nos nouvelles parutions.</p>
                    <input type="email" placeholder="Votre email">
                    <a href="#" class="btn">S'inscrire</a>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Sagesse Anima. Tous droits réservés.</p>
            </div>
        </div>
    </footer>

    <script>
        // Simple script for cart functionality
        document.addEventListener('DOMContentLoaded', function() {
            // Cart counter
            let cartCount = 0;
            const cartButton = document.querySelector('.panier-icon');
            
            // Update cart display
            function updateCart() {
                cartButton.textContent = `Panier (${cartCount})`;
            }
            
            // Add to cart buttons
            const addToCartButtons = document.querySelectorAll('.btn');
            addToCartButtons.forEach(button => {
                if (button.textContent === 'Découvrir') {
                    button.addEventListener('click', function(e) {
                        e.preventDefault();
                        cartCount++;
                        updateCart();
                        alert('Produit ajouté au panier !');
                    });
                }
            });
        });
    </script>
</body>
</html>
