package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "container_gc.go",
        "convert.go",
        "docker.go",
        "docker_manager.go",
        "docker_manager_linux.go",
        "exec.go",
        "fake_docker_client.go",
        "fake_manager.go",
        "images.go",
        "instrumented_docker.go",
        "kube_docker_client.go",
        "labels.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/v1:go_default_library",
        "//pkg/apis/meta/v1:go_default_library",
        "//pkg/client/record:go_default_library",
        "//pkg/credentialprovider:go_default_library",
        "//pkg/kubelet/cm:go_default_library",
        "//pkg/kubelet/container:go_default_library",
        "//pkg/kubelet/custommetrics:go_default_library",
        "//pkg/kubelet/events:go_default_library",
        "//pkg/kubelet/images:go_default_library",
        "//pkg/kubelet/leaky:go_default_library",
        "//pkg/kubelet/lifecycle:go_default_library",
        "//pkg/kubelet/metrics:go_default_library",
        "//pkg/kubelet/network:go_default_library",
        "//pkg/kubelet/network/hairpin:go_default_library",
        "//pkg/kubelet/prober/results:go_default_library",
        "//pkg/kubelet/qos:go_default_library",
        "//pkg/kubelet/types:go_default_library",
        "//pkg/kubelet/util/cache:go_default_library",
        "//pkg/kubelet/util/format:go_default_library",
        "//pkg/runtime:go_default_library",
        "//pkg/runtime/schema:go_default_library",
        "//pkg/security/apparmor:go_default_library",
        "//pkg/securitycontext:go_default_library",
        "//pkg/types:go_default_library",
        "//pkg/util/clock:go_default_library",
        "//pkg/util/errors:go_default_library",
        "//pkg/util/exec:go_default_library",
        "//pkg/util/flowcontrol:go_default_library",
        "//pkg/util/oom:go_default_library",
        "//pkg/util/procfs:go_default_library",
        "//pkg/util/runtime:go_default_library",
        "//pkg/util/selinux:go_default_library",
        "//pkg/util/sets:go_default_library",
        "//pkg/util/strings:go_default_library",
        "//pkg/util/term:go_default_library",
        "//vendor:github.com/coreos/go-semver/semver",
        "//vendor:github.com/docker/distribution/digest",
        "//vendor:github.com/docker/distribution/reference",
        "//vendor:github.com/docker/docker/pkg/jsonmessage",
        "//vendor:github.com/docker/docker/pkg/stdcopy",
        "//vendor:github.com/docker/engine-api/client",
        "//vendor:github.com/docker/engine-api/types",
        "//vendor:github.com/docker/engine-api/types/container",
        "//vendor:github.com/docker/engine-api/types/strslice",
        "//vendor:github.com/docker/engine-api/types/versions",
        "//vendor:github.com/docker/go-connections/nat",
        "//vendor:github.com/golang/glog",
        "//vendor:github.com/google/cadvisor/info/v1",
        "//vendor:golang.org/x/net/context",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "container_gc_test.go",
        "convert_test.go",
        "docker_manager_test.go",
        "docker_test.go",
        "images_test.go",
        "labels_test.go",
    ],
    data = [
        "fixtures/seccomp/sub/subtest",
        "fixtures/seccomp/test",
    ],
    library = "go_default_library",
    tags = [
        "automanaged",
        "skip",
    ],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/testapi:go_default_library",
        "//pkg/api/v1:go_default_library",
        "//pkg/apis/componentconfig:go_default_library",
        "//pkg/client/record:go_default_library",
        "//pkg/credentialprovider:go_default_library",
        "//pkg/kubelet/container:go_default_library",
        "//pkg/kubelet/container/testing:go_default_library",
        "//pkg/kubelet/events:go_default_library",
        "//pkg/kubelet/images:go_default_library",
        "//pkg/kubelet/network:go_default_library",
        "//pkg/kubelet/network/mock_network:go_default_library",
        "//pkg/kubelet/network/testing:go_default_library",
        "//pkg/kubelet/prober/results:go_default_library",
        "//pkg/kubelet/types:go_default_library",
        "//pkg/kubelet/util/format:go_default_library",
        "//pkg/runtime:go_default_library",
        "//pkg/security/apparmor:go_default_library",
        "//pkg/types:go_default_library",
        "//pkg/util/clock:go_default_library",
        "//pkg/util/exec:go_default_library",
        "//pkg/util/flowcontrol:go_default_library",
        "//pkg/util/hash:go_default_library",
        "//pkg/util/intstr:go_default_library",
        "//pkg/util/sets:go_default_library",
        "//pkg/util/strings:go_default_library",
        "//vendor:github.com/docker/docker/pkg/jsonmessage",
        "//vendor:github.com/docker/engine-api/types",
        "//vendor:github.com/docker/engine-api/types/container",
        "//vendor:github.com/docker/engine-api/types/strslice",
        "//vendor:github.com/docker/go-connections/nat",
        "//vendor:github.com/golang/mock/gomock",
        "//vendor:github.com/google/cadvisor/info/v1",
        "//vendor:github.com/stretchr/testify/assert",
    ],
)
