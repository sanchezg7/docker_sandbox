# Start container in detached mode and remove when container is stopped
docker run -p 3000:80 --name feedback-app --rm feedback-node