link download models: https://drive.google.com/file/d/1iSp9li4c2Cw5oMKLE-MO0VFJT5_uIWTP/view?usp=sharing
install library: pip install -r requirements.txt
face detection: python src/align_dataset_mtcnn.py  Dataset/FaceData/raw Dataset/FaceData/processed --image_size 160 --margin 32  --random_order --gpu_memory_fraction 0.25
train model: python src/classifier.py TRAIN Dataset/FaceData/processed Models/20180402-114759.pb Models/facemodel.pkl --batch_size 1000
run: python src/face_rec_cam.py 
