# 📚 Current Affairs Q&A Web App

A **responsive, interactive web application** to browse and practice **Current Affairs questions** by **Month** and **Category**.  
Built using **HTML, CSS, and Vanilla JavaScript**, this project is perfect for students, teachers, and quiz enthusiasts.

---

## 🚀 Features

- **Browse by Month** – Explore current affairs for a specific month.  
- **Browse by Category** – Sports, Awards, Books, Science & Tech, National & International Affairs, etc.  
- **Search Functionality** – Quickly filter questions using the search bar.  
- **Interactive UI** – Clean design with cards, modals, and smooth animations.  
- **Responsive Design** – Works on both desktop and mobile.  
- **Expandable Dataset** – Easy to add new questions via `script.js` or external JSON file.  

---

## 🛠️ Tech Stack

- **Frontend:** HTML5, CSS3, JavaScript (no frameworks)  
- **Styling:** Custom responsive CSS (grid, modals, cards)  
- **Data Handling:** JSON-like structure stored in `script.js`  
- **Hosting:** Can run locally or be deployed on GitHub Pages / Netlify  

---

## 📂 Project Structure

├── index.html # Home page
├── month.html # Browse by month
├── category.html # Browse by category
├── styles.css # Global styles (responsive, cards, modals)
├── script.js # Questions dataset + logic
├── questions.json # (Optional) external dataset file for contributors

yaml
 

---

## 💡 Usage Guide

1. Clone or download this repository:  
   ```bash
   git clone https://github.com/your-username/current-affairs-qa.git
   cd current-affairs-qa
Open index.html in your browser.

Navigate via top menu:

Home – overview of the app

By Month – search & browse questions by month

By Category – explore questions grouped into topics

Click a card → Opens a modal with Q&A list.

✍️ Contributor Guide – Adding New Questions
All questions live in script.js under the allQuestions object.
You can also use an external questions.json file for bulk updates.

🔹 Option 1: Edit script.js Directly
Example structure:

js
 
const allQuestions = {
  'December 2024': {
    "SPORTS 🏅": [
      {
        "q": "Who won the 2024 Syed Modi International Badminton Championship?",
        "a": "Lakshya Sen"
      },
      {
        "q": "Which country will host the FIFA World Cup 2034?",
        "a": "Saudi Arabia"
      }
    ],
    "AWARDS & HONOURS 🏆": [
      {
        "q": "Who has been honored as Indian Film Personality of the Year 2024?",
        "a": "Vikrant Massey"
      }
    ]
  }
};
To add a new question:

js
 
{
  "q": "Who became the youngest chess world champion?",
  "a": "D. Gukesh"
}


To add a new month:

js
 
'February 2025': {
  "SCIENCE & TECHNOLOGY 🔬": [
    {
      "q": "Which country launched the world’s first carbon-14 diamond battery?",
      "a": "United Kingdom"
    }
  ]
}
🔹 Option 2: Use questions.json
If you want contributors to edit questions without touching JavaScript, create a questions.json file like this:

json
 
{
  "January 2025": {
    "SPORTS 🏅": [
      {
        "q": "Which team won the Santosh Trophy 2025?",
        "a": "West Bengal"
      }
    ],
    "AWARDS & HONOURS 🏆": [
      {
        "q": "Who won the Golden Globe for Best Motion Picture 2025?",
        "a": "The Brutalist"
      }
    ]
  }
}
Then, in script.js, load it like:

js
 
fetch("questions.json")
  .then(response => response.json())
  .then(data => {
    allQuestions = data;
    // Continue with rendering logic
  });
🔹 Guidelines for Contributors
Always use "q" for question and "a" for answer.

Keep formatting consistent (use emojis for categories 🏅🏆📚🔬).

Avoid duplicate questions.

Prefer concise Q&A format.

📸 Screenshots
Home Page – Navigation cards

By Month – Searchable monthly list

By Category – Topic-based cards with modal Q&A

(Add screenshots here when hosted)

📌 Future Enhancements
✅ Import/export full datasets (CSV/JSON).

✅ Add quiz mode with scoring.

✅ User login & progress tracking.

✅ Dark mode theme.

✅ Admin panel for managing questions.

📄 License
This project is licensed under the MIT License.
You are free to use, modify, and distribute with attribution.
