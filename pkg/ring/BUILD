load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "consul_client.go",
        "consul_client_mock.go",
        "http.go",
        "model.go",
        "ring.go",
        "ring.pb.go",
        "util.go",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/gogo/protobuf/proto:go_default_library",
        "//vendor/github.com/gogo/protobuf/sortkeys:go_default_library",
        "//vendor/github.com/golang/protobuf/proto:go_default_library",
        "//vendor/github.com/golang/snappy:go_default_library",
        "//vendor/github.com/hashicorp/consul/api:go_default_library",
        "//vendor/github.com/hashicorp/go-cleanhttp:go_default_library",
        "//vendor/github.com/prometheus/client_golang/prometheus:go_default_library",
        "//vendor/github.com/prometheus/common/log:go_default_library",
    ],
)

filegroup(
    name = "go_default_library_protos",
    srcs = ["ring.proto"],
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["ring_test.go"],
    library = ":go_default_library",
)
