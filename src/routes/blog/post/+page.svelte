<script>
    import Header from "./header.svelte";
    import Footer from "../../footer.svelte";
    import { page } from '$app/stores';

    const blogPosts = {
        'christian-horizon': {
            title: "Christian Horizon is Expanding",
            date: "15 October, 2024",
            readTime: "5 min read",
            image: "/img4.jpg",
            content: [
                {
                    heading: "Heading 1",
                    text: "Lorem ipsum dolor sit amet consectetur. Tortor sapien in cras risus placerat. Enim fermentum scelerisque sollicitudin eleifend dignissim consequat..."
                },
                {
                    heading: "Heading 2",
                    text: "Cras et dictum porttitor habitant eu. Tempor facilisis ut et suspendisse egestas..."
                },
                {
                    heading: "Heading 3",
                    text: "At mauris eu et ut consectetur. Maecenas nunc nibis ipsum placerat purus sit amet..."
                }
            ]
        },
        'supporting': {
            title: "Supporting Our Community",
            date: "10 October, 2024",
            readTime: "3 min read",
            image: "/img2.jpg",
            content: [
                {
                    heading: "Community Support",
                    text: "Nam sollicitudin sed tellus lorem. Lorem sit amet consectetur adipiscing elit..."
                },
                {
                    heading: "Our Impact",
                    text: "Dignissim vivamus nisi elit sollicitudin sed placerat sit tellus..."
                }
            ]
        }
    };

    // Use $page.url.searchParams instead of window.location
    const postType = $page.url.searchParams.get('type') || 'christian-horizon';
    const post = blogPosts[postType];

    function getOptimizedImageUrl(imageUrl, width = 800) {
        // Base Cloudinary URL (you'll need to sign up and get your cloud name)
        const cloudinaryUrl = "https://res.cloudinary.com/your-cloud-name/image/fetch/";
        
        // Image optimization parameters
        const params = [
            "f_auto", // automatic format selection
            "q_auto", // automatic quality selection
            `w_${width}`, // width
            "c_limit", // crop mode
        ].join(",");
        
        return `${cloudinaryUrl}${params}/${encodeURIComponent(imageUrl)}`;
    }
</script>

<Header darkMode={true} />

<main>
    <article class="blog-post">
        <h1>{post.title}</h1>
        <div class="post-meta">
            <span class="date">{post.date}</span>
            <span class="read-time">{post.readTime}</span>
        </div>

        <div class="featured-image">
            <img 
                src={getOptimizedImageUrl(post.image, 800)}
                srcset="
                    ${getOptimizedImageUrl(post.image, 400)} 400w,
                    ${getOptimizedImageUrl(post.image, 800)} 800w,
                    ${getOptimizedImageUrl(post.image, 1200)} 1200w
                "
                sizes="(max-width: 768px) 100vw, 800px"
                alt={post.title}
                loading="lazy"
            />
        </div>

        <div class="post-content">
            {#each post.content as section}
                <h2>{section.heading}</h2>
                <p>{section.text}</p>
            {/each}
        </div>
    </article>
</main>

<Footer />

<style>
    main {
        max-width: 1200px;
        margin: 0 auto;
        padding: 120px 2rem 4rem;
    }

    .blog-post {
        max-width: 800px;
        margin: 0 auto;
    }

    h1 {
        font-size: 3rem;
        margin-bottom: 1rem;
        color: #1a1a1a;
    }

    .post-meta {
        display: flex;
        gap: 1rem;
        color: #666;
        margin-bottom: 2rem;
    }

    .featured-image {
        margin: 2rem 0;
        border-radius: 12px;
        overflow: hidden;
        background: #f0f0f0;
        min-height: 300px;
        position: relative;
    }

    .featured-image img {
        width: 100%;
        height: auto;
        object-fit: cover;
        transition: opacity 0.3s ease;
    }

    .post-content {
        line-height: 1.8;
    }

    h2 {
        font-size: 2rem;
        margin: 2rem 0 1rem;
        color: #1a1a1a;
    }

    p {
        margin-bottom: 1.5rem;
        color: #4B5563;
    }

    @media (max-width: 768px) {
        main {
            padding: 100px 1rem 2rem;
        }

        h1 {
            font-size: 2rem;
        }

        h2 {
            font-size: 1.5rem;
        }
    }
</style> 