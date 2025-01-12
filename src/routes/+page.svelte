<script>
    import Header from './header.svelte';
    import Who from './whoweare.svelte';
    import OurProgram from './ourprogram.svelte';
    import Partenrship from './partnership.svelte';
    import News from './news.svelte';
    import Newsletter from './newsletter.svelte';
    import Footer from './footer.svelte';
    import { scrollAnimation } from '$lib/scrollAnimation';
    import { fade, fly } from 'svelte/transition';
</script>
<Header />

<section class="hero-section">
    <div class="image-container" in:fade={{ duration: 1000, delay: 200 }}>
      <img src="./image1.png" alt="Hero Image" class="hero-image" />
    </div>
    <div class="content" 
         in:fly={{ y: 50, duration: 1000, delay: 800 }}
         use:scrollAnimation={{ animation: 'slideRight', delay: 300 }}>
      <h1>Building Brighter Futures<br>for Children and Communities</h1>
      <p>
        Empowering Ethiopian children, women, and people with disabilities<br>
        through education, care, and sustainable support.
      </p>
      <div class="buttons">
        <a href="https://docs.google.com/forms/d/e/1FAIpQLSc4ZuMzT9IX-1BuzhWawkH1V6uo0g4zrYc5ukJIKI5iu1T1ZQ/viewform?usp=dialog" 
           class="primary-btn" 
           target="_blank" 
           rel="noopener noreferrer">Get Involved</a>
      </div>
    </div>
</section>
<Who />
<OurProgram />
<Partenrship />
<News />
<Newsletter />
<Footer />
<style>
 .hero-section {
    position: relative;
    width: 100%;
    height: 100vh;
    color: white;
    display: flex;
    align-items: center;
    justify-content: flex-start; /* Change from center to flex-start */
    padding: 0 2rem;
  }
  
  .image-container {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
    z-index: 1;
  }
  
  .hero-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  
  .content {
    position: relative;
    z-index: 2;
    max-width: 1200px;
    margin-left: 3%;
    margin-top: 9%; /* Add bottom margin */
    text-align: left;
    padding-top: 4rem;
  }
  
  .content h1 {
    font-size: 4.5rem;
    line-height: 1.2;
    margin-bottom: 1.5rem;
    font-weight: 600;
  }
  
  .content p {
    font-size: 1.25rem;
    line-height: 1.6;
    margin-bottom: 2.5rem;
    opacity: 0.9;
  }
  
  .buttons {
    display: flex;
    gap: 1rem;
  }
  
  .primary-btn {
    padding: 1rem 2rem;
    font-size: 1.1rem;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 500;
    transition: all 0.3s ease;
  }
  
  .primary-btn {
    background-color: #fbbd23;
    color: #000;
  }
  
  .primary-btn:hover {
    background-color: #ffd15c;
  }

  @media (max-width: 768px) {
    .content h1 {
      font-size: 2rem;
    margin-bottom: 1rem;
    font-weight: 400;
    }
    
    .content p {
      font-size: 1rem;
    line-height: 1.6;
    margin-bottom: 1.3rem;
    opacity: 0.9;
    }
    .content {
    margin-left: 0%;
    margin-top: 50%; /* Add bottom margin */
    text-align: left;
    padding-top: 3rem;
  }
  
  }
</style>