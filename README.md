# 🧬 HOLOBION: Symbiosis Design System

**Version:** 1.0 | **Organization:** Holobion (Open Source)

## 1. DNA & Values (Project Philosophy)

Holobion is not just a software suite; it is a digital ecosystem. Just as in living organisms, each application (the symbiote) serves its own specific function but relies on a common underlying structure (the host) to thrive.

* **Interconnection:** No data or application exists in isolation. Everything is designed as a network (API-first, interoperability).
* **Organic Evolution:** As an open-source project, the organization grows through collective contributions, much like an organism adapting to its environment.
* **Scientific Clarity:** Aesthetics must serve information. The interfaces often manage complex data; they must remain legible, neutral, and highly precise.
* **Symbiosis:** The user and the interface must work in harmony, without friction.

## 2. Voice and Tone (How We Speak)

The way Holobion communicates (in code, documentation, error messages, and marketing) must reflect its DNA.

* **Professional yet Accessible:** We deal with science and code, but we are not elitist.
* **Metaphorical yet Precise:** We subtly use the lexicon of living things (*ecosystem, graft, nucleus, membrane, hybridization*), but **never** at the expense of technical clarity.
* **Collaborative ("We"):** Open-source implies a community. Use "We", "Together", "Our ecosystem".

✅ **DO:**

* *"Graft this module to your project to extend its capabilities."*
* *"The application's core (nucleus) has been updated."*
* *"Oops, the connection to the host was lost. Attempting to reconnect..."*

❌ **DON'T:**

* Overly mystical or sci-fi jargon (*"The quantum nexus has failed"* -> No).
* The cold, robotic tone of traditional SaaS (*"Error 404: Database not found"* -> Prefer *"We couldn't find this element in the ecosystem"*).

---

## 3. Typography (The Skeleton)

Our typographic choices rely on the contrast between organic shapes (headings) and scientific rigor (body text and data).

* **Headings (The Organic): `Outfit**` or **`Space Grotesk`**
* *Why:* Soft, geometric curves that evoke cellular shapes while remaining highly modern.
* *Usage:* H1, H2, H3, Application names.


* **Body Text (The Neutral): `Inter**`
* *Why:* The most readable typeface for screens. It is neutral and steps back to let the information shine.
* *Usage:* Paragraphs, descriptions, menus.


* **Code & Data (The Sequencing): `JetBrains Mono**`
* *Why:* Perfect for open-source. Maximum legibility for numbers, data tables, and code blocks.



---

## 4. Color Palette (The Pigmentation)

The system is built on the separation between "The Host" (background colors, common to all) and "The Symbiotes" (accent colors, specific to each app).

### 4.1. The Host (Base Colors)

These colors form the interface's foundation. They are soft, natural, and soothing to the eye.

* **Membrane (Main Background):** `#F8FAFC` (A very light blue/gray off-white, less harsh than pure white).
* **Cytoplasm (Card/Component Background):** `#FFFFFF` (Pure white, to make elements pop against the Membrane background).
* **Nucleus (Main Text):** `#0F172A` (A very deep midnight blue, almost black. Softer on the eyes than `#000000`).
* **Matrix (Secondary Text / Borders):** `#64748B` (Slate gray for subtitles and divider lines).

### 4.2. The Symbiotes (Accent Colors per App)

Each solution within the Holobion organization chooses **one primary color** from this nature-inspired palette. It will be used for buttons, links, and glowing halos.

* 🟩 **Chlorophyll:** `#10B981` (Vibrant emerald green) -> *Ideal for data, health, or monitoring apps.*
* 🟦 **Bioluminescence:** `#06B6D4` (Electric cyan) -> *Ideal for networks, APIs, data flows.*
* 🟪 **Mycelium:** `#8B5CF6` (Organic purple) -> *Ideal for AI, complex algorithms, machine learning.*
* 🟧 **Coral:** `#F43F5E` (Vivid pink/orange) -> *Ideal for alerts, security, critical infrastructure.*

---

## 5. UI & Graphic Elements (The Anatomy)

To ensure Holobion is recognizable at a glance, here are the component design rules:

### 5.1. Shapes (Squarcles & Radii)

The perfect right angle does not exist in nature.

* **Universal Border-Radius:** All containers (cards, modals) must have a generous rounding. The standard value is `16px` or `24px`.
* **Buttons and Badges:** Fully rounded (pill shape) for primary actions (`border-radius: 9999px`), or `12px` for secondary buttons.

### 5.2. Halos (Organic Shadows)

Instead of using harsh, gray drop shadows, we use colored "Halos" that make active elements look like they are emitting light (like bioluminescent organisms).

* *CSS Example:* `box-shadow: 0 10px 25px -5px rgba(SymbioteColor, 0.3);`

### 5.3. Semi-Permeable Membrane (Glassmorphism)

Navigation bars (Topbars) and floating menus should use a slight background blur effect. This adds depth and simulates the overlapping of organic tissues.

* *CSS Example:* `background: rgba(255, 255, 255, 0.8); backdrop-filter: blur(12px);`

### 5.4. The "Mycelium" Texture (The Signature Pattern)

To avoid large empty spaces (Empty States, login screen backgrounds), use a very subtle SVG pattern (3% to 5% opacity) representing a network of neurons, synapses, or interconnected mycelium. This pattern is the organization's visual signature.

---

## 6. Iconography and Imagery

* **Icons:** Use a line icon set such as *Lucide Icons* or *Phosphor Icons*.
* **Rule:** Stroke width of `1.5px`, round caps. Icons must be light, clean, and geometric.


* **Illustrations:** If illustrations are needed, opt for clean isometric styles or abstract 3D elements (spheres, point networks, gentle waves) that utilize the symbiote colors. Avoid flat, cartoony human characters (the "Corporate Memphis" style) which would dilute the brand's unique identity.

---

## 7. Implementation Guide (For Contributors)

To make life easy for open-source developers, this design system must be implementable via variables. (Example compatible with Tailwind CSS / Native CSS):

**The `theme-base.css` file (The Host):**

```css
:root {
  --hb-font-heading: 'Outfit', sans-serif;
  --hb-font-body: 'Inter', sans-serif;
  --hb-font-mono: 'JetBrains Mono', monospace;
  
  --hb-bg-membrane: #F8FAFC;
  --hb-bg-cytoplasm: #FFFFFF;
  --hb-text-nucleus: #0F172A;
  
  --hb-radius-cell: 16px;
  --hb-radius-pill: 9999px;
}

```

**The variant files (e.g., `symbiote-biolum.css`):**

```css
.theme-bioluminescence {
  --hb-color-primary: #06B6D4;
  --hb-glow-primary: rgba(6, 182, 212, 0.25);
  --hb-color-hover: #0891B2;
}

```

*The contributor only needs to add the `theme-bioluminescence` class to the `<body>` tag of their project, and all components (buttons, links, halos) will instantly adapt.*
