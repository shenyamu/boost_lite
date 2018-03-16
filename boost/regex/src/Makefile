#不同产品的目录是不一样的，需要根据实际的情况调整这里
include $(NGBILLING_SRC)/foundation/MakeCommon

#引用的头文件，需要根据实际的情况进行调整
USR_INCLUDE= -I../ -I../v4 -I../config -I../../../

.SUFFIXES: .cpp 
.cpp.o:
	$(CXX)  $(CXX_OPTIONS) -o $@ -c $< $(USR_INCLUDE)

SRCS  = c_regex_traits.o  cpp_regex_traits.o  cregex.o fileiter.o icu.o instances.o posix_api.o  regex.o  regex_debug.o \
	regex_raw_buffer.o regex_traits_defaults.o static_mutex.o  usinstances.o
	
OUTPUT =libboost_regex.so

all: $(OUTPUT)

$(OUTPUT): $(SRCS)
	$(SO) $(SO_OPTIONS) $@ $(SRCS)

install:
	cp -f $(OUTPUT)  $(NG_LIB)

install-aix:
	@echo "cp -f libboost_regex.so $(NG_LIB)";\
	cp -f libboost_regex.so.aix $(NG_LIB);\
	mv $(NG_LIB)/libboost_regex.so.aix $(NG_LIB)/libboost_regex.so