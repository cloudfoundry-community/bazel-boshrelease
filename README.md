# BOSH release for bazel

This BOSH release and deployment manifest deploy a cluster of bazel.

## Install

```
export BOSH_ENVIRONMENT=<bosh-alias>
export BOSH_DEPLOYMENT=bazel
bosh deploy manifests/bazel.yml --vars-store tmp/creds.yml
```

If your BOSH has Credhub, then you can omit `--vars-store` flag. It is used to generate any passwords/credentials/certificates required by `manifests/bazel.yml`.


## Development

As a developer of this release, create new releases, upload and deploy them:

```
bosh create-release --force && \
  bosh -n upload-release && \
  bosh deploy manifests/bazel.yml --vars-store tmp/creds.yml
```

If your BOSH has Credhub, then you can omit `--vars-store` flag. It is used to generate any passwords/credentials/certificates required by `manifests/bazel.yml`.
