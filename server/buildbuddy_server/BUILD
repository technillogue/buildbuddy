load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "buildbuddy_server",
    srcs = ["buildbuddy_server.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/buildbuddy_server",
    visibility = ["//visibility:public"],
    deps = [
        "//proto:api_key_go_proto",
        "//proto:bazel_config_go_proto",
        "//proto:execution_stats_go_proto",
        "//proto:group_go_proto",
        "//proto:invocation_go_proto",
        "//proto:scheduler_go_proto",
        "//proto:target_go_proto",
        "//proto:user_go_proto",
        "//proto:workflow_go_proto",
        "//server/build_event_protocol/build_event_handler",
        "//server/bytestream",
        "//server/environment",
        "//server/ssl",
        "//server/tables",
        "//server/target",
        "//server/util/capabilities",
        "//server/util/log",
        "//server/util/perms",
        "//server/util/request_context",
        "//server/util/status",
        "@com_github_golang_protobuf//proto:go_default_library",
        "@org_golang_google_grpc//codes",
        "@org_golang_google_grpc//status",
    ],
)
