load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
http_archive(
    name = "emsdk",
    sha256 = "67d68f4ed47aa0b97ab4d40b70a55f068455bb6e5821c6b04c7d6089b6495d20",
    strip_prefix = "emsdk-e41b8c68a248da5f18ebd03bd0420953945d52ff/bazel",
    url = "https://github.com/emscripten-core/emsdk/archive/e41b8c68a248da5f18ebd03bd0420953945d52ff.tar.gz",
)

load("@emsdk//:deps.bzl", emsdk_deps = "deps")
emsdk_deps()

load("@emsdk//:emscripten_deps.bzl", emsdk_emscripten_deps = "emscripten_deps")
emsdk_emscripten_deps(emscripten_version = "3.1.24")