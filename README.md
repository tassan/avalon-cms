
# Avalon CMS

Avalon CMS is a simple, lightweight, and flexible static blog generator that allows you to manage blog posts in Markdown with metadata. It can be easily configured using a YAML file (`avalon.conf`) and is designed to work as a terminal-based tool. Avalon CMS provides a clean and customizable structure for your blog and helps you convert Markdown files into fully rendered HTML blog posts.

## Features

- **Markdown Posts**: Write your blog posts in Markdown with YAML front matter for metadata.
- **Simple Setup**: Easily set up a new blog structure with the `avalon init` command.
- **Post Parsing**: Avalon automatically converts your Markdown posts into HTML.
- **Customizable Templates**: Define custom HTML templates for rendering posts and the homepage.
- **Static Output**: Generates static HTML files for hosting on any static web server or platform (e.g., GitHub Pages, Netlify).
- **Configuration File**: Configure your blog structure and metadata in a single `avalon.conf` YAML file.

## Table of Contents

1. [Installation](#installation)
2. [Configuration](#configuration)
3. [Usage](#usage)
4. [Development](#development)
5. [License](#license)

## Installation

1. Clone the repository or download the source code.

```bash
git clone https://github.com/yourusername/avalon-cms.git
cd avalon-cms
```

2. Install the required dependencies.

```bash
npm install
```

3. Make sure to add the command-line tool to your system's PATH if needed. Alternatively, run the tool directly with Node.js.

## Configuration

Before using Avalon CMS, create or modify the `avalon.conf` YAML configuration file in the root of your project. Here is an example configuration:

```yaml
blog:
  title: "My Awesome Blog"
  author: "John Doe"
  description: "A personal blog about tech and life"

directories:
  blog_root: "./blog"             # Root folder for the blog
  posts_dir: "./blog/posts"       # Folder for posts
  assets_dir: "./blog/assets"     # Folder for images and assets
  templates_dir: "./blog/templates" # Folder for templates

theme:
  style: "./blog/style.css"       # Path to the blog's CSS file

metadata:
  date_format: "YYYY-MM-DD"      # Format for post dates
  categories:
    - "Tech"
    - "Lifestyle"
    - "Tutorial"
```

## Usage

Avalon CMS provides several commands to manage your blog via the terminal:

### 1. Initialize a New Blog

Use the `init` command to create the necessary blog structure. Avalon will read the configuration from `avalon.conf` (or a custom YAML file) and create the directories, posts, templates, and style files for you.

```bash
node bin/avalon.js init avalon.conf
```

This will set up the following structure in your project:

```
blog/
  ├── posts/
  ├── assets/
  ├── templates/
  └── style.css
```

### 2. Generate Blog Posts

Once your blog structure is set up, use the `generate` command to parse your Markdown files and render them as HTML:

```bash
node bin/avalon.js generate
```

This will generate the HTML files in the `output/` directory.

### 3. Serve Your Blog Locally

You can serve your generated blog locally to preview it using the `serve` command. This can be done using a simple static server like `http-server` or by setting up a more complex solution with Express.

```bash
node bin/avalon.js serve
```

### 4. Customize Templates

You can customize the appearance and layout of your blog by editing the templates in the `templates/` folder and modifying the `style.css` file in the `blog/` folder.

## Development

1. Clone the repository:

```bash
git clone https://github.com/yourusername/avalon-cms.git
cd avalon-cms
```

2. Install dependencies:

```bash
npm install
```

3. Run tests (if applicable):

```bash
npm test
```

4. Submit pull requests or open issues for bug reports and feature requests.

## License

Avalon CMS is open-source software licensed under the **MIT License**.

You can find the full license in the [LICENSE](./LICENSE) file.

---

## License

Avalon CMS is licensed under the **MIT License**.

MIT License (MIT)

Copyright (c) 2024 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
