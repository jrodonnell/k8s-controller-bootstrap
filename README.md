# k8s-controller-bootstrap
A repository to help start writing a new k8s controller using code generators from [k8s.io/code-generator](k8s.io/code-generator) in as few steps as possible.

## Initialization Process
1. Determine the Group Name for your new API and set it in a few places:
    * Rename the `pkg/apis/GROUP_NAME` folder to match.
    * Set the `GROUP_NAME` variable in `hack/update-codegen.sh`
2. Determine the name for your new module and set the `MODULE` variable in `hack/update-codegen.sh`
3. Run `go mod init <MODULE>`
4. Define your types in `pkg/apis/GROUP_NAME/v1alpha1/types.go`
5. Run `./hack/update-codegen.sh`