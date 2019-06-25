load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")


android_sdk_repository(
    name = "androidsdk",
    api_level = 28,
    build_tools_version = "28.0.3"
)


RULES_JVM_EXTERNAL_TAG = "2.0.1"
RULES_JVM_EXTERNAL_SHA = "55e8d3951647ae3dffde22b4f7f8dee11b3f70f3f89424713debd7076197eaca"

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    sha256 = RULES_JVM_EXTERNAL_SHA,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [
        "androidx.appcompat:appcompat:1.0.2",
        "androidx.core:core:1.0.1",
        "androidx.constraintlayout:constraintlayout:1.1.3",
        "androidx.drawerlayout:drawerlayout:1.0.0",
        "androidx.fragment:fragment:1.0.0",
        "com.google.android.material:material:1.0.0",
    ],
    repositories = [
        "https://jcenter.bintray.com/",
        "https://maven.google.com",
        "https://repo1.maven.org/maven2",
    ],
    fetch_sources = True,
)