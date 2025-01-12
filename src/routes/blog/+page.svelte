<script>
    import Header from "../Header.svelte";
    import Footer from "../Footer.svelte";

    const blogPosts = [
        {
            id: 1,
            title: "Christian Horizon is Expanding",
            date: "15 October, 2024",
            readTime: "5 min read",
            image: "/img4.jpg",
            excerpt: "Lorem ipsum dolor sit amet consectetur. Tortor sapien in cras risus placerat. Enim fermentum scelerisque sollicitudin eleifend dignissim consequat.",
            type: "christian-horizon"
        },
        {
            id: 2,
            title: "Supporting Our Community",
            date: "10 October, 2024",
            readTime: "3 min read",
            image: "/img2.jpg",
            excerpt: "Nam sollicitudin sed tellus lorem. Lorem sit amet consectetur adipiscing elit. Dignissim vivamus nisi elit sollicitudin sed placerat.",
            type: "supporting"
        },
        // Add more blog posts here
    ];
</script>

<Header darkMode={true} />

<main>
    <section class="blog-header">
        <h1>Latest News</h1>
        <p>Stay updated with our latest stories and community impact</p>
    </section>

    <section class="blog-grid">
        {#each blogPosts as post}
            <article class="blog-card">
                <a href="/blog/post?type={post.type}" class="card-link">
                    <div class="card-image">
                        <img src={post.image} alt={post.title} />
                    </div>
                    <div class="card-content">
                        <div class="post-meta">
                            <span class="date">{post.date}</span>
                            <span class="read-time">{post.readTime}</span>
                        </div>
                        <h2>{post.title}</h2>
                        <p>{post.excerpt}</p>
                        <span class="read-more">Read more →</span>
                    </div>
                </a>
            </article>
        {/each}
    </section>
</main>

<Footer />

<style>
    main {
        max-width: 1200px;
        margin: 0 auto;
        padding: 120px 2rem 4rem;
    }

    .blog-header {
        text-align: center;
        margin-bottom: 4rem;
    }

    .blog-header h1 {
        font-size: 3rem;
        margin-bottom: 1rem;
        color: #1a1a1a;
    }

    .blog-header p {
        color: #666;
    }

    .blog-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
        gap: 2rem;
    }

    .blog-card {
        background: white;
        border-radius: 12px;
        overflow: hidden;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        transition: transform 0.3s ease;
    }

    .blog-card:hover {
        transform: translateY(-5px);
    }

    .card-link {
        text-decoration: none;
        color: inherit;
    }

    .card-image {
        width: 100%;
        height: 200px;
        overflow: hidden;
    }

    .card-image img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    .card-content {
        padding: 1.5rem;
    }

    .post-meta {
        display: flex;
        gap: 1rem;
        color: #666;
        font-size: 0.9rem;
        margin-bottom: 1rem;
    }

    .blog-card h2 {
        font-size: 1.5rem;
        margin-bottom: 1rem;
        color: #1a1a1a;
    }

    .blog-card p {
        color: #4B5563;
        margin-bottom: 1.5rem;
        line-height: 1.6;
    }

    .read-more {
        color: #1E40AF;
        font-weight: 500;
    }

    @media (max-width: 768px) {
        main {
            padding: 100px 1rem 2rem;
        }

        .blog-header h1 {
            font-size: 2rem;
        }

        .blog-grid {
            grid-template-columns: 1fr;
        }
    }
</style>
