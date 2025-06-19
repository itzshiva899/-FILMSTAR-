# -FILMSTAR-
# folder structure 
filmstar/
├── index.html
├── style.css
├── assets/
│   └── logo.png  <-- (Use your uploaded FILMSTAR logo here)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>FILMSTAR</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <img src="assets/logo.png" alt="FILMSTAR Logo" class="logo" />
    <nav>
      <ul>
        <li>Home</li>
        <li>Movies</li>
        <li>Genres</li>
        <li>Languages</li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="movie-row">
      <h2>Latest Movies</h2>
      <div class="movies">
        <div class="movie-card">
          <img src="https://via.placeholder.com/150x220" alt="Movie 1" />
          <p>Movie Title 1</p>
        </div>
        <div class="movie-card">
          <img src="https://via.placeholder.com/150x220" alt="Movie 2" />
          <p>Movie Title 2</p>
        </div>
        <!-- Add more cards -->
      </div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 FILMSTAR</p>
  </footer>
</body>
</html>
style.css
body {
  margin: 0;
  background-color: #0b0b0b;
  color: #fff;
  font-family: 'Segoe UI', sans-serif;
}

header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: #111;
  padding: 10px 20px;
}

.logo {
  width: 120px;
}

nav ul {
  list-style: none;
  display: flex;
  gap: 20px;
}

nav li {
  cursor: pointer;
  color: #ccc;
}

nav li:hover {
  color: #fff;
}

.movie-row {
  padding: 20px;
}

.movie-row h2 {
  margin-bottom: 10px;
}

.movies {
  display: flex;
  gap: 15px;
  overflow-x: auto;
  padding-bottom: 10px;
}

.movie-card {
  min-width: 150px;
  background: #222;
  border-radius: 8px;
  overflow: hidden;
  text-align: center;
}

.movie-card img {
  width: 100%;
  height: auto;
  display: block;
}

.movie-card p {
  padding: 5px;
  font-size: 14px;
}

footer {
  text-align: center;
  padding: 15px;
  background-color: #111;
  color: #888;
}

# update folder structure 
filmstar/
├── index.html
├── movie.html
├── style.css
├── assets/
│   ├── logo.png
│   └── movies/ (movie posters go here)

imdex.html ( search+filter)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>FILMSTAR</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>
  <header>
    <img src="assets/logo.png" alt="FILMSTAR Logo" class="logo" />
    <input type="text" placeholder="Search movies..." class="search-box"/>
  </header>

  <section class="filters">
    <button>All</button>
    <button>Action</button>
    <button>Drama</button>
    <button>Comedy</button>
    <button>Hindi</button>
    <button>Bengali</button>
  </section>

  <main>
    <section class="movie-row">
      <h2>Latest Releases</h2>
      <div class="movies">
        <a href="movie.html" class="movie-card">
          <img src="https://via.placeholder.com/150x220" alt="Movie 1"/>
          <p>Movie Title 1</p>
        </a>
        <a href="movie.html" class="movie-card">
          <img src="https://via.placeholder.com/150x220" alt="Movie 2"/>
          <p>Movie Title 2</p>
        </a>
      </div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 FILMSTAR</p>
  </footer>
</body>
</html>

# movie html (movie details page)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Movie Details - FILMSTAR</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>
  <header>
    <img src="assets/logo.png" alt="FILMSTAR Logo" class="logo" />
  </header>

  <main class="movie-detail">
    <img src="https://via.placeholder.com/200x300" alt="Movie Poster" class="poster"/>
    <div class="info">
      <h1>Movie Title</h1>
      <p><strong>Genres:</strong> Action, Thriller</p>
      <p><strong>Language:</strong> Hindi</p>
      <p><strong>Year:</strong> 2025</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Exciting story description here.</p>
      <a href="#" class="btn download">Download</a>
      <a href="#" class="btn watch">Watch Online</a>
    </div>
  </main>
</body>
</html>
# style.css (extra additions)
.search-box {
  padding: 8px 12px;
  margin-left: 10px;
  background: #1a1a1a;
  border: 1px solid #444;
  color: white;
  border-radius: 5px;
}

.filters {
  display: flex;
  gap: 10px;
  padding: 10px 20px;
  flex-wrap: wrap;
}

.filters button {
  background: #222;
  color: #fff;
  border: none;
  padding: 6px 12px;
  border-radius: 4px;
  cursor: pointer;
}

.filters button:hover {
  background: #e50914;
}

.movie-detail {
  display: flex;
  gap: 20px;
  padding: 20px;
}

.movie-detail .poster {
  width: 200px;
  border-radius: 8px;
}

.movie-detail .info {
  max-width: 600px;
}

.btn {
  display: inline-block;
  margin-top: 10px;
  padding: 10px 15px;
  background-color: #e50914;
  color: #fff;
  text-decoration: none;
  border-radius: 4px;
  margin-right: 10px;
}

.btn:hover {
  background-color: #ff1f29;
}

 # comment system ( no background+ basic)
<section class="comments">
  <h2>Comments</h2>
  <textarea id="commentInput" placeholder="Write a comment..."></textarea>
  <button onclick="postComment()">Post</button>
  <ul id="commentList"></ul>
</section>

<script>
  function postComment() {
    const input = document.getElementById("commentInput");
    const list = document.getElementById("commentList");
    const text = input.value.trim();
    if (text !== "") {
      const li = document.createElement("li");
      li.textContent = text;
      list.appendChild(li);
      input.value = "";
    }
  }
</script>
add in style.css 
.comments {
  margin-top: 30px;
}

.comments textarea {
  width: 100%;
  height: 80px;
  padding: 10px;
  border-radius: 5px;
  background-color: #1a1a1a;
  border: 1px solid #444;
  color: #fff;
}

.comments button {
  margin-top: 10px;
  background-color: #e50914;
  border: none;
  padding: 8px 15px;
  color: white;
  border-radius: 4px;
  cursor: pointer;
}

.comments ul {
  list-style: none;
  padding: 0;
  margin-top: 15px;
}

.comments li {
  background: #222;
  padding: 10px;
  margin-bottom: 8px;
  border-radius: 4px;
}

# Android app version (webviews)
# java code android studio 
import android.os.Bundle;
import android.webkit.WebView;
import android.webkit.WebViewClient;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    WebView webView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        webView = new WebView(this);
        setContentView(webView);
        webView.getSettings().setJavaScriptEnabled(true);
        webView.setWebViewClient(new WebViewClient());
        webView.loadUrl("https://yourfilmstarwebsite.com"); // Replace with your actual URL
    }
}

also update Android manifext.xml
<uses-permission android:name="android.permission.INTERNET" />

# language switcher 
 # EXAMPLE UI 
 <select id="languageSwitcher" onchange="switchLanguage(this.value)">
  <option value="en">English</option>
  <option value="hi">हिन्दी</option>
  <option value="bn">বাংলা</option>
</select>
# ADD THIS SCRIPT 
<script>
  const translations = {
    en: {
      title: "Movie Title",
      genre: "Genres",
      lang: "Language",
    },
    hi: {
      title: "फ़िल्म का नाम",
      genre: "शैली",
      lang: "भाषा",
    },
    bn: {
      title: "ছবির নাম",
      genre: "বিভাগ",
      lang: "ভাষা",
    }
  };

  function switchLanguage(lang) {
    document.getElementById("movieTitle").textContent = translations[lang].title;
    document.getElementById("genreLabel").textContent = translations[lang].genre;
    document.getElementById("langLabel").textContent = translations[lang].lang;
  }
</script>

# add in your HTML content 
<h1 id="movieTitle">Movie Title</h1>
<p><strong id="genreLabel">Genres:</strong> Action, Thriller</p>
<p><strong id="langLabel">Language:</strong> Hindi</p>

# INDEX FIREBASE SDK
<script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-firestore-compat.js"></script>

# firebase config & initialization
<script>
  const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_DOMAIN",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_BUCKET",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
  };

  firebase.initializeApp(firebaseConfig);
  const db = firebase.firestore();

  const commentList = document.getElementById("commentList");

  function postComment() {
    const input = document.getElementById("commentInput");
    const text = input.value.trim();
    if (text !== "") {
      db.collection("comments").add({
        text,
        created: new Date()
      });
      input.value = "";
    }
  }

  db.collection("comments").orderBy("created").onSnapshot(snapshot => {
    commentList.innerHTML = "";
    snapshot.forEach(doc => {
      const li = document.createElement("li");
      li.textContent = doc.data().text;
      commentList.appendChild(li);
    });
  });
</script>
# DOWNLOAD POPUP BOX
<button onclick="showDownloadPopup()" class="btn download">Download</button>

<div class="popup-overlay" id="popupOverlay">
  <div class="popup-box">
    <h3>Select Download Link</h3>
    <a href="https://drive.google.com" target="_blank" class="popup-btn">Google Drive</a>
    <a href="https://streamsb.net" target="_blank" class="popup-btn">StreamSB</a>
    <button onclick="hideDownloadPopup()">Close</button>
  </div>
</div>
add this css 
.popup-overlay {
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.8);
  display: none;
  align-items: center;
  justify-content: center;
  z-index: 1000;
}

.popup-box {
  background: #1a1a1a;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  color: white;
}

.popup-btn {
  display: block;
  background: #e50914;
  color: white;
  padding: 10px;
  margin: 10px 0;
  border-radius: 5px;
  text-decoration: none;
}

.popup-btn:hover {
  background: #ff1f29;
}
ad this JS 
<script>
  function showDownloadPopup() {
    document.getElementById("popupOverlay").style.display = "flex";
  }
  function hideDownloadPopup() {
    document.getElementById("popupOverlay").style.display = "none";
  }
</script>

# BASIC LOGIN UI
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Admin Login - FILMSTAR</title>
  <script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-app-compat.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-auth-compat.js"></script>
</head>
<body>
  <h1>FILMSTAR Admin Login</h1>
  <input type="email" id="email" placeholder="Email" />
  <input type="password" id="password" placeholder="Password" />
  <button onclick="login()">Login</button>

  <script>
    const firebaseConfig = {
      // Your Firebase config
    };
    firebase.initializeApp(firebaseConfig);
    const auth = firebase.auth();

    function login() {
      const email = document.getElementById("email").value;
      const password = document.getElementById("password").value;
      auth.signInWithEmailAndPassword(email, password)
        .then(() => window.location.href = "dashboard.html")
        .catch(err => alert(err.message));
    }
  </script>
</body>
</html>

# ADMIN DASHBOARD UI
<!DOCTYPE html>
<html lang="en">
<head>
  <title>FILMSTAR Dashboard</title>
</head>
<body>
  <h2>Add Movie by TMDb ID</h2>
  <input type="text" id="tmdbId" placeholder="Enter TMDb Movie ID" />
  <button onclick="fetchMovie()">Add Movie</button>
  <div id="movieResult"></div>

  <script>
    const apiKey = "35d4e8e4c9a45f8b6f2e4b81e9c1abcd"; // Your TMDb API key

    async function fetchMovie() {
      const id = document.getElementById("tmdbId").value;
      const res = await fetch(`https://api.themoviedb.org/3/movie/${id}?api_key=${apiKey}&language=en-US`);
      const data = await res.json();

      const result = `
        <h3>${data.title}</h3>
        <p>${data.overview}</p>
        <img src="https://image.tmdb.org/t/p/w200${data.poster_path}" />
      `;
      document.getElementById("movieResult").innerHTML = result;

      // TODO: Save to Firestore or your backend
    }
  </script>
</body>
</html>
You can later add a "save to database" button to store movie in firebase Firestore,like
firebase.firestore().collection("movies").add(data);
# Movie saving to Firestore  from dashboard 
<script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-firestore-compat.js"></script>
<script>
  const firebaseConfig = {
    // Your Firebase config
  };
  firebase.initializeApp(firebaseConfig);
  const db = firebase.firestore();

  let movieData = null;

  async function fetchMovie() {
    const id = document.getElementById("tmdbId").value;
    const res = await fetch(`https://api.themoviedb.org/3/movie/${id}?api_key=35d4e8e4c9a45f8b6f2e4b81e9c1abcd&language=en-US`);
    const data = await res.json();
    movieData = {
      title: data.title,
      overview: data.overview,
      poster: `https://image.tmdb.org/t/p/w500${data.poster_path}`,
      release_date: data.release_date,
      language: data.original_language,
      genre_ids: data.genre_ids,
      tmdb_id: data.id
    };
    document.getElementById("movieResult").innerHTML = `
      <h3>${movieData.title}</h3>
      <p>${movieData.overview}</p>
      <img src="${movieData.poster}" width="200" />
      <br><br><button onclick="saveMovie()">Save to FILMSTAR</button>
    `;
  }

  function saveMovie() {
    db.collection("movies").add(movieData)
      .then(() => alert("✅ Movie added successfully!"))
      .catch(err => alert("❌ Error: " + err));
  }
</script>

# Auto display on Homepage (inbex.html)
<script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-firestore-compat.js"></script>
at the bottom of index.html,just before </body), insert this 
<script>
  const firebaseConfig = {
    // Your Firebase config
  };
  firebase.initializeApp(firebaseConfig);
  const db = firebase.firestore();

  const moviesDiv = document.querySelector(".movies");
  db.collection("movies").orderBy("release_date", "desc").onSnapshot(snapshot => {
    moviesDiv.innerHTML = "";
    snapshot.forEach(doc => {
      const movie = doc.data();
      const card = `
        <a href="movie.html?mid=${doc.id}" class="movie-card">
          <img src="${movie.poster}" alt="${movie.title}" />
          <p>${movie.title}</p>
        </a>`;
      moviesDiv.innerHTML += card;
    });
  });
</script>

# pass mid in movie link ( Already Done )


<a href="movie.html?mid=${doc.id}" class="movie-card">

# HALPER FUNCTION TO GET URL PARAMETER
<script>
  function getParam(name) {
    const url = new URL(window.location.href);
    return url.searchParams.get(name);
  }
</script>

# FETCH MOVIE BY MID FROM FIRESTORE 
<script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-firestore-compat.js"></script>
<script>
  const firebaseConfig = {
    // Your Firebase config here
  };
  firebase.initializeApp(firebaseConfig);
  const db = firebase.firestore();

  const mid = getParam("mid");
  db.collection("movies").doc(mid).get().then(doc => {
    if (doc.exists) {
      const movie = doc.data();
      document.getElementById("movieTitle").textContent = movie.title;
      document.getElementById("poster").src = movie.poster;
      document.getElementById("movieLang").textContent = movie.language;
      document.getElementById("releaseDate").textContent = movie.release_date;
      document.getElementById("overview").textContent = movie.overview;
    } else {
      document.body.innerHTML = "<h2>Movie not found.</h2>";
    }
  });
</script>

# UPDATE movie.html MARKUP 
<body>
  <header>
    <img src="assets/logo.png" alt="FILMSTAR Logo" class="logo" />
  </header>

  <main class="movie-detail">
    <img id="poster" class="poster" src="" alt="Movie Poster" />
    <div class="info">
      <h1 id="movieTitle">Loading...</h1>
      <p><strong>Language:</strong> <span id="movieLang"></span></p>
      <p><strong>Release Date:</strong> <span id="releaseDate"></span></p>
      <p id="overview"></p>

      <button onclick="showDownloadPopup()" class="btn download">Download</button>

      <!-- Popup already added in earlier steps -->
    </div>
  </main>
</body>

# DYNAMIC FILTER (GENRE/LANGUAGE/YEAR)
UPDATE YOUR INDEX.HTML
<section class="filters">
  <select id="filterGenre"><option value="">All Genres</option></select>
  <select id="filterLang"><option value="">All Languages</option></select>
  <select id="filterYear"><option value="">All Years</option></select>
</section>
<main>
  <section class="movie-row">
    <div class="movies"></div>
  </section>
</main>

IN YOUR FIREBASE-INIT SCRIPT (button of index.html)
<script>
  // (1) Initialize Firebase / Firestore
  firebase.initializeApp({ /* your config */ });
  const db = firebase.firestore();

  // (2) State + DOM refs
  let allMovies = [];
  const moviesDiv = document.querySelector(".movies");
  const selGenre = document.getElementById("filterGenre");
  const selLang  = document.getElementById("filterLang");
  const selYear  = document.getElementById("filterYear");

  // (3) Render helpers
  function renderMovies(list) {
    moviesDiv.innerHTML = list.map(doc=>`
      <a href="movie.html?mid=${doc.id}" class="movie-card">
        <img src="${doc.poster}" alt="${doc.title}"/>
        <p>${doc.title}</p>
      </a>
    `).join("");
  }

  function populateFilter(selectEl, values) {
    values.forEach(v=>{
      const opt = document.createElement("option");
      opt.value = v; opt.textContent = v;
      selectEl.appendChild(opt);
    });
  }

  // (4) Fetch & build filters
  db.collection("movies").orderBy("release_date","desc")
    .get().then(snap=>{
      snap.forEach(d=> allMovies.push({ id: d.id, ...d.data() }));
      renderMovies(allMovies);

      // extract unique genres, langs, years
      const genres = new Set(), langs = new Set(), years = new Set();
      allMovies.forEach(m=>{
        (m.genre_ids||[]).forEach(g=>genres.add(g));
        langs.add(m.language);
        years.add( m.release_date.slice(0,4) );
      });
      populateFilter(selGenre, Array.from(genres).sort());
      populateFilter(selLang,  Array.from(langs).sort());
      populateFilter(selYear,  Array.from(years).sort().reverse());
    });

  // (5) Filter logic
  function applyFilters() {
    const g = selGenre.value, l = selLang.value, y = selYear.value;
    const filtered = allMovies.filter(m=>{
      const okG = !g || (m.genre_ids||[]).includes(Number(g));
      const okL = !l || m.language === l;
      const okY = !y || m.release_date.startsWith(y);
      return okG && okL && okY;
    });
    renderMovies(filtered);
  }
  selGenre.onchange = selLang.onchange = selYear.onchange = applyFilters;
</script>

In dashboard.html add below your "ADD MOVIE" UI 
<hr>
<h2>Manage Movies</h2>
<div id="manageList"></div>
ENHANCE YOUR SCRIPT 
<script>
  const manageDiv = document.getElementById("manageList");
  // (A) Fetch & render management table
  function loadManagement() {
    db.collection("movies").orderBy("release_date","desc")
      .get().then(snap=>{
        manageDiv.innerHTML = snap.docs.map(doc=>{
          const m = doc.data();
          return `
            <div class="manage-item" data-id="${doc.id}">
              <img src="${m.poster}" width="50"/>
              <strong>${m.title}</strong>
              <button onclick="editMovie('${doc.id}')">Edit</button>
              <button onclick="deleteMovie('${doc.id}')">Delete</button>
            </div>`;
        }).join("");
      });
  }
  loadManagement();

  // (B) Delete
  function deleteMovie(id) {
    if(confirm("Delete this movie?")) {
      db.collection("movies").doc(id).delete()
        .then(()=> { alert("Deleted"); loadManagement(); })
        .catch(e=> alert(e));
    }
  }

  // (C) Edit: prompt for new title & overview (you can expand to other fields)
  function editMovie(id) {
    db.collection("movies").doc(id).get().then(doc=>{
      const data = doc.data();
      const newTitle = prompt("Title:", data.title);
      const newOverview = prompt("Overview:", data.overview);
      if(newTitle !== null && newOverview !== null) {
        db.collection("movies").doc(id).update({
          title: newTitle,
          overview: newOverview
        }).then(()=>{
          alert("Updated");
          loadManagement();
        });
      }
    });
  }
</script>


# QUICK CSS (append to style.css)
.manage-item {
  display: flex; align-items: center; gap: 10px;
  padding: 8px; background: #111; margin-bottom: 5px;
}
.manage-item button {
  background: #e50914; border: none; padding: 4px 8px;
  color: #fff; border-radius: 3px; cursor: pointer;
}
.manage-item button:hover { opacity: 0.8; }

