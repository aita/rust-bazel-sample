load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_rust",
    sha256 = "0cc7e6b39e492710b819e00d48f2210ae626b717a3ab96e048c43ab57e61d204",
    urls = [
        "https://github.com/bazelbuild/rules_rust/releases/download/0.10.0/rules_rust-v0.10.0.tar.gz",
        "https://mirror.bazel.build/github.com/bazelbuild/rules_rust/releases/download/0.10.0/rules_rust-v0.10.0.tar.gz",
    ],
)

load("@rules_rust//rust:repositories.bzl", "rules_rust_dependencies", "rust_register_toolchains", "rust_repository_set")

rules_rust_dependencies()

rust_register_toolchains(
    edition = "2021",
    extra_target_triples = [
        "aarch64-unknown-linux-gnu",
        "x86_64-apple-darwin",
    ],
)
# rust_repository_set(
#     name = "rust_linux_aarch64",
#     edition = "2021",
#     exec_triple = "aarch64-unknown-linux-gnu",
#     extra_target_triples = [],
#     register_toolchain = True,
#     version = "1.64.0",
# )
