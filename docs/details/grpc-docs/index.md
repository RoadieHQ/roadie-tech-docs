humanName: grpc-docs
integrationType: OSS plugin
---

# Introduction

If your organization uses gRPC, you might be familiar with the [protoc-gen-doc](https://github.com/pseudomuto/protoc-gen-doc) plugin. Roadie can render your `protoc-gen-doc` generated JSON files to give a better viewing experience for your API definition page.

## Steps

To enable gRPC API docs, configure your API entity files with a `type: grpc-docs` and point your `spec.definition` to the generated `protoc-gen-doc json` file. Roadie will automatically pick up and render your API definition page.

Below is an example entity configuration for gRPC API docs.

```yaml
apiVersion: backstage.io/v1alpha1
kind: API
metadata:
  name: unquie-api-1
spec:
  type: grpc-docs
  lifecycle: production
  owner: group:engineering
  definition:
    $text: https://github.com/org/repo/blob/main/grpc-docs/example.json
```
