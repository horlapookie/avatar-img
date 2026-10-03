# Avatar Game Assets Repository

3D transparent-background assets for characters/skins, elixirs, and artifacts in the Avatar Bot & Game ecosystem.

Hosted directly via raw GitHub URLs.

---

## 🌐 URL Format (Raw GitHub)

All images are served in PNG format with transparent backgrounds.

### Base URL
```
https://raw.githubusercontent.com/horlapookie/avatar-img/main/
```

- **Skins:** `https://raw.githubusercontent.com/horlapookie/avatar-img/main/skins/<skin_id>.png`
- **Elixirs:** `https://raw.githubusercontent.com/horlapookie/avatar-img/main/elixir/<elixir_id>.png`
- **Artifacts:** `https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/<artifact_id>.png`

---

## 💻 How Applications Can Call These Images

### 1. JavaScript / TypeScript Helper

```javascript
const ASSET_BASE_URL = 'https://raw.githubusercontent.com/horlapookie/avatar-img/main';

export const getSkinUrl = (skinId) => `${ASSET_BASE_URL}/skins/${skinId}.png`;
export const getElixirUrl = (elixirId) => `${ASSET_BASE_URL}/elixir/${elixirId}.png`;
export const getArtifactUrl = (artifactId) => `${ASSET_BASE_URL}/artifacts/${artifactId}.png`;

// Example usage:
console.log(getArtifactUrl('spirit_blade'));
// -> https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/spirit_blade.png
```

### 2. React Component Example

```jsx
import React from 'react';

const RAW_BASE = 'https://raw.githubusercontent.com/horlapookie/avatar-img/main';

export const ItemCard = ({ type, id, name }) => {
  const src = `${RAW_BASE}/${type}/${id}.png`;
  return (
    <div className="item-card">
      <img src={src} alt={name} loading="lazy" />
      <p>{name}</p>
    </div>
  );
};

// Usage:
// <ItemCard type="artifacts" id="dragon_fang" name="Dragon Fang" />
// <ItemCard type="skins" id="aang" name="Aang" />
// <ItemCard type="elixir" id="dragon_brew" name="Dragon Brew" />
```

### 3. Telegram Bot (Node.js telegraf)

```javascript
const RAW_BASE = 'https://raw.githubusercontent.com/horlapookie/avatar-img/main';

bot.command('artifact', (ctx) => {
  const artifactId = 'celestial_ring';
  ctx.replyWithPhoto(`${RAW_BASE}/artifacts/${artifactId}.png`, {
    caption: `✨ *Celestial Ring* equipped!`,
    parse_mode: 'Markdown'
  });
});
```

---

## 📦 Asset Catalogs

### Artifacts (12 Total)
| Artifact ID | Raw Image Link |
| :--- | :--- |
| `spirit_blade` | [spirit_blade.png](https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/spirit_blade.png) |
| `chi_gauntlet` | [chi_gauntlet.png](https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/chi_gauntlet.png) |
| `storm_staff` | [storm_staff.png](https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/storm_staff.png) |
| `iron_shield` | [iron_shield.png](https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/iron_shield.png) |
| `dragon_fang` | [dragon_fang.png](https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/dragon_fang.png) |
| `shadow_bow` | [shadow_bow.png](https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/shadow_bow.png) |
| `moon_orb` | [moon_orb.png](https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/moon_orb.png) |
| `thunder_crown` | [thunder_crown.png](https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/thunder_crown.png) |
| `earth_core` | [earth_core.png](https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/earth_core.png) |
| `void_cloak` | [void_cloak.png](https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/void_cloak.png) |
| `celestial_ring` | [celestial_ring.png](https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/celestial_ring.png) |
| `avatar_spear` | [avatar_spear.png](https://raw.githubusercontent.com/horlapookie/avatar-img/main/artifacts/avatar_spear.png) |

### Elixirs (13 Total)
`dragon_brew`, `spirit_drop`, `chi_potion`, `moon_elixir`, `earth_elixir`, `monk_elixir`, `lion_turtle`, `avatar_elixir`, `world_cup_elixir`, `avatar_core`, `sun_fire_elixir`, `glacier_extract`, `lightning_core`.

### Skins (63 Total)
Includes standard bending masters, elemental warriors, DC/Marvel skins (`shazam`, `batman`, `iron_man`, `thor`), and superhero variants.
