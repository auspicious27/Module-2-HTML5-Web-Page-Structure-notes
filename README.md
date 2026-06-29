# Module 2: HTML5 Web Page Structure - Portfolio Project Based Notes

Language style: Simple Hinglish  
Teaching style: One sequence, one integrated project, every code explained in detail  
Final output: Learner ek basic multi-page portfolio website bana lega.

---

## Module Goal

Is module mein hum HTML5 ke topics ko alag-alag theory ke form mein nahi, balki ek real portfolio website banate hue seekhenge. Learner step by step ek static multi-page website create karega. Isi website ke andar HTML5 document structure, semantic tags, forms, validation, tables, lists, images, media, accessibility, SEO, and cross-browser basics cover honge.

Is approach ka benefit yeh hai ki learner ko har topic isolated nahi lagega. Har topic ka use directly project mein dikhega. Jab learner `header` seekhega toh usko website ka top part banega. Jab `nav` seekhega toh pages connect honge. Jab form seekhega toh contact page complete hoga. Jab accessibility seekhega toh image alt text and label ka real use samjhega.

---

## What We Will Build

Hum ek basic portfolio website banayenge:

```text
portfolio-site/
  index.html
  about.html
  projects.html
  contact.html
  media/
    profile.jpg
    intro.mp4
```

Website pages:

| Page | Purpose |
|---|---|
| `index.html` | Home page with intro and navigation |
| `about.html` | About page with skills list and education table |
| `projects.html` | Projects page with articles and media |
| `contact.html` | Contact form with validation |

Topics covered inside this project:

| Topic | Where We Use It |
|---|---|
| HTML5 document structure | Every page |
| Semantic tags | Header, nav, main, section, article, footer |
| Forms and validation | Contact page |
| Tables | About page education table |
| Lists | Skills list |
| Images and media | Profile image and intro video |
| Accessibility | Labels, alt text, heading order |
| SEO | Title, meta description, semantic layout |
| Cross-browser basics | Testing pages in browser |

---

# Step 1: Create Project Folder in VS Code

## Theory

Before writing code, project files should be properly organized. A website usually has multiple files: HTML pages, images, videos, CSS files, and JavaScript files. Day 2 par hum only HTML focus karenge, but folder structure clean rakhenge so future modules mein CSS and JavaScript add karna easy ho.

VS Code ek code editor hai. Isme folder open karke hum files create, edit and save kar sakte hain. Browser HTML files ko read karke webpage display karta hai.

## Practical Steps

1. VS Code open karo.
2. Documents/Desktop mein folder banao:

```text
portfolio-site
```

3. VS Code mein `File -> Open Folder` select karo.
4. `portfolio-site` folder open karo.
5. New files create karo:

```text
index.html
about.html
projects.html
contact.html
```

6. Ek folder create karo:

```text
media
```

7. Is folder mein later image/video rakhenge.

## Expected Folder View

```text
portfolio-site/
  index.html
  about.html
  projects.html
  contact.html
  media/
```

## Explanation

| Item | Explanation |
|---|---|
| `portfolio-site` | Main project folder |
| `index.html` | Home page; browser usually index page ko starting page maanta hai |
| `about.html` | About page |
| `projects.html` | Projects page |
| `contact.html` | Contact form page |
| `media` | Images/videos store karne ke liye folder |

---

# Step 2: Build the Home Page with HTML5 Document Structure

## Theory

Har HTML5 page ek basic structure follow karta hai. Is structure se browser ko samajh aata hai ki document HTML5 hai, page ki language kya hai, character encoding kya hai, mobile screen ke liye layout kaise behave karega, aur visible content kahan hai.

HTML page mainly do parts mein divide hota hai:

```text
head = page information, SEO, title, metadata
body = visible content jo user ko browser mein dikhta hai
```

`head` section directly page par visible nahi hota, lekin browser and search engines ke liye important hota hai. `body` section mein headings, paragraphs, navigation, images, forms, etc. visible content hota hai.

## Practical Code: `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Beginner portfolio website created using HTML5 semantic structure.">
  <title>My Portfolio - Home</title>
</head>
<body>
  <header>
    <h1>My Portfolio</h1>

    <nav>
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="projects.html">Projects</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>

  <main>
    <section>
      <h2>Welcome</h2>
      <p>Hello, my name is Rahul. I am learning web development.</p>
      <p>This portfolio website is created using HTML5.</p>
    </section>
  </main>

  <footer>
    <p>Copyright 2026 - My Portfolio</p>
  </footer>
</body>
</html>
```

## How to Execute

1. Code ko `index.html` mein paste karo.
2. File save karo.
3. File par right-click karo and browser mein open karo.
4. Output mein title, navigation, welcome section and footer dikhna chahiye.

## Expected Output

Browser page par yeh content dikhega:

```text
My Portfolio
Home About Projects Contact
Welcome
Hello, my name is Rahul. I am learning web development.
This portfolio website is created using HTML5.
Copyright 2026 - My Portfolio
```

## Line-by-Line Code Explanation

| Line / Code | Detailed Explanation |
|---|---|
| `<!DOCTYPE html>` | Yeh browser ko batata hai ki file HTML5 standard follow kar rahi hai. Agar yeh line na ho toh browser old/quirks mode mein page render kar sakta hai, jisse layout unpredictable ho sakta hai. Isliye har modern HTML page ke top par yeh line likhna best practice hai. |
| `<html lang="en">` | Yeh complete HTML document ka root element hai. Iske andar hi `head` aur `body` sections aate hain. `lang="en"` browser, search engine aur screen reader ko batata hai ki page English language mein hai. Agar website Hindi mein ho toh `lang="hi"` use kar sakte hain. |
| `<head>` | Is section mein page ki hidden information hoti hai, jaise metadata, title, SEO description, responsive settings, CSS links, etc. Iska content normally browser page par directly visible nahi hota, lekin browser aur search engines ke liye bahut important hota hai. |
| `<meta charset="UTF-8">` | Yeh text encoding set karta hai. UTF-8 use karne se English, Hindi, symbols, special characters, punctuation properly display hote hain. Agar encoding wrong ho toh characters broken/strange symbols ke form mein dikh sakte hain. |
| `<meta name="viewport"...>` | Yeh mobile responsiveness ke liye important hai. `width=device-width` browser ko bolta hai ki page device ki actual screen width ke according set ho. `initial-scale=1.0` page ka starting zoom normal rakhta hai. Agar yeh missing ho toh mobile par page zoomed-out ya awkward lag sakta hai. |
| `<meta name="description"...>` | Yeh page ka short summary search engines ke liye provide karta hai. Browser page par visible nahi hota, but SEO mein help karta hai. Search result mein kabhi-kabhi yahi description snippet ke form mein show ho sakta hai. |
| `<title>` | Browser tab mein jo text dikhai deta hai woh title tag se aata hai. SEO ke liye bhi important hai because search engines page title ko page topic samajhne ke liye use karte hain. Har page ka unique title hona chahiye, jaise Home, About, Contact. |
| `<body>` | Body ke andar woh content likha jaata hai jo user ko browser window mein visible hota hai. Headings, paragraphs, images, links, forms, tables, sections sab body ke andar aate hain. |
| `<header>` | Yeh page ka top semantic section hai. Isme website ka naam, logo, short tagline, aur navigation links rakhte hain. Header tag use karne se code meaningful hota hai aur screen readers ko page structure samajhne mein help milti hai. |
| `<h1>` | Page ka sabse important heading. Home page par usually website/person ka main name ya page topic h1 mein aata hai. Ek page par generally one clear h1 rakhna best practice hai. |
| `<nav>` | Navigation links ka semantic container. Isse browser/screen reader ko pata chalta hai ki is area mein page links hain. Multi-page website mein nav important hota hai because user Home, About, Projects, Contact pages ke beech move karta hai. |
| `<a href="index.html">Home</a>` | `a` anchor tag link create karta hai. `href` batata hai click karne par kaunsi file/page open hogi. `Home` visible clickable text hai. Agar file name wrong ho jaaye toh link broken ho sakta hai. |
| `<main>` | Page ka main unique content section. Header/footer common ho sakte hain, but main ke andar page-specific content hota hai. Accessibility ke liye main tag useful hai because assistive tools user ko direct main content par le ja sakte hain. |
| `<section>` | Related content ko group karta hai. Example: welcome section, skills section, contact section. Section ke andar heading rakhna good practice hai taaki content ka topic clear ho. |
| `<h2>` | Section heading ke liye use hota hai. Since page ka main heading `h1` hai, uske andar sections ke liye `h2` logical hierarchy banata hai. Proper heading order SEO and accessibility dono ke liye important hai. |
| `<p>` | Paragraph tag normal text explanation ke liye use hota hai. Agar content sentence/description form mein hai toh paragraph tag use karna semantic and readable hota hai. |
| `<footer>` | Page ka bottom semantic section. Isme copyright, contact info, social links ya extra navigation aa sakti hai. Footer se page ka ending area clearly identify hota hai. |

## Common Mistakes

- `head` ke andar visible content likhna.
- `body` close karna bhool jaana.
- `href` mein wrong file name likhna.
- `meta viewport` remove kar dena, jis se mobile layout issue ho sakta hai.

## Mini Task

`Rahul` ko apne naam se replace karo. Browser refresh karke output check karo.

---

# Step 3: Understand and Use Semantic HTML

## Theory

Semantic HTML ka matlab meaningful tags use karna. Agar hum har jagah `<div>` use karte hain, browser ko structure ka meaning clear nahi hota. Semantic tags jaise `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>` page ka meaning clear karte hain.

Semantic HTML ke benefits:

- Code readable hota hai.
- Search engines page structure better samajhte hain.
- Screen readers users ko better navigation dete hain.
- Team project mein code maintain karna easy hota hai.

## Semantic Tags Used in Our Portfolio

| Semantic Tag | Portfolio Mein Use |
|---|---|
| `<header>` | Website title and navigation |
| `<nav>` | Page links |
| `<main>` | Main page content |
| `<section>` | Content groups |
| `<article>` | Individual project cards |
| `<footer>` | Copyright info |

## Practical Improvement

Home page already semantic tags use kar raha hai. Ab hum same structure other pages mein repeat karenge. Multi-page static website mein navigation same rehna chahiye, taaki user pages ke beech move kar sake.

## Why Same Navigation on All Pages?

Agar `about.html` par user hai, usko home ya contact page par jaane ka option chahiye. Isliye same navigation har page mein copy karte hain.

```html
<nav>
  <a href="index.html">Home</a>
  <a href="about.html">About</a>
  <a href="projects.html">Projects</a>
  <a href="contact.html">Contact</a>
</nav>
```

## Code Explanation

| Code | Explanation |
|---|---|
| `<nav>` | Navigation area define karta hai. |
| `<a>` | Link create karta hai. |
| `href="about.html"` | Click karne par browser about page open karega. |
| Link text | User ko visible text. Example: `About`. |

## Mini Task

Home page ke navigation links click karo. Abhi pages blank ya basic honge, but browser URL change hoga. Yeh show karta hai ki links file navigation ke liye use hote hain.

---

# Step 4: Build About Page with Lists, Table and Image

## Theory

About page learner ke profile, skills and education details show karega. Is page mein hum lists, tables and images use karenge.

List ka use tab karte hain jab related points show karne ho. Example: skills, hobbies, services. Table ka use tab karte hain jab data rows and columns mein ho. Example: education details, course fees, timetable. Image ka use visual identity ke liye hota hai, but image ke saath `alt` text accessibility ke liye important hai.

## Practical Code: `about.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="About page of a beginner portfolio website with skills and education details.">
  <title>My Portfolio - About</title>
</head>
<body>
  <header>
    <h1>My Portfolio</h1>

    <nav>
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="projects.html">Projects</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>

  <main>
    <section>
      <h2>About Me</h2>
      <img src="media/profile.jpg" alt="Profile photo of Rahul" width="200">
      <p>I am a beginner web developer learning HTML, CSS, JavaScript and MERN stack.</p>
    </section>

    <section>
      <h2>My Skills</h2>
      <ul>
        <li>HTML5 Web Page Structure</li>
        <li>Semantic HTML</li>
        <li>Basic Forms</li>
        <li>Web Accessibility Basics</li>
      </ul>
    </section>

    <section>
      <h2>Education Details</h2>
      <table>
        <thead>
          <tr>
            <th>Course</th>
            <th>Institute</th>
            <th>Year</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>MERN Stack</td>
            <td>Learning Academy</td>
            <td>2026</td>
          </tr>
          <tr>
            <td>HTML5 Basics</td>
            <td>Online Practice</td>
            <td>2026</td>
          </tr>
        </tbody>
      </table>
    </section>
  </main>

  <footer>
    <p>Copyright 2026 - My Portfolio</p>
  </footer>
</body>
</html>
```

## How to Execute

1. Code ko `about.html` mein paste karo.
2. `media` folder mein `profile.jpg` naam ki image rakho.
3. File save karo.
4. Browser mein `about.html` open karo.
5. Image, skills list and education table show hone chahiye.

## Expected Output

Page par:

- About Me section
- Profile image
- Paragraph intro
- Skills bullet list
- Education table
- Header and footer

## Detailed Code Explanation

| Code | Explanation |
|---|---|
| `<img src="media/profile.jpg"...>` | Image show karta hai. `src` image path hai. |
| `alt="Profile photo of Rahul"` | Image description. Accessibility ke liye important. Agar image load na ho toh yeh text useful hota hai. |
| `width="200"` | Image width 200 pixels set karta hai. |
| `<ul>` | Unordered list start. Skills bullet points ke liye use. |
| `<li>` | List item. Har skill ek list item hai. |
| `<table>` | Table start. Rows and columns data ke liye. |
| `<thead>` | Table heading group. |
| `<tr>` | Table row. |
| `<th>` | Table heading cell. |
| `<tbody>` | Table main data group. |
| `<td>` | Table data cell. |

## Why These Tags Are Used?

Skills paragraph mein bhi likh sakte the, but list better hai because skills separate points hain. Education plain text mein bhi likh sakte the, but table better hai because course, institute and year structured columns hain. Image ke saath alt text use kiya because accessibility best practice hai.

## Common Mistakes

- Image file ka naam wrong likhna.
- `media` folder ke bahar image rakhna but path `media/profile.jpg` dena.
- `<tr>` ke andar directly text likhna instead of `<td>` or `<th>`.
- List item ke liye `<li>` bhool jaana.

## Mini Task

Skills list mein 2 new skills add karo. Table mein ek new row add karo.

---

# Step 5: Build Projects Page with Articles and Media

## Theory

Projects page portfolio ka important part hota hai. Is page par learner apne projects show karega. Har project independent content block hai, isliye `<article>` tag use karna meaningful hai.

Media ka use website ko more informative banata hai. HTML5 directly video and audio support karta hai. Video use karte time `controls` attribute important hota hai, warna user play/pause controls nahi dekh paayega.

## Practical Code: `projects.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Projects page showing beginner HTML5 portfolio projects.">
  <title>My Portfolio - Projects</title>
</head>
<body>
  <header>
    <h1>My Portfolio</h1>

    <nav>
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="projects.html">Projects</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>

  <main>
    <section>
      <h2>My Projects</h2>

      <article>
        <h3>Portfolio Website</h3>
        <p>This project is a multi-page static website created using HTML5.</p>
      </article>

      <article>
        <h3>Contact Form Page</h3>
        <p>This project uses HTML5 forms and input validation.</p>
      </article>
    </section>

    <section>
      <h2>Project Demo Video</h2>
      <video controls width="400">
        <source src="media/intro.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </section>
  </main>

  <footer>
    <p>Copyright 2026 - My Portfolio</p>
  </footer>
</body>
</html>
```

## How to Execute

1. Code ko `projects.html` mein paste karo.
2. Optional: `media` folder mein `intro.mp4` video rakho.
3. Browser mein `projects.html` open karo.
4. Project articles and video section observe karo.

## Expected Output

Page par projects list article style mein dikhegi. Agar video file available hai, browser video player show karega. Agar video file missing hai, video load nahi hoga, but page structure still visible rahega.

## Detailed Code Explanation

| Code | Explanation |
|---|---|
| `<article>` | Independent project block. Har project apne aap mein complete information hai. |
| `<h3>` | Project title. Since section heading `h2` hai, project heading `h3` use ki. |
| `<video controls width="400">` | Video player create karta hai. `controls` play/pause controls show karta hai. |
| `<source src="media/intro.mp4"...>` | Video file path and type define karta hai. |
| `type="video/mp4"` | Browser ko batata hai file MP4 video hai. |
| Fallback text | Agar browser video support nahi karta toh message show hota hai. |

## Why `article` Is Better Here?

Project cards independent content blocks hain. Har project ka title and description hai. Isliye `article` semantic tag meaningful hai. Agar sirf generic `div` use karte, code visually same ho sakta tha, but meaning less clear hota.

## Common Mistakes

- `controls` attribute miss karna.
- Video file path wrong dena.
- Heading order break karna, jaise `h2` ke baad directly `h5` use karna.
- Article ke andar heading na dena.

## Mini Task

Ek third project article add karo:

```text
Project Name: HTML Table Practice
Description: This project displays course information using an HTML table.
```

---

# Step 6: Build Contact Page with Form and Validation

## Theory

Forms user input collect karne ke liye use hote hain. Contact form, login form, signup form, feedback form, search form - sab form examples hain.

HTML5 form validation browser level par basic checking provide karta hai. `required` blank field prevent karta hai. `type="email"` email format validate karta hai. `minlength` minimum characters ensure karta hai. Lekin real applications mein backend validation bhi zaroori hoti hai, because frontend validation bypass ho sakti hai.

## Practical Code: `contact.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Contact page with HTML5 form validation.">
  <title>My Portfolio - Contact</title>
</head>
<body>
  <header>
    <h1>My Portfolio</h1>

    <nav>
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="projects.html">Projects</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>

  <main>
    <section>
      <h2>Contact Me</h2>

      <form>
        <label for="fullName">Full Name</label>
        <input type="text" id="fullName" name="fullName" minlength="3" required>

        <label for="email">Email Address</label>
        <input type="email" id="email" name="email" required>

        <label for="course">Interested Course</label>
        <select id="course" name="course" required>
          <option value="">Select a course</option>
          <option value="html">HTML5</option>
          <option value="mern">MERN Stack</option>
          <option value="javascript">JavaScript</option>
        </select>

        <label for="message">Message</label>
        <textarea id="message" name="message" rows="5" minlength="10" required></textarea>

        <button type="submit">Send Message</button>
      </form>
    </section>
  </main>

  <footer>
    <p>Copyright 2026 - My Portfolio</p>
  </footer>
</body>
</html>
```

## How to Execute

1. Code ko `contact.html` mein paste karo.
2. Browser mein `contact.html` open karo.
3. Blank form submit karne ki koshish karo.
4. Browser required field validation show karega.
5. Email field mein `abc` likho and submit karo.
6. Browser valid email maangega.
7. Message mein 10 characters se kam likho and submit karo.
8. Browser minlength validation show karega.

## Expected Output

Contact page par form fields dikhenge:

- Full Name
- Email Address
- Interested Course dropdown
- Message
- Send Message button

Validation test karne par browser error messages show karega.

## Detailed Code Explanation

| Code | Explanation |
|---|---|
| `<form>` | Form area create karta hai. User input fields isi ke andar hote hain. |
| `<label for="fullName">` | Label input se connect hota hai. `for` value input ke `id` se match honi chahiye. |
| `<input type="text"...>` | Normal text input for name. |
| `minlength="3"` | User ko at least 3 characters enter karne honge. |
| `required` | Field blank nahi chhod sakte. |
| `<input type="email"...>` | Email input. Browser email format check karta hai. |
| `<select>` | Dropdown field create karta hai. |
| `<option value="">` | Default empty option. Required validation ke liye useful. |
| `<textarea>` | Long message input ke liye. |
| `rows="5"` | Textarea height approx 5 rows. |
| `minlength="10"` | Message at least 10 characters ka hona chahiye. |
| `<button type="submit">` | Form submit button. |

## Accessibility Explanation

Labels form accessibility ke liye very important hain. Agar user label par click kare, connected input focus ho jaata hai. Screen reader users ko bhi field ka purpose samajh aata hai.

## Common Mistakes

- Label ka `for` and input ka `id` mismatch kar dena.
- Required field miss kar dena.
- Email field ko `type="text"` rakh dena.
- Dropdown ka default option value empty na rakhna.

## Mini Task

Form mein phone number field add karo:

```html
<label for="phone">Phone Number</label>
<input type="tel" id="phone" name="phone">
```

---

# Step 7: Accessibility, SEO and Cross-Browser Checklist

## Theory

Website sirf visually good nahi honi chahiye. Website accessible, SEO-friendly and different browsers mein workable honi chahiye.

Accessibility ka matlab website sab users ke liye usable ho. SEO ka matlab search engines page ko easily understand kar sakein. Cross-browser compatibility ka matlab page Chrome, Firefox, Safari, Edge mein properly open ho.

## Accessibility Checklist

| Rule | Our Portfolio Example |
|---|---|
| One clear `h1` | `My Portfolio` |
| Labels for inputs | Contact form labels |
| Alt text for images | Profile image alt |
| Semantic tags | Header, nav, main, section, footer |
| Meaningful links | Home, About, Projects, Contact |

## SEO Checklist

| SEO Rule | Our Portfolio Example |
|---|---|
| Proper title | `My Portfolio - Home` |
| Meta description | Added in every page |
| Heading hierarchy | h1, h2, h3 order |
| Semantic layout | main, section, article |
| Image alt text | Profile image description |

## Cross-Browser Testing Steps

1. `index.html` Chrome mein open karo.
2. Same file Safari/Firefox/Edge mein open karo.
3. Navigation links test karo.
4. Image load check karo.
5. Form validation test karo.
6. Table/list/video output check karo.

## Practical Output

If everything is correct:

- All pages open properly.
- Navigation links work.
- Contact form validation works.
- Image alt text is present.
- Page titles are meaningful.
- Layout basic but readable.

---

# Step 8: Final Beautiful Portfolio Code Pack

## Why This Final Code Pack Is Added

Ab tak humne topic-wise pages banaye. Ab is section mein same portfolio website ka final polished version diya gaya hai. Iska purpose hai ki learner ke paas ek clean, readable, properly formatted, semantic HTML portfolio website ka final reference ho.

Is section mein code thoda more professional structure mein hai. Har page mein same header, same navigation, proper `main`, meaningful `section`, proper headings, accessibility attributes, SEO meta description, and clean footer use kiya gaya hai.

Important: Ye abhi bhi HTML-focused project hai. Isme CSS styling intentionally add nahi ki gayi, kyunki Module 2 ka focus HTML5 structure hai. CSS next modules mein add ho sakti hai. Lekin HTML structure clean aur beautiful rakha gaya hai, taaki CSS add karna easy ho.

---

## Final Page 1: `index.html`

### Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Rahul's beginner portfolio website created with semantic HTML5.">
  <title>Rahul Portfolio | Home</title>
</head>
<body>
  <header>
    <h1>Rahul Sharma</h1>
    <p>Beginner Web Developer learning HTML5 and MERN Stack.</p>

    <nav aria-label="Main navigation">
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="projects.html">Projects</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>

  <main>
    <section>
      <h2>Welcome to My Portfolio</h2>
      <p>This website is created using HTML5 semantic tags.</p>
      <p>Here you can learn about my skills, projects, and contact details.</p>
    </section>

    <section>
      <h2>What I Am Learning</h2>
      <ul>
        <li>HTML5 page structure</li>
        <li>Semantic web layout</li>
        <li>Forms and validation</li>
        <li>Accessibility and SEO basics</li>
      </ul>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 Rahul Sharma. All rights reserved.</p>
  </footer>
</body>
</html>
```

### How to Execute

1. VS Code mein `index.html` file open karo.
2. Upar wala code paste karo.
3. File save karo.
4. Browser mein `index.html` open karo.
5. Output mein name, intro, navigation links, welcome section, learning list and footer dikhna chahiye.

### Every Line Explanation

| Line / Code | Detailed Simple Hinglish Explanation |
|---|---|
| `<!DOCTYPE html>` | Browser ko batata hai ki yeh HTML5 document hai. Yeh line browser ko modern HTML mode mein page read karne mein help karti hai. |
| `<html lang="en">` | Complete HTML document yahan se start hota hai. `lang="en"` batata hai page English language mein hai. Accessibility and SEO ke liye useful. |
| `<head>` | Head section page ki information rakhta hai. Yeh content direct page body mein visible nahi hota. |
| `<meta charset="UTF-8">` | Character encoding set karta hai. Isse normal text, symbols, special characters correctly show hote hain. |
| `<meta name="viewport"...>` | Mobile responsive behavior ke liye important hai. Browser ko bolta hai page device width ke according adjust ho. |
| `<meta name="description"...>` | Search engines ko page ka short summary deta hai. Yeh SEO-friendly HTML ka part hai. |
| `<title>Rahul Portfolio \| Home</title>` | Browser tab mein title show karta hai. Search result mein bhi title ka role hota hai. |
| `</head>` | Head section close karta hai. |
| `<body>` | Visible page content yahan start hota hai. User browser mein isi section ka output dekhta hai. |
| `<header>` | Page ka top section. Isme name, intro and navigation rakhe gaye hain. |
| `<h1>Rahul Sharma</h1>` | Page ka main heading. Portfolio owner ka name show karta hai. |
| `<p>Beginner Web Developer...</p>` | Short intro paragraph. Visitor ko immediately page owner ka context milta hai. |
| `<nav aria-label="Main navigation">` | Navigation section create karta hai. `aria-label` screen reader users ko batata hai ki yeh main navigation hai. |
| `<a href="index.html">Home</a>` | Home page link. Click karne par browser `index.html` open karta hai. |
| `<a href="about.html">About</a>` | About page link. Multi-page website navigation ka part. |
| `<a href="projects.html">Projects</a>` | Projects page link. User project details page par ja sakta hai. |
| `<a href="contact.html">Contact</a>` | Contact page link. User form page par ja sakta hai. |
| `</nav>` | Navigation links ka group close hota hai. |
| `</header>` | Header section close hota hai. |
| `<main>` | Page ka main unique content yahan start hota hai. Har page mein main content alag hota hai. |
| `<section>` | Related content ka section. Yahan welcome content group kiya gaya hai. |
| `<h2>Welcome to My Portfolio</h2>` | Section heading. `h1` ke baad logical subheading ke liye `h2` use hota hai. |
| `<p>This website...</p>` | Paragraph explain karta hai ki website semantic HTML5 se bani hai. |
| `<p>Here you can...</p>` | Visitor ko batata hai website mein kya information milegi. |
| `</section>` | Welcome section close hota hai. |
| `<section>` | Second section start hota hai, jisme learning topics list hain. |
| `<h2>What I Am Learning</h2>` | Section title. Iske neeche learning points aayenge. |
| `<ul>` | Unordered list start. Jab points bullet form mein show karne ho tab use hota hai. |
| `<li>HTML5 page structure</li>` | First list item. Learner ka topic show karta hai. |
| `<li>Semantic web layout</li>` | Second list item. Semantic layout topic show karta hai. |
| `<li>Forms and validation</li>` | Third list item. Forms topic show karta hai. |
| `<li>Accessibility and SEO basics</li>` | Fourth list item. Accessibility and SEO topic show karta hai. |
| `</ul>` | List close hoti hai. |
| `</section>` | Learning section close hota hai. |
| `</main>` | Main content close hota hai. |
| `<footer>` | Page ka bottom section. Usually copyright/contact/extra links rakhe jaate hain. |
| `<p>&copy; 2026 Rahul Sharma...</p>` | Copyright text. `&copy;` copyright symbol show karta hai. |
| `</footer>` | Footer close hota hai. |
| `</body>` | Visible body content close hota hai. |
| `</html>` | Complete HTML document close hota hai. |

---

## Final Page 2: `about.html`

### Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="About Rahul Sharma, his skills, education, and learning journey.">
  <title>Rahul Portfolio | About</title>
</head>
<body>
  <header>
    <h1>About Rahul</h1>

    <nav aria-label="Main navigation">
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="projects.html">Projects</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>

  <main>
    <section>
      <h2>Profile</h2>
      <img src="media/profile.jpg" alt="Rahul Sharma smiling in a profile photo" width="220">
      <p>I am learning web development step by step. My current focus is HTML5 web page structure.</p>
    </section>

    <section>
      <h2>Skills</h2>
      <ul>
        <li>Creating HTML5 document structure</li>
        <li>Using semantic HTML tags</li>
        <li>Building accessible forms</li>
        <li>Writing SEO-friendly HTML</li>
      </ul>
    </section>

    <section>
      <h2>Education</h2>
      <table>
        <thead>
          <tr>
            <th>Course</th>
            <th>Institute</th>
            <th>Year</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>MERN Stack Development</td>
            <td>Learning Academy</td>
            <td>2026</td>
          </tr>
          <tr>
            <td>HTML5 Fundamentals</td>
            <td>Self Practice</td>
            <td>2026</td>
          </tr>
        </tbody>
      </table>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 Rahul Sharma. All rights reserved.</p>
  </footer>
</body>
</html>
```

### How to Execute

1. `about.html` file open karo.
2. Code paste karo and save karo.
3. `media` folder mein `profile.jpg` image rakho.
4. Browser mein `about.html` open karo.
5. Profile section, image, skills list and education table output check karo.

### Every Line Explanation

| Line / Code | Detailed Simple Hinglish Explanation |
|---|---|
| `<!DOCTYPE html>` | HTML5 document declaration. Browser ko correct mode mein render karne mein help karta hai. |
| `<html lang="en">` | Page ka root element. `lang="en"` accessibility and SEO ke liye language define karta hai. |
| `<head>` | Metadata section start. Page information yahan hoti hai. |
| `<meta charset="UTF-8">` | Text encoding define karta hai. |
| `<meta name="viewport"...>` | Mobile screen ke liye page scale set karta hai. |
| `<meta name="description"...>` | About page ka SEO summary. Search engine ko page content samajhne mein help karta hai. |
| `<title>Rahul Portfolio \| About</title>` | Browser tab title. User ko pata chalta hai yeh about page hai. |
| `<body>` | Visible content start. |
| `<header>` | Top area start. Isme heading and navigation hai. |
| `<h1>About Rahul</h1>` | About page ka main heading. |
| `<nav aria-label="Main navigation">` | Accessible navigation. Screen reader ko navigation ka purpose clear hota hai. |
| `<a href="...">` | Har anchor tag ek page link create karta hai. |
| `<main>` | Main content start. About page ka unique content yahan hai. |
| `<section>` | Profile content group karne ke liye section. |
| `<h2>Profile</h2>` | Profile section ka heading. |
| `<img src="media/profile.jpg"...>` | Profile image load karta hai. `src` image location batata hai. |
| `alt="Rahul Sharma smiling..."` | Image ka meaningful text description. Accessibility ke liye important. |
| `width="220"` | Image ki display width set karta hai. |
| `<p>I am learning...</p>` | Profile paragraph. Learner ke baare mein short introduction. |
| `<section>` | Skills ke liye separate section start. |
| `<h2>Skills</h2>` | Skills section heading. |
| `<ul>` | Skills ko bullet list mein show karne ke liye unordered list. |
| `<li>...</li>` | Har skill ek list item hai. |
| `<section>` | Education table ke liye section. |
| `<h2>Education</h2>` | Education section heading. |
| `<table>` | Structured rows and columns data ke liye table start. |
| `<thead>` | Table heading rows ko group karta hai. |
| `<tr>` | Table row. |
| `<th>` | Table header cell. Column ka title show karta hai. |
| `<tbody>` | Table ka main data body. |
| `<td>` | Normal table data cell. |
| `</table>` | Table close karta hai. |
| `<footer>` | Bottom section. |
| `&copy;` | Copyright symbol render karta hai. |

---

## Final Page 3: `projects.html`

### Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Projects created by Rahul Sharma while learning HTML5 and web development.">
  <title>Rahul Portfolio | Projects</title>
</head>
<body>
  <header>
    <h1>My Projects</h1>

    <nav aria-label="Main navigation">
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="projects.html">Projects</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>

  <main>
    <section>
      <h2>Featured Work</h2>

      <article>
        <h3>Portfolio Website</h3>
        <p>A multi-page static portfolio created using semantic HTML5 tags.</p>
      </article>

      <article>
        <h3>Contact Form Page</h3>
        <p>A contact page using HTML5 form inputs and browser validation.</p>
      </article>
    </section>

    <section>
      <h2>Demo Video</h2>
      <video controls width="420">
        <source src="media/intro.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 Rahul Sharma. All rights reserved.</p>
  </footer>
</body>
</html>
```

### How to Execute

1. `projects.html` file mein code paste karo.
2. Optional video file `media/intro.mp4` add karo.
3. Browser mein page open karo.
4. Project articles and video player observe karo.

### Every Line Explanation

| Line / Code | Detailed Simple Hinglish Explanation |
|---|---|
| `<!DOCTYPE html>` | Browser ko HTML5 document type batata hai. |
| `<html lang="en">` | Root HTML element with language. |
| `<head>` | Page metadata start hota hai. |
| `<meta charset="UTF-8">` | Character support ke liye encoding. |
| `<meta name="viewport"...>` | Mobile-friendly page rendering ke liye. |
| `<meta name="description"...>` | Projects page ka SEO description. |
| `<title>Rahul Portfolio \| Projects</title>` | Browser tab mein projects page title. |
| `<body>` | Visible content start. |
| `<header>` | Page top area. |
| `<h1>My Projects</h1>` | Projects page ka main heading. |
| `<nav aria-label="Main navigation">` | Page links ka accessible navigation area. |
| `<main>` | Projects page ka main content. |
| `<section>` | Featured work group. |
| `<h2>Featured Work</h2>` | Section heading. |
| `<article>` | Independent project card. Article is useful because each project is a complete content item. |
| `<h3>Portfolio Website</h3>` | Project title. |
| `<p>A multi-page...</p>` | Project description. |
| Second `<article>` | Dusra independent project block. |
| `<section>` | Demo video ke liye separate section. |
| `<video controls width="420">` | Video player create karta hai. `controls` play/pause UI show karta hai. |
| `<source src="media/intro.mp4"...>` | Video file path and format define karta hai. |
| `type="video/mp4"` | Browser ko batata hai file MP4 video hai. |
| Fallback text | Agar browser video tag support na kare toh yeh message show hota hai. |
| `<footer>` | Bottom copyright section. |

---

## Final Page 4: `contact.html`

### Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Contact Rahul Sharma using an accessible HTML5 contact form.">
  <title>Rahul Portfolio | Contact</title>
</head>
<body>
  <header>
    <h1>Contact Me</h1>

    <nav aria-label="Main navigation">
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="projects.html">Projects</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>

  <main>
    <section>
      <h2>Send a Message</h2>

      <form>
        <label for="fullName">Full Name</label>
        <input type="text" id="fullName" name="fullName" minlength="3" required>

        <label for="email">Email Address</label>
        <input type="email" id="email" name="email" required>

        <label for="course">Interested Course</label>
        <select id="course" name="course" required>
          <option value="">Select a course</option>
          <option value="html">HTML5</option>
          <option value="css">CSS</option>
          <option value="mern">MERN Stack</option>
        </select>

        <label for="message">Message</label>
        <textarea id="message" name="message" rows="5" minlength="10" required></textarea>

        <button type="submit">Send Message</button>
      </form>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 Rahul Sharma. All rights reserved.</p>
  </footer>
</body>
</html>
```

### How to Execute

1. `contact.html` file mein code paste karo.
2. Browser mein open karo.
3. Blank submit karke validation check karo.
4. Wrong email type karke email validation check karo.
5. Message mein 10 characters se kam type karke minlength validation check karo.

### Every Line Explanation

| Line / Code | Detailed Simple Hinglish Explanation |
|---|---|
| `<!DOCTYPE html>` | HTML5 document declaration. |
| `<html lang="en">` | Root element and page language. |
| `<head>` | Metadata and SEO section. |
| `<meta charset="UTF-8">` | Character encoding. |
| `<meta name="viewport"...>` | Responsive page behavior. |
| `<meta name="description"...>` | Search engine friendly contact page summary. |
| `<title>Rahul Portfolio \| Contact</title>` | Browser tab title. |
| `<body>` | Visible page content start. |
| `<header>` | Top page section. |
| `<h1>Contact Me</h1>` | Main page heading. |
| `<nav aria-label="Main navigation">` | Accessible navigation links. |
| `<main>` | Main contact content. |
| `<section>` | Contact form section group. |
| `<h2>Send a Message</h2>` | Form section heading. |
| `<form>` | Form container. All input fields are inside this form. |
| `<label for="fullName">Full Name</label>` | Label for name input. `for` connects with input `id`. |
| `<input type="text"...>` | Text input field for full name. |
| `id="fullName"` | Unique identifier. Label uses this id to connect. |
| `name="fullName"` | Field name used when form data is submitted. |
| `minlength="3"` | Minimum 3 characters required. |
| `required` | Field cannot be empty. Browser validates it. |
| `<input type="email"...>` | Email input. Browser checks email format. |
| `<select id="course"...>` | Dropdown list for course selection. |
| `<option value="">Select a course</option>` | Default empty option. Required validation works because value is empty. |
| `<option value="html">HTML5</option>` | Dropdown option for HTML5. |
| `<textarea...>` | Multi-line message input. |
| `rows="5"` | Textarea height around five lines. |
| `minlength="10"` | Message must have at least 10 characters. |
| `<button type="submit">` | Form submit button. |
| `</form>` | Form ends here. |
| `<footer>` | Footer area. |

---

# Super Detailed Code Explanation Guide

## Why This Guide Is Important

Portfolio website ke pages mein kuch code lines baar-baar repeat hoti hain, jaise `DOCTYPE`, `html`, `head`, `meta`, `header`, `nav`, `main`, `footer`. Beginner learners ko yeh repeated lines boring lag sakti hain, lekin actually yahi HTML page ka foundation hain. Is guide mein har common line ko deeper way mein explain kiya gaya hai, taaki learner sirf code copy na kare, balki samjhe ki line ka exact role kya hai.

---

## A. Document Setup Lines

| Code | Deep Explanation |
|---|---|
| `<!DOCTYPE html>` | Yeh declaration browser ko batata hai ki document HTML5 standard use kar raha hai. Iska closing tag nahi hota. Yeh actual HTML element nahi, instruction hai. Agar yeh missing ho, browser old rendering mode use kar sakta hai. |
| `<html lang="en">` | Yeh page ka root wrapper hai. Saara HTML content isi ke andar hota hai. `lang="en"` language declare karta hai. Screen reader correct pronunciation ke liye language value use kar sakta hai. SEO tools bhi language understand karte hain. |
| `</html>` | Yeh complete HTML document ko close karta hai. Iske baad page ka content logically finish ho jaata hai. |

## B. Head Section Lines

| Code | Deep Explanation |
|---|---|
| `<head>` | Head page ka information center hai. Isme browser aur search engine ke liye instructions hoti hain. User ko direct page body mein yeh content visible nahi hota. |
| `<meta charset="UTF-8">` | Character encoding UTF-8 set karta hai. Isse letters, numbers, symbols, Hindi/English text, special characters properly display hote hain. |
| `<meta name="viewport" content="width=device-width, initial-scale=1.0">` | Mobile and responsive layout ke liye must-have line hai. `width=device-width` means page screen width ke according fit ho. `initial-scale=1.0` means default zoom normal ho. |
| `<meta name="description" content="...">` | Page ka short summary provide karta hai. Yeh user ko page par visible nahi hota, but search engines page ka purpose samajhne mein use kar sakte hain. Har page ka description unique hona chahiye. |
| `<title>...</title>` | Browser tab title set karta hai. Agar multiple tabs open hain, user title se page identify karta hai. SEO mein bhi title important hota hai. |
| `</head>` | Head section close karta hai. Iske baad visible content usually body mein start hota hai. |

## C. Body and Layout Lines

| Code | Deep Explanation |
|---|---|
| `<body>` | Body website ka visible area hai. Browser window mein jo bhi heading, paragraph, image, form, table, navigation dikh raha hai, woh body ke andar likha hota hai. |
| `<header>` | Page ka top area define karta hai. Portfolio mein name, tagline, navigation yahan rakha gaya. Semantic tag hone ki wajah se code ka meaning clear hota hai. |
| `<main>` | Page ka primary content define karta hai. Header and footer common support areas hain, but main content page ka actual topic hota hai. |
| `<section>` | Related content group karta hai. Example: Profile section, Skills section, Contact section. Section ko heading ke saath use karna best practice hai. |
| `<article>` | Independent content block ke liye use hota hai. Projects page mein har project ek article hai because each project has its own title and description. |
| `<footer>` | Page ka bottom area. Copyright, contact links, extra info footer mein rakha jaata hai. |

## D. Heading and Text Lines

| Code | Deep Explanation |
|---|---|
| `<h1>...</h1>` | Page ka main heading. Yeh page ke topic ko represent karta hai. Learner ko samjhao: h1 text bada karne ke liye nahi, main topic define karne ke liye hota hai. |
| `<h2>...</h2>` | Page ke major sections ke headings. Example: Welcome, Profile, Skills, Contact. |
| `<h3>...</h3>` | h2 ke andar subtopic ke liye. Projects page mein project title h3 hai because it belongs under Featured Work h2. |
| `<p>...</p>` | Paragraph text ke liye. Normal description, intro, explanation ke liye p tag use hota hai. |

## E. Navigation Lines

| Code | Deep Explanation |
|---|---|
| `<nav aria-label="Main navigation">` | Navigation section start karta hai. `aria-label` accessibility ke liye hai. Screen reader user ko pata chalega ki yeh main navigation links ka area hai. |
| `<a href="index.html">Home</a>` | Link create karta hai. `href` destination file ka path hai. `Home` clickable text hai. |
| `<a href="about.html">About</a>` | About page open karta hai. Multi-page website mein same nav all pages par rakhna user experience ke liye good hai. |
| `<a href="projects.html">Projects</a>` | Projects page ka link. Agar file name mismatch hua, link work nahi karega. |
| `<a href="contact.html">Contact</a>` | Contact form page ka link. |

## F. Image and Media Lines

| Code | Deep Explanation |
|---|---|
| `<img src="media/profile.jpg" alt="..." width="220">` | Image show karta hai. `src` file path hai. `alt` image description hai. `width` display size set karta hai. |
| `src="media/profile.jpg"` | Browser ko batata hai image `media` folder ke andar `profile.jpg` naam se available hai. Agar image path wrong hua toh image nahi dikhegi. |
| `alt="Rahul Sharma smiling..."` | Accessibility ke liye important. Screen reader alt text read karta hai. Image load fail hone par bhi alt text helpful hota hai. |
| `<video controls width="420">` | Video player create karta hai. `controls` play/pause/volume controls show karta hai. Agar controls na ho, user video easily control nahi kar paayega. |
| `<source src="media/intro.mp4" type="video/mp4">` | Video file location and file type define karta hai. Browser source tag se video file load karta hai. |
| `Your browser does not support...` | Fallback text. Agar browser video tag support nahi kare toh yeh text show ho sakta hai. |

## G. List and Table Lines

| Code | Deep Explanation |
|---|---|
| `<ul>` | Unordered list start karta hai. Jab points ka order important nahi hota, ul use karte hain. |
| `<li>...</li>` | List item. Har bullet point li tag mein hota hai. |
| `<table>` | Table create karta hai. Rows and columns data ke liye use hota hai. |
| `<thead>` | Table heading area group karta hai. |
| `<tbody>` | Table body data group karta hai. |
| `<tr>` | Table row. |
| `<th>` | Table header cell. Column heading ke liye. |
| `<td>` | Table data cell. Actual row data ke liye. |

## H. Form Lines

| Code | Deep Explanation |
|---|---|
| `<form>` | Form start karta hai. User input fields form ke andar grouped hote hain. |
| `<label for="fullName">Full Name</label>` | Label input ka name/purpose show karta hai. `for` attribute input ke `id` se connect hota hai. |
| `<input type="text" id="fullName" name="fullName" minlength="3" required>` | Text input create karta hai. `id` label connection ke liye, `name` submitted data key ke liye, `minlength` validation ke liye, `required` blank input prevent karne ke liye. |
| `<input type="email" id="email" name="email" required>` | Email input. Browser email format validate karta hai. |
| `<select id="course" name="course" required>` | Dropdown create karta hai. User ek option choose kar sakta hai. |
| `<option value="">Select a course</option>` | Default empty option. Required validation ke saath useful because user ko actual course select karna padega. |
| `<textarea id="message" name="message" rows="5" minlength="10" required></textarea>` | Multi-line text field. Message jaise long input ke liye useful. |
| `<button type="submit">Send Message</button>` | Submit button. Click karne par browser form validation run karta hai and valid hone par form submit hota hai. |

---

# Final Project Checklist

| Requirement | Completed |
|---|---|
| `index.html` created |  |
| `about.html` created |  |
| `projects.html` created |  |
| `contact.html` created |  |
| Same navigation on all pages |  |
| HTML5 structure used |  |
| Semantic tags used |  |
| Skills list added |  |
| Education table added |  |
| Image with alt text added |  |
| Video/media tag used |  |
| Contact form created |  |
| Form validation added |  |
| Meta description added |  |
| Browser testing done |  |

---

# Final Learning Summary

In this module, learner created a basic multi-page portfolio website using HTML5. This project covered all important HTML5 structure topics in one continuous flow. Learner started with `index.html`, then created about, projects and contact pages. During the project, learner used semantic tags, navigation, lists, tables, images, media, forms, validation, accessibility and SEO basics.

The most important learning is that HTML gives structure to a webpage. Semantic HTML gives meaning to that structure. Forms collect user input. Validation improves input quality. Accessibility makes the website usable for more people. SEO-friendly HTML helps search engines understand the page. Cross-browser testing makes sure the page works for different users.

After completing this module, learner will have a basic portfolio website and a strong foundation for CSS, JavaScript and MERN stack development.
