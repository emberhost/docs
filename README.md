# Contribution Guidelines for Ember Host Documentation

Thank you for your interest in contributing to the community-maintained Ember Host Documentation! To ensure consistency and quality across our guides, we have outlined the following general formatting rules and specifications. Please follow these guidelines when creating or updating documentation files.

<details>
<summary><strong>General Rules and Formatting Guide 📝 </strong></summary>

## **General Rules**
- **Descriptive Frontmatter:** Each file must include YAML frontmatter at the top for metadata. Example:
  ```yaml
  ---
  description: A brief description of what this page covers.
  ---

  # Name of this page
  ```
- **Headings:** Use concise and descriptive titles for each section. Structure your document with the following hierarchy:
  - `#` for the main title
  - `###` for subsections

- **Consistent Language:** 
  - Use second-person ("you" and "your") to directly address the reader.
  - Keep sentences clear and to the point.
  - Avoid jargon unless necessary, and explain technical terms when introduced.

---

## **Content Formatting**

### **Introductions**
- Start with a brief overview of the topic, including:
  - What the guide covers.
  - Any prerequisites or requirements.
- Use blockquotes (`>`) to format introductory notes:
  ```markdown
  > **Requirements**  
  > In order to follow this guide, ensure you have [specific prerequisites](link-to-resource).
  ```

### **Headings and Sections**
- Use descriptive headings for each section. Example:
  ```markdown
  ### Installing Mods
  ```
- Add short paragraphs and use bullet or numbered lists for clarity:
  ```markdown
  1. Navigate to your server's root directory.
  2. Locate the `mods` folder.
  3. Upload the mod file into this folder.
  ```

---

### **Callouts**
- Use callouts for important information, warnings, or tips. Example:
  ```markdown
  {% hint style="warning" %}
  **Mod Compatibility**  
  Ensure you're downloading the correct version of your mods! Forge and Fabric mods are usually not cross-compatible.
  {% endhint %}
  ```

- Supported callout styles:
  - **Info**
  - **Success**
  - **Warning**
  - **Danger**

```markdown
{% hint style="info" %}
**Info hints** are for showing general information, or providing tips and tricks.
{% endhint %}

{% hint style="success" %}
**Success hints** are for showing positive actions that a reader should take.
{% endhint %}

{% hint style="warning" %}
**Warning hints** are for showing important information or non-critical warnings.
{% endhint %}

{% hint style="danger" %}
**Danger hints** are for highlighting destructive actions or raising attention to critical information.
{% endhint %}
```

---

### **Links**
- Use relative paths for internal links. Example:
  ```markdown
  See our guide on [installing server plugins](../plugins/installing-plugins.md).
  ```

---

### **Images and Media**
- Include relevant screenshots or diagrams to enhance the guide.
- Ensure images are:
  - Clear and properly cropped.
  - Uploaded to the `/assets/images` folder with a logical name.
  - Inserted using Markdown syntax:
    ```markdown
    ![Descriptive Alt Text](../assets/images/image-name.png)
    ```

---

### **Code Blocks**
- Use fenced code blocks with the correct language for syntax highlighting:
  ```markdown
  ```bash
  git clone https://github.com/emberhost/docs.git
  `‎``
  ```
- Use inline code formatting (\`backticks\`) for short snippets within sentences.

---

## **Writing Style**
- **Active Voice:** Write in active voice wherever possible. Example:
  - ✅ "Restart your server to apply the changes."
  - ❌ "The server should be restarted to apply the changes."
- **Friendly Tone:** Maintain a professional but approachable tone. Avoid overly technical or formal language unless necessary.
- **Avoid Redundancy:** Do not repeat information unnecessarily. Cross-reference related guides where applicable.

---

## **Examples**

### **Frontmatter**
```yaml
---
description: How to install mods to customise your server!
---

# Installing Mods
```

### **Basic Structure**
```markdown

### Introduction

> **Requirements**  
> You must be using either [Forge](https://files.minecraftforge.net/net/minecraftforge/forge/) or [Fabric](https://fabricmc.net/use/server/).

{% hint style="warning" %}
**Mod Compatibility**  
Ensure you're downloading the correct version of your mods!
{% endhint %}

1. Locate the mod on [Modrinth](https://modrinth.com/mods) or [CurseForge](https://www.curseforge.com/minecraft/mc-mods).
2. Upload the mod file into the `mods` folder in your server's root directory.
3. Restart your server.
``` 
</details>

<details>
<summary><strong>How to Contribute 📚 </strong></summary>

## **Contributing Process**
1. **Fork the Repository:** Click the "Fork" button to create a personal copy.
2. **Clone Your Fork:** Download your forked repository:
   ```bash
   git clone https://github.com/your-username/docs.git
   ```
3. **Create a New Branch:** Work on your changes in a new branch:
   ```bash
   git checkout -b descriptive-branch-name
   ```
4. **Edit or Add Files:** Use the formatting rules and style guide outlined here.
5. **Commit and Push:**
   ```bash
   git add .
   git commit -m "Brief description of your changes"
   git push origin descriptive-branch-name
   ```
6. **Submit a Pull Request:** Navigate back to our [original repository](https://github.com/emberhost/docs) and submit a pull request.

Alternatively, you can send us your written text on our [Discord server](https://ember.host/discord) and we will publish it on our docs. 

</details>

# Hall of Fame

These are the helpful people who have contributed to our docs! If you have and you aren't listed here, let us know on our [Discord](https://ember.host/discord), and we'll also give you the helpful role.

- IceWaffles (`@icewaffles`)
- Sammy (`@goldenedit`)
