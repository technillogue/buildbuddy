load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "byte_stream_server",
    srcs = ["byte_stream_server.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/remote_cache/byte_stream_server",
    visibility = ["//visibility:public"],
    deps = [
        "//proto:api_key_go_proto",
        "//proto:remote_execution_go_proto",
        "//server/environment",
        "//server/interfaces",
        "//server/remote_cache/digest",
        "//server/remote_cache/hit_tracker",
        "//server/remote_cache/namespace",
        "//server/util/capabilities",
        "//server/util/devnull",
        "//server/util/prefix",
        "//server/util/status",
        "@go_googleapis//google/bytestream:bytestream_go_proto",
    ],
)

go_test(
    name = "byte_stream_server_test",
    size = "small",
    srcs = ["byte_stream_server_test.go"],
    embed = [":byte_stream_server"],
    deps = [
        "//proto:remote_execution_go_proto",
        "//server/remote_cache/digest",
        "//server/testutil/testenv",
        "//server/util/prefix",
        "//server/util/random",
        "@go_googleapis//google/bytestream:bytestream_go_proto",
        "@org_golang_google_grpc//:go_default_library",
        "@org_golang_google_grpc//status",
    ],
)
