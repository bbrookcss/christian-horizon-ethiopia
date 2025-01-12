<script>
    import Header from '../header.svelte';
    import Footer from '../footer.svelte';
</script>

<div class="disability-page">
    <Header darkMode={true} />
    
    <section class="hero">
        <div class="container">
            <div class="content">
                <span class="tag">Disability Support</span>
                <h1>Empowering Lives Through Inclusive Support</h1>
                <p>Our disability support program provides comprehensive services and resources to empower individuals with disabilities, ensuring they have equal opportunities for growth, independence, and community participation.</p>
            </div>
            <div class="hero-image">
                <img src="./Rroom4.jpg" alt="Disability Support Program" />
            </div>
        </div>
    </section>

    <section class="stats">
        <div class="container">
            <div class="stat-card">
                <h3>350+</h3>
                <p>Individuals Supported</p>
            </div>
            <div class="stat-card">
                <h3>24/7</h3>
                <p>Care Services</p>
            </div>
            <div class="stat-card">
                <h3>20+</h3>
                <p>Community Programs</p>
            </div>
            <div class="stat-card">
                <h3>95%</h3>
                <p>Community Impact</p>
            </div>
        </div>
    </section>

    <section class="programs">
        <div class="container">
            <h2>Our Support Programs</h2>
            <div class="image-grid">
                <div class="program-card">
                    <img src="./ecodis1.jpg" alt="Rehabilitation Services" />
                    <h3>Rehabilitation Services</h3>
                    <p>Comprehensive rehabilitation programs tailored to individual needs.</p>
                </div>
                <div class="program-card">
                    <img src="./ecodis2.jpg" alt="Skills Development" />
                    <h3>Skills Development</h3>
                    <p>Practical training to enhance independence and life skills.</p>
                </div>
                <div class="program-card">
                    <img src="./ecodis3.jpg" alt="Community Integration" />
                    <h3>Community Integration</h3>
                    <p>Programs fostering social inclusion and community participation.</p>
                </div>
            </div>
        </div>
    </section>

    <Footer />
</div>

<style>
    .disability-page {
        background-color: white;
    }

    .hero {
        padding: 120px 2rem 4rem;
    }

    .container {
        max-width: 1200px;
        margin: 0 auto;
    }

    .hero .container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        align-items: center;
    }

    .tag {
        display: inline-block;
        background-color: #DBEAFE;
        color: #004197;
        padding: 0.5rem 1rem;
        border-radius: 50px;
        font-size: 1rem;
        margin-bottom: 1.5rem;
    }

    h1 {
        font-size: 3rem;
        color: #000;
        margin-bottom: 1.5rem;
        line-height: 1.2;
    }

    .hero p {
        font-size: 1.2rem;
        color: #666;
        line-height: 1.6;
    }

    .hero-image img {
        width: 100%;
        border-radius: 1rem;
    }

    .stats {
        padding: 4rem 2rem;
        background-color: #F8FAFC;
    }

    .stats .container {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 2rem;
    }

    .stat-card {
        text-align: center;
        padding: 2rem;
        background: white;
        border-radius: 1rem;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
    }

    .stat-card h3 {
        font-size: 2.5rem;
        color: #004197;
        margin-bottom: 0.5rem;
    }

    .stat-card p {
        color: #666;
    }

    .programs {
        padding: 4rem 2rem;
    }

    .programs h2 {
        text-align: center;
        font-size: 2.5rem;
        margin-bottom: 3rem;
    }

    .image-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 2rem;
    }

    .program-card {
        text-align: center;
    }

    .program-card img {
        width: 100%;
        border-radius: 1rem;
        margin-bottom: 1.5rem;
    }

    .program-card h3 {
        font-size: 1.5rem;
        margin-bottom: 1rem;
    }

    .program-card p {
        color: #666;
        line-height: 1.6;
    }

    @media (max-width: 968px) {
        .hero .container {
            grid-template-columns: 1fr;
            gap: 2rem;
        }

        .stats .container {
            grid-template-columns: repeat(2, 1fr);
        }

        .image-grid {
            grid-template-columns: 1fr;
            gap: 3rem;
        }
    }

    @media (max-width: 580px) {
        .hero {
            padding: 100px 1rem 2rem;
        }

        h1 {
            font-size: 2rem;
        }

        .stats .container {
            grid-template-columns: 1fr;
        }
    }
</style> 