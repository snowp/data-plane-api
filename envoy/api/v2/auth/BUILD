load("//bazel:api_build_system.bzl", "api_proto_library", "api_go_proto_library")

licenses(["notice"])  # Apache 2

api_proto_library(
    name = "auth",
    srcs = ["auth.proto"],
    deps = [
        ":cert",
    ],
)

api_go_proto_library(
    name = "auth",
    proto = ":auth",
    deps = [
        ":cert_go_proto",
        "@googleapis//:rpc_status_go_proto",
    ],
)

api_proto_library(
    name = "cert",
    srcs = ["cert.proto"],
    deps = [
        "//envoy/api/v2:base",
        "//envoy/api/v2:config_source",
    ],
)

api_go_proto_library(
    name = "cert",
    proto = ":cert",
    deps = [
        "//envoy/api/v2:base_go_proto",
        "//envoy/api/v2:config_source_go_proto",
    ],
)
