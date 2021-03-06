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
        "apps.go",
        "autoscaling.go",
        "batch.go",
        "bootstrap.go",
        "certificates.go",
        "controllermanager.go",
        "core.go",
        "extensions.go",
        "plugins.go",
        "policy.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//cmd/kube-controller-manager/app/options:go_default_library",
        "//pkg/api:go_default_library",
        "//pkg/apis/batch:go_default_library",
        "//pkg/apis/componentconfig:go_default_library",
        "//pkg/client/clientset_generated/clientset:go_default_library",
        "//pkg/client/informers/informers_generated/externalversions:go_default_library",
        "//pkg/client/leaderelection:go_default_library",
        "//pkg/client/leaderelection/resourcelock:go_default_library",
        "//pkg/cloudprovider:go_default_library",
        "//pkg/cloudprovider/providers:go_default_library",
        "//pkg/cloudprovider/providers/aws:go_default_library",
        "//pkg/cloudprovider/providers/azure:go_default_library",
        "//pkg/cloudprovider/providers/gce:go_default_library",
        "//pkg/cloudprovider/providers/openstack:go_default_library",
        "//pkg/cloudprovider/providers/photon:go_default_library",
        "//pkg/cloudprovider/providers/vsphere:go_default_library",
        "//pkg/controller:go_default_library",
        "//pkg/controller/bootstrap:go_default_library",
        "//pkg/controller/certificates/approver:go_default_library",
        "//pkg/controller/certificates/signer:go_default_library",
        "//pkg/controller/cronjob:go_default_library",
        "//pkg/controller/daemon:go_default_library",
        "//pkg/controller/deployment:go_default_library",
        "//pkg/controller/disruption:go_default_library",
        "//pkg/controller/endpoint:go_default_library",
        "//pkg/controller/garbagecollector:go_default_library",
        "//pkg/controller/garbagecollector/metaonly:go_default_library",
        "//pkg/controller/job:go_default_library",
        "//pkg/controller/namespace:go_default_library",
        "//pkg/controller/node:go_default_library",
        "//pkg/controller/podautoscaler:go_default_library",
        "//pkg/controller/podautoscaler/metrics:go_default_library",
        "//pkg/controller/podgc:go_default_library",
        "//pkg/controller/replicaset:go_default_library",
        "//pkg/controller/replication:go_default_library",
        "//pkg/controller/resourcequota:go_default_library",
        "//pkg/controller/route:go_default_library",
        "//pkg/controller/service:go_default_library",
        "//pkg/controller/serviceaccount:go_default_library",
        "//pkg/controller/statefulset:go_default_library",
        "//pkg/controller/ttl:go_default_library",
        "//pkg/controller/volume/attachdetach:go_default_library",
        "//pkg/controller/volume/persistentvolume:go_default_library",
        "//pkg/features:go_default_library",
        "//pkg/quota/install:go_default_library",
        "//pkg/serviceaccount:go_default_library",
        "//pkg/util/configz:go_default_library",
        "//pkg/version:go_default_library",
        "//pkg/volume:go_default_library",
        "//pkg/volume/aws_ebs:go_default_library",
        "//pkg/volume/azure_dd:go_default_library",
        "//pkg/volume/azure_file:go_default_library",
        "//pkg/volume/cinder:go_default_library",
        "//pkg/volume/flexvolume:go_default_library",
        "//pkg/volume/flocker:go_default_library",
        "//pkg/volume/gce_pd:go_default_library",
        "//pkg/volume/glusterfs:go_default_library",
        "//pkg/volume/host_path:go_default_library",
        "//pkg/volume/local:go_default_library",
        "//pkg/volume/nfs:go_default_library",
        "//pkg/volume/photon_pd:go_default_library",
        "//pkg/volume/portworx:go_default_library",
        "//pkg/volume/quobyte:go_default_library",
        "//pkg/volume/rbd:go_default_library",
        "//pkg/volume/scaleio:go_default_library",
        "//pkg/volume/storageos:go_default_library",
        "//pkg/volume/util:go_default_library",
        "//pkg/volume/vsphere_volume:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/github.com/prometheus/client_golang/prometheus:go_default_library",
        "//vendor/github.com/spf13/cobra:go_default_library",
        "//vendor/github.com/spf13/pflag:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/serializer:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/server/healthz:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/util/feature:go_default_library",
        "//vendor/k8s.io/client-go/discovery:go_default_library",
        "//vendor/k8s.io/client-go/dynamic:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes/typed/core/v1:go_default_library",
        "//vendor/k8s.io/client-go/rest:go_default_library",
        "//vendor/k8s.io/client-go/tools/clientcmd:go_default_library",
        "//vendor/k8s.io/client-go/tools/record:go_default_library",
        "//vendor/k8s.io/client-go/util/cert:go_default_library",
        "//vendor/k8s.io/metrics/pkg/client/clientset_generated/clientset/typed/metrics/v1alpha1:go_default_library",
        "//vendor/k8s.io/metrics/pkg/client/custom_metrics:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//cmd/kube-controller-manager/app/options:all-srcs",
    ],
    tags = ["automanaged"],
)

go_test(
    name = "go_default_test",
    srcs = ["controller_manager_test.go"],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = ["//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library"],
)
