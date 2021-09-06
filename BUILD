load("@rules_python//python:defs.bzl", "py_binary")
load("@test//:requirements.bzl", "requirement")

py_binary(
    name = "server",
    srcs = ["server.py"],
    deps = [
        requirement("tensorflow"),
        requirement("tensorflow-io"),
    ],
)
