load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "blobstore",
    srcs = ["blobstore.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/backends/blobstore",
    visibility = ["//visibility:public"],
    deps = [
        "//server/config",
        "//server/interfaces",
        "//server/metrics",
        "//server/util/disk",
        "//server/util/log",
        "//server/util/status",
        "@com_github_aws_aws_sdk_go//aws",
        "@com_github_aws_aws_sdk_go//aws/awserr",
        "@com_github_aws_aws_sdk_go//aws/credentials",
        "@com_github_aws_aws_sdk_go//aws/session",
        "@com_github_aws_aws_sdk_go//service/s3",
        "@com_github_aws_aws_sdk_go//service/s3/s3manager",
        "@com_github_prometheus_client_golang//prometheus",
        "@com_google_cloud_go_storage//:storage",
        "@org_golang_google_api//option:go_default_library",
        "@org_golang_google_grpc//status",
    ],
)
