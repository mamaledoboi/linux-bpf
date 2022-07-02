cmake_minimum_required(VERSION 3.22)
project(linux_bpf C)

set(CMAKE_C_STANDARD 11)

include_directories(/Users/zhangxiaozheng/workspace/c/ubuntu-bionic/include)
include_directories(/Users/zhangxiaozheng/workspace/c/ubuntu-bionic/include/uapi)
include_directories(/Users/zhangxiaozheng/workspace/c/ubuntu-bionic/samples/bpf)
include_directories(/Users/zhangxiaozheng/workspace/c/ubuntu-bionic/tools/lib)
include_directories(/Users/zhangxiaozheng/workspace/c/ubuntu-bionic/tools/perf)
include_directories(/Users/zhangxiaozheng/workspace/c/ubuntu-bionic/tools/include)
include_directories(/Users/zhangxiaozheng/workspace/c/ubuntu-bionic/tools/testing/selftests/bpf)



add_executable(linux_bpf
        code/chapter-2/hello_world/bpf_program.c
        code/chapter-2/hello_world/loader.c
        code/chapter-3/bpf_fs/map_pinning_save.c
        code/chapter-3/map_pinning_fetch.c
        code/chapter-4/usdt/hello_usdt.c
        code/chapter-6/packet-filtering-raw-sockets/bpf_program.c
        code/chapter-6/packet-filtering-raw-sockets/loader.c
        code/chapter-6/tc-flow-bpf-cls/classifier.c
        code/chapter-7/bcc/program.c
        code/chapter-7/iproute2/program.c
        code/chapter-7/prog-test-run/program.c
        code/chapter-8/seccomp/main.c)
