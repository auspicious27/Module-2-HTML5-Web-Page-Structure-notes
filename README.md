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

| Semantic Tag | Detailed Explanation and Portfolio Use |
|---|---|
| `<header>` | `header` page ka top introduction area hota hai. Isme usually website name, logo, tagline, and navigation rakha jaata hai. Portfolio project mein `header` learner ka website title and nav links hold karta hai. Isse browser, screen reader, and developer ko clear hota hai ki yeh page ka starting/top identity area hai. |
| `<nav>` | `nav` navigation links ke liye semantic tag hai. Iske andar woh links aate hain jinke through user Home, About, Projects, Contact jaise pages par jaata hai. Agar links ko normal paragraph mein rakh denge toh browser ko navigation ka meaning clear nahi hoga, isliye menu links ke liye `nav` better hai. |
| `<main>` | `main` page ka primary content area hota hai. Header and footer har page par repeat ho sakte hain, lekin `main` ke andar current page ka actual content hota hai. Example: About page mein profile, skills, education; Contact page mein form. Ek page mein generally ek hi `main` use karna best practice hai. |
| `<section>` | `section` related content ko group karta hai. Jab page mein alag-alag topics hote hain, jaise Welcome section, Skills section, Education section, Contact section, tab `section` use karte hain. Section ke andar heading dena good practice hai, because heading se user ko section ka topic samajh aata hai. |
| `<article>` | `article` independent content block ke liye use hota hai. Portfolio mein har project apne aap mein complete content hai: title, description, maybe image/video. Isliye project card ke liye `article` meaningful hai. Agar kal project card ko kisi aur page par move karein, phir bhi woh independently samajh aayega. |
| `<footer>` | `footer` page ka bottom area hota hai. Isme copyright, contact info, quick links, ya extra note aa sakta hai. Portfolio mein footer se page complete feel hota hai aur learner ko page structure ka proper start-middle-end pattern samajh aata hai. |

## HTML5 and Semantic HTML - Deep Understanding

HTML5 sirf old HTML ka new version nahi hai. HTML5 ne web pages ko more meaningful, media-friendly, and modern banaya. Pehle developers layout ke liye mostly `<div>` use karte the. `div` ka meaning generic hota hai, matlab browser ko nahi pata ki yeh header hai, menu hai, article hai, ya footer hai. HTML5 semantic tags is problem ko solve karte hain.

Semantic HTML ka simple meaning hai: tag ka naam content ke role ko explain kare. Agar page ka top part hai toh `header`, navigation links hain toh `nav`, main content hai toh `main`, related block hai toh `section`, independent content hai toh `article`, bottom part hai toh `footer`. Isse code padhne wale learner ko immediately samajh aata hai ki page ka structure kya hai.

Real-world example: School building mein different rooms ka naam hota hai: classroom, office, library, lab. Agar sab rooms ka naam sirf “room” ho, toh confusion hoga. Same tarah website mein agar har jagah sirf `div` use karein, toh meaning clear nahi hota. Semantic tags room names ki tarah kaam karte hain.

Semantic tags ka benefit sirf readability nahi hai. Screen readers in tags ko use karke visually impaired users ko page navigate karne mein help kar sakte hain. Search engines bhi page ke important parts better understand kar sakte hain. Team project mein another developer code open karega toh usko quickly pata chalega ki kaunsa part navigation hai, kaunsa main content hai, aur kaunsa footer.

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
| `<img src="media/profile.jpg"...>` | Yeh image tag browser ko bolta hai ki page par ek image display karni hai. `src` ka full form source hota hai, yani image file ka path. Yahan `media/profile.jpg` ka meaning hai: current HTML file ke folder ke andar `media` folder mein jao, phir `profile.jpg` image load karo. Agar folder name ya file name galat hua, image show nahi hogi. |
| `alt="Profile photo of Rahul"` | `alt` alternative text hota hai. Agar image load nahi hoti toh browser yeh text show kar sakta hai. Screen reader users ke liye bhi yeh bahut important hai, kyunki screen reader image ko dekh nahi sakta, woh alt text read karta hai. Isliye alt text meaningful hona chahiye, jaise “Profile photo of Rahul”, sirf “image” nahi. |
| `width="200"` | Yeh image ki display width 200 pixels set karta hai. Isse image page par bahut badi nahi dikhegi. Important: yeh image file ka actual size change nahi karta, sirf browser mein display size control karta hai. Future mein CSS se image size aur better control kar sakte hain. |
| `<ul>` | `ul` unordered list start karta hai. Unordered list tab use hoti hai jab points ka order important nahi hota. Skills list mein HTML, CSS, JavaScript ka order compulsory nahi hai, isliye bullet list ke liye `ul` best hai. |
| `<li>` | `li` list item hota hai. `ul` ya `ol` ke andar har point ko `li` mein likhte hain. Agar learner direct text `ul` ke andar likhega bina `li` ke, structure incorrect ho jaayega. Har skill ek separate `li` item honi chahiye. |
| `<table>` | `table` rows and columns wala structured data create karta hai. Education details mein Course, Institute, Year alag columns hain, isliye table use karna correct hai. Plain paragraph mein data likhne se comparison/readability weak ho jaati. |
| `<thead>` | `thead` table ke heading area ko group karta hai. Iske andar usually column headings jaise Course, Institute, Year aate hain. Yeh browser and screen readers ko batata hai ki yeh table ka heading part hai, normal data rows nahi. |
| `<tr>` | `tr` table row create karta hai. Table mein har horizontal line ek row hoti hai. Heading row bhi `tr` se banti hai aur data row bhi `tr` se banti hai. `tr` ke andar direct text nahi, balki `th` ya `td` cells hone chahiye. |
| `<th>` | `th` table header cell hota hai. Column ke title ke liye use hota hai, jaise Course, Institute, Year. Browser by default `th` text ko bold and centered show kar sakta hai, but main reason styling nahi, semantic meaning hai. |
| `<tbody>` | `tbody` table ke main data area ko group karta hai. Headings `thead` mein hoti hain aur actual records `tbody` mein. Isse table ka structure clean, readable, and accessible hota hai. |
| `<td>` | `td` table data cell hota hai. Actual values jaise `HTML5 Basics`, `ABC Institute`, `2026` ko `td` ke andar likhte hain. Har row mein cells ka order column headings ke order ke according hona chahiye. |

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
| `<article>` | `article` independent content block ke liye use hota hai. Projects page mein har project ka apna title and description hai, isliye har project independently samajh aa sakta hai. Agar project card ko page se copy karke kisi blog ya portfolio section mein paste karein, tab bhi uska meaning complete rahega. |
| `<h3>` | `h3` project title ke liye use hua hai. Page structure mein pehle `h1` website title hai, phir `h2` section title hai, aur us section ke andar individual project title `h3` hai. Yeh heading hierarchy maintain karta hai, jo readability, accessibility, and SEO ke liye important hai. |
| `<video controls width="400">` | `video` tag HTML5 ka built-in media tag hai. Isse browser directly video player show karta hai. `controls` attribute play, pause, volume, seek bar jaise controls show karta hai. `width="400"` video player ki display width set karta hai, taaki video page layout mein manageable size mein dikhe. |
| `<source src="media/intro.mp4"...>` | `source` tag video file ki location define karta hai. `src="media/intro.mp4"` ka meaning hai ki video `media` folder ke andar `intro.mp4` naam se stored hai. Agar file path galat hai, video player show ho sakta hai but video play nahi hoga. |
| `type="video/mp4"` | Yeh browser ko file format batata hai. Browser pehle check karta hai ki kya woh MP4 video support karta hai. Correct MIME type dene se browser ko file handle karne mein help milti hai. |
| Fallback text | Video tag ke andar jo normal text likha hota hai, woh fallback text hai. Agar user ka browser video tag support nahi karta, toh yeh message show ho sakta hai. Isse user ko reason samajh aata hai ki video kyun nahi chal raha. |

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
| `<form>` | `form` user input collect karne ka container hai. Contact page mein name, email, course, and message fields form ke andar grouped hain. Jab user submit button click karta hai, browser isi form ke fields ko validate karta hai. Real backend project mein form data server ko send kiya ja sakta hai. |
| `<label for="fullName">` | `label` input field ka visible name/purpose batata hai. `for="fullName"` label ko us input se connect karta hai jiska `id="fullName"` hai. Is connection ka benefit: user label par click kare toh input focus ho jaata hai, aur screen reader field ka purpose clearly read kar sakta hai. |
| `<input type="text"...>` | `input` single-line user input field create karta hai. `type="text"` ka meaning hai ki user normal text enter karega, jaise full name. Is field mein `id`, `name`, `minlength`, and `required` jaise attributes add karke behavior control hota hai. |
| `minlength="3"` | Yeh browser validation rule hai. User ko minimum 3 characters enter karne honge. Example: `Ra` invalid ho sakta hai, but `Rahul` valid hoga. Yeh beginner-level validation ke liye useful hai, but real app mein backend validation bhi required hoti hai. |
| `required` | `required` field ko compulsory banata hai. Agar user field blank chhodkar submit karega, browser form submit nahi karega and warning message show karega. Isse empty data submit hone se prevent hota hai. |
| `<input type="email"...>` | Yeh email input field hai. Browser basic email pattern check karta hai, jaise value mein `@` and domain structure hona chahiye. Example: `rahul` invalid ho sakta hai, `rahul@gmail.com` valid format hai. |
| `<select>` | `select` dropdown field create karta hai. Jab options fixed hon, jaise interested course HTML/CSS/JavaScript, tab dropdown useful hota hai. Isse user random spelling mistake nahi karega, predefined option choose karega. |
| `<option value="">` | Yeh default empty option hai, usually text hota hai “Select a course”. `value=""` blank value rakhta hai. Jab `select` required hota hai, browser user ko actual option choose karne ke liye force kar sakta hai. |
| `<textarea>` | `textarea` multi-line text input ke liye use hota hai. Message, feedback, address, description jaise long text ke liye input type text se better hai. Opening and closing tag dono hote hain. |
| `rows="5"` | `rows` textarea ki visible height set karta hai. `rows="5"` ka meaning hai ki textarea approx 5 text lines ki height ke saath show hoga. User zyada text bhi type kar sakta hai, browser scroll add kar sakta hai. |
| `minlength="10"` | Message field ke liye minimum 10 characters rule lagata hai. Iska purpose hai ki user very short message jaise `hi` submit na kare. Learners ko samjhao ki validation data quality improve karta hai. |
| `<button type="submit">` | Submit button form validation trigger karta hai. Jab user is button par click karta hai, browser required, email, minlength jaise rules check karta hai. Agar form valid hai toh submit action proceed hota hai; agar invalid hai toh browser warning show karta hai. |

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
| `<!DOCTYPE html>` | Browser ko batata hai ki yeh HTML5 document hai. Yeh file ki first line honi chahiye, because browser isi instruction se modern HTML rules use karta hai. Agar yeh missing ho, browser old/quirks mode mein render kar sakta hai. |
| `<html lang="en">` | Complete HTML document ka root wrapper yahan se start hota hai. Saara `head` and `body` content isi ke andar aata hai. `lang="en"` page language English set karta hai, jo screen readers, browser translation, and SEO tools ke liye useful hai. |
| `<head>` | Head section page ka invisible information area hai. Isme title, meta tags, SEO description, responsive settings, and future CSS links aate hain. User ko yeh content page par directly nahi dikhta, but browser ke liye yeh very important hai. |
| `<meta charset="UTF-8">` | Character encoding set karta hai. UTF-8 use karne se English text, symbols, special characters, and many language characters properly display hote hain. Isko head ke andar top side par rakhna best practice hai. |
| `<meta name="viewport"...>` | Mobile responsive behavior ke liye important line hai. `width=device-width` browser ko bolta hai ki page device ki actual screen width ke according fit ho. `initial-scale=1.0` default zoom normal rakhta hai. |
| `<meta name="description"...>` | Search engines ko page ka short summary deta hai. Yeh text page body mein visible nahi hota, but Google/search tools page ka purpose understand karne ke liye use kar sakte hain. Har page ka description unique rakhna better hai. |
| `<title>Rahul Portfolio \| Home</title>` | Browser tab mein page title show karta hai. User ke multiple tabs open hon toh title se page identify hota hai. SEO mein bhi title important hota hai, isliye title meaningful and page-specific hona chahiye. |
| `</head>` | Head section close karta hai. Iske baad browser visible page content ke liye `body` section read karega. Closing tag structure ko clean and valid banata hai. |
| `<body>` | Body visible page content ka start point hai. Browser window mein jo heading, paragraph, list, nav, footer dikh raha hai, woh sab body ke andar likha hota hai. |
| `<header>` | Page ka top semantic section hai. Is home page mein website owner ka name, short intro, and navigation links header mein rakhe gaye hain. Header se page ki identity immediately clear hoti hai. |
| `<h1>Rahul Sharma</h1>` | Page ka main heading hai. Home page par portfolio owner ka naam main identity hai, isliye `h1` use kiya. Ek page par generally ek clear `h1` rakhna best practice hai. |
| `<p>Beginner Web Developer...</p>` | Short intro paragraph hai. Visitor ko quickly pata chal jaata hai ki Rahul kya learn kar raha hai and page ka context kya hai. Paragraph normal readable text ke liye use hota hai. |
| `<nav aria-label="Main navigation">` | Navigation area create karta hai. `aria-label="Main navigation"` screen reader users ko batata hai ki yeh main menu hai. Accessibility ke liye yeh helpful hai, especially jab page mein multiple navigation areas ho sakte hain. |
| `<a href="index.html">Home</a>` | Anchor link Home page ke liye hai. `href="index.html"` destination file path hai. Click karne par browser current folder ke andar `index.html` open karta hai. |
| `<a href="about.html">About</a>` | About page link hai. Same folder mein `about.html` file honi chahiye. Agar file name mismatch hua toh link work nahi karega. |
| `<a href="projects.html">Projects</a>` | Projects page link hai. User is link se projects details page par ja sakta hai. Multi-page website mein same navigation repeat karna user ke liye easy hota hai. |
| `<a href="contact.html">Contact</a>` | Contact page link hai. User is page par form fill karke message bhejne ka flow samajh sakta hai. `href` exact file name ke saath match hona chahiye. |
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
| `<!DOCTYPE html>` | Yeh line browser ko batati hai ki page HTML5 standard follow kar raha hai. About page bhi ek separate HTML document hai, isliye isme bhi same declaration top par required hai. |
| `<html lang="en">` | Page ka root element hai. `lang="en"` se browser and assistive tools ko language English pata chalti hai. Har page par language define karna professional habit hai. |
| `<head>` | About page ki invisible information yahan start hoti hai. Is section mein browser tab title, SEO description, encoding, and responsive settings rakhe gaye hain. |
| `<meta charset="UTF-8">` | Text encoding define karta hai. Learner ke naam, symbols, and special characters properly display karne ke liye UTF-8 safe choice hai. |
| `<meta name="viewport"...>` | Mobile devices ke liye page ko properly scale karne mein help karta hai. Portfolio agar phone par open ho, toh browser page ko device width ke according render karega. |
| `<meta name="description"...>` | About page ka SEO summary hai. Search engine ko batata hai ki is page mein Rahul ki skills, education, and learning journey ke baare mein content hai. |
| `<title>Rahul Portfolio \| About</title>` | Browser tab ka title hai. Is title se user ko pata chalta hai ki woh portfolio ke About page par hai, Home page par nahi. |
| `<body>` | Visible content start karta hai. About page mein user ko heading, navigation, image, profile paragraph, skills list, education table, and footer dikhte hain. |
| `<header>` | Top area start karta hai. Isme page heading and navigation links rakhe gaye hain, taaki user kisi bhi page par easily move kar sake. |
| `<h1>About Rahul</h1>` | About page ka main heading hai. Yeh page ka primary topic define karta hai. Heading hierarchy ke liye `h1` top-level heading hoti hai. |
| `<nav aria-label="Main navigation">` | Accessible navigation section hai. `aria-label` screen reader ko clear karta hai ki yeh main navigation menu hai. |
| `<a href="...">` | Har anchor tag ek clickable page link banata hai. `href` ke andar destination file ka naam hota hai, jaise `index.html`, `projects.html`, ya `contact.html`. |
| `<main>` | About page ka unique main content start karta hai. Header/footer common parts hain, but profile, skills, and education about page ka actual main content hai. |
| `<section>` | Profile content group karne ke liye section use hua hai. Section related content ko ek block mein organize karta hai. |
| `<h2>Profile</h2>` | Profile section ka heading hai. Since page ka main heading `h1` hai, section heading ke liye `h2` logical choice hai. |
| `<img src="media/profile.jpg"...>` | Profile image load karta hai. `src` image ka path batata hai. Browser current folder se `media` folder mein jaakar `profile.jpg` image dhundhega. |
| `alt="Rahul Sharma smiling..."` | Image ka meaningful text description hai. Agar image load nahi hoti ya screen reader use ho raha hai, toh yeh text image ka purpose explain karta hai. |
| `width="220"` | Image ki display width 220 pixels set karta hai. Yeh page layout ko controlled rakhta hai, taaki image unexpectedly huge na dikhe. |
| `<p>I am learning...</p>` | Profile paragraph hai. Isme learner apni learning journey simple text mein explain karta hai. Paragraph tag normal readable content ke liye best hai. |
| `<section>` | Skills ke liye separate section start hota hai. Separate section se profile and skills content mix nahi hota. |
| `<h2>Skills</h2>` | Skills section heading hai. User ko immediately pata chal jaata hai ki neeche skills ki list aayegi. |
| `<ul>` | Skills ko bullet list mein show karne ke liye unordered list use hoti hai. Skills ka order strict nahi hota, isliye `ul` correct choice hai. |
| `<li>...</li>` | Har skill ek separate list item hai. Isse skills readable and scannable banti hain. Har bullet point ko `li` ke andar hi likhna chahiye. |
| `<section>` | Education table ke liye separate section start hota hai. Yeh content profile/skills se alag topic hai. |
| `<h2>Education</h2>` | Education section ka heading hai. Heading se learner and screen reader dono ko table ka context milta hai. |
| `<table>` | Structured rows and columns data ke liye table start karta hai. Education details mein course, institute, year columns hain, isliye table meaningful hai. |
| `<thead>` | Table heading rows ko group karta hai. Column names ko `thead` mein rakhne se table structure clear hota hai. |
| `<tr>` | Table row create karta hai. Har row ke andar heading cells ya data cells aate hain. |
| `<th>` | Table header cell hai. Column title jaise Course, Institute, Year ke liye use hota hai. |
| `<tbody>` | Table ka main data body hai. Actual education records `tbody` ke andar rakhte hain. |
| `<td>` | Normal table data cell hai. Course name, institute name, and year jaise actual values `td` mein aati hain. |
| `</table>` | Table close karta hai. Is closing tag ke baad browser ko pata chalta hai ki education table complete ho gaya. |
| `<footer>` | Bottom section hai. Footer page ka closing area create karta hai, jahan copyright ya extra info rakhi ja sakti hai. |
| `&copy;` | HTML entity hai jo copyright symbol render karta hai. Direct symbol ke bajay entity use karna safe and standard approach hai. |

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
| `<!DOCTYPE html>` | Browser ko batata hai ki projects page HTML5 document hai. Har separate HTML page mein yeh declaration top par hona chahiye. |
| `<html lang="en">` | Root HTML element hai jo complete projects page ko wrap karta hai. `lang="en"` language define karta hai. |
| `<head>` | Page metadata start hota hai. Projects page ke title, description, encoding, and viewport settings yahan rakhe gaye hain. |
| `<meta charset="UTF-8">` | Character support ke liye encoding set karta hai. Yeh text and symbols ko correctly display karne mein help karta hai. |
| `<meta name="viewport"...>` | Mobile-friendly page rendering ke liye important hai. Iske bina mobile par page zoomed-out ya awkward dikhega. |
| `<meta name="description"...>` | Projects page ka SEO description hai. Search engine ko page ka topic samajh aata hai: Rahul ke projects and HTML5 learning work. |
| `<title>Rahul Portfolio \| Projects</title>` | Browser tab mein projects page title show karta hai. Page-specific title user navigation ko easy banata hai. |
| `<body>` | Visible projects page content start hota hai. Header, project articles, video section, and footer body mein dikhte hain. |
| `<header>` | Page ka top area hai. Isme main heading and navigation links rakhe gaye hain. |
| `<h1>My Projects</h1>` | Projects page ka main heading hai. Yeh user ko clearly batata hai ki page projects showcase ke liye hai. |
| `<nav aria-label="Main navigation">` | Page links ka accessible navigation area hai. Screen reader user ko navigation ka purpose clear hota hai. |
| `<main>` | Projects page ka main content start karta hai. Iske andar featured work and demo video sections aate hain. |
| `<section>` | Featured work group karta hai. Related project cards ko ek section ke andar organize karna clean structure deta hai. |
| `<h2>Featured Work</h2>` | Section heading hai. User ko pata chalta hai ki neeche featured projects listed hain. |
| `<article>` | Independent project card hai. Article isliye useful hai kyunki har project apne title and description ke saath complete content item hai. |
| `<h3>Portfolio Website</h3>` | Project title hai. `h3` use hota hai because yeh `h2` Featured Work ke andar sub-heading hai. |
| `<p>A multi-page...</p>` | Project description hai. Isme learner explain karta hai ki project kis cheez se bana hai and kya purpose hai. |
| Second `<article>` | Dusra independent project block hai. Har project ke liye separate article use karne se structure repeatable and clean banta hai. |
| `<section>` | Demo video ke liye separate section hai. Video content project cards se alag type ka content hai, isliye separate section readable hai. |
| `<video controls width="420">` | HTML5 video player create karta hai. `controls` user ko play/pause/volume controls deta hai. `width="420"` player ki display width set karta hai. |
| `<source src="media/intro.mp4"...>` | Video file path and format define karta hai. Browser `media` folder se `intro.mp4` load karega. |
| `type="video/mp4"` | Browser ko batata hai ki source file MP4 format ki video hai. Correct type browser ko media handle karne mein help karta hai. |
| Fallback text | Agar browser video tag support na kare ya video load na ho, toh fallback message user ko explain kar sakta hai ki video support available nahi hai. |
| `<footer>` | Bottom copyright section hai. Footer page ka ending area create karta hai. |

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
| `<!DOCTYPE html>` | Contact page bhi HTML5 document hai, isliye top par declaration required hai. Browser is instruction ke basis par modern HTML mode use karta hai. |
| `<html lang="en">` | Complete contact page ka root element hai. `lang="en"` language define karta hai, jo accessibility and SEO ke liye helpful hai. |
| `<head>` | Metadata and SEO section start hota hai. Contact page ka title, description, encoding, and viewport settings yahan rakhe gaye hain. |
| `<meta charset="UTF-8">` | Character encoding set karta hai. Isse form labels, symbols, and normal text correctly render hote hain. |
| `<meta name="viewport"...>` | Responsive page behavior ke liye important hai. Contact form mobile screen par properly scale ho sake, iske liye viewport meta tag use hota hai. |
| `<meta name="description"...>` | Search engine friendly contact page summary hai. Search engine ko samajh aata hai ki yeh accessible HTML5 contact form wala page hai. |
| `<title>Rahul Portfolio \| Contact</title>` | Browser tab title set karta hai. User ko clearly pata chalta hai ki woh Contact page par hai. |
| `<body>` | Visible page content start karta hai. Contact page mein heading, nav, form fields, submit button, and footer body ke andar visible hote hain. |
| `<header>` | Top page section hai. Isme page heading and navigation links aate hain. |
| `<h1>Contact Me</h1>` | Main page heading hai. User ko page ka purpose immediately clear hota hai: yahan contact/message send karna hai. |
| `<nav aria-label="Main navigation">` | Accessible navigation links ka group hai. `aria-label` screen reader users ko batata hai ki yeh main navigation menu hai. |
| `<main>` | Main contact content start karta hai. Contact form page ka primary content form hai, isliye form main ke andar rakha gaya hai. |
| `<section>` | Contact form section group karta hai. Section use karne se form-related heading and form fields ek meaningful block mein aa jaate hain. |
| `<h2>Send a Message</h2>` | Form section heading hai. User ko batata hai ki neeche message send karne ka form hai. |
| `<form>` | Form container hai. Saare input fields isi ke andar hain. Browser submit button click hone par isi form ke validation rules check karta hai. |
| `<label for="fullName">Full Name</label>` | Label name input ka purpose batata hai. `for="fullName"` input ke `id="fullName"` se connect hota hai, jisse accessibility and click behavior improve hota hai. |
| `<input type="text"...>` | Text input field hai jahan user apna full name enter karega. Single-line normal text ke liye `type="text"` use hota hai. |
| `id="fullName"` | Unique identifier hai. Label isi `id` ko use karke input se connect hota hai. Same page par same id repeat nahi karna chahiye. |
| `name="fullName"` | Field ka submitted data name hai. Backend ya form processing mein yeh key ban sakti hai, jaise `fullName=Rahul Sharma`. |
| `minlength="3"` | Browser validation rule hai. User ko minimum 3 characters enter karne honge. Yeh very short/invalid name input ko prevent karta hai. |
| `required` | Field compulsory banata hai. User blank chhodkar submit karega toh browser warning show karega and form submit nahi hoga. |
| `<input type="email"...>` | Email input field hai. Browser basic email format validate karta hai, jaise `name@example.com`. Yeh normal text input se better hai because built-in email validation milti hai. |
| `<select id="course"...>` | Dropdown list create karta hai. Jab options fixed hon, dropdown user ko correct option choose karne mein help karta hai and spelling mistakes avoid karta hai. |
| `<option value="">Select a course</option>` | Default empty option hai. Required dropdown ke saath yeh useful hai, kyunki user ko actual course choose karna padega. Blank value valid selection nahi maana jaata. |
| `<option value="html">HTML5</option>` | Dropdown option hai. User ko screen par `HTML5` dikhega, aur submit hone par value `html` ja sakti hai. Value usually lowercase/short rakhi jaati hai. |
| `<textarea...>` | Multi-line message input hai. Contact message normal input se lamba ho sakta hai, isliye textarea use karna better hai. |
| `rows="5"` | Textarea ki visible height approx five lines set karta hai. User zyada text type kare toh textarea scroll ya resize behavior show kar sakta hai. |
| `minlength="10"` | Message ke liye minimum 10 characters required karta hai. Isse user very short message submit nahi karega and input quality better hogi. |
| `<button type="submit">` | Form submit button hai. Is button par click karne se browser pehle validation run karta hai, phir form submit process start karta hai. |
| `</form>` | Form yahan close hota hai. Is closing tag se browser ko pata chalta hai ki form fields ka group complete ho gaya. |
| `<footer>` | Footer area hai. Page ka bottom section create karta hai jahan copyright ya closing information rakhi ja sakti hai. |

---

# Small Code Snippets and Output Blocks - Detailed Explanation

## Why This Section Is Added

Document mein full HTML pages ke saath-saath kuch small snippets bhi hain, jaise folder structure, file names, expected output, mini task code, and small form fields. Beginner learner ke liye yeh small snippets bhi important hote hain, because practical class mein confusion mostly yahi hota hai: file kahan save karni hai, path ka meaning kya hai, output kaise check karna hai, and small tag ka role kya hai. Is section mein un chhote snippets ko bhi detail mein explain kiya gaya hai.

---

## 1. Project Folder Structure Snippet

Snippet:

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

| Line / Code | Detailed Hinglish Explanation |
|---|---|
| `portfolio-site/` | Yeh main project folder hai. Iske andar website ki saari files rahengi. Slash `/` ka meaning hai ki yeh folder hai, normal file nahi. VS Code mein isi folder ko open karna hai. |
| `index.html` | Yeh home page file hai. Static website mein usually `index.html` starting page hota hai. GitHub Pages bhi root URL par mostly `index.html` ko hi load karta hai. |
| `about.html` | Yeh second page hai jahan learner apni profile, skills, and education details rakhega. Isse multi-page website ka concept clear hota hai. |
| `projects.html` | Yeh projects page hai. Portfolio mein learner apne projects yahan show karega. Is page mein `article` and `video` jaise tags ka practical use hota hai. |
| `contact.html` | Yeh contact page hai. Is page mein form, input, labels, validation, button, dropdown, textarea jaise HTML5 form topics cover hote hain. |
| `media/` | Yeh folder images and videos ke liye hai. Agar images ko alag folder mein rakhenge, project clean and professional lagega. |
| `profile.jpg` | Profile photo image file. Isko `about.html` mein `<img src="media/profile.jpg">` se use karenge. File name same hona chahiye, warna image show nahi hogi. |
| `intro.mp4` | Demo video file. Isko `projects.html` mein `<video>` tag ke andar use karenge. Agar file missing hai toh video player blank ya error show kar sakta hai. |

Teaching point: Learner ko bolna hai ki file name, extension, and folder path exact match hona chahiye. `Profile.jpg` and `profile.jpg` same nahi hote, especially hosting/server par.

---

## 2. VS Code File Creation Snippets

Snippet:

```text
portfolio-site
```

| Line / Code | Detailed Hinglish Explanation |
|---|---|
| `portfolio-site` | Yeh folder ka naam hai. Folder ka naam simple, lowercase, and without spaces rakhna best hai. Spaces se URL/path handling mein beginners ko confusion ho sakta hai. |

Snippet:

```text
index.html
about.html
projects.html
contact.html
```

| Line / Code | Detailed Hinglish Explanation |
|---|---|
| `index.html` | Home page create karne ke liye yeh file banegi. `.html` extension browser ko batata hai ki yeh HTML document hai. |
| `about.html` | About page ke liye separate file. Separate file ka benefit hai ki content organized rahta hai. |
| `projects.html` | Project listing ke liye page. Isme learner future mein apne real projects add kar sakta hai. |
| `contact.html` | User input collect karne ke liye contact page. Isme forms and validation practice hoti hai. |

Snippet:

```text
media
```

| Line / Code | Detailed Hinglish Explanation |
|---|---|
| `media` | Yeh assets folder hai. Assets ka matlab images, videos, audio, PDFs, etc. Day 2 mein hum image/video rakh rahe hain. Future mein CSS/JS folders bhi add ho sakte hain. |

---

## 3. Head and Body Meaning Snippet

Snippet:

```text
head = page information, SEO, title, metadata
body = visible content jo user ko browser mein dikhta hai
```

| Line / Code | Detailed Hinglish Explanation |
|---|---|
| `head = page information, SEO, title, metadata` | `head` browser and search engine ke liye hota hai. Isme page ka title, description, mobile viewport, character encoding jaise settings hoti hain. Yeh content normally page body mein visible nahi hota. |
| `body = visible content jo user ko browser mein dikhta hai` | `body` website ka visible area hai. Jo learner browser mein dekhta hai, jaise heading, paragraph, image, nav links, form, table, woh sab body ke andar hota hai. |

Real-world example: Restaurant ka kitchen and menu system `head` jaisa hai, customer ko directly nahi dikhta but important hai. Dining table par jo food serve hota hai, woh `body` jaisa visible content hai.

---

## 4. Expected Output Blocks Explanation

Expected output snippets code nahi hote, lekin learner ko yeh batate hain ki browser mein result kaisa dikhega. Jab learner HTML file run karta hai, usko exact same styling nahi milegi kyunki CSS abhi add nahi kiya. But structure same hona chahiye.

| Output Line / Idea | Detailed Hinglish Explanation |
|---|---|
| Website title show hona | Browser page ke top area mein `My Portfolio` heading dikhni chahiye. Agar heading nahi dikh rahi, toh `<h1>` ya file save issue ho sakta hai. |
| Navigation links show hona | Home, About, Projects, Contact links visible hone chahiye. Click karne par related HTML file open honi chahiye. |
| Paragraph text show hona | `<p>` ke andar jo intro/description likha hai, woh browser mein normal text ki tarah show hoga. |
| Image show hona | Agar `profile.jpg` media folder mein hai and path correct hai, image dikhegi. Agar nahi dikhegi toh path/file name check karna hai. |
| Table show hona | Education details rows and columns mein dikhni chahiye. Agar table broken lage, `<tr>`, `<th>`, `<td>` nesting check karo. |
| Form validation work hona | Required field blank chhod kar submit karoge toh browser warning dega. Yeh HTML5 validation ka practical proof hai. |
| Video player show hona | `controls` attribute ki wajah se play/pause buttons visible hone chahiye. Agar video file missing hai, page structure phir bhi visible rahega. |

---

## 5. Navigation Mini Snippet Explanation

Snippet:

```html
<nav>
  <a href="index.html">Home</a>
  <a href="about.html">About</a>
  <a href="projects.html">Projects</a>
  <a href="contact.html">Contact</a>
</nav>
```

| Line / Code | Detailed Hinglish Explanation |
|---|---|
| `<nav>` | Yeh navigation area start karta hai. Browser and assistive tools ko clear signal milta hai ki andar page links hain. |
| `<a href="index.html">Home</a>` | `a` anchor tag hai. `href` destination batata hai. Jab user Home par click karega, browser `index.html` open karega. |
| `<a href="about.html">About</a>` | About link learner ko profile page par le jaata hai. File name exact same hona chahiye. |
| `<a href="projects.html">Projects</a>` | Projects page open karta hai. Multi-page website mein navigation repeat karna user experience ke liye important hai. |
| `<a href="contact.html">Contact</a>` | Contact form page open karta hai. User website owner se connect karne ke liye is page ka use karega. |
| `</nav>` | Navigation area close karta hai. Closing tag se browser ko pata chalta hai ki navigation links yahin tak the. |

Important teaching point: `href` file path wrong hua toh link click karne par page not found ya blank issue aa sakta hai.

---

## 6. Mini Task Project Snippet Explanation

Snippet:

```text
Project Name: HTML Table Practice
Description: This project displays course information using an HTML table.
```

| Line / Code | Detailed Hinglish Explanation |
|---|---|
| `Project Name: HTML Table Practice` | Yeh project ka title hai. Learner isko `<h3>` ke andar likh sakta hai because yeh Projects section ke andar ek sub-heading hai. |
| `Description: This project displays course information using an HTML table.` | Yeh project ka short explanation hai. Isko `<p>` tag ke andar likhna chahiye because yeh normal paragraph content hai. |

How to convert into HTML:

```html
<article>
  <h3>HTML Table Practice</h3>
  <p>This project displays course information using an HTML table.</p>
</article>
```

| Line / Code | Detailed Hinglish Explanation |
|---|---|
| `<article>` | Ek independent project block start karta hai. Har project card ko article banana semantic HTML ke according better hai. |
| `<h3>HTML Table Practice</h3>` | Project ka title show karta hai. `h3` use hota hai because parent section ka heading usually `h2` hota hai. |
| `<p>This project displays...</p>` | Project ka description show karta hai. Paragraph user ko batata hai ki project mein kya banaya gaya. |
| `</article>` | Project block close karta hai. Iske baad next project ka article start ho sakta hai. |

---

## 7. Phone Number Field Mini Snippet Explanation

Snippet:

```html
<label for="phone">Phone Number</label>
<input type="tel" id="phone" name="phone">
```

| Line / Code | Detailed Hinglish Explanation |
|---|---|
| `<label for="phone">Phone Number</label>` | Label user ko batata hai ki field mein phone number enter karna hai. `for="phone"` label ko input ke `id="phone"` se connect karta hai. |
| `<input type="tel" id="phone" name="phone">` | Phone input field create karta hai. `type="tel"` browser ko batata hai ki yeh telephone number input hai. Mobile device par number-friendly keyboard open ho sakta hai. |
| `id="phone"` | Unique ID hai. Label connection ke liye use hota hai. Same page par same `id` repeat nahi karna chahiye. |
| `name="phone"` | Jab form submit hota hai, backend ko data key ke form mein `phone` naam milta hai. Example: `phone=9876543210`. |

Optional better validation:

```html
<input type="tel" id="phone" name="phone" pattern="[0-9]{10}" required>
```

| Line / Code | Detailed Hinglish Explanation |
|---|---|
| `pattern="[0-9]{10}"` | Browser ko bolta hai ki input exactly 10 digits ka hona chahiye. `[0-9]` means digit allowed, `{10}` means 10 digits. |
| `required` | Field blank nahi chhod sakte. Submit karne se pehle browser validation karega. |

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
