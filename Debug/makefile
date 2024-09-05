################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (12.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
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

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := atv micro 1  enxuto
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
atv\ micro\ 1\ \ enxuto.elf \

MAP_FILES += \
atv\ micro\ 1\ \ enxuto.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
atv\ micro\ 1\ \ enxuto.list \

OBJCOPY_HEX += \
atv\ micro\ 1\ \ enxuto.hex \

OBJCOPY_BIN += \
atv\ micro\ 1\ \ enxuto.bin \


# All Target
all: main-build

# Main-build Target
main-build: atv\ micro\ 1\ \ enxuto.elf secondary-outputs

# Tool invocations
atv\ micro\ 1\ \ enxuto.elf atv\ micro\ 1\ \ enxuto.map: $(OBJS) $(USER_OBJS) /home/juan/STM32CubeIDE/workspace_1.15.1/atv\ micro\ 1\ \ enxuto/STM32F103C8TX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "atv micro 1  enxuto.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/juan/STM32CubeIDE/workspace_1.15.1/atv micro 1  enxuto/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="atv micro 1  enxuto.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

atv\ micro\ 1\ \ enxuto.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "atv micro 1  enxuto.list"
	@echo 'Finished building: $@'
	@echo ' '

atv\ micro\ 1\ \ enxuto.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "atv micro 1  enxuto.hex"
	@echo 'Finished building: $@'
	@echo ' '

atv\ micro\ 1\ \ enxuto.bin: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "atv micro 1  enxuto.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) atv\ micro\ 1\ \ enxuto.bin atv\ micro\ 1\ \ enxuto.elf atv\ micro\ 1\ \ enxuto.hex atv\ micro\ 1\ \ enxuto.list atv\ micro\ 1\ \ enxuto.map atv\\ micro\\ 1\\ \\ enxuto.elf default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
