load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "testauth",
    testonly = 1,
    srcs = ["testauth.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/testutil/testauth",
    visibility = ["//visibility:public"],
    deps = [
        "//proto:api_key_go_proto",
        "//proto:context_go_proto",
        "//proto:user_id_go_proto",
        "//server/interfaces",
        "//server/tables",
        "//server/util/capabilities",
        "//server/util/log",
        "//server/util/status",
        "@com_github_dgrijalva_jwt_go//:jwt-go",
        "@org_golang_google_grpc//metadata",
    ],
)
