# 🏏 Virat Kohli: A Legacy in Formats — Power BI Dashboard

This Power BI dashboard is a tribute to the legendary career of **Virat Kohli**, blending deep cricket analytics with cinematic visuals and poetic storytelling. It showcases his performance across formats — **Test**, **ODI**, and **T20I** — using interactive visuals, dynamic images, and heartfelt captions.

---

## 🎯 Features

- 📊 **Interactive Format Slicer**  
  Switch between Test, ODI, and T20I using a button slicer that filters visuals and updates the central image dynamically.

- 🖼️ **Dynamic Image Visuals**  
  Format-specific images are displayed using embeddable URLs from WallpaperAccess. These visuals anchor the emotional tone of each format.

- 📈 **Performance Metrics**
  - Runs by opposition
  - Centuries by team
  - Run distribution against SENA nations
  - Batting position analysis

- 🧠 **Data Modeling**
  - Format-specific tables (`Test_Table`, `ODI_Table`, `T20I_Table`)
  - Joined with `FormatImages` using Power Query M code
  - Dynamic image rendering via `ImageURL` column categorized as `Image URL`

---

## 🔧 Power Query Snippets

### Join FormatImages with Main Table
```m
JoinedTable = Table.Join(
    MainTable, "Format",
    FormatImages, "Format",
    JoinKind.LeftOuter
)
