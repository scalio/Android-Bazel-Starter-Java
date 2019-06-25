load("@rules_jvm_external//:defs.bzl", "artifact")

android_library(
    name = "main_activity",
    srcs = [
        "java/io/scal/bazel/MainActivity.java",
    ],
    custom_package = "io.scal.bazel",
    manifest = "AndroidManifest.xml",
    resource_files = glob(["res/**"]),
    deps = [
        artifact("androidx.appcompat:appcompat"),
        artifact("androidx.constraintlayout:constraintlayout"),
        artifact("androidx.core:core"),
        artifact("androidx.drawerlayout:drawerlayout"),
        artifact("androidx.fragment:fragment"),
        artifact("com.google.android.material:material"),
    ],
)

android_binary(
    name = "bazel",
    manifest = "AndroidManifest.xml",
    manifest_values = {
        "minSdkVersion": "21",
        "versionCode" : "2",
        "versionName" : "0.2",
        "targetSdkVersion": "28",
    },
    srcs = glob(["java/**"]),
    resource_files = glob(["res/**"]),
    deps = [
        "main_activity",
        artifact("androidx.appcompat:appcompat"),
        artifact("androidx.constraintlayout:constraintlayout"),
        artifact("androidx.core:core"),
        artifact("androidx.drawerlayout:drawerlayout"),
        artifact("androidx.fragment:fragment"),
        artifact("com.google.android.material:material"),
    ],
)