load("@io_bazel_rules_go//go:def.bzl", "go_library")

genrule(
    name = "bazel-3.7.0_crossplatform",
    testonly = 1,
    srcs = select({
        "@bazel_tools//src/conditions:darwin": ["@io_bazel_bazel-3.7.0-darwin-x86_64//file:downloaded"],
        "//conditions:default": ["@io_bazel_bazel-3.7.0-linux-x86_64//file:downloaded"],
    }),
    outs = ["bazel-3.7.0"],
    cmd_bash = "cp $(SRCS) $@",
    visibility = ["//visibility:public"],
)

go_library(
    name = "bazel",
    testonly = 1,
    srcs = ["bazel.go"],
    data = [":bazel-3.7.0"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/testutil/bazel",
    visibility = ["//visibility:public"],
    deps = [
        "@io_bazel_rules_go//go/tools/bazel:go_default_library",
    ],
)
