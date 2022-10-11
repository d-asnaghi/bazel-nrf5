# WORKSPACE
workspace(name = "nRF5")

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

#---------------------------------------------------------------------
# nRF SDK
#---------------------------------------------------------------------
load("@nRF5//:deps.bzl", "nRF5_deps")

nRF5_deps()
#---------------------------------------------------------------------
# ARM none eabi GCC
#---------------------------------------------------------------------
git_repository(
    name = "arm_none_eabi",
    commit = "2c681610589b7b6b54691ed5873176fea903b38a",
    remote = "https://github.com/hexdae/bazel-arm-none-eabi",
    shallow_since = "1665467736 -0700",
)

load("@arm_none_eabi//:deps.bzl", "arm_none_eabi_deps")

arm_none_eabi_deps()
#---------------------------------------------------------------------