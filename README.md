# Module 2: HTML5 - Web Page Structure Complete Notes

Language style: Simple Hinglish  
Goal: Learners ko HTML5 web page structure starting se samjhana, practical karwana, aur code ka har important part explain karna.

---

# Beginner Teaching Approach - Module 2 Ko Kaise Padhana Hai

Module 2 mein learners HTML5 seekhenge. HTML web development ka foundation hai. Agar learner HTML structure clearly samajh leta hai, toh CSS, JavaScript, React aur full stack development ka base strong ho jaata hai. Is module ko padhate time humein sirf tags yaad nahi karwane. Humein yeh samjhana hai ki browser HTML ko kaise read karta hai, tags ka meaning kya hota hai, aur real website mein unka use kahan hota hai.

Day 2 par students abhi beginner stage par hote hain. Isliye har topic ko teen layer mein explain karo. Pehle simple theory, phir real-world example, phir small practical. Jab practical karwao, toh code likhne ke baad output observe karwana must hai. Learner ko yeh clear hona chahiye ki kaunsi line browser mein kya effect create kar rahi hai.

## Teaching Flow

```text
Concept explain karo
-> Real-world example do
-> Small code likhwao
-> Browser output dikhao
-> Har line ka meaning explain karo
-> Common mistake batao
-> Small task do
```

## HTML Ko Ek Simple Story Se Samjho

Website ek document ki tarah hoti hai. Jaise school project file mein title, headings, paragraphs, images, tables aur sections hote hain, waise website mein bhi content structured hota hai. HTML browser ko batata hai ki kaunsa part heading hai, kaunsa paragraph hai, kaunsi image hai, kaunsa navigation hai, aur kaunsa form hai.

Browser HTML ko read karta hai aur visual page bana deta hai. HTML khud design language nahi hai. HTML structure deta hai. CSS design deta hai. JavaScript behavior/logic deta hai.

```text
HTML = Structure
CSS = Styling
JavaScript = Interaction
```

Example:

```text
HTML: Button create karta hai
CSS: Button ka color/size set karta hai
JavaScript: Button click hone par action perform karta hai
```

---

## Index - Is Module Mein Kya Seekhenge

| No. | Topic | Main Idea |
|---|---|---|
| 1 | HTML5 Document Structure | Basic page skeleton |
| 2 | Semantic HTML Elements | Meaningful layout tags |
| 3 | Forms and Input Validation | User input lena and validate karna |
| 4 | Tables, Lists, Images and Media | Content ko structured way mein show karna |
| 5 | Accessibility Best Practices | Website sab users ke liye usable banana |
| 6 | SEO-Friendly HTML Layouts | Search engines ke liye clear structure |
| 7 | Cross-Browser Compatibility | Different browsers mein page correctly work kare |
| 8 | Project 2 | Multi-page static website |

---

# Day/Class Setup - VS Code Practical Start

HTML ka practical karne ke liye humein heavy setup nahi chahiye. Sirf VS Code aur browser enough hai.

## Required Tools

| Tool | Use |
|---|---|
| VS Code | HTML files create/edit karne ke liye |
| Chrome Browser | Page output dekhne ke liye |
| Live Server extension optional | Auto refresh ke liye |
| Folder | Project files organize karne ke liye |

## Folder Setup

1. Ek folder banao:

```text
module-2-html-practice
```

2. VS Code open karo.
3. `File -> Open Folder` se folder open karo.
4. New file banao:

```text
index.html
```

5. Browser mein file open karo.

---

# 1. HTML5 Document Structure

## Starting Theory

HTML ka full form HyperText Markup Language hai. HTML website ka structure banata hai. Jaise building banane se pehle pillars, rooms, doors aur windows ka structure hota hai, waise website banane ke liye HTML basic structure provide karta hai.

HTML programming language nahi hai; yeh markup language hai. Iska kaam browser ko batana hota hai ki kaunsa content heading hai, kaunsa paragraph hai, kaunsi image hai, kaunsa form hai, aur kaunsa section hai.

HTML5 HTML ka modern version hai. HTML5 mein semantic tags, audio/video support, better form input types aur modern web page structure ke liye improvements aaye.

## Basic HTML5 Skeleton

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My First HTML5 Page</title>
</head>
<body>
  <h1>Welcome to HTML5</h1>
  <p>This is my first structured web page.</p>
</body>
</html>
```

## Line-by-Line Explanation

| Line | Code | Explanation |
|---|---|---|
| 1 | `<!DOCTYPE html>` | Browser ko batata hai ki yeh HTML5 document hai. |
| 2 | `<html lang="en">` | Complete HTML page ka root element. `lang="en"` batata hai ki page language English hai. |
| 3 | `<head>` | Head section mein page ki information hoti hai, jo usually screen par directly visible nahi hoti. |
| 4 | `<meta charset="UTF-8">` | Character encoding set karta hai. Isse text, symbols properly render hote hain. |
| 5 | `<meta name="viewport"...>` | Mobile responsive layout ke liye important hai. Browser ko screen width ke according page set karne ko bolta hai. |
| 6 | `<title>` | Browser tab mein jo title show hota hai. |
| 7 | `</head>` | Head section close karta hai. |
| 8 | `<body>` | Body mein visible page content hota hai. |
| 9 | `<h1>` | Main heading show karta hai. |
| 10 | `<p>` | Paragraph text show karta hai. |
| 11 | `</body>` | Body close karta hai. |
| 12 | `</html>` | HTML document close karta hai. |


## Browser HTML Ko Kaise Samajhta Hai?

Jab browser HTML file open karta hai, woh file ko top se bottom read karta hai. Browser tags ko identify karta hai aur phir page ka structure banata hai. Is structure ko DOM yani Document Object Model bhi bolte hain. Beginner level par simply samjho: browser HTML tags ko page elements mein convert karta hai.

Example:

```html
<h1>Hello</h1>
<p>Welcome to my page.</p>
```

Browser output:

```text
Hello                  -> large heading
Welcome to my page.    -> normal paragraph
```

Yahan `<h1>` browser ko bol raha hai ki yeh main heading hai. `<p>` browser ko bol raha hai ki yeh paragraph text hai.

## Opening Tag and Closing Tag

Most HTML elements opening aur closing tag ke saath likhe jaate hain.

```html
<p>This is a paragraph.</p>
```

| Part | Meaning |
|---|---|
| `<p>` | Opening tag |
| `This is a paragraph.` | Content |
| `</p>` | Closing tag |

Agar closing tag miss ho jaaye, browser kabhi-kabhi page ko guess karke render karta hai, lekin correct practice hamesha proper closing tag likhna hai.

## Empty / Self-Closing Type Elements

Kuch elements ke andar text content nahi hota, jaise image aur meta.

```html
<img src="photo.jpg" alt="Profile photo">
<meta charset="UTF-8">
```

In tags ka kaam attributes ke through hota hai. `img` image show karta hai, `meta` page information provide karta hai.

## Attributes Kya Hote Hain?

Attributes tag ko extra information dete hain.

```html
<a href="about.html">About</a>
```

Yahan `href="about.html"` attribute hai. Yeh browser ko batata hai ki link click karne par user ko `about.html` page par le jaana hai.

---

## Small Practical 1: First HTML Page

Create `index.html` and paste the skeleton code. Browser mein open karo.

### What Students Should Observe

- Browser tab mein title show hota hai.
- Page par heading and paragraph show hote hain.
- Agar `<title>` change karte hain, browser tab ka title change hota hai.
- Agar `<h1>` text change karte hain, page heading change hoti hai.

### Learning Outcome

Students samjhenge ki HTML page ek proper document structure follow karta hai. Har HTML page ka base skeleton similar hota hai.

---

# 2. Semantic HTML Elements

## Starting Theory

Semantic ka meaning hota hai meaningful. Semantic HTML tags browser, developer, screen reader aur search engine ko content ka meaning batate hain.

Example:

```html
<div>Header content</div>
```

Yeh browser ko sirf generic box lagta hai.

But:

```html
<header>Header content</header>
```

Yeh clearly batata hai ki content page ka header hai.

Semantic HTML clean, readable, accessible aur SEO-friendly hota hai.

## Important Semantic Tags

| Tag | Use |
|---|---|
| `<header>` | Page ya section ka top area |
| `<nav>` | Navigation links |
| `<main>` | Page ka main content |
| `<section>` | Related content ka section |
| `<article>` | Independent content, blog/card/news |
| `<footer>` | Page bottom information |

## Semantic Layout Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Semantic Page</title>
</head>
<body>
  <header>
    <h1>My Learning Website</h1>
    <nav>
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>

  <main>
    <section>
      <h2>About This Course</h2>
      <p>This course teaches web development step by step.</p>
    </section>

    <article>
      <h2>Why Learn HTML?</h2>
      <p>HTML is the foundation of every web page.</p>
    </article>
  </main>

  <footer>
    <p>Copyright 2026 - My Learning Website</p>
  </footer>
</body>
</html>
```

## Code Explanation

| Code | Explanation |
|---|---|
| `<header>` | Page ka top part, usually logo/title/navigation. |
| `<h1>` | Page ka main title. Usually ek page mein one main `h1` best hota hai. |
| `<nav>` | Navigation links group karta hai. |
| `<a href="...">` | Link create karta hai. `href` destination file/page batata hai. |
| `<main>` | Main unique content rakhta hai. |
| `<section>` | Related content group karta hai. |
| `<article>` | Independent content block. Blog post, news item, card, etc. |
| `<footer>` | Bottom area, copyright/contact/social links. |

## Small Practical 2: Convert Div Layout to Semantic Layout

### Objective

Learners ko yeh samjhana ki generic `<div>` se page ban sakta hai, lekin semantic tags se page ka meaning clear hota hai. Browser output similar dikh sakta hai, but code quality, accessibility aur SEO semantic tags se better hoti hai.

Students ko pehle yeh show karo:

```html
<div>
  <h1>Website</h1>
</div>
<div>
  <p>Main content</p>
</div>
<div>
  <p>Footer</p>
</div>
```

Then semantic version:

```html
<header>
  <h1>Website</h1>
</header>
<main>
  <p>Main content</p>
</main>
<footer>
  <p>Footer</p>
</footer>
```

### What Students Should Compare

- Dono code browser mein almost same text show kar sakte hain.
- Semantic version padhne mein easy hai.
- Screen reader aur search engine ko semantic version better samajh aata hai.
- Team project mein semantic code maintain karna easy hota hai.

### Learning Outcome

Students samjhenge ki dono browser mein similar dikh sakte hain, lekin semantic version meaningfully better hai. HTML sirf output ke liye nahi, meaning aur structure ke liye bhi likha jaata hai.

---

# 3. Forms and Input Validation

## Starting Theory

Forms website ka important part hain because forms user se data collect karte hain. Login form, signup form, contact form, search bar, feedback form, payment form - sab forms ke examples hain.

Input validation ka matlab user ke input ko check karna. Agar required field blank hai, email format galat hai, password short hai, ya number range galat hai, toh form submit nahi hona chahiye.

HTML5 built-in validation provide karta hai, jaise `required`, `type="email"`, `minlength`, `maxlength`, `min`, `max`, `pattern`.

## Contact Form Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Contact Form</title>
</head>
<body>
  <main>
    <h1>Contact Us</h1>

    <form>
      <label for="name">Full Name</label>
      <input type="text" id="name" name="name" required>

      <label for="email">Email Address</label>
      <input type="email" id="email" name="email" required>

      <label for="message">Message</label>
      <textarea id="message" name="message" rows="5" required></textarea>

      <button type="submit">Send Message</button>
    </form>
  </main>
</body>
</html>
```

## Line-by-Line Explanation

| Code | Explanation |
|---|---|
| `<form>` | Form area start karta hai. User input fields isi ke andar hote hain. |
| `<label for="name">` | Input ka label. `for="name"` input ke `id="name"` se connect hota hai. |
| `<input type="text"...>` | Text input field create karta hai. |
| `id="name"` | Unique ID. Label connect karne and JS/CSS targeting ke liye useful. |
| `name="name"` | Form submit hone par field ka key/name hota hai. |
| `required` | Field blank nahi chhod sakte. Browser validation karega. |
| `type="email"` | Email format validation automatically karta hai. |
| `<textarea>` | Long message input ke liye. |
| `rows="5"` | Textarea ki height approximate 5 rows. |
| `<button type="submit">` | Form submit button. |

## Small Practical 3: Form Validation Test

### Objective

Students ko form validation ka practical feel dena. Yeh samjhana ki browser HTML attributes jaise `required` aur `type="email"` ke basis par basic validation automatically kar sakta hai.

1. Contact form browser mein open karo.
2. Name blank chhodkar submit karo.
3. Browser required field warning show karega.
4. Email field mein `abc` likho and submit karo.
5. Browser valid email maangega.

### Expected Browser Behavior

- Required field blank hone par browser message show karega.
- Invalid email likhne par browser email format correct karne ko bolega.
- Form tab tak submit nahi hoga jab tak required fields valid na ho.

### Learning Outcome

Students samjhenge ki HTML5 without JavaScript bhi basic validation kar sakta hai. Lekin real applications mein backend validation bhi zaroori hoti hai, kyunki frontend validation user bypass kar sakta hai.

## More Input Types

| Input Type | Use |
|---|---|
| `text` | Normal text |
| `email` | Email validation |
| `password` | Password hidden input |
| `number` | Numeric input |
| `date` | Date picker |
| `radio` | Single choice |
| `checkbox` | Multiple choice |
| `file` | File upload |

## Signup Form Practical

```html
<form>
  <label for="username">Username</label>
  <input type="text" id="username" name="username" minlength="3" required>

  <label for="password">Password</label>
  <input type="password" id="password" name="password" minlength="6" required>

  <label for="age">Age</label>
  <input type="number" id="age" name="age" min="18" max="60">

  <button type="submit">Create Account</button>
</form>
```

## Code Explanation

| Code | Explanation |
|---|---|
| `minlength="3"` | Username minimum 3 characters hona chahiye. |
| `type="password"` | Password characters hide karta hai. |
| `minlength="6"` | Password minimum 6 characters. |
| `type="number"` | Number input field. |
| `min="18"` | Minimum age 18. |
| `max="60"` | Maximum age 60. |

---

# 4. Tables, Lists, Images and Media

## Starting Theory

Web page par content sirf paragraph nahi hota. Kabhi humein data table mein dikhana hota hai, kabhi points list mein, kabhi image show karni hoti hai, kabhi audio/video add karna hota hai.

HTML content ko structured format mein show karne ke liye tags provide karta hai.

## Lists

### Unordered List

```html
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

Explanation:

| Code | Explanation |
|---|---|
| `<ul>` | Unordered list. Bullets show karta hai. |
| `<li>` | List item. Har item ke liye use hota hai. |

### Ordered List

```html
<ol>
  <li>Create folder</li>
  <li>Create HTML file</li>
  <li>Open in browser</li>
</ol>
```

`<ol>` numbering show karta hai.

## Tables

```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Course</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Aman</td>
      <td>MERN Stack</td>
    </tr>
    <tr>
      <td>Priya</td>
      <td>HTML5</td>
    </tr>
  </tbody>
</table>
```

## Table Code Explanation

| Code | Explanation |
|---|---|
| `<table>` | Table start karta hai. |
| `<thead>` | Table header group. |
| `<tr>` | Table row. |
| `<th>` | Header cell. Bold/heading style hoti hai. |
| `<tbody>` | Main table body. |
| `<td>` | Normal table data cell. |

## Images

```html
<img src="student.jpg" alt="Student learning HTML" width="300">
```

Explanation:

| Code | Explanation |
|---|---|
| `<img>` | Image show karta hai. |
| `src="student.jpg"` | Image file path. |
| `alt="..."` | Image load na ho ya screen reader use ho toh text description. |
| `width="300"` | Image width set karta hai. |

## Media: Video

```html
<video controls width="400">
  <source src="intro.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

Explanation:

| Code | Explanation |
|---|---|
| `<video>` | Video player create karta hai. |
| `controls` | Play/pause controls show karta hai. |
| `<source>` | Video file and type define karta hai. |
| Fallback text | Agar browser support na kare toh message show hota hai. |

## Small Practical 4: Profile Page with List, Table and Image

Create `profile.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Student Profile</title>
</head>
<body>
  <main>
    <h1>Student Profile</h1>

    <img src="student.jpg" alt="Student profile photo" width="200">

    <h2>Skills</h2>
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
    </ul>

    <h2>Course Details</h2>
    <table>
      <tr>
        <th>Course</th>
        <th>Duration</th>
      </tr>
      <tr>
        <td>MERN Stack</td>
        <td>6 Months</td>
      </tr>
    </table>
  </main>
</body>
</html>
```

### Practical Explanation

This page combines multiple HTML concepts. Image shows profile photo, list shows skills, and table shows structured course details. Learners can see how different tags are used for different content types.

---

# 5. Accessibility Best Practices

## Starting Theory

Accessibility ka matlab website ko sab users ke liye usable banana, including users with disabilities. Some users screen reader use karte hain, kuch users keyboard se navigate karte hain, kuch users low vision ke saath website use karte hain.

Good HTML accessibility ka start semantic tags, proper labels, alt text, readable headings, and keyboard-friendly structure se hota hai.

## Important Accessibility Rules

| Rule | Why Important |
|---|---|
| Images mein `alt` use karo | Screen reader image ka meaning read kar sake |
| Form inputs ke saath `label` use karo | User ko field ka purpose clear ho |
| Headings order follow karo | Page structure clear hota hai |
| Buttons actual `<button>` se banao | Keyboard and screen reader support better |
| Links meaningful rakho | `Click here` ke badle clear text use karo |

## Bad vs Good Example

Bad:

```html
<input type="text">
```

Good:

```html
<label for="fullName">Full Name</label>
<input type="text" id="fullName" name="fullName">
```

## Explanation

Label se user ko input ka meaning samajh aata hai. Screen reader bhi label read kar sakta hai. Accessibility ke liye form fields ko labels ke saath connect karna best practice hai.

## Small Practical 5: Accessibility Check

Students apne form mein check karein:

- Har input ka label hai?
- Har image ka alt text hai?
- Page mein one clear `h1` hai?
- Navigation links meaningful hain?

---

# 6. SEO-Friendly HTML Layouts

## Starting Theory

SEO ka full form Search Engine Optimization hai. SEO-friendly HTML ka matlab aisa structure banana jise search engines easily understand kar sakein.

Search engines page ke headings, title, meta description, links, image alt text, and semantic tags ko read karte hain. Agar HTML structure clear hai, toh search engine ko page ka topic samajhne mein help milti hai.

## SEO Basics

| Element | Use |
|---|---|
| `<title>` | Browser tab and search result title |
| `<meta name="description">` | Page summary for search engines |
| One `<h1>` | Main topic |
| Proper headings | Content hierarchy |
| Semantic tags | Meaningful layout |
| Image alt text | Image meaning |
| Descriptive links | Clear navigation |

## SEO-Friendly Head Example

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Learn HTML5 web page structure with simple examples and practical exercises.">
  <title>HTML5 Web Page Structure Notes</title>
</head>
```

## Code Explanation

| Code | Explanation |
|---|---|
| `meta charset` | Text encoding set karta hai. |
| `viewport` | Mobile responsiveness ke liye important. |
| `meta description` | Search engine ko page summary deta hai. |
| `title` | Browser tab and SEO title. |

## Small Practical 6: Add SEO Tags

Students apne `index.html` ke `<head>` mein meta description add karein:

```html
<meta name="description" content="This is my first HTML5 learning page.">
```

Browser par direct visual change nahi dikhega, but page metadata improve hoga.

---

# 7. Cross-Browser Compatibility Basics

## Starting Theory

Cross-browser compatibility ka matlab website Chrome, Firefox, Safari, Edge jaise different browsers mein properly work kare. Har browser rendering engine slightly different ho sakta hai, isliye developer ko basic standards follow karne chahiye.

HTML5 standard tags use karne se compatibility improve hoti hai. Outdated tags avoid karne chahiye. Modern CSS/JS features use karte time browser support check karna chahiye.

## Basic Rules

| Rule | Meaning |
|---|---|
| Use valid HTML | Browser errors kam honge |
| Use semantic tags | Structure clear rahega |
| Add viewport meta tag | Mobile layout better |
| Test in multiple browsers | Issues jaldi milte hain |
| Avoid outdated tags | Modern standards follow karo |

## Small Practical 7: Test Same Page in Two Browsers

1. `index.html` Chrome mein open karo.
2. Same file Safari/Firefox/Edge mein open karo.
3. Output compare karo.
4. Check karo heading, form, image, table same dikh rahe hain ya nahi.

### Learning Outcome

Students samjhenge ki developer ko sirf apne browser mein nahi, multiple browsers mein output check karna chahiye.

---


---

# Deep Explanation: Important HTML Tags Learners Must Understand

## Heading Tags: `h1` to `h6`

HTML mein headings content hierarchy banati hain. `h1` sabse important heading hoti hai. `h2` subheading hoti hai. `h3` uske andar smaller heading hoti hai. Headings sirf text bada karne ke liye use nahi karni chahiye. Headings ka real purpose page structure define karna hai.

Example:

```html
<h1>Learning Academy</h1>
<h2>Courses</h2>
<h3>HTML Course</h3>
```

Meaning:

```text
Website/page main topic = Learning Academy
Section topic = Courses
Sub-topic = HTML Course
```

Good heading order accessibility aur SEO dono ke liye useful hota hai.

## Paragraph Tag: `p`

Paragraph normal text content ke liye use hota hai. Agar learners long explanation likhna chahte hain, toh `<p>` tag use karein.

```html
<p>HTML is used to create the structure of a web page.</p>
```

Browser paragraph ko normal readable text ke form mein show karta hai.

## Link Tag: `a`

Anchor tag links create karta hai. Multi-page website mein navigation links ke liye yeh very important hai.

```html
<a href="about.html">About Us</a>
```

Explanation:

| Part | Meaning |
|---|---|
| `<a>` | Anchor/link tag |
| `href="about.html"` | Link destination |
| `About Us` | Clickable text |

Agar `href` wrong file name dega, link click karne par page not found ho sakta hai.

## Image Tag: `img`

Image show karne ke liye `img` tag use hota hai. Image tag mein `src` and `alt` important attributes hain.

```html
<img src="images/classroom.jpg" alt="Students learning HTML in classroom">
```

`src` image ka path hai. `alt` image ka text description hai. Agar image load nahi hoti, alt text help karta hai. Screen reader users ke liye bhi alt text important hai.

## Button Tag: `button`

Button user action ke liye use hota hai.

```html
<button type="submit">Submit</button>
```

Form ke andar submit button form submit karta hai. Normal button JavaScript actions ke liye use ho sakta hai.

## Div vs Semantic Tags

`div` generic container hai. Jab specific meaning wala tag available ho, semantic tag use karna better hai.

| Generic | Better Semantic Option |
|---|---|
| `<div class="header">` | `<header>` |
| `<div class="nav">` | `<nav>` |
| `<div class="main">` | `<main>` |
| `<div class="footer">` | `<footer>` |

---

# More Small Practicals for Better Understanding

## Practical 8: Create a Navigation Menu

Create file: `nav-practice.html`

```html
<header>
  <h1>My Website</h1>
  <nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="contact.html">Contact</a>
  </nav>
</header>
```

### Explanation

This practical teaches navigation structure. `header` contains website title and navigation links. `nav` groups all links. Each `a` tag connects to another page. In a multi-page website, this same navigation should be used on all pages.

## Practical 9: Create an Accessible Image Section

```html
<section>
  <h2>Our Classroom</h2>
  <img src="images/classroom.jpg" alt="Students sitting in classroom and learning HTML" width="400">
  <p>This is our web development classroom.</p>
</section>
```

### Explanation

This section uses semantic `section`, proper heading, image with descriptive alt text, and paragraph. This is better than placing image alone without context.

## Practical 10: Build a Course List

```html
<section>
  <h2>Available Courses</h2>
  <ul>
    <li>HTML5 Basics</li>
    <li>CSS Styling</li>
    <li>JavaScript Fundamentals</li>
  </ul>
</section>
```

### Explanation

List is used because courses are multiple related items. `ul` creates bullet list and `li` creates each list item. This is better than writing all courses in one paragraph because list is easier to read.

## Practical 11: Create a Basic Fees Table

```html
<table>
  <tr>
    <th>Course</th>
    <th>Duration</th>
    <th>Fees</th>
  </tr>
  <tr>
    <td>HTML5</td>
    <td>1 Week</td>
    <td>Free</td>
  </tr>
</table>
```

### Explanation

Table is useful when data has rows and columns. Here course, duration and fees are related data columns. `th` is used for headings and `td` is used for normal data cells.

## Practical 12: Form With Different Inputs

```html
<form>
  <label for="fullName">Full Name</label>
  <input type="text" id="fullName" name="fullName" required>

  <label for="email">Email</label>
  <input type="email" id="email" name="email" required>

  <label for="joiningDate">Joining Date</label>
  <input type="date" id="joiningDate" name="joiningDate">

  <button type="submit">Register</button>
</form>
```

### Explanation

This practical shows text input, email input, date input and submit button. Labels are connected with inputs using `for` and `id`. This improves accessibility and form usability.

---

# 8. Project 2: Multi-Page Static Website

## Project Objective

Is project mein learners 4-5 page static website create karenge. Website semantic HTML use karegi, forms with validation use karegi, images/lists/tables use karegi, accessibility rules follow karegi, and SEO basics include karegi.

## Suggested Website Pages

```text
index.html      -> Home page
about.html      -> About page
courses.html    -> Courses page
gallery.html    -> Gallery page
contact.html    -> Contact form page
```

## Folder Structure

```text
multi-page-website/
  index.html
  about.html
  courses.html
  gallery.html
  contact.html
  images/
    student.jpg
    classroom.jpg
```

## Common Navigation Code

Har page mein same navigation use karo:

```html
<header>
  <h1>Learning Academy</h1>
  <nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="courses.html">Courses</a>
    <a href="gallery.html">Gallery</a>
    <a href="contact.html">Contact</a>
  </nav>
</header>
```

## Navigation Code Explanation

| Code | Explanation |
|---|---|
| `<header>` | Page ka top section. |
| `<h1>` | Website title. |
| `<nav>` | Navigation links group. |
| `<a href="index.html">` | Home page link. |
| `<a href="contact.html">` | Contact page link. |

## Home Page Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Learning Academy provides beginner-friendly web development courses.">
  <title>Learning Academy - Home</title>
</head>
<body>
  <header>
    <h1>Learning Academy</h1>
    <nav>
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="courses.html">Courses</a>
      <a href="gallery.html">Gallery</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>

  <main>
    <section>
      <h2>Welcome to Learning Academy</h2>
      <p>We teach web development from basic to advanced level.</p>
    </section>

    <section>
      <h2>Why Choose Us?</h2>
      <ul>
        <li>Beginner-friendly teaching</li>
        <li>Practical projects</li>
        <li>Step-by-step learning</li>
      </ul>
    </section>
  </main>

  <footer>
    <p>Copyright 2026 - Learning Academy</p>
  </footer>
</body>
</html>
```

## Home Page Code Explanation

| Code | Explanation |
|---|---|
| `DOCTYPE` | HTML5 document define karta hai. |
| `lang="en"` | Page language English. |
| `meta description` | SEO ke liye page summary. |
| `title` | Browser tab and search title. |
| `header` | Website top area. |
| `nav` | Multi-page links. |
| `main` | Unique page content. |
| `section` | Content groups. |
| `ul/li` | Bullet list. |
| `footer` | Bottom copyright area. |

## Contact Page Form Example

```html
<main>
  <h2>Contact Us</h2>

  <form>
    <label for="name">Full Name</label>
    <input type="text" id="name" name="name" required>

    <label for="email">Email</label>
    <input type="email" id="email" name="email" required>

    <label for="course">Select Course</label>
    <select id="course" name="course" required>
      <option value="">Choose a course</option>
      <option value="html">HTML5</option>
      <option value="mern">MERN Stack</option>
    </select>

    <label for="message">Message</label>
    <textarea id="message" name="message" rows="5" required></textarea>

    <button type="submit">Submit</button>
  </form>
</main>
```

## Contact Form Explanation

| Code | Explanation |
|---|---|
| `<form>` | User input area. |
| `label for` | Label ko input id se connect karta hai. |
| `input type="text"` | Name input. |
| `input type="email"` | Email validation. |
| `<select>` | Dropdown create karta hai. |
| `<option>` | Dropdown option. |
| `<textarea>` | Long message field. |
| `required` | Field blank nahi chhod sakte. |
| `button type="submit"` | Form submit karta hai. |

## Project Checklist

| Requirement | Done |
|---|---|
| 4-5 pages created |  |
| Same navigation on all pages |  |
| Semantic tags used |  |
| Contact form with validation |  |
| Images with alt text |  |
| Table/list used |  |
| Meta description added |  |
| Page titles proper |  |
| Tested in browser |  |

---

# 9. Quick Revision

| Topic | Meaning |
|---|---|
| HTML | Web page structure language |
| HTML5 | Modern HTML version |
| Semantic Tags | Meaningful layout tags |
| Form | User input collection |
| Validation | Input checking |
| Table | Rows and columns data |
| List | Ordered/unordered points |
| Image Alt | Image description |
| Accessibility | Website usable for all users |
| SEO | Search engine friendly structure |
| Cross-browser | Works in different browsers |
| Static Website | Fixed files based website |

---

# 10. Day 2 Practice Tasks

## Task 1

Create one `index.html` page with:

- Proper HTML5 skeleton
- Header
- Navigation
- Main content
- Footer

## Task 2

Create a contact form with:

- Name
- Email
- Message
- Required validation

## Task 3

Create a course table with:

- Course name
- Duration
- Fees

## Task 4

Create a multi-page website with:

- Home
- About
- Courses
- Gallery
- Contact

## Task 5

Check accessibility:

- Labels added
- Image alt text added
- Heading order correct
- Links meaningful

