# 🌿 RoutineCare

**Care coordination platform for families, caregivers, and the people they love.**

RoutineCare centralizes appointments, medications, and daily routines in one place — built for anyone managing care for someone who needs it, including from thousands of miles away.

---

## 💡 The Idea

This project came from a real place.

I work at a group home in Saskatoon supporting people with physical and intellectual disabilities. A few years ago, I also lost my mother to cancer while living in Canada — she was in Brazil. Managing her care from a distance was chaotic in a way that felt completely unnecessary. Tracking appointments, medications, who was doing what and when — it was scattered across messages, notes, and memory.

I brought this idea to my Le Wagon capstone team. They connected with the purpose immediately. We built it from scratch in two weeks.

---

## 🚀 Features

- **Care recipient profiles** — centralized information for each person being cared for
- **Appointment scheduling** — track upcoming and past appointments across multiple caregivers
- **Medication management** — log medications, dosages, and routines
- **Caregiver coordination** — multiple caregivers can manage the same care recipient
- **AI-assisted suggestions** — intelligent prompts to anticipate care needs based on routines
- **Authentication & roles** — secure login with role-based access (caregiver vs. family member)
- **Responsive UI** — designed to work on mobile and desktop

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Backend | Ruby on Rails (MVC) |
| Database | PostgreSQL |
| Authentication | Devise |
| Frontend | HTML, SCSS, JavaScript, Stimulus |
| File Storage | Active Storage |
| Deployment | Heroku / Docker |
| Version Control | Git + GitHub |

---

## 🗄 Database Design

The schema was one of the most interesting challenges. Key relationships:

- A **CareRecipient** can have many **Caregivers** (through a join table)
- An **Appointment** belongs to a CareRecipient and can involve multiple caregivers
- **Medications** are linked to CareRecipients with schedule and dosage tracking
- Cascading deletes and overlapping schedule edge cases required careful modeling

---

## ⚙️ Getting Started

```bash
# Clone the repository
git clone https://github.com/wendybezerra/routine-care.git
cd routine-care

# Install dependencies
bundle install

# Setup database
rails db:create db:migrate db:seed

# Start the server
rails server
```

Visit `http://localhost:3000`

---

## 🐳 Docker

```bash
docker build -t routine-care .
docker run -p 3000:3000 routine-care
```

---

## 👥 Team

Built in 2 weeks as a Le Wagon capstone project by a team of four.

**My contributions:**
- Concept ideation and product definition
- UI/UX design and user flow mapping
- Backend logic and Rails MVC architecture
- Database schema design and relational modeling
- RESTful API implementation
- Authentication system (Devise)
- AI-assisted feature integration

---

## 🌱 What I Learned

Building under a real deadline with a real purpose taught me more than any tutorial. The hardest part wasn't the code — it was making pragmatic architectural decisions under pressure, iterating on data models that kept growing in complexity, and shipping something that actually worked for real people.

---

## 📬 Contact

**Wendy Bezerra**
[wendybezerra.dev@gmail.com](mailto:wendybezerra.dev@gmail.com)
[linkedin.com/in/wendymbezerra](https://www.linkedin.com/in/wendymbezerra/)
[wendybezerra.github.io/portfolio](https://wendybezerra.github.io/portfolio/)

Rails app generated with [lewagon/rails-templates](https://github.com/lewagon/rails-templates), created by the [Le Wagon coding bootcamp](https://www.lewagon.com) team.
