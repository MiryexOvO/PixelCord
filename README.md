# PixelCord


**Material You, for Discord.** A Pixel-inspired theme by **Miryex** for BetterDiscord and Vencord.

Warm charcoal surfaces, dusty rose accents, rounded panels, customizable wallpaper, message bubbles, and an expandable avatar-only member list with status rings.

Version: **0.9.0** · Preview release · Not affiliated with Google, Discord, or BetterDiscord.

## Download and install

[Download PixelCord.theme.css](https://github.com/MiryexOvO/PixelCord/raw/refs/heads/main/PixelCord.theme.css) — save the actual CSS file, not an HTML page.

- **BetterDiscord:** Settings → Themes → Open Themes Folder. Copy `PixelCord.theme.css` there and enable PixelCord.
- **Vencord:** Settings → Themes → Open Themes Folder, then enable PixelCord. On Windows the folder is usually `%APPDATA%\Vencord\themes`.
- Disable other themes and the old **Pixel Bloom** version to avoid overlapping rules. Toggle the theme off/on after an update.

The GitHub download link becomes available after this repository is published. This project is **not currently listed or approved on the BetterDiscord theme directory**.

## Customize

Edit the variables near the top of `PixelCord.theme.css`:

```css
--pb-wallpaper: none; /* Flat background by default */
/* Replace the line above to use your own image: */
/* --pb-wallpaper: url("https://example.com/wallpaper.jpg"); */
--pb-wallpaper-position: center;
--pb-wallpaper-blur: 10px; /* 0px disables wallpaper blur */
--pb-panel-opacity: 86%;
--pb-gap: 12px;
--pb-members-collapsed: 76px;
--pb-members-expanded: 248px;
```

Use an accessible direct HTTPS image URL or an image data URI. A Windows file path or an image sharing page is not a direct image URL. Wallpaper is optional and is loaded by your Discord client from its host.

The theme follows Discord light/dark mode. Customize the paired `--pb-accent` and `--pb-on-accent` colors in each palette together to maintain readable labels. Code blocks retain a monospace font.

## Fonts and performance

Nunito Sans and Noto Sans SC load from Google Fonts; system fonts are used if unavailable. Remove the opening font `@import` for offline-only use.

A separate wallpaper layer uses a stationary image blur. Panels do **not** use live `backdrop-filter`. No blanket `will-change` or GPU-forcing rules are applied. Member expansion still changes layout; actual performance depends on the Discord build and hardware.

## Known limitations

- Primarily tested by the author in Vencord; BetterDiscord client compatibility has not been fully verified.
- Discord class changes can break selectors. Please report the affected screen, client version, theme version and a screenshot with personal details removed through [GitHub Issues](https://github.com/MiryexOvO/PixelCord/issues).
- Member rings recognize native SVG status masks. Unrecognized structures retain their original status indicator.

## 中文说明

将主题文件放进 BetterDiscord 或 Vencord 的 Themes 文件夹并启用。先关闭旧版 Pixel Bloom 和其他主题。顶部变量可替换背景、调整透明度和头像成员栏宽度。公开版默认使用纯色背景，不包含个人壁纸。

