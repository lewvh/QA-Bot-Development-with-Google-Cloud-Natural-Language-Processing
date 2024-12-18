# QA-Bot-Development-with-Google-Cloud-Natural-Language-Processing

## Project Overview
This chatbot provides a customer support solution for a real estate agency. It is designed to answer frequently asked questions (FAQs) about rental details, sales, and other real estate inquiries. The bot uses Google Cloud Natural Language Processing (NLP) for entity recognition and pandas for processing FAQ data stored in an Excel file.

## Features
- **Automated Responses:** Answers user queries based on a pre-defined FAQ dataset.
- **Entity Recognition:** Utilizes Google Cloud NLP to extract entities from user messages.
- **FAQ Integration:** Matches recognized entities to question IDs in the FAQ dataset.
- **Fallback Mechanism:** Provides default responses when queries cannot be matched.
- **Extensible:** Easy to integrate additional functionality such as buttons, menus, or custom intents.

## Technologies Used
- **Python**
- **pandas**: For processing and querying FAQ data.
- **Google Cloud Natural Language Processing (NLP)**: For extracting entities from user input.
- **Microsoft Bot Framework**: To handle user interactions and implement the chatbot logic.

## Prerequisites
- Python 3.8+
- A Google Cloud Platform (GCP) account with the Natural Language API enabled.
- An Excel file containing the FAQ dataset with the following columns:
  - `Q.ID`: Unique identifiers for questions.
  - `QUESTION`: The question text.
  - `RESPONSE`: The corresponding answer.

## Setup Instructions
### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd real-estate-faq-chatbot
```

### Step 2: Install Dependencies
Install the required Python libraries:
```bash
pip install -r requirements.txt
```

### Step 3: Configure Environment Variables
Create a `.env` file in the project root and define the following variables:
```env
GOOGLE_APPLICATION_CREDENTIALS=<path-to-your-google-cloud-credentials-json>
FILE_PATH=<path-to-your-excel-file>
```

### Step 4: Run the Chatbot
Run the chatbot locally:
```bash
python main.py
```

## File Structure
```
real-estate-faq-chatbot/
|-- main.py                  # Entry point for the chatbot
|-- config.py                # Configuration file for environment variables
|-- bot.py                   # Chatbot logic
|-- requirements.txt         # Python dependencies
|-- README.md                # Project documentation
|-- data/
    |-- faq_data.xlsx        # Example FAQ dataset
```

## Usage
1. Start the bot using the `main.py` script.
2. Interact with the bot by typing questions related to real estate properties.
3. The bot will provide relevant answers based on the FAQ data or fallback if no match is found.

## Example FAQ Dataset
| Q.ID   | QUESTION                | RESPONSE                                |
|--------|-------------------------|-----------------------------------------|
| house1 | "Details about house 1" | "House 1 is available for $1000/month."|
| abuja  | "Properties in Abuja"   | "We have several properties in Abuja." |

## Future Enhancements
- Add a menu or button-based interface for easier navigation.
- Improve fallback responses using additional NLP techniques.
- Integrate multi-language support for wider accessibility.
- Implement custom entity recognition to handle unique real estate terminology.

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature-name`
5. Open a pull request.

## Contact
For any questions or support, please contact:
- **Email:** [lewizhen@gmail.com]
- **GitHub Issues:** Open an issue in this repository.
