exports_files(
    glob(["*.bzl"]) + [
        "assets/ghci_script",
        "private/ghci_repl_wrapper.sh",
        "private/haddock_wrapper.sh.tpl",
        "private/coverage_wrapper.sh.tpl",
        "private/osx_cc_wrapper.sh.tpl",
    ],
)

# to make functions visible to unit tests
exports_files(
    ["private/actions/link.bzl"],
    visibility = ["//tests/unit-tests:__pkg__"],
)

# used on Windows to get shorter paths in order to stay under the MAX_PATH
# limit of 260 chars.
exports_files(
    ["private/short_path.bat"],
    visibility = ["//visibility:public"],
)

py_binary(
    name = "ls_modules",
    srcs = ["private/ls_modules.py"],
    visibility = ["//visibility:public"],
)

# toolchains must have a valid toolchain_type from bazel 0.21
toolchain_type(
    name = "toolchain",
    visibility = ["//visibility:public"],
)

toolchain_type(
    name = "doctest-toolchain",
    visibility = ["//visibility:public"],
)
