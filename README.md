# TemanSawit-ml-api
## Ripeness Model API

This endpoint provides a function to detect objects in images that relate to the maturity level of oil palm fruits. Users can submit an image to the API, and the API will return the detected objects with a bounding box and the two highest predicted ripeness values from the input palm fruit image. The API uses a pre-trained object detection model for fast and accurate object detection.

**Base URL:**
tbc

**Method:**
>POST

- **Object Detection**
```bash
POST {{Host}}/api/predict
```
- **Body form-data:**

    |      File      |                     Value                     |
    | --------------| ----------------------------------------------|
    | Download sample |https://media.istockphoto.com/id/482549452/id/foto/tandan-buah-kelapa-sawit.jpg?s=1024x1024&w=is&k=20&c=XZCIAFUT81rkLwOmBjFqTZPCNNFUh7S8UTBbYXmrBKU= |
    
**Response:**

```JSON
    {
    "classes": [
        "empty_bunch",
        "overripe",
        "ripe",
        "rotten",
        "underripe",
        "unripe"
    ],
    "prob": [
        6.216210022103041e-05,
        0.025118131190538406,
        0.6271576285362244,
        7.381191971944645e-05,
        0.3363390564918518,
        0.011249292641878128
    ],
    "top_2": {
        "ripe": 0.6271576285362244,
        "underripe": 0.3363390564918518
    }
  }
```

## Step
1. Clone the repository.
```bash
git clone https://github.com/TemanSawit/TemanSawit-ml-api.git
```
2. Install the required dependencies.
```bash
pip install -r requirements.txt
```
3. Navigate to the directory.
4. Run the following command in the directory terminal:
```bash
python .\server.py
```
or
```bash
python3 .\server.py
```
6. After the application startup complete, send a request to ```http://localhost:8080/api/predict``` with a photo of oil palm fruit as an argument called ```file```.
7. The api will returned some datas related to the predictions.
