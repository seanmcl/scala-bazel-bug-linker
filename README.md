Demonstrates bug in scala-bazel rules.  They don't set
java.library.path correctly from cc_library deps.


    $ bazel run src:java
    INFO: Found 1 target...
    Target //src:java up-to-date:
      bazel-bin/src/java.jar
      bazel-bin/src/java
    INFO: Elapsed time: 0.285s, Critical Path: 0.12s

    INFO: Running command line: bazel-bin/src/java
    java.library.path property: /private/var/tmp/_bazel_seanmcl/245e420e52697013918f782fd5b4af8b/execroot/scala-bazel-bug-linker/bazel-out/local-fastbuild/bin/src/java.runfiles/tiros/_solib_darwin/_U_S_Slib_Cnative___Ulib
    ~/save/src/scala-bazel-bug-linker ‹master*›  [2017-02-09 21:37:35]
    [0]$ bazel run src:scala
    INFO: Found 1 target...
    Target //src:scala up-to-date:
      bazel-bin/src/scala
    INFO: Elapsed time: 0.202s, Critical Path: 0.00s

    INFO: Running command line: bazel-bin/src/scala
    java.library.path property: /Users/seanmcl/Library/Java/Extensions:/Library/Java/Extensions:/Network/Library/Java/Extensions:/System/Library/Java/Extensions:/usr/lib/java:.
