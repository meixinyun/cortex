load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "digest.go",
        "digester.go",
        "doc.go",
        "set.go",
        "verifiers.go",
    ],
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = [
        "digest_test.go",
        "digester_resumable_test.go",
        "set_test.go",
        "verifiers_test.go",
    ],
    library = ":go_default_library",
    deps = [
        "//vendor/github.com/stevvooe/resumable:go_default_library",
        "//vendor/github.com/stevvooe/resumable/sha256:go_default_library",
    ],
)
