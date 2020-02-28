# Collection for rails dockerfiles

## Todo
- [x] Minimum installation
- [x] Development
- [x] Production

## Note
We don't have a staging dockerfile because it should use the production version

# Minimum installation

## Usage

### Building the image
```
docker build -t docker-create-rails --build-arg USER_ID=$(id -u) --build-arg GROUP_ID=$(id -g) -f Dockerfile.rails .
```

### Creating a new rails app
```
docker run -it -v $PWD:/opt/app docker-create-rails rails new --skip-bundle RAILS_APP_NAME
```
