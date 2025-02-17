# Smart ATS

Smart ATS is a Streamlit application designed to enhance and evaluate resumes against job descriptions using Google Generative AI's Gemini model. The application acts as an advanced ATS (Applicant Tracking System), providing feedback on the resume, including a percentage match with the job description, missing keywords, and profile summaries. It helps users improve their resumes to align better with the job market requirements.

## Features
- Upload resumes in PDF format.
- Paste job descriptions for analysis.
- Uses Google Generative AI (Gemini model) to evaluate resumes.
- Outputs a JSON response containing:
  - Percentage Match with the job description.
  - Missing Keywords.
  - Profile Summary.
- User-friendly interface built with Streamlit.

## How It Works
1. **Job Description Input**: Users paste the job description into a text area.
2. **Resume Upload**: Users upload their resume in PDF format.
3. **AI Evaluation**: The application extracts the text from the uploaded PDF, formats the input for the AI model, and sends it to the Gemini API.
4. **Response Parsing**: The AI evaluates the resume against the job description and returns a JSON response with a percentage match, missing keywords, and a profile summary.
5. **Output**: Results are displayed on the Streamlit interface.

## Installation
Follow these steps to set up and run the project on your local machine:

### Prerequisites
- Python 3.7 or higher
- Streamlit
- PyPDF2
- google-generativeai
- python-dotenv

### Installation Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/smart-ats.git
   cd smart-ats
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up your environment variables:
   - Create a `.env` file in the root directory of the project.
   - Add your Google Generative AI API key to the `.env` file:
     ```
     GOOGLE_API_KEY=your-google-api-key
     ```

5. Run the application:
   ```bash
   streamlit run app.py
   ```

6. Open your web browser and navigate to `http://localhost:8501` to use the app.

## Usage
1. Paste the job description into the provided text area.
2. Upload your resume in PDF format.
3. Click the "Submit" button to analyze your resume.
4. View the results, including:
   - Missing Keywords.
   - Profile Summary.
   - Percentage Match.

## Project Structure
```
smart-ats/
├── app.py             # Main application file
├── requirements.txt   # Python dependencies
├── .env               # Environment variables (ignored by Git)
├── README.md          # Project documentation
```

## Dependencies
- **Streamlit**: For creating the web interface.
- **PyPDF2**: For extracting text from uploaded PDF resumes.
- **google-generativeai**: For interacting with Google Generative AI's Gemini model.
- **python-dotenv**: For managing environment variables.

## Example Output
**Input:**
- Job Description: "Data Scientist with experience in Python, Machine Learning, and Big Data."
- Resume: PDF with relevant skills and experience.

**Output:**
- Percentage Match: 85%
- Missing Keywords: ["Big Data"]
- Profile Summary: "Python, Machine Learning, Data Analysis, Statistics"

## Contributing
Feel free to open issues or submit pull requests for feature enhancements or bug fixes. Contributions are welcome!

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements
- Google Generative AI for providing the Gemini model.
- Streamlit for its seamless UI development.
- PyPDF2 for PDF text extraction.

---

Start optimizing your resume today with Smart ATS!
