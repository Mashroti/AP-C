################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include USB_DEVICE/Target/subdir.mk
-include USB_DEVICE/App/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Core/Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Src/subdir.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
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
AeroPendulum_CDC.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
AeroPendulum_CDC.list \

OBJCOPY_HEX += \
AeroPendulum_CDC.hex \

OBJCOPY_BIN += \
AeroPendulum_CDC.bin \


# All Target
all: AeroPendulum_CDC.elf secondary-outputs

# Tool invocations
AeroPendulum_CDC.elf: $(OBJS) $(USER_OBJS) C:\Users\Mashroti\STM32CubeIDE\workspace_1.4.0\AeroPendulum_CDC\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "AeroPendulum_CDC.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\Mashroti\STM32CubeIDE\workspace_1.4.0\AeroPendulum_CDC\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="AeroPendulum_CDC.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -u _printf_float -u _scanf_float -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

AeroPendulum_CDC.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "AeroPendulum_CDC.list"
	@echo 'Finished building: $@'
	@echo ' '

AeroPendulum_CDC.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "AeroPendulum_CDC.hex"
	@echo 'Finished building: $@'
	@echo ' '

AeroPendulum_CDC.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "AeroPendulum_CDC.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
