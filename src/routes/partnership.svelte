<section class="partners">
  <div class="container">
    <div class="left-content">
      <span class="tag">Partnerships & Sponsorships</span>
      
      <div class="partners-header">
        <h2>Our Partners</h2>
        <p>
          We collaborate with national and international organizations to achieve
          our mission of empowering marginalized communities.
        </p>
      </div>
    </div>

    <div class="partner-logos">
      <img src="/karis.png" alt="Karis Disability Services" class="karis-logo" />
      <div class="secondary-logos">
        <img src="/lmi.png" alt="Leadership Management International" />
        <img src="/wise.png" alt="Wise" />
      </div>
    </div>
  </div>

  <div class="cta-container">
    <div class="cta-section">
      <div class="cta-card">
        <h3>Volunteer</h3>
        <p>
          Join us as a volunteer and help us uplift vulnerable communities through
          education, rehabilitation, and socio-economic support.
        </p>
        <button class="cta-button">Get Involved</button>
      </div>

      <div class="cta-card">
        <h3>Donate</h3>
        <p>
          Your donation helps us provide essential services to children, women,
          and people with disabilities, making a lasting impact.
        </p>
        <button class="cta-button">Donate Now</button>
      </div>

      <img 
        src="/decorative-arrow.svg" 
        alt="" 
        class="decorative-arrow" 
        aria-hidden="true"
      />
      <span class="join-text">Join us in<br>making difference</span>
    </div>
  </div>
</section>

<style>
  .partners {
    padding: 3rem 2rem;
    background-color: white;
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    align-items: center;
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

  .partners-header {
    max-width: 600px;
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

  .partner-logos {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    gap: 3rem;
  }

  .partner-logos img {
    height: 100px;
    object-fit: contain;
  }

  .cta-container {
    padding: 2rem 2rem;
    margin-top: 5rem;
  }

  .cta-section {
    max-width: 1200px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    position: relative;
  }

  .cta-card {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  h3 {
    font-size: 1.8rem;
    color: #004197;
    font-weight: 600;
  }

  .cta-button {
    background-color: #FFB800;
    color: #000;
    padding: 0.8rem 2rem;
    border-radius: 50px;
    border: none;
    font-weight: 500;
    font-size: 1rem;
    cursor: pointer;
    align-self: flex-start;
    transition: background-color 0.3s ease;
  }

  .cta-button:hover {
    background-color: #FFA600;
  }

  .decorative-arrow {
    position: absolute;
    bottom: -50px;
    left: 160px;
    width: 150px;
  }

  .join-text {
    position: absolute;
    bottom: -60px;
    left: 320px;
    color: #FF6B00;
    font-size: 1.2rem;
    font-style: italic;
    line-height: 1.2;
  }

  @media (max-width: 968px) {
    .container {
      grid-template-columns: 1fr;
      gap: 2rem;
      padding: 0 1rem;
    }
    .left-content {
      text-align: left;
    }

    .partner-logos {
      align-items: start;
      text-align: start;
      display: grid;
      margin: 0 auto;
    }
    .decorative-arrow {
    position: absolute;
    bottom: 230px;
    left: 160px;
    width: 100px;
  }

  .join-text {
    bottom: 210px;
    left: 250px;
  }
    .karis-logo{
      justify-content: start;
      text-align: start;
    }

    .secondary-logos {
      justify-content: start;
      width: 100%;
    }

    .cta-section {
      grid-template-columns: 1fr;
      gap: 4rem;
      padding: 0 1rem;
      text-align: left;
    }

    .cta-card {
      text-align: left;
    }
  }

  @media (max-width: 580px) {
    .partners,
    .cta-container {
      padding: 2rem 1rem;
      margin-top: 2rem;
    }

    .partners-header {
      text-align: left;
    }

    .tag {
      display: inline-block;
    }
  }
</style> 