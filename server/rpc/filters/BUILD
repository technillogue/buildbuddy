load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "filters",
    srcs = ["filters.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/rpc/filters",
    visibility = ["//visibility:public"],
    deps = [
        "//server/environment",
        "//server/util/log",
        "//server/util/uuid",
        "@com_github_grpc_ecosystem_go_grpc_prometheus//:go-grpc-prometheus",
        "@org_golang_google_grpc//:go_default_library",
        "@org_golang_google_grpc//metadata",
    ],
)
