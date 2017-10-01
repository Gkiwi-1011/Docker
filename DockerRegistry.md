### Docker Registry
- Centrally manage docker images.

##### `docker tag web-image localhost:5000/web-image`
- Set tag name to upload web-image.

##### `docker push localhost:5000/web-image`
- Upload web-image to docker registry.

##### `docker pull localhost:5000/web-image`
- Download web-image from docker registry.

##### Using S3
- `docker run -d --name registry -p 5000:5000 -e REGISTRY_STORAGE=S3 .... -e REGISTRY_ROOTDIRECTRY=/BUCKET_NAME registry:2.0`
- `docker push localhost:5000/web-image`
- `docker pull localhost:5000/web-image`

