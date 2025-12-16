# Huyen Quang Content Management Guide

This guide explains how to add and update content on the Huyen Quang website by adding JSON files to this repository.

## 📁 Directory Structure

- **`upcoming_events/`**: For future events shown on the "Upcoming Events" page and Home page.
- **`past_events/`**: For completed events shown on the "Past Events" page.
- **`the_art_of_mindful_living/`**: For mindfulness articles and teachings.
- **`dharma-learning/`**: For Dharma activities and compassionate projects.
- **`announcements/`**: For general announcements (if applicable).

---

## 📝 How to Add Content

1.  **Choose the correct folder** based on the type of content.
2.  **Create a new JSON file**. naming it consistently (e.g., `event-002.json` or `charity-drive-2025.json`).
3.  **Copy a template below** and fill in your details.
4.  **Upload images/PDFs** (optional) to the repo or use external URLs.
5.  **Commit the file**. The website will automatically fetch this new data securely.

---

## 📄 Templates

### 1. Upcoming / Past Events
**File Location**: `upcoming_events/` or `past_events/`

```json
{
  "id": "unique-id-here", 
  "title": "Event Title Here",
  "subtitle": "Subtitle or Vietnamese Title",
  "image": "https://example.com/image.jpg", 
  "date": "December 25, 2025",
  "location": "Main Temple Hall",
  "description": "Full description of the event. You can use \\n for new lines.",
  "pdfUrl": "https://link-to-flyer.pdf", 
  "registration": {
    "deadline": "December 20, 2025",
    "contact": "info@huyenquang.org",
    "fee": "Free"
  },
  "schedule": [
    { "time": "09:00 AM", "activity": "Opening Ceremony" },
    { "time": "10:30 AM", "activity": "Dharma Talk" }
  ],
  "published": true,
  "order": 1
}
```

*   `id`: Must be unique (e.g., `vesak-2025`).
*   `image`: URL to an image. Can be hosted here or external (Unsplash, etc.).
*   `order`: Controls display order (lower numbers appear first).
*   `published`: Set to `false` to hide from the website.

### 2. Dharma Learning / Activities
**File Location**: `dharma-learning/`

```json
{
  "id": "project-001",
  "title": "Clean Water Project",
  "subtitle": "Supporting Highlands Communities",
  "category": "Charity", 
  "image": "https://example.com/project.jpg",
  "date": "November 2024",
  "location": "Ha Giang, Vietnam",
  "description": "Description of the project...",
  "published": true,
  "order": 1
}
```

*   `category`: Optional tag like "Charity", "Education", "Healthcare", "Meditation".

### 3. Art of Mindful Living
**File Location**: `the_art_of_mindful_living/`

```json
{
  "id": "mindfulness-001",
  "title": "Walking Meditation",
  "subtitle": "Thiền Hành",
  "image": "https://example.com/meditation.jpg",
  "description": "A guide to walking with awareness...",
  "pdfUrl": "https://link-to-guide.pdf",
  "published": true
}
```

---

## 🖼️ Hosting Images & PDFs
You can upload images or PDFs directly to this repository (e.g., create an `images/` folder).
Then use the "Raw" GitHub link in your JSON:
`https://raw.githubusercontent.com/ddag-ai/huyenquang-public/main/images/my-photo.jpg`
