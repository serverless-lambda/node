# node
node images for nodejs beautify check, lint, and unit test (mocha). Mostly used for serverless projects.

If you need add more common packages for serverless project, raise PR.

## Usage

New generation CI/CD pipeline can use docker image to run the build and deploy commands, this image is mostly used for this purpose.

### js beautify

Add below steps in CI/CD pipeline, such Circle CI, Drone, Buildkite, bitbucket pipeline, etc.

    - if [ `find . -name "*.js" -exec js-beautify -r {} \; |grep -v unchanged |wc -l` -ne 0 ]; then echo "Some js files need be formatted, run 'js-beautify -r <name>.js' to fix"; exit 1; fi
