This directory contains a Jenkinsfile which can be used to build
kylie-nodejs using an OpenShift build pipeline.

To do this, run:

```bash
# create the nodejs example as usual
oc new-app https://github.com/monodot/kylie-nodejs

# now create the pipeline build controller from the openshift/pipeline
# subdirectory
oc new-app https://github.com/monodot/kylie-nodejs \
  --context-dir=openshift/pipeline --name kylie-pipeline
```
