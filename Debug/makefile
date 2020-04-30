################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
can-receiver.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
can-receiver.list \

OBJCOPY_BIN += \
can-receiver.bin \


# All Target
all: can-receiver.elf secondary-outputs

# Tool invocations
can-receiver.elf: $(OBJS) $(USER_OBJS) C:\Users\fao9ca\Documents\02\ -\ Start\ Stop\ Retrofit\ -\ Fase\ 3\03\ -\ Placa\ da\ cabine\STM32CubeIDE\workspace\can-receiver\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "can-receiver.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\fao9ca\Documents\02 - Start Stop Retrofit - Fase 3\03 - Placa da cabine\STM32CubeIDE\workspace\can-receiver\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="can-receiver.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

can-receiver.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "can-receiver.list"
	@echo 'Finished building: $@'
	@echo ' '

can-receiver.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "can-receiver.bin"
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
