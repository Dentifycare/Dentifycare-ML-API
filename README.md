# DentifyCare ML API
DentifyCare is a FastAPI-based API used to diagnose dental diseases based on uploaded images. This API uses a machine learning model trained to detect several categories of dental diseases.

## API URL

- **Base URL**: (https://dentifycare-ml-api-363002036886.asia-southeast2.run.app


## Endpoints

### 1. `/` - Root Endpoint

**Method**: `GET`

This endpoint will return a message indicating that the API is running properly.

**Response**:
```json
    {
    "message": "DENTIFYCARE"
    }
```
---
### 2. `/`predict - Dental Disease Prediction
Method: POST

This endpoint receives image files from the user, processes the images, and returns a diagnosis of the dental disease along with its accuracy level.

Input:

file (type: multipart/form-data): The image to be predicted.
Response:
```json
{
  "Diagnosis": "calculus",
  "Accuracy": "85.62%"
}
```
If an error occurs in processing the image or prediction, the response will return an error message:
```json
{
  "error": "Error description here"
}
```
---
## Tools
1. **FastAPI**               : A framework for building web applications with Python.
2. **Uvicorn**               : An ASGI server for running FastAPI applications.
3. **TensorFlowPP**          : A machine learning library for loading and consuming models.
4. **Pillow**                :A library for manipulating images.
5. **NumPy**                 : A library for manipulating numeric arrays.
6. **Google Cloud Storage**  : Used to download models stored in cloud storage.

---

## Instalasi
1. Clone repositori:
```bash
git clone <repository_url>
cd dentifycare-ml-api
```
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Run the application: To run the application, you can use uvicorn:
```bash
uvicorn main:app --host 0.0.0.0 --port 8080
```
The application is now accessible via 

---

## Model
The model used by this API is a machine learning model trained to detect various dental diseases. This model is stored in Google Cloud Storage with the file name modeldentifycare.keras.

This model can be downloaded to the server when the application starts, so it does not need to be called manually.

---

## Docker
To run an application using Docker, you can build and run a container with the following command:

1. Build Docker image:
```bash
docker build -t dentifycare-ml-api .
```
2. Run the Docker container:
```bash
docker run -d -p 8080:8080 dentifycare-ml-api
```
The application is now accessible via 

---

## Link Model

The models used in this API can be downloaded via Google Drive:

[Download modeldentifycare.keras](https://drive.google.com/file/d/1-39RTzx1TgT9jJWFaKJOUL6rpVQWg8dD/view?usp=drive_link)







