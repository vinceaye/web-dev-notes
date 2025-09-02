# HTML/CSS Quick Reference Guide 📚

Based on your code files, here's a beginner-friendly guide to the HTML and CSS patterns you're using.

## HTML Basics

### 1. **Basic Structure**
```html
<div class="container-name">
  <!-- Content goes here -->
</div>
```
- `<div>` = Think of this as an invisible box that groups related content together, like putting items in a folder
- `class="name"` = This gives the element a specific name/label so CSS can find it and apply styles to it, like putting a name tag on the box

### 2. **Common HTML Elements You Use**

#### Headers & Text
```html
<h1>Main Title</h1>          <!-- The biggest, most important heading on your page, like a book title -->
<h3>Section Title</h3>       <!-- A medium-sized heading for sections, like chapter titles -->
<p>Regular paragraph text</p> <!-- Normal text content, like paragraphs in a book or article -->
<span>Small text piece</span> <!-- A small piece of inline text that doesn't break to a new line -->
```

#### Links & Buttons
```html
<a href="https://example.com" class="button-style" target="_blank">
  <span>Button Text</span>
</a>
```
- `href` = The web address where this link will take you when clicked, like a street address
- `target="_blank"` = Opens the link in a new browser tab so users don't lose your current page
- `class` = The style name that tells CSS how to make this link look like a button

#### Containers & Layout
```html
<div class="programs-grid">        <!-- The main container that arranges items in a grid pattern, like a photo album layout -->
  <div class="program-card">       <!-- Each individual card/box that holds one program's information -->
    <div class="program-header">   <!-- The top section of each card, usually containing the title and main info -->
      <!-- Content -->
    </div>
  </div>
</div>
```

### 3. **Your Common HTML Patterns**

#### Navigation Tabs
```html
<div class="navigator-tabs">
  <a href="link1.html" class="nav-tab-link">
    <span class="tab-icon">🎯</span>
    <div><strong>Tab Title</strong></div>
  </a>
</div>
```
<!-- This creates clickable tabs at the top of your page, like tabs in a filing cabinet or browser tabs -->

#### Program Cards
```html
<div class="program-card">
  <div class="program-header">
    <div class="program-title">
      <div class="program-icon">📚</div>    <!-- Visual icon to represent the program type -->
      <span>Program Name</span>             <!-- The actual name/title of the program -->
    </div>
  </div>
  <div class="quick-info">
    <!-- Program details like duration, level, instructor, etc. -->
  </div>
</div>
```

---

## CSS Basics

### 1. **CSS Structure**
```css
.class-name {
  property: value;           /* Each line sets one visual aspect of the element */
  another-property: another-value;
}
```
<!-- CSS works like giving instructions: "Find all elements with this class name, then apply these visual changes to them" -->

### 2. **Common CSS Properties You Use**

#### Colors & Backgrounds
```css
.element {
  color: white;                    /* Changes the text color inside this element */
  background: #f8f9fa;            /* Sets a solid background color (light gray in this case) */
  background: linear-gradient(135deg, #406494 0%, #2c3e50 100%);  /* Creates a smooth color transition from blue to dark blue at a 135-degree angle */
}
```

#### Spacing & Size
```css
.element {
  padding: 20px;          /* Adds space inside the element, between the border and content (like padding in a box) */
  margin: 10px;           /* Adds space outside the element, pushing other elements away from it */
  width: 100%;            /* Makes the element take up the full width of its container */
  max-width: 1200px;      /* Prevents the element from getting wider than 1200 pixels, even on very large screens */
  height: 50px;           /* Sets the exact height of the element to 50 pixels */
}
```

#### Layout & Positioning
```css
.container {
  display: flex;          /* Turns this into a flexible container that can arrange its children in rows or columns */
  flex-direction: row;    /* Arranges child elements horizontally in a row (use 'column' for vertical stacking) */
  justify-content: center; /* Centers all child elements horizontally within this container */
  align-items: center;    /* Centers all child elements vertically within this container */
  gap: 20px;             /* Adds 20 pixels of space between each child element, like automatic spacing */
}

.grid-container {
  display: grid;                    /* Creates a grid layout system, like a table with invisible lines */
  grid-template-columns: 1fr 1fr;   /* Creates two columns of equal width (1fr = 1 fraction of available space) */
  gap: 20px;                       /* Adds 20 pixels of space between all grid items, both horizontally and vertically */
}
```

#### Text Styling
```css
.text {
  font-family: 'Segoe UI', sans-serif;  /* Sets the font type, with backup fonts if the first isn't available */
  font-size: 1.2rem;                    /* Makes text 20% larger than the default size (1rem = default size) */
  font-weight: 600;                     /* Makes text semi-bold (normal = 400, bold = 700) */
  text-align: center;                   /* Centers the text horizontally within its container */
  line-height: 1.5;                     /* Sets space between lines to 1.5 times the font size for better readability */
}
```

#### Borders & Shadows
```css
.card {
  border-radius: 16px;                           /* Rounds the corners of the element by 16 pixels, making it look softer */
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);   /* Creates a drop shadow: 0px horizontal, 15px down, 35px blur, black at 10% opacity */
  border: 3px solid transparent;                  /* Creates a 3-pixel invisible border (useful for hover effects) */
}
```

### 3. **Your Common CSS Patterns**

#### Card Styling
```css
.program-card {
  background: white;                      /* Sets a clean white background for each program card */
  border-radius: 16px;                    /* Rounds the corners to make cards look modern and friendly */
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);  /* Adds a subtle shadow to make cards appear to float above the page */
  padding: 25px;                          /* Adds space inside each card so content isn't cramped against the edges */
  transition: all 0.3s ease;              /* Makes any changes to this card happen smoothly over 0.3 seconds */
}

.program-card:hover {
  transform: translateY(-5px);            /* When someone hovers over the card, moves it up 5 pixels for a "lifting" effect */
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.15);  /* Makes the shadow bigger and darker when hovering, enhancing the lift effect */
}
```

#### Button Styling
```css
.nav-tab-link {
  padding: 20px 12px;                     /* Adds space inside the button: 20px top/bottom, 12px left/right */
  background: linear-gradient(135deg, #ffffff 0%, #f1f3f4 100%);  /* Creates a subtle gradient from white to light gray */
  border-radius: 12px;                    /* Rounds the button corners for a modern look */
  transition: all 0.3s ease;              /* Makes hover effects smooth and professional-looking */
  cursor: pointer;                        /* Changes mouse cursor to a hand when hovering, indicating it's clickable */
  text-decoration: none;                  /* Removes the default underline that appears on links */
}

.nav-tab-link:hover {
  transform: translateY(-2px);            /* Slightly lifts the button when hovered, giving tactile feedback */
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);  /* Changes to a slightly darker gradient on hover */
}
```

#### Responsive Design (Mobile-friendly)
```css
@media (max-width: 768px) {              /* These styles only apply when screen width is 768 pixels or smaller (tablets/phones) */
  .programs-grid {
    grid-template-columns: 1fr;          /* Changes from multiple columns to just one column on small screens */
  }
  
  .program-title {
    font-size: 1.1rem;                   /* Makes text slightly smaller on mobile devices for better fit */
  }
}
```

---

## Your Specific Patterns

### 1. **Web Part Structure**
```html
<div class="jwf-programs-webpart">       <!-- Main container that wraps your entire component -->
  <style>
    /* CSS styles go here - keeping styles with the HTML makes it self-contained */
  </style>
  
  <!-- HTML content goes here - all your actual page content -->
</div>
```

### 2. **Header with Gradient**
```css
.programs-header {
  background: linear-gradient(135deg, #406494 0%, #2c3e50 100%);  /* Creates a diagonal blue gradient that looks professional */
  color: white;                           /* Makes text white so it shows up clearly on the dark background */
  padding: 25px 30px;                     /* Adds breathing room around the header text */
  text-align: center;                     /* Centers the header text for a balanced, formal look */
}
```

### 3. **Grid Layout for Cards**
```css
.programs-grid {
  display: grid;                          /* Creates a grid system for organizing program cards */
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));  /* Creates columns that are at least 350px wide, automatically fitting as many as possible */
  gap: 25px;                             /* Adds consistent spacing between all cards */
  padding: 30px;                         /* Adds space around the entire grid so cards don't touch the container edges */
}
```

### 4. **Hover Effects**
```css
.element {
  transition: all 0.3s ease;              /* Tells the browser to smoothly animate any changes over 0.3 seconds with easing */
}

.element:hover {
  transform: translateY(-2px);            /* Moves the element up by 2 pixels when user hovers over it */
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);  /* Increases the shadow to make the "floating" effect more pronounced */
}
```

---

## CSS Conditionals & Logic

### 1. **Media Queries (Responsive Design)**
```css
@media (max-width: 768px) {
  /* These styles only apply when the screen width is 768 pixels or smaller */
  .programs-grid {
    grid-template-columns: 1fr;
  }
}

@media (min-width: 1200px) {
  /* These styles only apply when the screen width is 1200 pixels or larger */
  .container {
    max-width: 1400px;
  }
}
```
- Media queries are like "if statements" for CSS - they check conditions about the device/screen
- Common breakpoints: 480px (phones), 768px (tablets), 1024px (small laptops), 1200px (desktops)

### 2. **Pseudo-Classes (State-Based Conditionals)**
```css
.button {
  background: blue;
}

.button:hover {
  /* Only applies when user hovers over the button */
  background: darkblue;
}

.button:focus {
  /* Only applies when the button has keyboard focus */
  outline: 2px solid orange;
}

.button:active {
  /* Only applies while the button is being clicked */
  transform: scale(0.98);
}

.button:disabled {
  /* Only applies when the button is disabled */
  background: gray;
  cursor: not-allowed;
}
```

### 3. **Structural Pseudo-Classes**
```css
.program-card:first-child {
  /* Only targets the first program card */
  margin-top: 0;
}

.program-card:last-child {
  /* Only targets the last program card */
  margin-bottom: 0;
}

.program-card:nth-child(odd) {
  /* Targets every odd-numbered card (1st, 3rd, 5th, etc.) */
  background: #f8f9fa;
}

.program-card:nth-child(even) {
  /* Targets every even-numbered card (2nd, 4th, 6th, etc.) */
  background: white;
}
```

### 4. **Feature Detection (@supports)**
```css
@supports (display: grid) {
  /* Only applies if the browser supports CSS Grid */
  .programs-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  }
}

@supports not (display: grid) {
  /* Only applies if the browser does NOT support CSS Grid */
  .programs-grid {
    display: flex;
    flex-wrap: wrap;
  }
}
```

### 5. **Combining Conditionals**
```css
/* Multiple conditions: applies only on large screens when hovering */
@media (min-width: 1024px) {
  .program-card:hover {
    transform: translateY(-8px);
  }
}

/* Chain multiple pseudo-classes */
.nav-tab-link:hover:not(:disabled) {
  /* Only applies when hovering AND the link is not disabled */
  background: lightblue;
}

/* Target specific children in specific contexts */
.programs-grid .program-card:first-child {
  /* Only targets the first program card inside a programs-grid */
  border: 2px solid gold;
}
```

### 6. **Dark Mode Support**
```css
@media (prefers-color-scheme: dark) {
  /* Automatically applies when user has dark mode enabled in their system */
  .program-card {
    background: #2d3748;
    color: white;
  }
  
  .programs-header {
    background: linear-gradient(135deg, #1a202c 0%, #2d3748 100%);
  }
}

@media (prefers-color-scheme: light) {
  /* Applies when user prefers light mode */
  .program-card {
    background: white;
    color: black;
  }
}
```

### 7. **Common Conditional Patterns You Might Use**

#### Show/Hide Elements
```css
.mobile-only {
  display: none;
}

@media (max-width: 768px) {
  .mobile-only {
    display: block;
  }
  
  .desktop-only {
    display: none;
  }
}
```

#### Progressive Enhancement
```css
/* Basic styles that work everywhere */
.program-card {
  background: white;
  padding: 20px;
  margin: 10px;
}

/* Enhanced styles for modern browsers */
@supports (backdrop-filter: blur(10px)) {
  .program-card {
    background: rgba(255, 255, 255, 0.8);
    backdrop-filter: blur(10px);
  }
}
```

#### Print Styles
```css
@media print {
  /* Special styles for when the page is printed */
  .navigation, .buttons {
    display: none; /* Hide interactive elements */
  }
  
  .program-card {
    page-break-inside: avoid; /* Keep each card on one page */
    box-shadow: none; /* Remove shadows for cleaner printing */
  }
}
```

---

## HTML Conditionals (If/Else Logic)

### 1. **Basic If/Else Structure**
```html
<!-- Simple conditional display -->
<div id="welcome-message">
  <script>
    if (userIsLoggedIn) {
      document.getElementById('welcome-message').innerHTML = '<h2>Welcome back, User!</h2>';
    } else {
      document.getElementById('welcome-message').innerHTML = '<h2>Please log in</h2>';
    }
  </script>
</div>
```

### 2. **Template Conditionals (Common in Frameworks)**
```html
<!-- Angular-style conditionals -->
<div *ngIf="userIsLoggedIn">
  <h2>Welcome back, {{userName}}!</h2>
  <button>Logout</button>
</div>
<div *ngIf="!userIsLoggedIn">
  <h2>Please log in</h2>
  <button>Login</button>
</div>

<!-- React-style conditionals -->
{isLoggedIn ? (
  <div>
    <h2>Welcome back, {userName}!</h2>
    <button>Logout</button>
  </div>
) : (
  <div>
    <h2>Please log in</h2>
    <button>Login</button>
  </div>
)}
```

### 3. **JavaScript Conditionals in HTML**
```html
<div class="program-card">
  <script>
    const programLevel = 'beginner';
    const cardElement = document.querySelector('.program-card');
    
    if (programLevel === 'beginner') {
      cardElement.innerHTML += '<span class="badge beginner">Beginner</span>';
    } else if (programLevel === 'intermediate') {
      cardElement.innerHTML += '<span class="badge intermediate">Intermediate</span>';
    } else {
      cardElement.innerHTML += '<span class="badge advanced">Advanced</span>';
    }
  </script>
</div>
```

### 4. **Conditional Classes**
```html
<div class="program-card" id="card-1">
  <script>
    const card = document.getElementById('card-1');
    const isFeatured = true;
    const isPopular = false;
    
    if (isFeatured) {
      card.classList.add('featured');
    }
    
    if (isPopular) {
      card.classList.add('popular');
    } else {
      card.classList.add('standard');
    }
  </script>
</div>
```

### 5. **Conditional Content Based on Data**
```html
<div class="programs-grid">
  <script>
    const programs = [
      { name: 'Web Development', level: 'beginner', instructor: 'John Doe' },
      { name: 'Advanced CSS', level: 'intermediate', instructor: 'Jane Smith' },
      { name: 'JavaScript Mastery', level: 'advanced', instructor: 'Bob Wilson' }
    ];
    
    const gridContainer = document.querySelector('.programs-grid');
    
    programs.forEach(program => {
      let cardHTML = `
        <div class="program-card ${program.level}">
          <div class="program-header">
            <div class="program-title">
              <div class="program-icon">📚</div>
              <span>${program.name}</span>
            </div>
          </div>
          <div class="quick-info">
            <p><strong>Level:</strong> ${program.level}</p>
            <p><strong>Instructor:</strong> ${program.instructor}</p>
      `;
      
      // Conditional content based on level
      if (program.level === 'beginner') {
        cardHTML += '<p class="duration">Duration: 4 weeks</p>';
      } else if (program.level === 'intermediate') {
        cardHTML += '<p class="duration">Duration: 6 weeks</p>';
      } else {
        cardHTML += '<p class="duration">Duration: 8 weeks</p>';
      }
      
      cardHTML += '</div></div>';
      gridContainer.innerHTML += cardHTML;
    });
  </script>
</div>
```

### 6. **Conditional Navigation**
```html
<nav class="navigator-tabs">
  <script>
    const currentPage = 'programs';
    const navContainer = document.querySelector('.navigator-tabs');
    
    const navItems = [
      { id: 'home', title: 'Home', icon: '🏠', active: currentPage === 'home' },
      { id: 'programs', title: 'Programs', icon: '📚', active: currentPage === 'programs' },
      { id: 'about', title: 'About', icon: 'ℹ️', active: currentPage === 'about' }
    ];
    
    navItems.forEach(item => {
      const navHTML = `
        <a href="${item.id}.html" class="nav-tab-link ${item.active ? 'active' : ''}">
          <span class="tab-icon">${item.icon}</span>
          <div><strong>${item.title}</strong></div>
        </a>
      `;
      navContainer.innerHTML += navHTML;
    });
  </script>
</nav>
```

### 7. **Conditional Forms**
```html
<form class="registration-form">
  <div class="form-group">
    <label for="user-type">User Type:</label>
    <select id="user-type" onchange="updateForm()">
      <option value="student">Student</option>
      <option value="teacher">Teacher</option>
      <option value="admin">Administrator</option>
    </select>
  </div>
  
  <div id="conditional-fields">
    <!-- This content will change based on user type selection -->
  </div>
  
  <script>
    function updateForm() {
      const userType = document.getElementById('user-type').value;
      const fieldsContainer = document.getElementById('conditional-fields');
      
      if (userType === 'student') {
        fieldsContainer.innerHTML = `
          <div class="form-group">
            <label for="grade">Grade Level:</label>
            <input type="number" id="grade" min="1" max="12">
          </div>
          <div class="form-group">
            <label for="parent-email">Parent Email:</label>
            <input type="email" id="parent-email">
          </div>
        `;
      } else if (userType === 'teacher') {
        fieldsContainer.innerHTML = `
          <div class="form-group">
            <label for="subject">Subject Area:</label>
            <input type="text" id="subject">
          </div>
          <div class="form-group">
            <label for="experience">Years of Experience:</label>
            <input type="number" id="experience" min="0">
          </div>
        `;
      } else {
        fieldsContainer.innerHTML = `
          <div class="form-group">
            <label for="department">Department:</label>
            <input type="text" id="department">
          </div>
        `;
      }
    }
    
    // Initialize form on page load
    updateForm();
  </script>
</form>
```

### 8. **Conditional Error Messages**
```html
<div class="error-container">
  <script>
    const hasErrors = false;
    const errorMessage = 'Please fix the following errors:';
    const errors = ['Email is required', 'Password must be at least 8 characters'];
    
    if (hasErrors) {
      document.querySelector('.error-container').innerHTML = `
        <div class="error-message">
          <h3>${errorMessage}</h3>
          <ul>
            ${errors.map(error => `<li>${error}</li>`).join('')}
          </ul>
        </div>
      `;
    } else {
      document.querySelector('.error-container').innerHTML = '';
    }
  </script>
</div>
```

### 9. **Conditional Loading States**
```html
<div class="content-container">
  <div id="loading-state" class="loading">
    <p>Loading programs...</p>
  </div>
  
  <div id="content-state" class="content" style="display: none;">
    <!-- Actual content goes here -->
  </div>
  
  <script>
    const isLoading = true;
    const loadingElement = document.getElementById('loading-state');
    const contentElement = document.getElementById('content-state');
    
    if (isLoading) {
      loadingElement.style.display = 'block';
      contentElement.style.display = 'none';
    } else {
      loadingElement.style.display = 'none';
      contentElement.style.display = 'block';
    }
  </script>
</div>
```

### 10. **Common Conditional Patterns**

#### Show/Hide Elements
```html
<div class="conditional-element">
  <script>
    const shouldShow = true;
    const element = document.querySelector('.conditional-element');
    
    if (shouldShow) {
      element.style.display = 'block';
    } else {
      element.style.display = 'none';
    }
  </script>
</div>
```

#### Conditional Styling
```html
<div class="status-indicator">
  <script>
    const status = 'success';
    const indicator = document.querySelector('.status-indicator');
    
    if (status === 'success') {
      indicator.className = 'status-indicator success';
    } else if (status === 'warning') {
      indicator.className = 'status-indicator warning';
    } else if (status === 'error') {
      indicator.className = 'status-indicator error';
    }
  </script>
</div>
```

### 11. **Pure HTML "Not Equal" Conditionals**

#### Using CSS :not() Selector for "Not Equal" Conditions
```html
<!-- Show content when data attribute is NOT equal to a specific value -->
<div class="program-card" data-status="active">
  <h3>Active Program</h3>
  <p>This program is currently running</p>
</div>

<div class="program-card" data-status="pending">
  <h3>Pending Program</h3>
  <p>This program is waiting to start</p>
</div>

<div class="program-card" data-status="completed">
  <h3>Completed Program</h3>
  <p>This program has finished</p>
</div>

<style>
  /* Hide all program cards by default */
  .program-card {
    display: none;
  }
  
  /* Show only cards that are NOT "completed" */
  .program-card:not([data-status="completed"]) {
    display: block;
  }
  
  /* Alternative: Show only cards that are NOT "pending" */
  .program-card:not([data-status="pending"]) {
    display: block;
  }
  
  /* Show only cards that are NOT "active" */
  .program-card:not([data-status="active"]) {
    display: block;
  }
</style>
```

#### Using "Not Equal" with Form Values
```html
<!-- Show different content based on what a form field is NOT equal to -->
<form class="filter-form">
  <label for="program-type">Filter by Program Type:</label>
  <select id="program-type">
    <option value="all">All Programs</option>
    <option value="web">Web Development</option>
    <option value="mobile">Mobile Development</option>
    <option value="data">Data Science</option>
  </select>
</form>

<div class="program-list">
  <!-- Web Development Programs -->
  <div class="program-item" data-type="web">
    <h4>Web Development Bootcamp</h4>
    <p>Learn HTML, CSS, and JavaScript</p>
  </div>
  
  <!-- Mobile Development Programs -->
  <div class="program-item" data-type="mobile">
    <h4>Mobile App Development</h4>
    <p>Learn React Native and iOS development</p>
  </div>
  
  <!-- Data Science Programs -->
  <div class="program-item" data-type="data">
    <h4>Data Science Fundamentals</h4>
    <p>Learn Python and machine learning</p>
  </div>
</div>

<style>
  /* Hide all programs by default */
  .program-item {
    display: none;
  }
  
  /* Show all programs when "all" is selected */
  #program-type[value="all"]:checked ~ .program-list .program-item,
  #program-type:not([value="all"]):not([value="web"]) ~ .program-list .program-item[data-type="web"] {
    display: block;
  }
  
  /* Show only programs that are NOT web development */
  #program-type[value="mobile"]:checked ~ .program-list .program-item:not([data-type="web"]) {
    display: block;
  }
  
  /* Show only programs that are NOT mobile development */
  #program-type[value="web"]:checked ~ .program-list .program-item:not([data-type="mobile"]) {
    display: block;
  }
  
  /* Show only programs that are NOT data science */
  #program-type[value="web"]:checked ~ .program-list .program-item:not([data-type="data"]) {
    display: block;
  }
</style>
```

#### Using "Not Equal" with Checkbox States
```html
<!-- Show content when checkbox is NOT checked -->
<input type="checkbox" id="hide-completed" class="filter-checkbox">
<label for="hide-completed">Hide Completed Programs</label>

<div class="programs-container">
  <!-- Active Program -->
  <div class="program-card" data-status="active">
    <h3>Active Program</h3>
    <p>Currently running</p>
  </div>
  
  <!-- Completed Program -->
  <div class="program-card" data-status="completed">
    <h3>Completed Program</h3>
    <p>Finished successfully</p>
  </div>
  
  <!-- Pending Program -->
  <div class="program-card" data-status="pending">
    <h3>Pending Program</h3>
    <p>Starting soon</p>
  </div>
</div>

<style>
  /* Show all programs by default */
  .program-card {
    display: block;
  }
  
  /* When checkbox is checked, hide completed programs */
  .filter-checkbox:checked ~ .programs-container .program-card[data-status="completed"] {
    display: none;
  }
  
  /* Alternative: Show only programs that are NOT completed when checkbox is checked */
  .filter-checkbox:checked ~ .programs-container .program-card:not([data-status="completed"]) {
    display: block;
  }
  
  /* When checkbox is NOT checked, show all programs */
  .filter-checkbox:not(:checked) ~ .programs-container .program-card {
    display: block;
  }
</style>
```

#### Using "Not Equal" with Multiple Conditions
```html
<!-- Show content when multiple conditions are NOT met -->
<div class="program-card" data-level="beginner" data-category="web" data-status="active">
  <h3>Beginner Web Development</h3>
  <p>Active beginner web course</p>
</div>

<div class="program-card" data-level="advanced" data-category="mobile" data-status="pending">
  <h3>Advanced Mobile Development</h3>
  <p>Pending advanced mobile course</p>
</div>

<div class="program-card" data-level="intermediate" data-category="data" data-status="completed">
  <h3>Intermediate Data Science</h3>
  <p>Completed intermediate data course</p>
</div>

<style>
  /* Show all programs by default */
  .program-card {
    display: block;
  }
  
  /* Show only programs that are NOT beginner level */
  .program-card:not([data-level="beginner"]) {
    display: block;
  }
  
  /* Show only programs that are NOT web category */
  .program-card:not([data-category="web"]) {
    display: block;
  }
  
  /* Show only programs that are NOT completed */
  .program-card:not([data-status="completed"]) {
    display: block;
  }
  
  /* Show only programs that are NOT beginner AND NOT web */
  .program-card:not([data-level="beginner"]):not([data-category="web"]) {
    display: block;
  }
  
  /* Show only programs that are NOT beginner AND NOT completed */
  .program-card:not([data-level="beginner"]):not([data-status="completed"]) {
    display: block;
  }
</style>
```

#### Using "Not Equal" with Text Content
```html
<!-- Show content based on what text is NOT present -->
<div class="content-filter">
  <input type="text" id="search-term" placeholder="Search programs...">
</div>

<div class="programs-list">
  <div class="program-item" data-title="Web Development">
    <h4>Web Development</h4>
    <p>Learn HTML, CSS, JavaScript</p>
  </div>
  
  <div class="program-item" data-title="Mobile Development">
    <h4>Mobile Development</h4>
    <p>Learn React Native</p>
  </div>
  
  <div class="program-item" data-title="Data Science">
    <h4>Data Science</h4>
    <p>Learn Python and ML</p>
  </div>
</div>

<style>
  /* Show all programs by default */
  .program-item {
    display: block;
  }
  
  /* Hide programs that contain the search term (requires JavaScript for full functionality) */
  /* This is a simplified version - full text search would need JavaScript */
  
  /* Alternative: Show only programs that do NOT have a specific class */
  .program-item:not(.featured) {
    display: block;
  }
  
  .program-item.featured {
    display: none;
  }
</style>
```

---

## Quick Tips 💡

### CSS Selectors
- `.class-name` = Targets all elements that have this specific class attribute
- `#id-name` = Targets the single element that has this unique ID (only one per page)
- `element.class` = Targets only specific HTML elements (like div or p) that also have this class
- `.parent .child` = Targets child elements that are inside a parent element with the parent class

### Common Units
- `px` = Exact pixels on the screen (16px = 16 tiny dots on your monitor)
- `rem` = Relative to the root font size (1.2rem = 20% larger than normal text)
- `%` = Percentage of the parent container (100% = takes up all available space)
- `fr` = Fraction of available space in grid layouts (1fr = 1 part, 2fr = 2 parts)

### Colors
- Named: `white`, `red`, `blue` = Use common color names (limited selection)
- Hex: `#ffffff` (white), `#000000` (black) = Six-digit codes where each pair represents red, green, blue
- RGB: `rgb(255, 255, 255)` (white) = Specify red, green, blue values from 0-255
- RGBA: `rgba(0, 0, 0, 0.5)` (black with 50% transparency) = Same as RGB but with alpha (transparency) from 0-1

This should help you understand and modify your HTML/CSS code! 🚀