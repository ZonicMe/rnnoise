add_library(rnnoise)

target_sources(
    rnnoise PRIVATE 
    arch.h
    celt_lpc.h
    cpu_support.h
    common.h
    denoise.h
    _kiss_fft_guts.h
    kiss_fft.h
    nnet.h
    nnet_arch.h
    opus_types.h
    pitch.h
    rnn.h
    rnnoise_data_little.h
    vec_neon.h
    vec.h
    vec_avx.h
)

target_sources(
    rnnoise PRIVATE 
    denoise.c 
    rnn.c 
    pitch.c 
    kiss_fft.c
    celt_lpc.c
    nnet.c
    nnet_default.c 
    parse_lpcnet_weights.c 
    rnnoise_data_little.c
    rnnoise_tables.c
)
