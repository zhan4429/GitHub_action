```
- name: Docker Push
  uses: docker/build-push-action@v4
  with:
    context: .
    push: true
    tags: ${{ vars.DOCKERHUB_USERNAME }}/solar-system:${{ github.sha }}
```