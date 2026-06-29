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
| `<!DOCTYPE html>` | Browser ko batata hai ki yeh HTML5 document hai. Isko top par likhna best practice hai. |
| `<html lang="en">` | HTML document ka root element. `lang="en"` page language English set karta hai. Screen readers and SEO ke liye useful. |
| `<head>` | Page ki information start hoti hai. Isme metadata, title, SEO info aati hai. |
| `<meta charset="UTF-8">` | Text encoding set karta hai. Isse special characters and symbols properly show hote hain. |
| `<meta name="viewport"...>` | Mobile responsive behavior ke liye important hai. Page device width ke according render hota hai. |
| `<meta name="description"...>` | Search engines ko page ka short description deta hai. SEO-friendly layout ka part hai. |
| `<title>` | Browser tab mein title show karta hai. Search result mein bhi use ho sakta hai. |
| `<body>` | Visible page content yahan start hota hai. |
| `<header>` | Page ka top section. Isme usually website title/logo and navigation hota hai. |
| `<h1>` | Page ka main heading. Home page ka main identity title. |
| `<nav>` | Navigation links ko group karta hai. Semantic HTML mein nav important hai. |
| `<a href="index.html">Home</a>` | Anchor link. Click karne par `index.html` open hota hai. |
| `<main>` | Page ka main unique content. Har page mein main section ideally ek hota hai. |
| `<section>` | Related content ka group. Yahan welcome section banaya hai. |
| `<h2>` | Section heading. `h1` ke baad subheading ke liye `h2` use hota hai. |
| `<p>` | Paragraph text. Normal readable content ke liye use hota hai. |
| `<footer>` | Page ka bottom area. Copyright, contact, links yahan aa sakte hain. |

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

