# Find-Your-Place-in-His-Presence
Spiritual Blog
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Find Your Place in His Presence</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: Arial, sans-serif; line-height: 1.6; background: #f4f4f9; color: #333; }
    header { background: #222; color: #fff; padding: 20px 0; text-align: center; }
    header h1 { font-size: 2rem; }
    nav ul { list-style: none; display: flex; justify-content: center; margin-top: 10px; }
    nav ul li { margin: 0 15px; }
    nav ul li a { color: #fff; text-decoration: none; font-weight: bold; }
    nav ul li a:hover { text-decoration: underline; }
    main { max-width: 900px; margin: 20px auto; padding: 0 20px; }
    .posts { display: grid; grid-template-columns: 1fr; gap: 30px; }
    .post { background: #fff; padding: 20px; border-radius: 10px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); transition: transform 0.2s; }
    .post:hover { transform: scale(1.02); }
    .post img { max-width: 100%; border-radius: 10px; margin-bottom: 15px; }
    .post h2 { margin-bottom: 10px; color: #222; }
    .post p { color: #555; }
    footer { text-align: center; padding: 20px; background: #222; color: #fff; margin-top: 40px; }
    .dark-mode { background: #121212; color: #f4f4f9; }
    .dark-mode header, .dark-mode footer { background: #1e1e1e; }
    .dark-mode .post { background: #1e1e1e; color: #f4f4f9; }
    #darkModeBtn { margin-top: 10px; padding: 5px 10px; cursor: pointer; background: #444; color: #fff; border: none; border-radius: 5px; }
    #darkModeBtn:hover { background: #666; }
  </style>
</head>
<body>

  <header>
    <h1>Find Your Place in His Presence</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
    <button id="darkModeBtn">Toggle Dark Mode</button>
  </header>

  <main id="home">
    <section class="posts" id="postsContainer">
      <!-- Posts will be dynamically loaded here -->
    </section>

    <section id="about" style="margin-top:50px;">
      <h2>About This Blog</h2>
      <p>This blog is dedicated to helping seekers find their place in His presence. Explore spiritual insights, mystical teachings, and sacred wisdom to awaken and deepen your connection with the Divine.</p>
    </section>

    <section id="contact" style="margin-top:50px;">
      <h2>Contact</h2>
      <p>Email: <a href="mailto:spiritualinsights@example.com">spiritualinsights@example.com</a></p>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Find Your Place in His Presence. All rights reserved.</p>
  </footer>

  <script>
    // Dark Mode Toggle
    const toggleBtn = document.getElementById('darkModeBtn');
    toggleBtn.addEventListener('click', () => {
      document.body.classList.toggle('dark-mode');
    });

    // Dynamic Posts
    const posts = [
      {
        title: "The Discipline of Receiving",
        img: "https://content.codecademy.com/courses/learn-html/elements-and-structure/profile.jpg",
        excerpt: "Explore how to receive divine guidance in daily life and open your heart to higher wisdom.",
        link: "#post1"
      },
      {
        title: "Mysteries of the Akashic Records",
        img: "https://content.codecademy.com/courses/learn-html/elements-and-structure/profile.jpg",
        excerpt: "Discover hidden knowledge about destiny, spiritual evolution, and accessing sacred records.",
        link: "#post2"
      },
      {
        title: "Peace as the First Principle",
        img: "https://content.codecademy.com/courses/learn-html/elements-and-structure/profile.jpg",
        excerpt: "Understand how peace forms the womb of harmony and governs the spiritual universe.",
        link: "#post3"
      }
    ];

    const postsContainer = document.getElementById('postsContainer');

    posts.forEach(post => {
      const postEl = document.createElement('article');
      postEl.className = 'post';
      postEl.innerHTML = `
        <img src="${post.img}" alt="${post.title}">
        <h2><a href="${post.link}">${post.title}</a></h2>
        <p>${post.excerpt}</p>
      `;
      postsContainer.appendChild(postEl);
    });
  </script>

</body>
</html>
