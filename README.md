# 💡 Light Box Movie Poster Gallery

https://govindjindal.github.io/Light_Box_Animation-IWT-2/#

A responsive movie poster gallery featuring a pure CSS **Lightbox** effect for viewing posters in full size.

This project uses modern HTML5 and CSS3 features, including **CSS Grid** (via `flex-wrap: wrap` and `gap`) for the layout and the **`:target`** pseudo-class for the lightbox functionality without relying on JavaScript.

---

## ✨ Features

* **Responsive Grid Layout:** Posters are displayed in a flexible grid that adapts to different screen sizes.
* **Hover Animation:** Subtle **`transform: scale(1.1)`** transition on poster hover for enhanced user interaction.
* **Pure CSS Lightbox:** Clicking a poster opens a full-screen, semi-transparent overlay to display the image.
* **Smooth Transition:** The lightbox uses a **`transition: 0.5s ease;`** for a smooth reveal and close effect.
* **Dark Aesthetic Background:** A background gradient is used to provide an immersive, cinematic feel.

---

## 🛠️ Technologies Used

* **HTML5:** Structure and content.
* **CSS3:** Styling, animations, and the lightbox mechanism.

---

## 🖼️ How the Lightbox Works (Pure CSS)

The core mechanism for the lightbox is achieved without any JavaScript, utilizing the anchor (`<a>`) tag and the CSS **`:target`** selector:

1.  **Triggering the Lightbox:** Each thumbnail image is wrapped in an anchor tag with an `href` attribute pointing to a specific ID (e.g., `<a href="#img-1">...</a>`).
2.  **Changing the URL:** When the thumbnail is clicked, the URL hash changes (e.g., `...#img-1`).
3.  **Activating the Lightbox:** A corresponding hidden **`.lightbox`** `div` with a matching ID (e.g., `<div class="lightbox" id="img-1">`) is present in the HTML.
4.  **The `:target` Selector:** The CSS rule `.lightbox:target` is activated when the URL hash matches the element's ID. This rule changes the `opacity` from `0` to `1` and enables `pointer-events`, making the lightbox visible and interactive.
5.  **Closing the Lightbox:** The lightbox contains a full-size anchor tag `<a href="#" class="close"></a>`. Clicking anywhere on this area changes the URL hash back to `#` (or removes the hash), deactivating the `:target` state and smoothly hiding the lightbox.

---

## 🚀 Getting Started

To view or deploy this project, simply follow these steps:

1.  **Clone the Repository:**
    ```bash
    git clone [Your Repository URL]
    ```
2.  **Navigate to the Project Directory:**
    ```bash
    cd Light_Box_Animation
    ```
3.  **Open the File:**
    * Locate the **`Light_Box_Animation.htm`** file.
    * Open it directly in any modern web browser (Google Chrome, Firefox, Edge, etc.).

---

## 💻 Code Structure Highlights

### HTML (`Light_Box_Animation.htm`)

```html
<body>
    <a href="#img-1" class="a"><img src="..." ></a> 
    <div class="lightbox" id="img-1">
        <a href="#" class="close"></a> <img src="..." class="b">
    </div>
    </body>
