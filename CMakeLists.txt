cmake_minimum_required(VERSION 3.10)
project(GA)

include_directories(${PROJECT_SOURCE_DIR})

set(gas_gen_SRCS
        gasgen.c
        gen_task.c
        mem.c
        util.c
        conf.c
        conf_gasgen.c
        gen_network.c
        gen_netcommander.c
        cloud.c
        offloadingratio.c
        network.c
        net_commander.c)

set(gas_task_SRCS
        gastask.c
        GA.c
        task.c
        cpu.c
        mem.c
        util.c
        conf.c
        conf_gastask.c
        report.c
        cloud.c
        offloadingratio.c
        network.c
        net_commander.c)

add_executable(gasgen ${gas_gen_SRCS})
add_executable(gastask ${gas_task_SRCS})
target_link_libraries(gastask m)
