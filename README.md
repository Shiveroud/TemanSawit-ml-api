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
    
