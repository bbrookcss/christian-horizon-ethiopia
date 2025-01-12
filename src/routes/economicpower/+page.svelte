<script>
    import Header from '../header.svelte';
    import Footer from '../footer.svelte';
</script>

<div class="economic-page">
    <Header darkMode={true} />
    
    <section class="hero">
        <div class="container">
            <div class="content">
                <span class="tag">Economic Empowerment</span>
                <h1>Building Economic Independence</h1>
                <p>Our economic empowerment program focuses on providing skills training, financial literacy, and entrepreneurship support to help individuals and families achieve sustainable economic independence.</p>
            </div>
            <div class="hero-image">
                <img src="./ecodis4.jpg" alt="Economic Empowerment Program" />
            </div>
        </div>
    </section>

    <section class="impact">
        <div class="container">
            <div class="stat-card">
                <h3>85%</h3>
                <p>Success Rate</p>
            </div>
            <div class="stat-card">
                <h3>200+</h3>
                <p>Active Projects</p>
            </div>
            <div class="stat-card">
                <h3>$50K+</h3>
                <p>Microloans Distributed</p>
            </div>
        </div>
    </section>

    <section class="initiatives">
        <div class="container">
            <h2>Our Economic Initiatives</h2>
            <div class="initiatives-grid">
                <div class="initiative-card">
                    <img src="./ecodis5.jpg" alt="Skills Training" />
                    <div class="content">
                        <h3>Skills Training</h3>
                        <p>Comprehensive vocational training programs to develop marketable skills.</p>
                        <a href="#" class="learn-more">Learn more →</a>
                    </div>
                </div>
                <div class="initiative-card">
                    <img src="./BBS3.jpg" alt="Microfinance Support" />
                    <div class="content">
                        <h3>Microfinance Support</h3>
                        <p>Access to small business loans and financial management training.</p>
                        <a href="#" class="learn-more">Learn more →</a>
                    </div>
                </div>
                <div class="initiative-card">
                    <img src="./ecodis2.jpg" alt="Business Mentorship" />
                    <div class="content">
                        <h3>Business Mentorship</h3>
                        <p>One-on-one guidance from experienced business professionals.</p>
                        <a href="#" class="learn-more">Learn more →</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <Footer />
</div>

<style>
    .economic-page {
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
        background-color: #FED7AA;
        color: #9A3412;
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

    .impact {
        padding: 4rem 2rem;
        background-color: #FFF7ED;
    }

    .impact .container {
        max-width: 1200px;
        margin: 0 auto;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
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
        color: #EA580C;
        margin-bottom: 0.5rem;
    }

    .stat-card p {
        color: #666;
    }

    .initiatives {
        padding: 4rem 2rem;
    }

    .initiatives h2 {
        text-align: center;
        font-size: 2.5rem;
        margin-bottom: 3rem;
    }

    .initiatives-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 2rem;
    }

    .initiative-card {
        background: white;
        border-radius: 1rem;
        overflow: hidden;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
    }

    .initiative-card img {
        width: 100%;
        height: 200px;
        object-fit: cover;
    }

    .initiative-card .content {
        padding: 1.5rem;
    }

    .initiative-card h3 {
        font-size: 1.5rem;
        margin-bottom: 1rem;
    }

    .initiative-card p {
        color: #666;
        line-height: 1.6;
        margin-bottom: 1rem;
    }

    .learn-more {
        color: #EA580C;
        text-decoration: none;
        font-weight: 500;
    }

    @media (max-width: 968px) {
        .hero .container {
            grid-template-columns: 1fr;
            gap: 2rem;
        }

        .impact .container {
            grid-template-columns: repeat(2, 1fr);
        }

        .initiatives-grid {
            grid-template-columns: 1fr;
            gap: 2rem;
        }
    }

    @media (max-width: 580px) {
        .hero {
            padding: 100px 1rem 2rem;
        }

        h1 {
            font-size: 2rem;
        }

        .impact .container {
            grid-template-columns: 1fr;
        }
    }
</style> 