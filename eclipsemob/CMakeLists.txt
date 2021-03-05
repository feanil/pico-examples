add_executable(eclipsemob
        eclipsemob.c
        )

# Pull in our pico_stdlib which pulls in commonly used features
target_link_libraries(eclipsemob pico_stdlib hardware_adc)

# create map/bin/hex file etc.
pico_add_extra_outputs(eclipsemob)

# add url via pico_set_program_url
example_auto_set_url(eclipsemob)

pico_enable_stdio_usb(eclipsemob 1)
pico_enable_stdio_uart(eclipsemob 0)
