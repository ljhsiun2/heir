package(
    default_applicable_licenses = ["@heir//:license"],
    default_visibility = ["//visibility:public"],
)

cc_library(
    name = "Transforms",
    hdrs = [
        "@heir//include/Dialect/Secret/Transforms:Passes.h",
    ],
    deps = [
        ":ForgetSecrets",
        "@heir//include/Dialect/Secret/Transforms:pass_inc_gen",
        "@heir//lib/Dialect/Secret/IR:Dialect",
        "@llvm-project//mlir:IR",
    ],
)

cc_library(
    name = "ForgetSecrets",
    srcs = ["ForgetSecrets.cpp"],
    hdrs = [
        "@heir//include/Dialect/Secret/Transforms:ForgetSecrets.h",
    ],
    includes = ["@heir//include"],
    deps = [
        "@heir//include/Dialect/Secret/Transforms:pass_inc_gen",
        "@heir//lib/Dialect/Secret/IR:Dialect",
        "@heir//lib/Dialect/Secret/IR:SecretOps",
        "@llvm-project//mlir:FuncDialect",
        "@llvm-project//mlir:FuncTransforms",
        "@llvm-project//mlir:IR",
        "@llvm-project//mlir:Pass",
        "@llvm-project//mlir:Transforms",
    ],
)
