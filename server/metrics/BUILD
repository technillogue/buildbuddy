load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "metrics",
    srcs = ["metrics.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/metrics",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_prometheus_client_golang//prometheus",
        "@com_github_prometheus_client_golang//prometheus/promauto",
    ],
)
