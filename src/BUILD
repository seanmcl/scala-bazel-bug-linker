load("@io_bazel_rules_scala//scala:scala.bzl", "scala_library", "scala_binary", "scala_test")

scala_binary(
    name = "scala",
    srcs = ["Foo.scala"],
    main_class = "Foo",
    deps = [
        "//lib:native",
    ],
    visibility = ["//visibility:public"],
)

java_binary(
    name = "java",
    srcs = ["Foo.java"],
    main_class = "Foo",
    deps = [
        "//lib:native",
    ]
)
