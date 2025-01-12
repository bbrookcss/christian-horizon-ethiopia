<script>
    import { scrollAnimation } from '$lib/scrollAnimation';
</script>
<div class="mission-vision-container">
    <div class="section" use:scrollAnimation={{ animation: 'slideRight', delay: 300 }}>
        <div class="tag">Our Mission</div>
        <h2>Support Those in Need</h2>
        <p>
            Our mission is to empower people living in vulnerability, whether due to 
            economic hardship or disability, by offering them the necessary support for 
            a better life.
        </p>
    </div>

    <div class="section" use:scrollAnimation={{ animation: 'slideLeft', delay: 300 }}>
        <div class="tag">Our Vision</div>
        <h2>A Place for Everyone</h2>
        <p>
            We envision a community where every person, regardless of their disability 
            or economic status, has the opportunity to live a decent life and achieve 
            their full potential.
        </p>
    </div>
</div>

<style>
    .mission-vision-container {
        display: flex;
        gap: 64px;
        padding: 70px;
        background: #FFF5EB;
        justify-content: center;
    }
    .section {
        max-width: 600px;
        flex: 1;
    }

    h2 {
        font-size: 36px;
        margin-bottom: 24px;
        color: #1A1A1A;
    }

    p {
        font-size: 18px;
        line-height: 1.6;
        color: #666666;
    }

    @media (max-width: 768px) {
        .mission-vision-container {
            flex-direction: column;
            padding: 40px 24px;
            gap: 40px;
        }

        .section {
            max-width: 100%;
        }

        

        h2 {
            font-size: 28px;
            margin-bottom: 16px;
        }

        p {
            font-size: 16px;
            line-height: 1.5;
        }
    }
</style>
