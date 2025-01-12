<script>
  import Header from '../header.svelte';
  import Footer from '../footer.svelte';
</script>

<div class="education-page">
  <Header darkMode={true} />

  <main>
    <section class="education-hero">
      <h1>Christian Horizon Education Program</h1>
      <p>Our education program provides comprehensive support and resources to empower individuals with exceptional needs, fostering an inclusive learning environment where every student can thrive and reach their full potential.</p>
      
      <div class="hero-image">
        <img src="./eduimg.jpg" alt="Christian Horizon Education Program Students">
      </div>
    </section>

    <section class="stats-section">
      <div class="stat-card">
        <h3>200+</h3>
        <p>Students Supported</p>
      </div>
      <div class="stat-card">
        <h3>45+</h3>
        <p>Dedicated Educators</p>
      </div>
      <div class="stat-card">
        <h3>15+</h3>
        <p>Years of Excellence</p>
      </div>
    </section>

    <section class="our-approach">
      <h2>Our Educational Approach</h2>
      <div class="approach-grid">
        <div class="approach-card">
          <div class="icon">🎯</div>
          <h3>Individualized Learning</h3>
          <p>Tailored educational plans that meet each student's unique needs and learning style.</p>
        </div>
        <div class="approach-card">
          <div class="icon">🤝</div>
          <h3>Inclusive Environment</h3>
          <p>Creating a supportive atmosphere where every student feels valued and respected.</p>
        </div>
        <div class="approach-card">
          <div class="icon">📚</div>
          <h3>Quality Education</h3>
          <p>Delivering high-standard education with modern teaching methodologies.</p>
        </div>
        <div class="approach-card">
          <div class="icon">🌱</div>
          <h3>Holistic Development</h3>
          <p>Focus on academic, social, and personal growth of each student.</p>
        </div>
      </div>
    </section>

    <section class="highlights">
      <h2>Program Highlights</h2>
      <p>Experience our comprehensive educational approach that empowers students to learn, grow, and excel.</p>
      
      <div class="image-grid">
        <img src="./eduimg1.jpg" alt="Education Program Activity 1">
        <img src="./eduimg2.jpg" alt="Education Program Activity 2">
        <img src="./eduimg3.jpg" alt="Education Program Activity 3">
        <img src="./eduimg4.jpg" alt="Education Program Activity 4">
      </div>
    </section>

    <section class="programs">
      <h2>Our Programs</h2>
      <div class="programs-container">
        <div class="program-card">
          <h3>Early Childhood Education</h3>
          <p>Foundation learning programs for young children focusing on essential developmental skills.</p>
          <a href="#" class="learn-more">Learn More →</a>
        </div>
        <div class="program-card">
          <h3>Special Education</h3>
          <p>Specialized support and resources for students with unique learning needs.</p>
          <a href="#" class="learn-more">Learn More →</a>
        </div>
        <div class="program-card">
          <h3>Vocational Training</h3>
          <p>Practical skills development preparing students for future employment opportunities.</p>
          <a href="#" class="learn-more">Learn More →</a>
        </div>
      </div>
    </section>

    <section class="cta-section">
      <div class="cta-content">
        <h2>Join Our Educational Community</h2>
        <p>Take the first step towards accessible education for all.</p>
        <div class="cta-buttons">
          <a href="#" class="btn-primary">Get Started</a>
          <a href="#" class="btn-secondary">Contact Us</a>
        </div>
      </div>
    </section>
  </main>

  <Footer />
</div>

<style>
  .education-page {
    background-color: white;
  }

  main {
    padding-top: 80px;
  }

  .education-hero {
    background-color: #f8f9fa;
    padding: 6rem 2rem;
    text-align: center;
    max-width: 100%;
    margin: 0 auto;
  }

  .education-hero h1 {
    font-size: 2.5rem;
    color: #004197;
    margin-bottom: 1.5rem;
  }

  .education-hero p {
    font-size: 1.2rem;
    color: #666;
    max-width: 800px;
    margin: 0 auto 2rem;
    line-height: 1.6;
  }

  .hero-image {
    max-width: 1000px;
    margin: 0 auto;
  }

  .hero-image img {
    width: 100%;
    height: auto;
    border-radius: 12px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
  }

  .stats-section {
    display: flex;
    justify-content: center;
    gap: 4rem;
    padding: 4rem 2rem;
    background-color: white;
    max-width: 1200px;
    margin: 0 auto;
  }

  .stat-card {
    text-align: center;
    padding: 2rem;
    background-color: #fff;
    border-radius: 12px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
    min-width: 200px;
  }

  .stat-card h3 {
    font-size: 2.5rem;
    color: #fbbd23;
    margin-bottom: 0.5rem;
  }

  .stat-card p {
    color: #666;
    font-size: 1.1rem;
  }

  .highlights {
    padding: 4rem 2rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .highlights h2 {
    text-align: center;
    color: #004197;
    font-size: 2rem;
    margin-bottom: 1rem;
  }

  .highlights > p {
    text-align: center;
    color: #666;
    max-width: 700px;
    margin: 0 auto 3rem;
    font-size: 1.1rem;
  }

  .image-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
    margin: 0 auto;
  }

  .image-grid img {
    width: 100%;
    height: 300px;
    object-fit: cover;
    border-radius: 12px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
  }

  .image-grid img:hover {
    transform: scale(1.02);
  }

  @media (max-width: 768px) {
    .education-hero {
      padding: 4rem 1rem;
    }

    .education-hero h1 {
      font-size: 2rem;
    }

    .stats-section {
      flex-direction: column;
      gap: 2rem;
      padding: 2rem 1rem;
    }

    .image-grid {
      grid-template-columns: 1fr;
      gap: 1rem;
    }

    .image-grid img {
      height: 250px;
    }
  }

  .our-approach {
    padding: 6rem 2rem;
    background-color: #f8f9fa;
  }

  .our-approach h2 {
    text-align: center;
    color: #004197;
    font-size: 2rem;
    margin-bottom: 3rem;
  }

  .approach-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .approach-card {
    background: white;
    padding: 2rem;
    border-radius: 12px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
    text-align: center;
    transition: transform 0.3s ease;
  }

  .approach-card:hover {
    transform: translateY(-5px);
  }

  .approach-card .icon {
    font-size: 2.5rem;
    margin-bottom: 1rem;
  }

  .approach-card h3 {
    color: #004197;
    margin-bottom: 1rem;
  }

  .approach-card p {
    color: #666;
    line-height: 1.6;
  }

  .programs {
    padding: 6rem 2rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .programs h2 {
    text-align: center;
    color: #004197;
    font-size: 2rem;
    margin-bottom: 3rem;
  }

  .programs-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
  }

  .program-card {
    background: #f8f9fa;
    padding: 2rem;
    border-radius: 12px;
    transition: transform 0.3s ease;
  }

  .program-card:hover {
    transform: translateY(-5px);
  }

  .program-card h3 {
    color: #004197;
    margin-bottom: 1rem;
  }

  .program-card p {
    color: #666;
    margin-bottom: 1.5rem;
    line-height: 1.6;
  }

  .learn-more {
    color: #fbbd23;
    text-decoration: none;
    font-weight: 600;
    transition: color 0.3s ease;
  }

  .learn-more:hover {
    color: #004197;
  }

  .cta-section {
    background-color: #004197;
    padding: 6rem 2rem;
    margin-top: 4rem;
  }

  .cta-content {
    max-width: 800px;
    margin: 0 auto;
    text-align: center;
    color: white;
  }

  .cta-content h2 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
  }

  .cta-content p {
    font-size: 1.2rem;
    margin-bottom: 2rem;
    opacity: 0.9;
  }

  .cta-buttons {
    display: flex;
    gap: 1rem;
    justify-content: center;
  }

  .btn-primary {
    background: #fbbd23;
    color: #000;
    padding: 1rem 2rem;
    border-radius: 8px;
    text-decoration: none;
    font-weight: 600;
    transition: transform 0.3s ease;
  }

  .btn-secondary {
    background: transparent;
    color: white;
    padding: 1rem 2rem;
    border-radius: 8px;
    text-decoration: none;
    font-weight: 600;
    border: 2px solid white;
    transition: all 0.3s ease;
  }

  .btn-primary:hover,
  .btn-secondary:hover {
    transform: translateY(-2px);
  }

  @media (max-width: 768px) {
    .approach-grid {
      grid-template-columns: 1fr;
    }

    .programs-container {
      grid-template-columns: 1fr;
    }

    .cta-buttons {
      flex-direction: column;
    }

    .cta-content h2 {
      font-size: 2rem;
    }
  }
</style>
