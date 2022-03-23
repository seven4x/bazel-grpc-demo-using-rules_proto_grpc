load("@rules_proto_grpc//java:defs.bzl", "java_grpc_library", "java_proto_compile")

java_grpc_library(
    name = "thing_java_grpc",
    protos = ["@rules_proto_grpc//example/proto:thing_proto"],
    visibility = ["//visibility:public"],
)

java_grpc_library(
    name = "greeter_java_grpc",
    protos = ["@rules_proto_grpc//example/proto:greeter_grpc"],
    visibility = ["//visibility:public"],
    deps = ["thing_java_grpc"],
)

java_binary(
    name = "server",
    srcs = ["server/GreetingServer.java"],
    main_class = "example.app.java.server.GreetingServer",
    deps = [
        "greeter_java_grpc",
        "thing_java_grpc",
    ],
)
