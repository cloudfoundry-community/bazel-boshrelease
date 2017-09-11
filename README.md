# BOSH release for bazel

I packaged up https://bazel.build/ once, then realized I didn't need it. So I'll put it in its own BOSH release for the next person who wants the `bazel` package.

## Install

```
export BOSH_ENVIRONMENT=<bosh-alias>
export BOSH_DEPLOYMENT=bazel
bosh deploy manifests/bazel.yml
```

## Reuse package

You can copy the package into your own BOSH release:

```
gem install bosh-gen
bosh sync-blobs
cd ../my-boshrelease
bosh-gen extract-pkg ../bazel-boshrelease/packages/bazel
```
