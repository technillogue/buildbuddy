load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "build_event_handler",
    srcs = ["build_event_handler.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/build_event_protocol/build_event_handler",
    visibility = ["//visibility:public"],
    deps = [
        "//proto:build_event_stream_go_proto",
        "//proto:build_events_go_proto",
        "//proto:cache_go_proto",
        "//proto:invocation_go_proto",
        "//proto:publish_build_event_go_proto",
        "//proto:user_id_go_proto",
        "//server/build_event_protocol/accumulator",
        "//server/build_event_protocol/build_status_reporter",
        "//server/build_event_protocol/event_parser",
        "//server/build_event_protocol/target_tracker",
        "//server/environment",
        "//server/interfaces",
        "//server/metrics",
        "//server/remote_cache/hit_tracker",
        "//server/tables",
        "//server/util/log",
        "//server/util/perms",
        "//server/util/protofile",
        "//server/util/status",
        "@com_github_golang_protobuf//proto:go_default_library",
        "@com_github_golang_protobuf//ptypes:go_default_library_gen",
        "@com_github_prometheus_client_golang//prometheus",
        "@org_golang_google_grpc//status",
    ],
)

go_test(
    name = "build_event_handler_test",
    srcs = ["build_event_handler_test.go"],
    deps = [
        ":build_event_handler",
        "//proto:build_event_stream_go_proto",
        "//proto:build_events_go_proto",
        "//proto:invocation_go_proto",
        "//proto:publish_build_event_go_proto",
        "//server/testutil/testauth",
        "//server/testutil/testenv",
        "@com_github_stretchr_testify//assert",
        "@io_bazel_rules_go//proto/wkt:any_go_proto",
    ],
)
