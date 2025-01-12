<script>
    import Header from '../header.svelte';
</script>


<div class="about-container">
    <div class="content-section">
        <div class="tag">Who we are</div>
        <h1>Christian Horizons Ethiopia</h1>
        <p>
            Christian Horizons Ethiopia (CHE) has been dedicated to supporting 
            vulnerable people for over 30 years. We focus on helping children, families, 
            and individuals with disabilities, making sure they feel supported, included, 
            and valued. Our work is all about giving people the opportunity to live 
            better, more independent lives by meeting their needs and building strong, 
            caring communities.
        </p>
    </div>
    <div class="image-section">
        <img src="./aboutiimg1.jpg" alt="Christian Horizons Ethiopia Community" />
    </div>
</div>

<style>
    .about-container {
        display: flex;
        gap: 64px;
        padding: 0 80px;
        max-width: 1440px;
        margin: 0 auto;
        min-height: calc(100vh - 60px);
        align-items: center;
    }

    .content-section {
        flex: 1;
        max-width: 600px;
    }


    h1 {
        font-size: 48px;
        font-weight: bold;
        margin-bottom: 24px;
        color: #1A1A1A;
    }

    p {
        font-size: 18px;
        line-height: 1.6;
        color: #666666;
    }

    .image-section {
        flex: 1;
    }

    .image-section img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        border-radius: 16px;
    }

    @media (max-width: 768px) {
        .about-container {
            flex-direction: column;
            padding: 24px;
            gap: 32px;
            margin-top: 60px;
            min-height: auto;
        }

        .content-section {
            max-width: 100%;
        }


        h1 {
            font-size: 36px;
            margin-bottom: 16px;
        }

        p {
            font-size: 16px;
            line-height: 1.5;
        }

        .image-section img {
            border-radius: 12px;
            aspect-ratio: 16/9;
            object-fit: cover;
        }
    }
</style>