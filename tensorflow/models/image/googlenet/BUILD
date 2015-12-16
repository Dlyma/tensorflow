# Description:
# Example TensorFlow models for CIFAR-10

licenses(["notice"])  # Apache 2.0

exports_files(["LICENSE"])

py_library(
    name = "googlenet_input",
    srcs = ["googlenet_input.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//tensorflow:tensorflow_py",
    ],
)

py_test(
    name = "googlenet_input_test",
    srcs = ["googlenet_input_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":googlenet_input",
        "//tensorflow:tensorflow_py",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform_test",
    ],
)

py_library(
    name = "googlenet",
    srcs = ["googlenet.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":googlenet_input",
        "//tensorflow:tensorflow_py",
    ],
)

py_binary(
    name = "googlenet_eval",
    srcs = [
        "googlenet_eval.py",
    ],
    srcs_version = "PY2AND3",
    visibility = ["//tensorflow:__subpackages__"],
    deps = [
        ":googlenet",
    ],
)

py_binary(
    name = "googlenet_train",
    srcs = [
        "googlenet_train.py",
    ],
    srcs_version = "PY2AND3",
    visibility = ["//tensorflow:__subpackages__"],
    deps = [
        ":googlenet",
    ],
)

py_binary(
    name = "googlenet_multi_gpu_train",
    srcs = [
        "googlenet_multi_gpu_train.py",
    ],
    srcs_version = "PY2AND3",
    visibility = ["//tensorflow:__subpackages__"],
    deps = [
        ":googlenet",
    ],
)

filegroup(
    name = "all_files",
    srcs = glob(
        ["**/*"],
        exclude = [
            "**/METADATA",
            "**/OWNERS",
        ],
    ),
    visibility = ["//tensorflow:__subpackages__"],
)
