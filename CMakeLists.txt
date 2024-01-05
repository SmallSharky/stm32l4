# cmake_minimum_required(VERSION 3.24)

# project(stm32l4_drivers LANGUAGES C)

# set(CMAKE_C_STANDARD 20)


set(STM32L4_CMSIS_DIR ${CMAKE_CURRENT_SOURCE_DIR}/cmsis_device_l4)
set(STM32L4_CMSIS_INC_DIR ${STM32L4_CMSIS_DIR}/Include)
set(STM32L4_CMSIS_CORE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/cmsis-core-l4)
set(STM32L4_CMSIS_CORE_INC_DIR ${STM32L4_CMSIS_CORE_DIR}/Include)


add_library(
    stm32l4xx_cmsis
    INTERFACE
)

target_include_directories(
    stm32l4xx_cmsis
    INTERFACE
    ${STM32L4_CMSIS_INC_DIR}
    ${STM32L4_CMSIS_CORE_INC_DIR}
)




set(STM32L4_HAL_DIR ${CMAKE_CURRENT_SOURCE_DIR}/stm32l4xx_hal_driver)
set(STM32L4_HAL_SRC_DIR ${STM32L4_HAL_DIR}/Src)
set(STM32L4_HAL_INC_DIR ${STM32L4_HAL_DIR}/Inc)



add_library(
    stm32l4xx_hal
    STATIC EXCLUDE_FROM_ALL
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_adc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_adc_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_can.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_comp.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_cortex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_crc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_crc_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_cryp.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_cryp_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_dac.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_dac_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_dcmi.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_dfsdm.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_dfsdm_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_dma2d.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_dma.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_dma_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_dsi.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_exti.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_firewall.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_flash.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_flash_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_flash_ramfunc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_gfxmmu.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_gpio.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_hash.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_hash_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_hcd.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_i2c.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_i2c_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_irda.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_iwdg.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_lcd.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_lptim.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_ltdc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_ltdc_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_mmc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_mmc_ex.c
    # ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_msp_template.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_nand.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_nor.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_opamp.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_opamp_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_ospi.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_pcd.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_pcd_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_pka.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_pssi.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_pwr.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_pwr_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_qspi.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_rcc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_rcc_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_rng.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_rng_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_rtc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_rtc_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_sai.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_sai_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_sd.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_sd_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_smartcard.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_smartcard_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_smbus.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_smbus_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_spi.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_spi_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_sram.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_swpmi.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_tim.c
    # ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_timebase_tim_template.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_tim_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_tsc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_uart.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_uart_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_usart.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_usart_ex.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_hal_wwdg.c

)



target_include_directories(stm32l4xx_hal INTERFACE ${STM32L4_HAL_INC_DIR} PRIVATE ${STM32L4_HAL_INC_DIR})
target_include_directories(stm32l4xx_hal INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/configs PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/configs)

# target_compile_options(stm32l4xx_hal PRIVATE -Wmissing-prototypes)
target_link_libraries(stm32l4xx_hal PRIVATE stm32l4xx_cmsis)



add_library(
    stm32l4xx_ll
    STATIC EXCLUDE_FROM_ALL
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_adc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_comp.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_crc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_crs.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_dac.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_dma2d.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_dma.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_exti.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_fmc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_gpio.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_i2c.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_lptim.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_lpuart.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_opamp.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_pka.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_pwr.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_rcc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_rng.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_rtc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_sdmmc.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_spi.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_swpmi.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_tim.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_usart.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_usb.c
    ${STM32L4_HAL_SRC_DIR}/stm32l4xx_ll_utils.c
)

target_include_directories(stm32l4xx_ll INTERFACE ${STM32L4_HAL_INC_DIR} PRIVATE ${STM32L4_HAL_INC_DIR})
target_include_directories(stm32l4xx_ll INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/configs PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/configs)
# target_compile_options(stm32l4xx_ll PRIVATE -Wmissing-prototypes)
target_link_libraries(stm32l4xx_ll PRIVATE stm32l4xx_cmsis)