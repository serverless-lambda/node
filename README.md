# node
node images for nodejs beautify check, lint, and unit test. Mostly used for serverless projects.

## Usage

Add below steps in CI/CD pipeline, such Circle CI, Drone, Buildkite, bitbucket pipeline, etc.

### js beautify

    - if [ `find . -name "*.js" -exec js-beautify -r {} \; |grep -v unchanged |wc -l` -ne 0 ]; then echo "Some js files need be formatted, run 'js-beautify -r <name>.js' to fix"; exit 1; fi
