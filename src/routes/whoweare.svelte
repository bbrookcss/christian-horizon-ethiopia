<script>
  import { fade, fly } from 'svelte/transition';
  import { scrollAnimation } from '$lib/scrollAnimation';
  let showDetails = false;
  let hoveredCard = null;
</script>

{#if hoveredCard}
  <div class="global-overlay" transition:fade={{ duration: 200 }}></div>
{/if}

<section class="who-we-are">
    <div class="container">
      <div class="left-content" use:scrollAnimation={{ animation: 'slideRight' }}>
        <span class="tag">Who we are</span>
        <h2>We are Christian Horizon Ethiopia</h2>
        <p>
          For over 30 years, Christian Horizons Ethiopia has been transforming the
          lives of marginalized children, women, and people with disabilities. Guided
          by our mission to serve those in need, we provide education, rehabilitation,
          and sustainable economic empowerment to create lasting change in
          communities.
        </p>
        <a href="/about" class="learn-more">
          Learn more <span class="arrow">→</span>
        </a>
      </div>
  
      <div class="stats-grid">
        <div class="stat-card orange" 
          on:mouseenter={() => hoveredCard = 'families'} 
          on:mouseleave={() => hoveredCard = null}>
          <h3>660+</h3>
          <p>Families Supported</p>
          {#if hoveredCard === 'families'}
            <div class="card-details" transition:fly={{ y: 20, duration: 300 }}>
              <h4>In Family Support We Are Covering 660+ Children</h4>
              <p>We are providing education, rehabilitation, and sustainable economic empowerment to create lasting change in communities.</p>
            </div>
          {/if}
        </div>
        
        <div class="stat-card blue"
          on:mouseenter={() => hoveredCard = 'daycare'} 
          on:mouseleave={() => hoveredCard = null}>
          <h3>80+</h3>
          <p>Weekend Daycare</p>
          {#if hoveredCard === 'daycare'}
            <div class="card-details" transition:fly={{ y: 20, duration: 300 }}>
              <h4>Weekend Daycare Program</h4>
              <p>We are providing safe and nurturing weekend care for children, allowing parents to work and improve their family's economic situation.</p>
            </div>
          {/if}
        </div>
        
        <div class="stat-card blue"
          on:mouseenter={() => hoveredCard = 'development'} 
          on:mouseleave={() => hoveredCard = null}>
          <h3>24</h3>
          <p>Children Development Unit</p>
          {#if hoveredCard === 'development'}
            <div class="card-details" transition:fly={{ y: 20, duration: 300 }}>
              <h4>Children Development Unit</h4>
              <p>We focus on nurturing and developing children's skills and abilities through various programs and activities.</p>
            </div>
          {/if}
        </div>
        
        <div class="stat-card orange"
          on:mouseenter={() => hoveredCard = 'sponsored'} 
          on:mouseleave={() => hoveredCard = null}>
          <h3>530+</h3>
          <p>Sponsored Children</p>
          {#if hoveredCard === 'sponsored'}
            <div class="card-details" transition:fly={{ y: 20, duration: 300 }}>
              <h4>Sponsored Children</h4>
              <p>Our sponsorship program supports over 530 children, providing them with education and essential resources.</p>
            </div>
          {/if}
        </div>
      </div>
    </div>
  </section>
  
  <style>
    .who-we-are {
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
  
    .tag {
      display: inline-block;
      background-color: #DBEAFE;
      color: #004197;
      padding: 0.5rem 1rem;
      border-radius: 50px;
      font-size: 1.2rem;
      margin-bottom: 1.5rem;
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
  
    .learn-more {
      color: #ff6b00;
      text-decoration: none;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-weight: 500;
    }
  
    .arrow {
      transition: transform 0.3s ease;
    }
  
    .learn-more:hover .arrow {
      transform: translateX(5px);
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
      position: relative;
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
  
    .card-details {
      position: absolute;
      top: 10%;
      left: 5%;
      right: 0;
      background: white;
      padding: 1.5rem;
      border-radius: 1rem;
      box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
      z-index: 10;
      margin-top: 0.5rem;
      min-width: 300px;
    }
  
    .card-details h4 {
      font-size: 1.25rem;
      margin-bottom: 0.75rem;
      color: #000;
    }
  
    .card-details p {
      font-size: 0.875rem;
      color: #666;
      margin-bottom: 0;
    }
  
    @media (max-width: 968px) {
      .container {
        grid-template-columns: 1fr;
        gap: 3rem;
      }
  
      .left-content {
        max-width: 100%;
      }
  
      .card-details {
        min-width: 250px;
      }
    }
  
    @media (max-width: 580px) {
      .who-we-are {
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