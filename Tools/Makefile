##########################################
# LIST_CAMERA MAKEFILE
##########################################

TARGET = list_camera
CXX = g++
CXXFLAGS += -fPIC -std=gnu++11
INCLUDE += \
	-I$(PWD)/../mvIMPACT/include/ \

SRCS = list_cameras.cpp
OBJS = $(SRCS:.cpp=.o)
vpath %.cpp $(PWD)/../src/

LDFLAGS += \
	-L$(PWD)/../mvIMPACT/lib/x86_64/

LIBS = \
	-lmvDeviceManager \
	-lboost_system \
	-lboost_program_options \

all: $(TARGET)

$(TARGET): $(OBJS)
	$(Q_) $(CXX) $(CXXFLAGS) $(INCLUDE) $^ $(LDFLAGS) -o $@ $(LIBS)

$(OBJS): $(SRCS)
	$(CXX) $(INCLUDE) $(CXXFLAGS) -c $< -o $@

clean:
	$(RM) $(TARGET)
	$(RM) *.o
