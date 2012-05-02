TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

# INSTALL Documentation
HTMLS += s7plc.html

# INSTALL Test TCL Script
SCRIPTS_Linux += server.tcl

# =============================================
# Build as a static library for an linking
# in with an external IOC application:
# ============================================
LIBRARY_IOC += s7plcLib


# s7plcLib.dbd will be installed
DBD += s7plcLib.dbd


# s7plcLib_registerRecordDeviceDriver.cpp derives from s7plcLib.dbd
s7plcLib_SRCS += s7plcLib_registerRecordDeviceDriver.cpp

# Library Source files
s7plcLib_SRCS += drvS7plc.c
s7plcLib_SRCS += devS7plc.c

# Finally link to the EPICS Base libraries
s7plcLib_LIBS += $(EPICS_BASE_IOC_LIBS)

#===================================================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

