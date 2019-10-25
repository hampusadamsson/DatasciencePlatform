1) Anslut till notebook-containern.
docker exec -it trackingserver_notebook_1 bash

2) Kör igång modellen
mlflow models serve -m /artifacts/1/dae71823c5bc4a71ad8e60c877dc25a5/artifacts/model/ -p 5000 -h 0.0.0.0

