<script>
    import { onMount } from 'svelte';
    let lastScrollY = 0;
  let isHeaderVisible = true;
  let isScrollingUp = false;
  let isMobileMenuOpen = false;

  // Existing dropdown states
  let isProgramsOpen = false;
  let isAboutUsOpen = false;
  let isMediaOpen = false;
  let isInvolvedOpen = false;

  function handleScroll() {
    const currentScrollY = window.scrollY;
    isScrollingUp = currentScrollY < lastScrollY;
    
    // Show header when scrolling up or at top of page
    if (isScrollingUp || currentScrollY === 0) {
      isHeaderVisible = true;
    } else {
      isHeaderVisible = false;
    }
    
    lastScrollY = currentScrollY;
  }

  function toggleMobileMenu() {
    isMobileMenuOpen = !isMobileMenuOpen;
    // Prevent body scroll when menu is open
    if (isMobileMenuOpen) {
      document.body.style.overflow = 'hidden';
    } else {
      document.body.style.overflow = 'auto';
    }
  }

  onMount(() => {
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
    return () => {
      document.body.style.overflow = 'auto';
    };
  });
  </script>
  
  <header class="header" class:visible={isHeaderVisible} class:scrolled={lastScrollY > 0}>
    <div class="container">
      <a href="/" class="logo">
        <img src="logo.png" alt="Christian Horizons Logo" class="logo-image">
      </a>
   <!-- Hamburger Menu Button -->
   <button class="mobile-menu-btn" on:click={toggleMobileMenu}>
    <span class="hamburger" class:active={isMobileMenuOpen}>
      <span></span>
      <span></span>
      <span></span>
    </span>
  </button>
      <!-- Navigation Menu -->
      <nav class="nav" class:mobile-open={isMobileMenuOpen}>
        <a href="/" class="nav-item">Home</a>
        
        <!-- About Us Dropdown -->
        <div class="nav-item dropdown" on:mouseenter={() => isAboutUsOpen = true} on:mouseleave={() => isAboutUsOpen = false}>
            <span>About Us 
              
            </span>
            
          </div>
        <!-- Programs Dropdown -->
        <div class="nav-item dropdown" on:mouseenter={() => isProgramsOpen = true} on:mouseleave={() => isProgramsOpen = false}>
          <span>Programs</span>
          <i class={isProgramsOpen ? "fas fa-angle-up" : "fas fa-angle-down"}></i>
          {#if isProgramsOpen}
            <div class="dropdown-menu">
              <a href="#" class="dropdown-item">Disability</a>
              <hr>
              <a href="#" class="dropdown-item">economic power</a>
              <hr>
              <a href="#" class="dropdown-item">Education</a>
            </div>
          {/if}
        </div>
  
        <!-- Get Involved Dropdown -->
        <div class="nav-item dropdown" on:mouseenter={() => isInvolvedOpen = true} on:mouseleave={() => isInvolvedOpen = false}>
          <span>IG</span>
          <i class={isInvolvedOpen ? "fas fa-angle-up" : "fas fa-angle-down"}></i>
          {#if isInvolvedOpen}
            <div class="dropdown-menu">
              <a href="#" class="dropdown-item">Horizon school</a>
            </div>
          {/if}
        </div>
  
        <!-- Media & Resources Dropdown -->
        <div class="nav-item dropdown" on:mouseenter={() => isMediaOpen = true} on:mouseleave={() => isMediaOpen = false}>
          <span>Vlog & Media </span>
          <i class={isMediaOpen ? "fas fa-angle-up" : "fas fa-angle-down"}></i>
          {#if isMediaOpen}
            <div class="dropdown-menu">
              <a href="#" class="dropdown-item">Videos</a>
              <hr>
              <a href="#" class="dropdown-item">Blogs</a>
            </div>
          {/if}
        </div>
  
        <a href="#" class="nav-item">Contact Us</a>
        <a href="#" class="btn-donate mobile-donate">Donate Now</a>
      </nav>
  
      <!-- Donate Button -->
      <a href="#" class="btn-donate desktop-donate">Donate Now</a>
    </div>
  </header>
  
  <style>
.header {
  background-color: rgba(0, 0, 0, 0.171);
  padding: 0.5rem 2rem;
  box-shadow: 0 2px 10px rgba(255, 255, 255, 0.1);
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  transform: translateY(-100%);
    transition: transform 0.3s ease;
  z-index: 1000; /* High z-index to ensure it overlays other elements */
}
/* Dropdown menu - Ensure proper alignment and stacking */

.header.visible {
    transform: translateY(0);
  }

  .header.scrolled {
    backdrop-filter: blur(10px);
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    position: fixed;
  }
    .container {
      width: 100%;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  
    /* Logo */
    .logo-image {
      height: 60px;
    }
    /* Navigation Menu */
    .nav {
      display: flex;
      align-items: center;
      height: 100%;
      gap: 2rem;
    }
  
    .nav-item {
      color: white;
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
  border-radius: 10px;
  flex-direction: column;
  width: 200px;
  padding: 0; /* Remove padding */
}

/* Full-width hover effect for dropdown items */
.dropdown-item {
  padding: 1rem;
  color: #00093e;
  text-decoration: none;
  width: 100%;
  cursor: pointer;
}

.dropdown-item:hover {
  background-color: #eeeeee;
  
  padding: 1rem; /* Ensure padding stays consistent on hover */
}

  .dropdown-menu hr{
    width: 100%;
    border: 1px solid #f6f6f6;
  }
   /* Gradient Donate Button with logo colors */
.btn-donate {
  background: #fbbd23; /* Blue to Orange gradient */
  color: black;
  padding: 0.8rem 2rem;
  text-decoration: none;
  border-radius: 10px;
  font-weight: 600;
  border: none;
  transition: all 0.3s ease;
  cursor: pointer;
}

/* Hover Effect - reverse gradient */
.btn-donate:hover {
  transition: all 0.3s ease;
  background-color: #ffcb48;
}
.mobile-menu-btn {
    display: none;
    background: none;
    border: none;
    cursor: pointer;
    padding: 10px;
    z-index: 1001;
  }

  .hamburger {
    display: flex;
    flex-direction: column;
    gap: 6px;
    width: 30px;
  }

  .hamburger span {
    display: block;
    width: 100%;
    height: 2px;
    background-color: white;
    transition: all 0.3s ease;
  }
  .hamburger.active span {
    background-color: #000; /* Changes to black when menu is open */
  }

  .hamburger.active span:nth-child(1) {
    transform: rotate(45deg) translate(7px, 7px);
  }

  .hamburger.active span:nth-child(2) {
    opacity: 0;
  }

  .hamburger.active span:nth-child(3) {
    transform: rotate(-45deg) translate(7px, -7px);
  }

  .mobile-donate {
    display: none;
  }
  @media (max-width: 1124px){
    .nav{
      gap: 1rem;
    }
    .nav-item {
      font-size: .9rem;
    }
  /* Style for dropdown icons */
.nav-item i {
  margin-left: 0.5rem; /* Space between text and icon */
  font-size: 0.9rem; /* Adjust size */
  transition: transform 0.2s ease-in-out;
  animation: .3s;
}
  }
  @media (max-width: 950px) {
    .mobile-menu-btn {
      display: block;
    }

    .desktop-donate {
      display: none;
    }
    .mobile-donate {
      display: block;
      margin-top: 3rem;
    }
   
    .nav {
      position: fixed;
      top: 0;
      left: 0;
      height: 100vh;
      right: 0;
      bottom: 0;
      background-color: white;
      flex-direction: column;
      padding: 80px 2rem 2rem;
      transform: translateX(-100%);
      transition: transform 0.3s ease;
      z-index: 99;
      overflow-y: auto; /* Allow scrolling within the menu if needed */
    }

    .nav.mobile-open {
      transform: translateX(0);
    }

    .nav-item {
      color: #00093e;
      padding: 1rem 0;
      width: 100%;
      font-size: 1rem;
      text-align: left;
      border-bottom: 1px solid #dfdfdf;
    }

    .dropdown {
      width: 100%;
    }
    .container {
      padding: 0 1rem;
    }

    .logo-image {
      height: 40px; /* Smaller logo for mobile */
    }
    .dropdown-menu {
    position: absolute; /* Ensure it's correctly positioned relative to the dropdown */
    top: 0;
    left: 0;
    z-index: 10;
    background-color: white;
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
    width: 100%; /* Ensure the dropdown fills the available space */
    display: flex;
    flex-direction: column;
  }

  .dropdown-item {
    width: 100%; /* Ensure it takes full width on mobile */
  }
  }

  </style>
  