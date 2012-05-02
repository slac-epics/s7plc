TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE


#=============================
# Build the IOC application
# ============================
PROD_IOC = s7plcTest

# s7plcTest.dbd will be created and installed
DBD += s7plcTest.dbd

# s7plcTest.dbd will be made up from these files:
s7plcTest_DBD += base.dbd
s7plcTest_DBD += s7plcLib.dbd

# s7plcTest_registerRecordDeviceDriver.cpp derives from s7plcTest.dbd
s7plcTest_SRCS += s7plcTest_registerRecordDeviceDriver.cpp

# Build the main IOC entry point on workstation OSs.
s7plcTest_SRCS_DEFAULT += s7plcTestMain.cpp
s7plcTest_SRCS_vxWorks += -nil-


# Link in the code from s7plcLib library
s7plcTest_LIBS += s7plcLib


# Finally link to the EPICS Base libraries
s7plcTest_LIBS += $(EPICS_BASE_IOC_LIBS)

#=============================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

