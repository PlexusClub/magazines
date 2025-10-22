# Plexus Club Magazine Collection

Welcome to the official GitHub repository for the **Plexus Club Magazine Collection**!

This repository hosts the web interface for viewing all digital editions of the Plexus Club Magazine, presented as interactive flipbooks.

---

## Getting Started

To view the magazine collection, simply visit the deployed website link (usually through **GitHub Pages** if enabled for this repository).

### Viewing the Magazines

1.  **Open the Live Site**: Navigate to the main page of this repository's deployed site.
2.  **Browse the Shelf**: You'll see a bookshelf layout with magazine covers.
3.  **Click to Read**: Click on any available magazine cover to open it in an interactive flipbook viewer powered by **dFlip**.

Magazines marked "Coming Soon" have their covers displayed but are not yet available to read.

---

## Repository Structure

This project is a static website utilizing JavaScript to dynamically load magazine data from a JSON file.

| File/Folder | Description |
| :--- | :--- |
| `index.html` | The main HTML file that renders the bookshelf and flipbook viewer. |
| `data.json` | Contains the **metadata** (title, description, source path) for all magazines in the collection. |
| `dflip/` | Contains the essential files (CSS/JS) for the **dFlip** flipbook library. |
| `magazines/` | *(Expected)* Directory to store the **PDF** files of the magazines themselves. |
| `covers/` | *(Expected)* Directory to store the **thumbnail images** used for the magazine covers. |

---

## Contributing

We currently focus on maintaining and updating the magazine collection. If you are a member of the Plexus Club team responsible for publication, here’s how you can add a new magazine:

1.  **Add Files**: Upload the magazine PDF to the `magazines/` folder and its thumbnail image to the `covers/` folder.
2.  **Update `data.json`**: Add a new object to the `magazines` array in `data.json`.
    * Set the `source` field to the path of the new PDF.
    * Set the `thumb` field to the path of the new cover image.
    * Set the `title` and `desc` fields.

*Example `data.json` entry:*

```json
{
    "title": "Issue X: The Future of AI",
    "desc": "Winter 2024 Edition",
    "source": "magazines/issue_x.pdf",
    "thumb": "covers/issue_x_thumb.jpg",
    "thumbname": "Issue X Cover"
}