
---

# 🌍 Mapty – Your Personal Workout Tracker

**Mapty** is a **web-based running and cycling tracker** that lets users log workouts on an interactive map. Designed with **modern JavaScript, Leaflet.js, and LocalStorage**, Mapty allows you to visualize workouts, track stats, and navigate your fitness journey effortlessly.

---

## 🚀 Features

* **Interactive Map:** Click anywhere to log a workout at your exact location.
* **Running & Cycling Workouts:** Track distance, duration, cadence (running), or elevation gain (cycling).
* **Automatic Calculations:**

  * Running: Pace (min/km)
  * Cycling: Speed (km/h)
* **Workout Description:** Generates descriptive titles with type and date.
* **Map Markers:** Workouts appear as markers with popup summaries.
* **Workout List:** Displays all workouts with detailed stats in a user-friendly list.
* **Navigation:** Click a workout in the list to pan and zoom to its map location.
* **Persistent Storage:** Workouts are saved in **LocalStorage** to retain data across sessions.
* **Dynamic Form Fields:** Cadence or elevation input changes automatically based on workout type.
* **Reset Option:** Clear all workouts and start fresh.

---

## 🛠️ Technologies Used

* **JavaScript (ES6+)** – Core app logic, object-oriented programming.
* **HTML5 & CSS3** – Responsive layout and styling.
* **Leaflet.js** – Interactive map rendering and markers.
* **LocalStorage API** – Store workouts in the browser.
* **Geolocation API** – Automatically detect user location.

---

## 📦 Installation & Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/mapty.git
   ```
2. Open `index.html` in your browser.
3. Allow location access when prompted.
4. Click on the map to log a workout.
5. Fill in workout details and submit.
6. View workouts on the map and in the list below.

---

## 🏗 Project Structure

```
mapty/
│
├─ index.html        # Main HTML file
├─ style.css         # Styles for map, form, and list
├─ script.js         # JavaScript logic for Mapty
├─ README.md         # Project documentation
└─ assets/
   └─ images/        # Screenshots or icons
```

---

## 🧩 Classes & Architecture

Mapty uses **object-oriented programming (OOP)**:

1. **Workout (Base Class)**

   * Properties: `date`, `id`, `coords`, `distance`, `duration`
   * Methods: `setDescription()` – auto-generates a descriptive title

2. **Running (Subclass)**

   * Additional properties: `cadence`, `pace`
   * Methods: `calcPace()`

3. **Cycling (Subclass)**

   * Additional properties: `elevationGain`, `speed`
   * Methods: `calcSpeed()`

4. **App (Controller)**

   * Manages map, form, workout data, and LocalStorage
   * Core methods include:

     * `_getPosition()` – Detect user location
     * `_loadMap()` – Initialize map
     * `_showForm()` / `_hideForm()` – Form handling
     * `_toggleElevationField()` – Switch between cadence/elevation inputs
     * `_newWorkout()` – Validate, create, and save workouts
     * `_renderWorkoutMarker()` – Map markers
     * `_renderWorkout()` – Workout list rendering
     * `_moveToPopup()` – Pan/zoom map on workout click
     * `_setLocalStorage()` / `_getLocalStorage()` – Persist workouts

---

## ⚡ How Mapty Works

1. **Get Location:** Map centers on the user's current geolocation.
2. **Add Workout:** Click map → Fill in details → Submit.
3. **Validation:** Ensures positive numbers for distance, duration, cadence/elevation.
4. **Rendering:** Workouts are shown as markers on the map and as cards in the workout list.
5. **Navigation:** Click a workout card to focus the map on that workout.
6. **Persistence:** Workouts are stored in LocalStorage for future sessions.

---

## 📈 Future Improvements

* Mobile-first responsive design with touch-friendly interactions.
* Charts and stats for weekly/monthly distance, duration, and pace/speed trends.
* Filter workouts by type or date range.
* Cloud storage for multi-device synchronization.
* Push notifications to remind users to log workouts.

---

## 🎯 Why Mapty

Mapty is perfect for anyone who wants a **simple yet powerful personal fitness tracker** without installing heavy apps. Its interactive map, real-time calculations, and persistent storage make it an ideal web app for runners and cyclists.

---

## 🖼 Screenshots

![Mapty Screenshot](https://mdasif-ai.github.io/Mapty-GeoLocation/)

---

## 🔗 Live Demo

Try Mapty live: [https://mdasif-ai.github.io/Mapty-GeoLocation/]


