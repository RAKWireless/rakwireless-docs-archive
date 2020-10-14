---
type: page
title: RUI Interface General Format
listed: true
slug: rui-interface-general-format
---published

This part support all module with BSP API.

## General Format

**rui_"Interface Type"_xxx()**

## General Definition

### RUI_UART_DEF

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum RUI_UART_DEF\n{\n\tRUI_UART0 = 0,\n\tRUI_UART1 = 1,\n\tRUI_UART2 = 2,\n\tRUI_UART3 = 3\n}RUI_UART_DEF;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_IF_READ_WRITE

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum RUI_IF_READ_WRITE\n{\n\tRUI_IF_READ = 0,\n\tRUI_IF_WRITE = 1\n}RUI_IF_READ_WRITE;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_I2C_ST

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef struct RUI_I2C_ST\n{\n\tuint32_t INSTANCE_ID;\n\tuint32_t PIN_SDA;   \/\/ SDA pin num\n\tuint32_t PIN_SCL;   \/\/ SCL pin num\n\tuint32_t FREQUENCY;\n\tuint32_t REG_NULL; \/\/ if no reg , should be 0xAA\n}RUI_I2C_ST;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_I2C_FREQ_ST

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum RUI_I2C_FREQ_ST\n{\n\tRUI_I2C_FREQ_100K,\n\tRUI_I2C_FREQ_400K\t\n}RUI_I2C_FREQ_ST;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_SPI_ST

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef struct\n{\n\tuint32_t INSTANCE_ID;\n\tuint32_t PIN_CS;   \/\/ \n\tuint32_t PIN_SCL;   \/\/ \n\tuint32_t PIN_MISO;   \/\/ \n\tuint32_t PIN_MOSI;   \/\/ \n\tuint32_t FREQUENCY;\n} RUI_SPI_ST;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_SPI_FREQ_ST

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum RUI_SPI_FREQ_ST\n{\n\tRUI_I2C_FREQ_125K,\n\tRUI_I2C_FREQ_250K,\n\tRUI_I2C_FREQ_500K,\n\tRUI_I2C_FREQ_1M,\n\tRUI_I2C_FREQ_2M,\n\tRUI_I2C_FREQ_4M,\n\tRUI_I2C_FREQ_8M\n}RUI_SPI_FREQ_ST;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_GPIO_PIN_DIR_ST

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum\n{\n\tRUI_GPIO_PIN_DIR_INPUT, \/\/ Input.\n\tRUI_GPIO_PIN_DIR_OUTPUT \/\/ Output.\n} RUI_GPIO_PIN_DIR_ST;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_GPIO_PIN_PULL_ST

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum\n{\n\tRUI_GPIO_PIN_NOPULL,   \/\/  Pin pull-up resistor disabled.\n\tRUI_GPIO_PIN_PULLDOWN, \/\/  Pin pull-down resistor enabled.\n\tRUI_GPIO_PIN_PULLUP    \/\/  Pin pull-up resistor enabled.\n} RUI_GPIO_PIN_PULL_ST;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_GPIO_INTERRUPT_EDGE

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum \n{\n    RUI_GPIO_EDGE_RAISE,\n    RUI_GPIO_EDGE_FALL,\n    RUI_GPIO_EDGE_FALL_RAISE\n} RUI_GPIO_INTERRUPT_EDGE;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_GPIO_INTERRUPT_PRIORITY

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum \n{\n    RUI_GPIO_IRQ_HIGH_PRIORITY,\n    RUI_GPIO_IRQ_NORMAL_PRIORITY,\n    RUI_GPIO_IRQ_LOW_PRIORITY,\n} RUI_GPIO_INTERRUPT_PRIORITY;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_GPIO_ST

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef struct\n{\n\tuint32_t pin_num;\n\tRUI_GPIO_PIN_DIR_ST dir;\n\tRUI_GPIO_PIN_PULL_ST pull;\n}RUI_GPIO_ST;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_TIMER_MODE_ST

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum\n{\n\tRUI_TIMER_MODE_SINGLE_SHOT,     \/**< The timer will expire only once. *\/\n\tRUI_TIMER_MODE_REPEATED        \/**< The timer will restart each time it expires. *\/\n} RUI_TIMER_MODE_ST;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_TIMER_ST

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef void (* TIMER_CALLBACK) (void);\n\ntypedef struct{\n\tuint32_t timeout_ms;\n\tRUI_TIMER_MODE_ST timer_mode;\n\tTIMER_CALLBACK timer_callback;\n}RUI_TIMER_ST;",
                "language": "c"
            }
        ]
    }
}]$

### RUI_FLASH_MOD

$plugin[{
    "type": "code-block",
    "data": {
        "languageBlocks": [
            {
                "code": "typedef enum\n{\n    RUI_FLASH_USER = 0,                  \/\/ a region for user , less than 128 bytes\n    RUI_FLASH_ORIGIN              \/\/inner struct region , advise not modify it \n}RUI_FLASH_MODE;",
                "language": "c"
            }
        ]
    }
}]$

