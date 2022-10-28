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
mini_projekat_1_jovan_anicic.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
mini_projekat_1_jovan_anicic.list \

OBJCOPY_HEX += \
mini_projekat_1_jovan_anicic.hex \

OBJCOPY_BIN += \
mini_projekat_1_jovan_anicic.bin \


# All Target
all: mini_projekat_1_jovan_anicic.elf secondary-outputs

# Tool invocations
mini_projekat_1_jovan_anicic.elf: $(OBJS) $(USER_OBJS) D:\4.\ godina\Prvi\ semestar\Mikroprocesorski\ sistemi\moji_cube_ide\mini_projekat_1_jovan_anicic\STM32F103C6TX_FLASH.ld
	arm-none-eabi-gcc -o "mini_projekat_1_jovan_anicic.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"D:\4. godina\Prvi semestar\Mikroprocesorski sistemi\moji_cube_ide\mini_projekat_1_jovan_anicic\STM32F103C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="mini_projekat_1_jovan_anicic.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

mini_projekat_1_jovan_anicic.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "mini_projekat_1_jovan_anicic.list"
	@echo 'Finished building: $@'
	@echo ' '

mini_projekat_1_jovan_anicic.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "mini_projekat_1_jovan_anicic.hex"
	@echo 'Finished building: $@'
	@echo ' '

mini_projekat_1_jovan_anicic.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "mini_projekat_1_jovan_anicic.bin"
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
