#Gitlab CI templates

## Available templates

### `.docker-build.yml`

#### Variables

* IMAGE_HUB
* IMAGE_NAME
* IMAGE_TAG
* SERVICE_TO_BUILD

#### Sample job

```
include:
  - remote: https://raw.githubusercontent.com/jacops/gitlab-ci-templates/master/.docker-build.yml

stages:
  - build

docker:
  extends: .docker-build
  stage: build
  variables:
    SERVICE_TO_BUILD: app
```

