<script>
    import { scrollAnimation } from '$lib/scrollAnimation';
</script>
<section class="values-container">
    <div class="container">
        <div class="left-content" use:scrollAnimation={{ animation: 'slideRight', delay: 300 }}>
            <div class="tag">Our Values</div>
            <h2>Compassion, Integrity, and Inclusion</h2>

            <div class="values-list">
                <div class="value-item">
                    <h3>Inclusiveness</h3>
                    <p>We welcome and serve everyone, ensuring our programs are open to all people, no matter their situation.</p>
                </div>

                <div class="value-item">
                    <h3>Community-Focused</h3>
                    <p>We work alongside the people we help, ensuring our efforts meet their real needs and bring lasting change.</p>
                </div>

                <div class="value-item">
                    <h3>Sustainability</h3>
                    <p>We aim to create lasting impact, helping people become self-sufficient and thrive beyond our involvement.</p>
                </div>

                <div class="value-item">
                    <h3>Partnerships</h3>
                    <p>We believe in working together and building strong partnerships to achieve more for the people we serve.</p>
                </div>

                <div class="value-item">
                    <h3>Compassion and Integrity</h3>
                    <p>Everything we do is driven by kindness, honesty, and a commitment to serving others with respect.</p>
                </div>
            </div>
        </div>

        <div class="image-grid" use:scrollAnimation={{ animation: 'slideUp', delay: 400 }}>
            <img src="/img1.jpg" alt="Community work" class="grid-img img1">
            <img src="/img2.jpg" alt="Community work" class="grid-img img2">
            <img src="/img3.jpg" alt="Community work" class="grid-img img3">
            <img src="/img4.jpg" alt="Community work" class="grid-img img4">
        </div>
    </div>
</section>

<style>
    .values-container {
        padding: 6rem 2rem;
        background-color: #F0F7FF;
    }

    .container {
        max-width: 1200px;
        margin: 0 auto;
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        align-items: center;
    }

    .left-content {
        max-width: 540px;
    }

    h2 {
        font-size: 2.5rem;
        color: #000;
        margin-bottom: 2.5rem;
        line-height: 1.2;
    }

    .values-list {
        display: flex;
        flex-direction: column;
        gap: 2rem;
    }

    .value-item h3 {
        color: #0438a1;
        font-size: 1.25rem;
        margin-bottom: 0.5rem;
        font-weight: 600;
    }

    .value-item p {
        color: #666;
        line-height: 1.6;
        font-size: 1rem;
    }

    .image-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 1.5rem;
        position: relative;
        margin-top: 2rem;
    }

    .grid-img {
        width: 100%;
        height: 240px;
        object-fit: cover;
        border-radius: 1rem;
        transition: transform 0.3s ease;
    }

    .img1 { transform: rotate(-5deg) translateY(20px); }
    .img2 { transform: rotate(5deg) translateY(-20px); }
    .img3 { transform: rotate(5deg) translateY(20px); }
    .img4 { transform: rotate(-5deg) translateY(-20px); }

    @media (max-width: 968px) {
        .container {
            grid-template-columns: 1fr;
            gap: 3rem;
        }

        .image-grid {
            margin-top: 1rem;
        }

        .grid-img {
            height: 200px;
            border: 2px solid #ffffff;
        }

        .left-content {
            max-width: 100%;
        }
    }

    @media (max-width: 580px) {
        .values-container {
            padding: 4rem 1.5rem;
        }

        h2 {
            font-size: 2rem;
        }

        .image-grid {
            gap: 1rem;
        }

        .value-item h3 {
            font-size: 1.1rem;
        }
    }

    @media (max-width: 400px) {
        .image-grid {
            grid-template-columns: 1fr;
        }
    }
</style> 