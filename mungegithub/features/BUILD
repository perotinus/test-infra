package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["repo-updates_test.go"],
    library = ":go_default_library",
    deps = [
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/github.com/google/go-github/github:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/util/sets:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = [
        "branch-protection.go",
        "features.go",
        "repo-updates.go",
        "server.go",
    ],
    deps = [
        "//mungegithub/github:go_default_library",
        "//mungegithub/mungeopts:go_default_library",
        "//mungegithub/options:go_default_library",
        "//mungegithub/sharedmux:go_default_library",
        "//vendor/github.com/NYTimes/gziphandler:go_default_library",
        "//vendor/github.com/ghodss/yaml:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/github.com/prometheus/client_golang/prometheus:go_default_library",
        "//vendor/github.com/prometheus/client_golang/prometheus/promhttp:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/util/sets:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/util/yaml:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
