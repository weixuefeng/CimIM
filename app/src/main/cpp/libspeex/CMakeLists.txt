#AUX_SOURCE_DIRECTORY(. SRC_LIST)
list(APPEND SRC_LIST
       speex_jni.cpp 
       bits.c 
       buffer.c 
       cb_search.c 
       exc_10_16_table.c 
       exc_10_32_table.c 
       exc_20_32_table.c 
       exc_5_256_table.c 
       exc_5_64_table.c 
       exc_8_128_table.c 
       fftwrap.c 
       filterbank.c 
       filters.c 
       gain_table.c 
       gain_table_lbr.c 
       hexc_10_32_table.c 
       hexc_table.c 
       high_lsp_tables.c 
       jitter.c 
       kiss_fft.c 
       kiss_fftr.c 
       lpc.c 
       lsp.c 
       lsp_tables_nb.c 
       ltp.c 
       mdf.c 
       modes.c 
       modes_wb.c 
       nb_celp.c 
       preprocess.c 
       quant_lsp.c 
       resample.c 
       sb_celp.c 
       scal.c 
       smallft.c 
       speex.c 
       speex_callbacks.c 
       speex_header.c 
       stereo.c 
       vbr.c 
       vq.c 
       window.c
       )

ADD_DEFINITIONS(-DFIXED_POINT -DUSE_KISS_FFT -DEXPORT= -UHAVE_CONFIG_H)

INCLUDE_DIRECTORIES(. ${CMAKE_CURRENT_SOURCE_DIR}/../include)

#LINK_DIRECTORIES(.)
ADD_LIBRARY(speex SHARED ${SRC_LIST})

#TARGET_LINK_LIBRARIES(security) 
 
