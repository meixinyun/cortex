load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["jwt.go"],
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/golang.org/x/net/context:go_default_library",
        "//vendor/golang.org/x/oauth2:go_default_library",
        "//vendor/golang.org/x/oauth2/internal:go_default_library",
        "//vendor/golang.org/x/oauth2/jws:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["jwt_test.go"],
    library = ":go_default_library",
    deps = ["//vendor/golang.org/x/oauth2/jws:go_default_library"],
)

go_test(
    name = "go_default_xtest",
    srcs = ["example_test.go"],
    deps = ["//vendor/golang.org/x/oauth2/jwt:go_default_library"],
)
