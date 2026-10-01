# 🌌 Avatar Game Assets CDN (`avatar-img`)

High-resolution 3D rendered character skins and consumable elixir assets with isolated transparent backgrounds for the Avatar game, Discord bots, Telegram bots, web apps, and mobile clients.

---

## ⚡ Quick Start: Calling Images

All assets are hosted directly in this repository and can be consumed via high-speed global CDNs (recommended for caching and low latency) or directly through GitHub raw content.

### 1. jsDelivr CDN (Recommended)

Fastest delivery, edge-cached across global Cloudflare / Fastly nodes:

```text
# Character Skin
https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/{SKIN_ID}.png

# Elixir / Potion
https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/{ELIXIR_ID}.png
```

### 2. GitHub Raw URLs

Direct un-cached access:

```text
https://raw.githubusercontent.com/horlapookie/avatar-img/main/skins/{SKIN_ID}.png
https://raw.githubusercontent.com/horlapookie/avatar-img/main/elixir/{ELIXIR_ID}.png
```

---

## 💻 Code Examples

### JavaScript / TypeScript Helper

```javascript
const ASSET_BASE_URL = "https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main";

export function getSkinUrl(skinId) {
  return `${ASSET_BASE_URL}/skins/${skinId}.png`;
}

export function getElixirUrl(elixirId) {
  return `${ASSET_BASE_URL}/elixir/${elixirId}.png`;
}

// Usage:
console.log(getSkinUrl("aang"));
// => "https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/aang.png"

console.log(getElixirUrl("avatar_core"));
// => "https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/avatar_core.png"
```

### HTML / React / Vue

```jsx
// React Component
export function CharacterAvatar({ skinId, name }) {
  const src = `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/${skinId}.png`;
  return (
    <img 
      src={src} 
      alt={name || skinId} 
      width={256} 
      height={256} 
      loading="lazy" 
      style={{ objectFit: "contain" }} 
    />
  );
}
```

### Discord.js Bot Embed

```javascript
const { EmbedBuilder } = require("discord.js");

function createCharacterProfileEmbed(character) {
  const skinUrl = `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/${character.skinId}.png`;
  
  return new EmbedBuilder()
    .setTitle(`${character.name} - Level ${character.level}`)
    .setColor(0x00ae86)
    .setImage(skinUrl)
    .setFooter({ text: "Avatar RPG" });
}
```

### Telegram Bot (Node-Telegram-Bot-API)

```javascript
bot.sendPhoto(chatId, `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/${skinId}.png`, {
  caption: `<b>${characterName}</b> ready for duel!`,
  parse_mode: "HTML"
});
```

---

## 📦 Asset Directory Catalog

### 🧪 Elixirs (13 Total)

| Asset ID | Filename | jsDelivr CDN URL |
| :--- | :--- | :--- |
| `avatar_elixir` | `avatar_elixir.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/avatar_elixir.png` |
| `chi_fragment` | `chi_fragment.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/chi_fragment.png` |
| `chi_potion` | `chi_potion.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/chi_potion.png` |
| `dragon_brew` | `dragon_brew.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/dragon_brew.png` |
| `earth_elixir` | `earth_elixir.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/earth_elixir.png` |
| `lion_turtle` | `lion_turtle.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/lion_turtle.png` |
| `monk_elixir` | `monk_elixir.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/monk_elixir.png` |
| `moon_elixir` | `moon_elixir.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/moon_elixir.png` |
| `spirit_drop` | `spirit_drop.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/spirit_drop.png` |
| `spirit_dust` | `spirit_dust.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/spirit_dust.png` |
| `spirit_ember` | `spirit_ember.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/spirit_ember.png` |
| `training_grain` | `training_grain.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/training_grain.png` |
| `world_cup_elixir` | `world_cup_elixir.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/elixir/world_cup_elixir.png` |

---

### 🥋 Character Skins (59 Total)

| Asset ID | Filename | jsDelivr CDN URL |
| :--- | :--- | :--- |
| `a_train` | `a_train.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/a_train.png` |
| `aang` | `aang.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/aang.png` |
| `air_monk_battle` | `air_monk_battle.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/air_monk_battle.png` |
| `azula` | `azula.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/azula.png` |
| `black_noir` | `black_noir.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/black_noir.png` |
| `bolin` | `bolin.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/bolin.png` |
| `boulder_beast` | `boulder_beast.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/boulder_beast.png` |
| `boulder_crusher` | `boulder_crusher.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/boulder_crusher.png` |
| `cloud_dancer` | `cloud_dancer.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/cloud_dancer.png` |
| `combustion_man` | `combustion_man.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/combustion_man.png` |
| `comet_rider` | `comet_rider.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/comet_rider.png` |
| `crimson_phoenix` | `crimson_phoenix.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/crimson_phoenix.png` |
| `crystal_weaver` | `crystal_weaver.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/crystal_weaver.png` |
| `dragon_disciple` | `dragon_disciple.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/dragon_disciple.png` |
| `dragon_lord` | `dragon_lord.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/dragon_lord.png` |
| `earth_brawler` | `earth_brawler.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/earth_brawler.png` |
| `earth_colossus` | `earth_colossus.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/earth_colossus.png` |
| `ember_blade` | `ember_blade.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/ember_blade.png` |
| `fire_dancer` | `fire_dancer.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/fire_dancer.png` |
| `flame_empress` | `flame_empress.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/flame_empress.png` |
| `frostbite` | `frostbite.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/frostbite.png` |
| `gale_force` | `gale_force.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/gale_force.png` |
| `heavenly_predicament_skin` | `heavenly_predicament_skin.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/heavenly_predicament_skin.png` |
| `homelander` | `homelander.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/homelander.png` |
| `ice_maiden` | `ice_maiden.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/ice_maiden.png` |
| `inferno_king` | `inferno_king.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/inferno_king.png` |
| `inferno_lord` | `inferno_lord.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/inferno_lord.png` |
| `iroh` | `iroh.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/iroh.png` |
| `iron_fist` | `iron_fist.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/iron_fist.png` |
| `iron_monk` | `iron_monk.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/iron_monk.png` |
| `katara` | `katara.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/katara.png` |
| `king_bumi` | `king_bumi.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/king_bumi.png` |
| `korra` | `korra.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/korra.png` |
| `kyoshi` | `kyoshi.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/kyoshi.png` |
| `lava_lord` | `lava_lord.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/lava_lord.png` |
| `monk_gyatso` | `monk_gyatso.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/monk_gyatso.png` |
| `moon_spirit_warrior` | `moon_spirit_warrior.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/moon_spirit_warrior.png` |
| `ocean_empress` | `ocean_empress.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/ocean_empress.png` |
| `pakku` | `pakku.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/pakku.png` |
| `rain_dancer` | `rain_dancer.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/rain_dancer.png` |
| `roku` | `roku.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/roku.png` |
| `sand_queen` | `sand_queen.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/sand_queen.png` |
| `seismic_striker` | `seismic_striker.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/seismic_striker.png` |
| `sky_nomad` | `sky_nomad.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/sky_nomad.png` |
| `solar_flare` | `solar_flare.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/solar_flare.png` |
| `solar_phoenix` | `solar_phoenix.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/solar_phoenix.png` |
| `spiderman` | `spiderman.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/spiderman.png` |
| `starlight` | `starlight.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/starlight.png` |
| `stone_guardian` | `stone_guardian.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/stone_guardian.png` |
| `stone_titan` | `stone_titan.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/stone_titan.png` |
| `storm_sister` | `storm_sister.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/storm_sister.png` |
| `terrakin` | `terrakin.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/terrakin.png` |
| `tide_walker` | `tide_walker.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/tide_walker.png` |
| `toph` | `toph.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/toph.png` |
| `void_monk` | `void_monk.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/void_monk.png` |
| `volcano_spirit` | `volcano_spirit.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/volcano_spirit.png` |
| `wind_phantom` | `wind_phantom.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/wind_phantom.png` |
| `zaheer` | `zaheer.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/zaheer.png` |
| `zuko` | `zuko.png` | `https://cdn.jsdelivr.net/gh/horlapookie/avatar-img@main/skins/zuko.png` |

---

## 📐 Asset Specifications

- **Format:** PNG with 32-bit alpha channel (transparent background)
- **Resolution:** 1024 x 1024 px
- **Style:** 3D stylized game character & item renders
- **Subject Framing:** Full-body centered character models / centered potion bottles
