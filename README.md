# Go Web Application

This is a simple website written in Golang. It uses the `net/http` package to serve HTTP requests.

## Running the server

To run the server, execute the following command:

```bash
go run main.go
```

The server will start on port 9000. You can access it by navigating to `http://localhost:9000/courses` in your web browser.

#containerize application and deploy it to EKS using helm
docker build -t anithapatcha/go-web-app:latest .
docker run -it -p 9000:9000 anithapatcha/go-web-app:latest
docker push anithapatcha/go-web-app
helm folder -- create helm chart
helm create go-web-app-chart
Chart.yaml - metadata of chart
templates - add deployment.yaml and svc.yaml
values.yaml - update tag and any other required info. we can pass these values as arguments in templates
helm install go-web-app ./go-web-app-chart

