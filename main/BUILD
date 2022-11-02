load("@rules_cc//cc:defs.bzl", "cc_binary", "cc_library")
load("@emsdk//emscripten_toolchain:wasm_rules.bzl", "wasm_cc_binary")

cc_library(
    name = "hello-greet",
    srcs = ["hello-greet.cc"],
    hdrs = ["hello-greet.h"],
    copts = ["-flto"]
)

cc_binary(
    name = "entry-point",
    srcs = ["hello-world.cc"],
    deps = [
        ":hello-greet",
        "//lib:hello-time",
    ],
    linkopts = ["-sWASM=2"],
    copts = ["-flto"]
)

wasm_cc_binary(
    name = "wasm-binary-target",
    cc_target = ":entry-point",
    outputs = [
        "entry-point.js",
        "entry-point.wasm"
    ],
)