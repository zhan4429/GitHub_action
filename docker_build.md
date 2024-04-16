```
- name: Docker Build For Testing
  uses: docker/build-push-action@v4
  with: 
    context: . ## The path where the Dockerfile is located
    push: false  ## Wheter to push to Docker hub
    tags: ${{ vars.DOCKERHUB_USERNAME }}/solar-system:${{ github.sha }}

- name: Docker Image Test
  run: |
    docker images
    docker run --name solar-system-app -d \
        -p 3000:3000 \
        $${{ vars.DOCKERHUB_USERNAME }}/solar-system:${{ github.sha }}
```