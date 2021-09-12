load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
http_archive(
    name = "rules_python",
    url = "https://github.com/bazelbuild/rules_python/releases/download/0.3.0/rules_python-0.3.0.tar.gz",
    sha256 = "934c9ceb552e84577b0faf1e5a2f0450314985b4d8712b2b70717dc679fdc01b",
)

load("@rules_python//python:pip.bzl", "pip_install")

pip_install(
   name = "test",
   requirements = "//:requirements.txt",
    python_interpreter_target = "@python_interpreter//:python/install/bin/python3.8"
)

load("//tools/build/bazel/py_toolchain:py_interpreter.bzl", "python_build_standalone_interpreter")

python_build_standalone_interpreter(
    name = "python_interpreter",
)

register_toolchains("//tools/build/bazel/py_toolchain:py_toolchain")
