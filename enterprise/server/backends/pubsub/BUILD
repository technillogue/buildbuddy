load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "pubsub",
    srcs = ["pubsub.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/enterprise/server/backends/pubsub",
    visibility = [
        "//enterprise:__subpackages__",
        "@buildbuddy_internal//enterprise:__subpackages__",
    ],
    deps = [
        "//server/interfaces",
        "@com_github_go_redis_redis_v8//:redis",
    ],
)
