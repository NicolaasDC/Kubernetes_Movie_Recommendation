# IMDB Movie Recommendation with Kubernetes

This is a continuation of the [IMDB Movie recommendation](https://github.com/NicolaasDC/IMDB_Movie_Recommendation) project. This project is deployed locally using kubernetes


## 📦 Repo structure
```
.
├── MovieLens_data/
│   ├── movies.csv
│   └── ratings.csv
├── .gitignore
├── streamlit.py
├── requirements.txt
├── Dockerfile
├── deployment.yaml
├── service.yaml
└── README.md
```

## 🤖 Usage
Have Docker desktop and minikubes running on your local pc.
[Minikube](https://minikube.sigs.k8s.io/docs/start/)
[Docker desktop](https://www.docker.com/products/docker-desktop/)

1. Build and push Docker Image to Docker Hub
```
docker login
```
Enter your Docker Hub username and password
```
docker build -t your_dockerhub_username/movie-recommendation:latest .
docker push your_dockerhub_username/movie-recommendation:latest
```

2. Deploy to Kubernetes
```
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

3. Open the movie recommendation app
```
minikube service movie-recommendation-service
```
This should open the app in your default browser

## 👱 Personal Situation
This project was done as part of the AI Boocamp at BeCode.org.

Connect to me on [LinkedIn](https://www.linkedin.com/in/nicolaas-de-clercq/)


