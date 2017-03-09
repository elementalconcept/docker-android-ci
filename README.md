# elementalconcept/android-ci

This is an example of how to embed Android project dependencies into the docker image
for faster CI times. *Cacher* project inside *assets* folder will install its dependecies
together with all Android SDK related stuff during `docker build` and will cache them
inside the image. To start using it:

1. Make sure you are familiar with Docker.
2. CLone elementalconcept/android-ci repo.
3. Update dependencies to your needs in *assets/cacher/app/build.gradle*.
4. Build your own image `$ docker build -t TAG_NAME .`.
5. Push the image to the docker hub or use internally.

This image is using [r0adkll/android-ci](https://github.com/r0adkll/android-ci)
as a base, feel free to change it to suit your needs.
