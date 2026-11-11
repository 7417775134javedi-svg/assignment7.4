Here is the complete, production-ready solution for Assignment 7.4 — Modern Landing Page Header & Hero Section.

The code below is packaged into a single, self-contained index.html file that fulfills all requirements, including a sticky header, side-by-side Flexbox hero layout, a styled footer, and media queries for mobile responsiveness.

Complete Code (index.html)
You can save this code as an index.html file on your computer and open it in any web browser to test the layout.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.4 — Modern Landing Page Header & Hero</title>
    <style>
        /* Global Reset & Typography */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f8fafc;
            color: #1e293b;
            line-height: 1.6;
        }

        /* Step 6: Sticky Header Section */
        header {
            position: sticky;
            top: 0;
            background-color: #ffffff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 5%;
        }

        /* Step 1: Logo Styling */
        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: #2563eb;
            text-decoration: none;
        }

        /* Step 1: Navigation Links */
        .nav-links {
            list-style: none;
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: #475569;
            font-weight: 500;
            transition: color 0.2s ease;
        }

        .nav-links a:hover {
            color: #2563eb;
        }

        /* Step 1: Header CTA Button */
        .btn-header {
            background-color: #2563eb;
            color: #ffffff;
            border: none;
            padding: 10px 20px;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.2s ease;
        }

        .btn-header:hover {
            background-color: #1d4ed8;
        }

        /* Hero Section Container */
        .hero-section {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 80px 5%;
            max-width: 1280px;
            margin: 0 auto;
            gap: 50px;
        }

        /* Step 2 & 5: Hero Text & Content Alignment */
        .hero-content {
            flex: 1;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
        }

        .hero-content h1 {
            font-size: 3rem;
            font-weight: 800;
            color: #0f172a;
            line-height: 1.2;
            margin-bottom: 20px;
        }

        .hero-content p {
            font-size: 1.15rem;
            color: #64748b;
            margin-bottom: 30px;
        }

        /* Step 2: Hero CTA Button */
        .btn-hero {
            background-color: #0f172a;
            color: #ffffff;
            border: none;
            padding: 14px 28px;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.2s ease;
        }

        .btn-hero:hover {
            background-color: #334155;
        }

        /* Step 3: Illustration / Image */
        .hero-image-container {
            flex: 1;
            display: flex;
            justify-content: center;
        }

        .hero-image-container img {
            width: 100%;
            max-width: 500px;
            height: auto;
            border-radius: 12px;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }

        /* Step 6: Footer Styling using earlier CSS concepts */
        footer {
            background-color: #0f172a;
            color: #94a3b8;
            text-align: center;
            padding: 30px 20px;
            margin-top: 50px;
            font-size: 0.9rem;
        }

        /* Step 7: Media Queries for Responsiveness across different widths */
        @media (max-width: 900px) {
            .hero-section {
                flex-direction: column-reverse; /* Stack image on top or text on top depending on layout choice */
                text-align: center;
                padding: 40px 5%;
            }

            .hero-content {
                align-items: center;
            }

            .hero-content h1 {
                font-size: 2.2rem;
            }

            .nav-links {
                display: none; /* Hides standard nav on smaller screens (simplification for mobile) */
            }
        }
    </style>
</head>
<body>

    <!-- Step 1 & 6: Sticky Header with Logo, Navigation, and CTA -->
    <header>
        <a href="#" class="logo">BrandName</a>
        <ul class="nav-links">
            <li><a href="#">Home</a></li>
            <li><a href="#">Features</a></li>
            <li><a href="#">Pricing</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
        <button class="btn-header">Get Started</button>
    </header>

    <!-- Step 2, 3, 4, 5: Hero Section (Side-by-side Flexbox layout) -->
    <main class="hero-section">
        <div class="hero-content">
            <h1>Build Better Products Faster</h1>
            <p>Empower your workflow with our modern SaaS platform. Scale seamlessly, collaborate in real-time, and drive growth with data-driven insights.</p>
            <button class="btn-hero">Start Free Trial</button>
        </div>
        <div class="hero-image-container">
            <img src="https://picsum.photos/seed/dashboard/600/450" alt="Platform Dashboard Illustration">
        </div>
    </main>

    <!-- Step 6: Footer Section -->
    <footer>
        <p>&copy; 2026 BrandName Inc. All rights reserved. Built with HTML & Flexbox.</p>
    </footer>

</body>
</html>
How Each Assignment Step is Implemented:
Header Elements: Implemented inside the <header> element using a Flexbox layout (justify-content: space-between), containing a .logo, a list of .nav-links, and a .btn-header CTA button.

Hero Text Content: Created a main heading (<h1>), a descriptive paragraph (<p>), and a primary .btn-hero action button inside the .hero-content container.

Illustration/Image: Included a high-quality dashboard image placeholder using an <img> tag wrapped inside .hero-image-container.

Side-by-side Flexbox Arrangement: Applied display: flex; on .hero-section to cleanly divide the screen space evenly between the text column and the image column.

Proper Alignment: Used align-items: center; and controlled margins/gaps so the text and image balance visually across the viewport.

Sticky Section / Footer: Made the navigation header position: sticky; top: 0; so it stays locked to the top during scrolling, and styled a clean slate-colored footer.

Responsive Layout Checks (@media (max-width: 900px)): Added a media query that transforms the side-by-side layout into a stacked column structure on smaller screens and mobile widths.
