AM_CPPFLAGS= -I$(TBLIB_ROOT)/include/tbsys \
	     -I$(TBLIB_ROOT)/include/tbnet \
	     -I${top_srcdir}/src/storage

if WITH_COMPRESS
COMPRESS_CPPFLAGS= compressor.hpp snappy_compressor.hpp
endif

AM_LDFLAGS= -rdynamic ${GCOV_LIB} \
      -lz -lrt -lpthread \
      -ldl

LDADD=$(TBLIB_ROOT)/lib/libtbnet.a \
      $(TBLIB_ROOT)/lib/libtbsys.a

base_src=data_dumpper.cpp	\
	 stat_helper.cpp	\
	 util.cpp	\
	 data_dumpper.hpp	\
	 data_entry.hpp	\
	 data_entry.cpp	\
	 key_value_pack.hpp \
	 define.hpp	\
	 dump_data_info.hpp	\
	 hash.hpp	\
	 item_data_info.hpp	\
	 log.hpp	\
	 mmap_file.hpp	\
	 stat_helper.hpp	\
	 stat_info.hpp	\
	 util.hpp	\
	 wait_object.hpp	 \
         file_op.hpp file_op.cpp \
	 BlockQueueEx.hpp \
	 blockqueue.hpp \
	 syncproc.hpp \
	 scoped_wrlock.hpp \
	 $(COMPRESS_CPPFLAGS) \
         file_list_factory.hpp \
	 counter_wrapper.hpp tair_atomic.hpp record_logger.hpp record_logger_util.hpp record_logger_util.cpp

noinst_LIBRARIES=libtair_common.a

include_HEADERS=item_data_info.hpp data_entry.hpp define.hpp util.hpp hash.hpp log.hpp inval_stat.hpp key_value_pack.hpp $(COMPRESS_CPPFLAGS)

libtair_common_a_SOURCES = ${base_src}

