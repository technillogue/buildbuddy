load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "grpc_server",
    srcs = ["grpc_server.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/util/grpc_server",
    visibility = ["//visibility:public"],
    deps = [
        "//server/environment",
        "//server/rpc/filters",
        "//server/util/log",
        "@com_github_grpc_ecosystem_go_grpc_prometheus//:go-grpc-prometheus",
        "@org_golang_google_grpc//:go_default_library",
    ],
)
