################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
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
operationmodes.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
operationmodes.list \

OBJCOPY_BIN += \
operationmodes.bin \


# All Target
all: operationmodes.elf secondary-outputs

# Tool invocations
operationmodes.elf: $(OBJS) $(USER_OBJS) G:\OSAMAA\Embedded\ System\27-AdvancedEmbedded_Amgad\02-\ Architecture&interfacing\ part(1)\workspace\operationmodes\STM32F446RETX_FLASH.ld
	arm-none-eabi-gcc -o "operationmodes.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"G:\OSAMAA\Embedded System\27-AdvancedEmbedded_Amgad\02- Architecture&interfacing part(1)\workspace\operationmodes\STM32F446RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="operationmodes.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

operationmodes.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "operationmodes.list"
	@echo 'Finished building: $@'
	@echo ' '

operationmodes.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "operationmodes.bin"
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
