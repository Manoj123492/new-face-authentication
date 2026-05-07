TASK - 1
Amazon Product Scraper (Python)

1. Overview

This project is a simple Amazon product scraper built using Python, Requests, and BeautifulSoup.

The script takes a product name as input, searches it on Amazon India, and extracts product details such as:

- Title
- Price
- Rating
- Image URL
- Ad/Organic status

The scraped data is saved into a CSV file with a timestamp.

2.Features

- Dynamic product search (user input)
- Scrapes multiple pages
- Extracts important product details
- Saves data into CSV format
- Basic error handling included

3. Technologies Used

- Python
- Requests
- BeautifulSoup
- CSV module
- Datetime module


TASK - 2 
Face Authentication (Face Verification)

1.Overview:
This project is a simple Face Authentication system developed using Python and FastAPI.  
The purpose of this project is to verify whether two face images belong to the same person or not.
The system detects faces from the uploaded images, extracts face embeddings using a pretrained InsightFace model, and compares them using cosine similarity.

2.Features:
- Upload two face images
- Detect faces automatically
- Extract face embeddings
- Compare similarity between faces
- Return similarity score and verification result
- FastAPI API implementation

3.Technologies Used
- Python
- FastAPI
- OpenCV
- InsightFace
- NumPy
- Scikit-learn

4.Project Structure
face-auth/

train.py
test.py
app.py
requirements.txt
README.md

5. Installation

Create virtual environment:
python -m venv venv

Activate environment:

Windows
venv\Scripts\activate


Linux / Mac
bash
source venv/bin/activate

Install required packages:
pip install -r requirements.txt

6.Running the Application

Start FastAPI server:
uvicorn app:app --reload

Open browser and go to:

You can test the API directly from the Swagger UI.



7. API Endpoint

POST /verify/

Upload two face images and the API returns:

- Verification result
- Similarity score
- Bounding boxes of detected faces

---

8. Example Response

```json
{
  "verification_result": "same person",
  "similarity_score": 0.81,
  "face1_bbox": [120, 80, 300, 350],
  "face2_bbox": [100, 60, 280, 330]
}
```

---

9. How It Works

1. Face detection is performed on both images
2. Face embeddings are extracted using InsightFace
3. Cosine similarity is calculated between embeddings
4. Based on the similarity score, the system decides whether both faces belong to the same person

---


Notes

- Only the first detected face is used
- Similarity threshold is set to `0.5`
- Works on CPU

---

10. requirements.txt


fastapi
uvicorn
opencv-python
numpy
scikit-learn
insightface
python-multipart
onnxruntime




11. Future Improvements

- Multi-face support
- Face alignment
- Liveness detection
- Database integration
- GPU optimization



