# TF-FatFS Module Structure

## 1. Physical Layer

(a)  SPI Communication functions in STM32G4XX HAL drivers

(b)  FATFS/Target/user_diskio_spi.c (SD-SPI Driver added)

(c)  FATFS/Target/user_diskio_spi.h (SD-SPI Driver added)

*Some basic SD's command sending / response handling functions are defined here*

## 2. Middleware Layer

(a) Middlewares/Third_Party/FatFs/src/diskio.c

(b) Middlewares/Third_Party/FatFs/src/diskio.h

*These two files are used to link self-defined sd-spi drivers HAL-generateded FatFs system*



(c) Middlewares/Third_Party/FatFs/src/ff_gen_drv.c

(d) Middlewares/Third_Party/FatFs/src/ff_gen_drv.h

*A linking driver that connect application layers with physical layers*



(e) Middlewares/Third_Party/FatFs/src/ff.c

(f) Middlewares/Third_party/FatFs/src/ff.h

*FatFs core file which includes diskio.h*



(g) FATFS/Target/ffconf.h

*Configuration*

## 3. Application Layer

(a) FATFS/App/app_fatfs.c

(b) FATFS/App/app_fatfs.h

*main.c includes them* 





