# Mini Search Engine for Articles

## Overview

This project is a **Mini Search Engine for Articles** built with Node.js and Express. It allows users to upload articles, search for articles based on keywords, and retrieve articles based on their unique ID. The search results can be sorted by relevance (keyword frequency) or by date.

The project uses in-memory storage for articles, but optionally supports persistence by saving articles to a `data.json` file.

## Features

- **Add Articles**: Users can add articles with a title, content, and tags.
- **Search Articles**: Search articles by keywords in the title, content, or tags.
- **Sort Results**: Sort the search results by relevance (keyword frequency) or by date.
- **Get Article by ID**: Retrieve the full details of an article using its ID.

## API Endpoints

### 1. **Add Article**
- **Endpoint**: `POST /articles`
- **Request Body** (JSON):
    ```json
    {
        "title": "Article Title",
        "content": "This is the content of the article.",
        "tags": ["tag1", "tag2"]
    }
    ```
- **Response**: The newly created article with `id`, `title`, `content`, and `tags`.

### 2. **Search Articles**
- **Endpoint**: `GET /articles/search`
- **Query Parameters**:
    - `keyword`: The keyword to search for in the title, content, or tags.
    - `sortBy`: Sort results by `relevance` or `date`.
- **Response**: A list of articles matching the search criteria, sorted by the selected parameter.

### 3. **Get Article by ID**
- **Endpoint**: `GET /articles/:id`
- **Path Parameters**:
    - `id`: The ID of the article to retrieve.
- **Response**: The article with the specified ID.

## Requirements

- Node.js (v14.0.0 or later)
- Express (Installable via npm)

## Installation

### Clone the Repository

```bash
git clone https://github.com/yourusername/mini-search-engine.git
cd mini-search-engine
