load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "aspect_rules_js",
    sha256 = "538049993bec3ee1ae9b1c3cd669156bca04eb67027b222883e47b0a2aed2e67",
    strip_prefix = "rules_js-1.0.0",
    url = "https://github.com/aspect-build/rules_js/archive/refs/tags/v1.0.0.tar.gz",
)

load("@aspect_rules_js//js:repositories.bzl", "rules_js_dependencies")

rules_js_dependencies()

load("@rules_nodejs//nodejs:repositories.bzl", "DEFAULT_NODE_VERSION", "nodejs_register_toolchains")

nodejs_register_toolchains(
    name = "nodejs",
    node_version = DEFAULT_NODE_VERSION,
)

load("@aspect_rules_js//npm:npm_import.bzl", "npm_translate_lock")

#npm_translate_lock(
#    name = "npm",
#    pnpm_lock = "//:pnpm-lock.yaml",
#    verify_node_modules_ignored = "//:.bazelignore",
#)
#
#load("@npm//:repositories.bzl", "npm_repositories")
#
#npm_repositories()
