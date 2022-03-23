load("@rules_proto_grpc//go:defs.bzl", "go_grpc_library", "go_proto_compile")

go_grpc_library(
    name = "greeter_go_grpc",
    importpath = "github.com/seven4x/bazel-grpc-demo-using-rules_proto_grpc/example/go/proto",
    protos = [
        "@rules_proto_grpc//example/proto:greeter_grpc",
        "@rules_proto_grpc//example/proto:thing_proto",
    ],
)
