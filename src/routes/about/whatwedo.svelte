<section class="whatwedo-container">
    <div class="container">
        <div class="left-content">
            <div class="tag">What we do</div>
            <h2>Inclusive Development and Support</h2>
            <p>
                At CHE, we implement inclusive development interventions aimed at 
                promoting the social, economic, and political inclusion of marginalized 
                groups. Our programs focus on providing access to quality education for 
                children with disabilities, delivering rehabilitation services, and offering 
                economic empowerment initiatives for women, youth, and persons with 
                disabilities. We are committed to breaking the cycle of poverty through 
                sustainable, community-led initiatives.
            </p>
        </div>

        <div class="stats-grid">
            <div class="stat-card orange">
                <h3>660+</h3>
                <p>Families Supported</p>
            </div>
            <div class="stat-card blue">
                <h3>80+</h3>
                <p>Weekend Daycare</p>
            </div>
            <div class="stat-card blue">
                <h3>24</h3>
                <p>Child Development Unit</p>
            </div>
            <div class="stat-card orange">
                <h3>530+</h3>
                <p>Sponsored Children</p>
            </div>
        </div>
    </div>
</section>

<style>
    .whatwedo-container {
        padding: 6rem 2rem;
        background-color: white;
    }

    .container {
        max-width: 1200px;
        margin: 0 auto;
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
    }

    .left-content {
        max-width: 540px;
    }

    h2 {
        font-size: 2.5rem;
        color: #000;
        margin-bottom: 1.5rem;
        line-height: 1.2;
    }

    p {
        color: #666;
        line-height: 1.6;
        margin-bottom: 2rem;
    }

    .stats-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 1.5rem;
        align-content: center;
    }

    .stat-card {
        padding: 2rem;
        border-radius: 1rem;
        text-align: left;
    }

    .stat-card.orange {
        background-color: #FED7AA;
    }

    .stat-card.blue {
        background-color: #BFDBFE;
    }

    .stat-card h3 {
        font-size: 3rem;
        margin-bottom: 1rem;
        color: #000;
    }

    .stat-card p {
        margin: 0;
        color: #000;
        font-size: 1.1rem;
    }

    @media (max-width: 968px) {
        .container {
            grid-template-columns: 1fr;
            gap: 3rem;
        }

        .left-content {
            max-width: 100%;
        }
    }

    @media (max-width: 580px) {
        .whatwedo-container {
            padding: 4rem 1.5rem;
        }

        h2 {
            font-size: 2rem;
        }

        .stats-grid {
            gap: 1rem;
        }

        .stat-card {
            padding: 1.5rem;
        }

        .stat-card h3 {
            font-size: 2.5rem;
        }

        .stat-card p {
            font-size: 1rem;
        }
    }

    @media (max-width: 400px) {
        .stats-grid {
            grid-template-columns: 1fr;
        }
    }
</style> 