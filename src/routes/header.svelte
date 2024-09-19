<script>
    // You can add functionality for toggling dropdowns here
    let isProgramsOpen = false;
    let isAboutUsOpen = false;
    let isMediaOpen = false;
    let isInvolvedOpen = false;
  </script>
  
  <header class="header">
    <div class="container">
      <a href="/" class="logo">
        <img src="logo.png" alt="Christian Horizons Logo" class="logo-image">
      </a>
  
      <!-- Navigation Menu -->
      <nav class="nav">
        <a href="/" class="nav-item">Home</a>
        
        <!-- About Us Dropdown -->
        <div class="nav-item dropdown" on:mouseenter={() => isAboutUsOpen = true} on:mouseleave={() => isAboutUsOpen = false}>
            <span>About Us 
              <i class={isAboutUsOpen ? "fas fa-angle-up" : "fas fa-angle-down"}></i>
            </span>
            {#if isAboutUsOpen}
              <div class="dropdown-menu">
                <a href="/about/who-we-are" class="dropdown-item">Who We Are</a>
                <a href="/about/our-team" class="dropdown-item">Our Team</a>
              </div>
            {/if}
          </div>
          
          
          
        
        <!-- Programs Dropdown -->
        <div class="nav-item dropdown" on:mouseenter={() => isProgramsOpen = true} on:mouseleave={() => isProgramsOpen = false}>
          <span>Programs</span>
          <i class={isProgramsOpen ? "fas fa-angle-up" : "fas fa-angle-down"}></i>
          {#if isProgramsOpen}
            <div class="dropdown-menu">
              <a href="/programs/our-work" class="dropdown-item">Our Work</a>
              <hr>
              <a href="/programs/projects" class="dropdown-item">Projects</a>
            </div>
          {/if}
        </div>
  
        <!-- Get Involved Dropdown -->
        <div class="nav-item dropdown" on:mouseenter={() => isInvolvedOpen = true} on:mouseleave={() => isInvolvedOpen = false}>
          <span>Get Involved</span>
          <i class={isInvolvedOpen ? "fas fa-angle-up" : "fas fa-angle-down"}></i>
          {#if isInvolvedOpen}
            <div class="dropdown-menu">
              <a href="/involved/volunteer" class="dropdown-item">Volunteer</a>
              <hr>
              <a href="/involved/donate" class="dropdown-item">Donate</a>
            </div>
          {/if}
        </div>
  
        <!-- Media & Resources Dropdown -->
        <div class="nav-item dropdown" on:mouseenter={() => isMediaOpen = true} on:mouseleave={() => isMediaOpen = false}>
          <span>Media & Resources</span>
          <i class={isMediaOpen ? "fas fa-angle-up" : "fas fa-angle-down"}></i>
          {#if isMediaOpen}
            <div class="dropdown-menu">
              <a href="/media/videos" class="dropdown-item">Videos</a>
              <hr>
              <a href="/media/blogs" class="dropdown-item">Blogs</a>
            </div>
          {/if}
        </div>
  
        <a href="/contact" class="nav-item">Contact Us</a>
      </nav>
  
      <!-- Donate Button -->
      <a href="/donate" class="btn btn-donate">Donate</a>
    </div>
  </header>
  
  <style>
    /* Basic header and container setup */
    .header {
      background-color: white;
      padding: 0.5rem 2rem;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 10;
    }
  
    .container {
      width: 100%;
      max-width: 85%;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  
    /* Logo */
    .logo-image {
      height: 65px;
    }
    /* Navigation Menu */
    .nav {
      display: flex;
      align-items: center;
      height: 100%;
      gap: 2rem;
    }
  
    .nav-item {
      color: #00093e;
      text-decoration: none;
      font-weight: 500;
      font-size: 1.1rem;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      height: 65px;
      position: relative;
      cursor: pointer;
    }
  /* Style for dropdown icons */
.nav-item i {
  margin-left: 0.5rem; /* Space between text and icon */
  font-size: 0.9rem; /* Adjust size */
  transition: transform 0.2s ease-in-out;
  animation: .3s;
}

.nav-item:hover i {
  transform: rotate(0deg); /* Reset transform */
}

    /* Dropdown menu */
    /* Dropdown menu - Show under the header */
/* Dropdown menu - adjust position under the header */
.dropdown-menu {
  position: absolute;
  top: 100%; /* Ensures it starts just below the header */
  left: 0;
  text-align: start;
  background-color: white;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
  border-radius: 0px; /* No border radius to fill the entire box */
  display: flex;
  flex-direction: column;
  border-radius: 10px;
  width: 200px;
  padding: 0; /* Remove padding */
}

/* Full-width hover effect for dropdown items */
.dropdown-item {
  padding: 1rem;
  color: #00093e;
  text-decoration: none;
  width: 100%;
}

.dropdown-item:hover {
  background-color: #001068;
  color: white;
  
  padding: 1rem; /* Ensure padding stays consistent on hover */
}

  
   /* Gradient Donate Button with logo colors */
.btn-donate {
  background: linear-gradient(90deg, #0066cc, #ff6f00); /* Blue to Orange gradient */
  color: white;
  padding: 0.8rem 2rem;
  text-decoration: none;
  border-radius: 10px;
  font-weight: 600;
  border: none;
  cursor: pointer;
}

/* Hover Effect - reverse gradient */
.btn-donate:hover {
  background: linear-gradient(90deg, #ff6f00, #00509e); /* Orange to Blue on hover */
  color: white;
}


  </style>
  