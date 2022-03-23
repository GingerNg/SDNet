
docker run --name sdnet -v /data/ginger/Projects/Learning/SDNet:/data/SDNet -d f962c82b3847

conda create -n sdnet python=3.6

#### download dataset and word-embedding
wget https://nlp.stanford.edu/data/glove.840B.300d.zip
wget http://downloads.cs.stanford.edu/nlp/data/coqa/coqa-train-v1.0.json
wget http://downloads.cs.stanford.edu/nlp/data/coqa/coqa-dev-v1.0.json

#### just run it
python3 main.py train ./coqa/conf

[coqa-dataset](https://stanfordnlp.github.io/coqa/)