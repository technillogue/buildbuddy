load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "interfaces",
    srcs = ["interfaces.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/interfaces",
    visibility = ["//visibility:public"],
    deps = [
        "//proto:acl_go_proto",
        "//proto:api_key_go_proto",
        "//proto:execution_stats_go_proto",
        "//proto:group_go_proto",
        "//proto:invocation_go_proto",
        "//proto:publish_build_event_go_proto",
        "//proto:remote_execution_go_proto",
        "//proto:scheduler_go_proto",
        "//proto:telemetry_go_proto",
        "//proto:workflow_go_proto",
        "//proto/api/v1:api_v1_go_proto",
        "//server/tables",
    ],
)
