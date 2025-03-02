---
source: https://www.blackbox.ai/
tags:
  - coding
  - python
  - bookmarks
category: "[[AI Assistant]]"
type:
  - "[[Coding]]"
creation date: "[[../08 Daily Notes/2025-02-25|2025-02-25]]"
---
Certainly! Building a bookmark manager or link scraper in Python can be a fun project. Below, I'll guide you through creating a simple bookmark manager that allows you to save, view, and delete bookmarks. Additionally, I'll show you how to scrape links from a webpage.

### Step 1: Setting Up Your Environment

Make sure you have Python installed on your machine. You can use `pip` to install any necessary libraries. For this project, we will use `requests` for web scraping and `BeautifulSoup` for parsing HTML.

You can install these libraries using:

```bash
pip install requests beautifulsoup4
```

### Step 2: Creating the Bookmark Manager

We'll create a simple command-line interface (CLI) for managing bookmarks. The bookmarks will be stored in a JSON file.

#### Bookmark Manager Code

```python
import json
import os

BOOKMARKS_FILE = 'bookmarks.json'

def load_bookmarks():
    if os.path.exists(BOOKMARKS_FILE):
        with open(BOOKMARKS_FILE, 'r') as f:
            return json.load(f)
    return []

def save_bookmarks(bookmarks):
    with open(BOOKMARKS_FILE, 'w') as f:
        json.dump(bookmarks, f, indent=4)

def add_bookmark(url, title):
    bookmarks = load_bookmarks()
    bookmarks.append({'url': url, 'title': title})
    save_bookmarks(bookmarks)
    print(f'Bookmark added: {title} - {url}')

def view_bookmarks():
    bookmarks = load_bookmarks()
    if not bookmarks:
        print("No bookmarks found.")
        return
    for i, bookmark in enumerate(bookmarks):
        print(f"{i + 1}. {bookmark['title']} - {bookmark['url']}")

def delete_bookmark(index):
    bookmarks = load_bookmarks()
    if 0 <= index < len(bookmarks):
        removed = bookmarks.pop(index)
        save_bookmarks(bookmarks)
        print(f'Removed bookmark: {removed["title"]} - {removed["url"]}')
    else:
        print("Invalid index.")

def main():
    while True:
        print("\nBookmark Manager")
        print("1. Add Bookmark")
        print("2. View Bookmarks")
        print("3. Delete Bookmark")
        print("4. Exit")
        choice = input("Choose an option: ")

        if choice == '1':
            url = input("Enter URL: ")
            title = input("Enter Title: ")
            add_bookmark(url, title)
        elif choice == '2':
            view_bookmarks()
        elif choice == '3':
            index = int(input("Enter bookmark index to delete: ")) - 1
            delete_bookmark(index)
        elif choice == '4':
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
```

### Step 3: Scraping Links from a Webpage

Now, let's create a simple function to scrape links from a given URL.

#### Link Scraper Code

```python
import requests
from bs4 import BeautifulSoup

def scrape_links(url):
    try:
        response = requests.get(url)
        response.raise_for_status()  # Raise an error for bad responses
        soup = BeautifulSoup(response.text, 'html.parser')
        
        links = []
        for a_tag in soup.find_all('a', href=True):
            links.append(a_tag['href'])
        
        return links
    except Exception as e:
        print(f"Error scraping {url}: {e}")
        return []

# Example usage
if __name__ == "__main__":
    url_to_scrape = input("Enter a URL to scrape links from: ")
    links = scrape_links(url_to_scrape)
    print("Links found:")
    for link in links:
        print(link)
```

### Step 4: Integrating the Scraper with the Bookmark Manager

You can integrate the link scraper into the bookmark manager by allowing users to scrape links and add them as bookmarks. You can modify the `main()` function to include an option for scraping links.

### Final Thoughts

This is a basic implementation of a bookmark manager and link scraper. You can expand upon this by adding features like:

- Categorizing bookmarks
- Searching bookmarks
- Exporting bookmarks to HTML
- Adding a GUI using libraries like Tkinter or PyQt

Feel free to ask if you have any questions or need further assistance!

What specific features do you want in your bookmark manager?
Can you clarify the types of links you want to scrape?
What libraries or frameworks are you considering for this project?
How do you plan to store the scraped links and bookmarks?
Are there any performance concerns or limitations you anticipate?
