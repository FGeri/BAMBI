################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include emlib/subdir.mk
-include Drivers/subdir.mk
-include CMSIS/efm32gg/subdir.mk
-include BSP/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: STK3700_touch.axf

# Tool invocations
STK3700_touch.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: GNU ARM C Linker'
	arm-none-eabi-gcc -g -gdwarf-2 -mcpu=cortex-m3 -mthumb -T "STK3700_touch.ld" -Xlinker --gc-sections -Xlinker -Map="STK3700_touch.map" --specs=nano.specs -o STK3700_touch.axf "./src/touchdemo.o" "./emlib/em_acmp.o" "./emlib/em_assert.o" "./emlib/em_cmu.o" "./emlib/em_emu.o" "./emlib/em_gpio.o" "./emlib/em_int.o" "./emlib/em_lcd.o" "./emlib/em_lesense.o" "./emlib/em_rtc.o" "./emlib/em_system.o" "./emlib/em_vcmp.o" "./Drivers/caplesense.o" "./Drivers/rtcdriver.o" "./Drivers/segmentlcd.o" "./Drivers/vddcheck.o" "./CMSIS/efm32gg/startup_efm32gg.o" "./CMSIS/efm32gg/system_efm32gg.o" "./BSP/bsp_trace.o" -Wl,--start-group -lgcc -lc -lnosys -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

	@echo 'Building hex file: STK3700_touch.hex'
	arm-none-eabi-objcopy -O ihex "STK3700_touch.axf" "STK3700_touch.hex"
	@echo ' '

	@echo 'Building bin file: STK3700_touch.bin'
	arm-none-eabi-objcopy -O binary "STK3700_touch.axf" "STK3700_touch.bin"
	@echo ' '

	@echo 'Running size tool'
	arm-none-eabi-size "STK3700_touch.axf"
	@echo ' '

# Other Targets
clean:
	-$(RM) $(OBJS)$(C_DEPS)$(EXECUTABLES) STK3700_touch.axf
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
