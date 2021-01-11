################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
T4_L25_RTC.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
T4_L25_RTC.list \

OBJCOPY_BIN += \
T4_L25_RTC.bin \


# All Target
all: T4_L25_RTC.elf secondary-outputs

# Tool invocations
T4_L25_RTC.elf: $(OBJS) $(USER_OBJS) C:\Users\matpac\STM32CubeIDE\MSalamon\T4_L25_RTC\STM32F411VETX_FLASH.ld
	arm-none-eabi-gcc -o "T4_L25_RTC.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\matpac\STM32CubeIDE\MSalamon\T4_L25_RTC\STM32F411VETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="T4_L25_RTC.map" -Wl,--gc-sections -static -u_printf_float --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

T4_L25_RTC.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "T4_L25_RTC.list"
	@echo 'Finished building: $@'
	@echo ' '

T4_L25_RTC.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "T4_L25_RTC.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
