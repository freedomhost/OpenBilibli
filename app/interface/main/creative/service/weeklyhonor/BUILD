package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_test",
    "go_library",
)

go_test(
    name = "go_default_test",
    srcs = ["service_test.go"],
    embed = [":go_default_library"],
    tags = ["automanaged"],
    deps = [
        "//app/interface/main/creative/conf:go_default_library",
        "//app/interface/main/creative/dao/up:go_default_library",
        "//app/interface/main/creative/dao/weeklyhonor:go_default_library",
        "//app/interface/main/creative/model/weeklyhonor:go_default_library",
        "//app/interface/main/creative/service:go_default_library",
        "//app/service/main/up/model:go_default_library",
        "//library/time:go_default_library",
        "//vendor/github.com/bouk/monkey:go_default_library",
        "//vendor/github.com/smartystreets/goconvey/convey:go_default_library",
    ],
)

go_library(
    name = "go_default_library",
    srcs = ["service.go"],
    importpath = "go-common/app/interface/main/creative/service/weeklyhonor",
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
    deps = [
        "//app/interface/main/creative/conf:go_default_library",
        "//app/interface/main/creative/dao/account:go_default_library",
        "//app/interface/main/creative/dao/archive:go_default_library",
        "//app/interface/main/creative/dao/up:go_default_library",
        "//app/interface/main/creative/dao/weeklyhonor:go_default_library",
        "//app/interface/main/creative/model/weeklyhonor:go_default_library",
        "//app/interface/main/creative/service:go_default_library",
        "//app/service/main/account/model:go_default_library",
        "//app/service/main/archive/api:go_default_library",
        "//app/service/main/up/model:go_default_library",
        "//library/cache/memcache:go_default_library",
        "//library/ecode:go_default_library",
        "//library/log:go_default_library",
        "//library/sync/errgroup:go_default_library",
        "//library/sync/pipeline/fanout:go_default_library",
        "//library/time:go_default_library",
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
    visibility = ["//visibility:public"],
)
