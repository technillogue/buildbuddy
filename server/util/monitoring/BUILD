load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "monitoring",
    srcs = ["monitoring.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/util/monitoring",
    visibility = ["//visibility:public"],
    deps = [
        "//server/util/log",
        "@com_github_prometheus_client_golang//prometheus/promhttp",
    ],
)
