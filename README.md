# Face-recognition

## Prerequisite
- Install dlib, CUDNN and CUDA
- Already have an account on Bing Image Search API 
## How to use

- Download dataset
  
  `mkdir dataset/<name>
 python search_bing_api.py --query "<name>" --output dataset/<name>`

- Encoding dataset

  `python encode_faces.py --dataset dataset --encodings encodings.pickle`

- Recognize face in images:

  `python recognize_faces_image.py --encodings encodings.pickle  --image <image-location>`

- Recognize face in video file:

  `python recognize_faces_video_file.py --encodings encodings.pickle 	--input <input-video> --output <output-location> --display 0`

- Recognize face in video stream:
  `python recognize_faces_video.py --encodings encodings.pickle  --output <output-location> --display 1`
