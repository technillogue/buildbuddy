load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "content_addressable_storage_server",
    srcs = ["content_addressable_storage_server.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/remote_cache/content_addressable_storage_server",
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
        "//server/util/log",
        "//server/util/prefix",
        "//server/util/status",
        "@com_github_golang_protobuf//proto:go_default_library",
        "@go_googleapis//google/rpc:status_go_proto",
        "@org_golang_google_grpc//codes",
        "@org_golang_x_sync//errgroup",
    ],
)

go_test(
    name = "content_addressable_storage_server_test",
    srcs = ["content_addressable_storage_server_test.go"],
    deps = [
        ":content_addressable_storage_server",
        "//proto:remote_execution_go_proto",
        "//server/backends/memory_cache",
        "//server/interfaces",
        "//server/testutil/testdigest",
        "//server/testutil/testenv",
        "//server/util/prefix",
        "@com_github_stretchr_testify//assert",
        "@org_golang_google_grpc//:go_default_library",
        "@org_golang_google_grpc//codes",
    ],
)
