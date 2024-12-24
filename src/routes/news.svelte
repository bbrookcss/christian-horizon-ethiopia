<section class="news">
  <div class="container">
    <span class="tag">News & Updates</span>
    
    <div class="news-header">
      <h2>Spotlights</h2>
      <p>
        We collaborate with national and international organizations to achieve
        our mission of empowering marginalized communities.
      </p>
    </div>

    <div class="news-grid">
      <div class="news-card">
        <img src="/logo.png" alt="Christian Horizons Logo" />
        <h3>2024 - 2028 Strategy Plan</h3>
        <a href="/news/strategy-plan" class="read-more">
          Read article <span>→</span>
        </a>
      </div>

      <div class="news-card">
        <img src="/newsimg1.jpg" alt="Board Meeting" />
        <h3>Christian Horizon Board Meeting</h3>
        <a href="/news/board-meeting" class="read-more">
          Read article <span>→</span>
        </a>
      </div>

      <div class="news-card">
        <img src="/newsimg2.jpg" alt="Graduation Ceremony" />
        <h3>Horizon Academy Graduation 2023</h3>
        <a href="/news/graduation-2023" class="read-more">
          Read article <span>→</span>
        </a>
      </div>
    </div>
  </div>
</section>

<style>
  .news {
    padding: 6rem 2rem;
    background-color: #F0F7FF;
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
  }

  .tag {
    display: inline-block;
    background-color: #DBEAFE;
    color: #004197;
    padding: 0.5rem 1rem;
    border-radius: 50px;
    font-size: 1.2rem;
    margin-bottom: 2rem;
  }

  .news-header {
    max-width: 600px;
    margin-bottom: 4rem;
  }

  h2 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    font-weight: 600;
  }

  p {
    color: #666;
    line-height: 1.6;
  }

  .news-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
  }

  .news-card {
    background: white;
    border-radius: 1rem;
    overflow: hidden;
    transition: transform 0.3s ease;
  }

  .news-card:hover {
    transform: translateY(-5px);
  }

  .news-card img {
    width: 100%;
    aspect-ratio: 16/9;
    object-fit: cover;
  }

  .news-card h3 {
    padding: 1.5rem;
    padding-bottom: 0;
    font-size: 1.3rem;
    color: #000;
    font-weight: 500;
  }

  .read-more {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    color: #004197;
    text-decoration: none;
    padding: 1.5rem;
    font-weight: 500;
  }

  .read-more span {
    transition: transform 0.3s ease;
  }

  .read-more:hover span {
    transform: translateX(5px);
  }

  @media (max-width: 968px) {
    .container {
      padding: 0;
    }

    .news-header {
      padding: 0 2rem;
    }

    .news-grid {
      display: flex;
      overflow-x: auto;
      gap: 1rem;
      padding: 1rem 2rem;
      scroll-snap-type: x mandatory;
      -webkit-overflow-scrolling: touch;
    }

    .news-card {
      min-width: 280px; /* Fixed width for cards */
      scroll-snap-align: start;
      margin-right: 0.5rem;
    }

    /* Hide scrollbar but keep functionality */
    .news-grid::-webkit-scrollbar {
      display: none;
    }
    
    .news-grid {
      -ms-overflow-style: none;
      scrollbar-width: none;
    }
  }

  @media (max-width: 580px) {
    .news {
      padding: 4rem 1.5rem; /* Remove horizontal padding */
    }

    .news-header {
      padding: 0 .2rem;
    }

    .news-grid {
      padding: 1rem 1.5rem;
    }

    h2 {
      font-size: 2rem;
    }
  }
</style> 