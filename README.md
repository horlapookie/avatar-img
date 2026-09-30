# Avatar Assets (3D Transparent)

3D high-resolution transparent PNG assets for the Avatar Battle Bot, web dashboards, and related client applications.

## Directory Structure

```text
avatar-img/
├── skins/                 # Character skin models (3D transparent full-body)
│   ├── aang.png
│   ├── katara.png
│   ├── toph.png
│   ├── zuko.png
│   └── ...
└── elixir/                # Consumable elixirs & potions (3D transparent icons)
    ├── training_grain.png
    ├── chi_fragment.png
    ├── spirit_ember.png
    ├── spirit_dust.png
    └── ...
```

---

## How Applications Call These Images

Applications (such as WhatsApp bots, Discord bots, React dashboards, or Express servers) can access these images using either direct GitHub raw links or the global jsDelivr CDN.

### 1. jsDelivr CDN (Recommended for High Speed & Global Caching)

- **Character Skins:**
  ```text
  https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/{skin_id}.png
  ```
  Example: `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/aang.png`

- **Elixirs:**
  ```text
  https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/{elixir_id}.png
  ```
  Example: `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/training_grain.png`

---

### 2. GitHub Raw URL

- **Character Skins:**
  ```text
  https://raw.githubusercontent.com/horlapookie/avatar-img/main/skins/{skin_id}.png
  ```
- **Elixirs:**
  ```text
  https://raw.githubusercontent.com/horlapookie/avatar-img/main/elixir/{elixir_id}.png
  ```

---

### 3. Usage Examples in Code

#### Node.js / Bot Helper (`src/utils/assets.js`)

```javascript
const CDN_BASE = 'https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main'

function getSkinImageUrl(skinId) {
  return `${CDN_BASE}/skins/${skinId}.png`
}

function getElixirImageUrl(elixirId) {
  return `${CDN_BASE}/elixir/${elixirId}.png`
}

module.exports = { getSkinImageUrl, getElixirImageUrl }
```

#### React / Dashboard Image Tag

```jsx
<img 
  src={`https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/${skin.id}.png`} 
  alt={skin.name} 
  className="w-24 h-24 object-contain" 
/>
```
