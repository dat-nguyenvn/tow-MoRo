docker build -t moro-flask .

docker run -it --network host --device /dev/video0:/dev/video0 moro-flask

python3 app.py
