load("@rules_cc//cc:defs.bzl", "cc_binary", "cc_library")
load("@emsdk//emscripten_toolchain:wasm_rules.bzl", "wasm_cc_binary")

cc_library(
    name = "hello-greet",
    srcs = ["hello-greet.cc"],
    hdrs = ["hello-greet.h"],
)

cc_binary(
    name = "main",
    srcs = ["hello-world.cc"],
    deps = [
        ":hello-greet",
    ],
)

wasm_cc_binary(
    name = "main-wasm",
    cc_target = ":main",
)