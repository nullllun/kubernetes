package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = ["validation.go"],
    importpath = "k8s.io/kubernetes/plugin/pkg/admission/podtolerationrestriction/apis/podtolerationrestriction/validation",
    deps = [
        "//pkg/api/validation:go_default_library",
        "//plugin/pkg/admission/podtolerationrestriction/apis/podtolerationrestriction:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/validation/field:go_default_library",
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

go_test(
    name = "go_default_test",
    srcs = ["validation_test.go"],
    importpath = "k8s.io/kubernetes/plugin/pkg/admission/podtolerationrestriction/apis/podtolerationrestriction/validation",
    library = ":go_default_library",
    deps = [
        "//pkg/api:go_default_library",
        "//plugin/pkg/admission/podtolerationrestriction/apis/podtolerationrestriction:go_default_library",
    ],
)
