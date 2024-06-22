import requests
from bs4 import BeautifulSoup

def get_paragraphs_with_word(url, word):
    # Send a GET request to the webpage
    response = requests.get(url)
    if response.status_code != 200:
        return f"Failed to retrieve the webpage. Status code: {response.status_code}"

    # Parse the webpage content
    soup = BeautifulSoup(response.content, 'html.parser')

    # Find all paragraphs containing the specific word
    paragraphs = []
    for p in soup.find_all('p'):
        if word.lower() in p.get_text().lower():
            paragraphs.append(p.get_text())

    return paragraphs

# Example usage with a fixed news site URL
news_url = 'https://www.yna.co.kr'  # Replace with your desired news site URL
specific_word = input("Enter the specific word to search for: ")

# Scrape the webpage for paragraphs containing the specific word
paragraphs_with_word = get_paragraphs_with_word(news_url, specific_word)

# Display the results
if paragraphs_with_word:
    for idx, paragraph in enumerate(paragraphs_with_word, 1):
        print(f"{idx}. {paragraph}\n")
else:
    print(f"No paragraphs found containing the word '{specific_word}'.")
