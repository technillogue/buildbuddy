load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "memcache",
    srcs = ["memcache.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/enterprise/server/backends/memcache",
    visibility = [
        "//enterprise:__subpackages__",
        "@buildbuddy_internal//enterprise:__subpackages__",
    ],
    deps = [
        "//proto:remote_execution_go_proto",
        "//server/interfaces",
        "//server/remote_cache/digest",
        "//server/util/prefix",
        "//server/util/status",
        "@com_github_bradfitz_gomemcache//memcache",
        "@org_golang_x_sync//errgroup",
    ],
)
