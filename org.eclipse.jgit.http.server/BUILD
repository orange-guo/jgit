load("@rules_java//java:defs.bzl", "java_library")

package(default_visibility = ["//visibility:public"])

filegroup(
    name = "jgit-servlet-resources",
    srcs = glob(["resources/**"]),
)

java_library(
    name = "jgit-servlet",
    srcs = glob(["src/**/*.java"]),
    resource_strip_prefix = "org.eclipse.jgit.http.server/resources",
    resources = [":jgit-servlet-resources"],
    deps = [
        "//lib:servlet-api",
        # We want these deps to be provided_deps
        "//org.eclipse.jgit:jgit",
    ],
)
