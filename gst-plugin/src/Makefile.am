# Note: plugindir is set in configure

##############################################################################
# TODO: change libgstplugin.la to something else, e.g. libmysomething.la     #
##############################################################################
plugin_LTLIBRARIES = libanttest.la

##############################################################################
# TODO: for the next set of variables, name the prefix if you named the .la, #
#  e.g. libmysomething.la => libmysomething_la_SOURCES                       #
#                            libmysomething_la_CFLAGS                        #
#                            libmysomething_la_LIBADD                        #
#                            libmysomething_la_LDFLAGS                       #
##############################################################################

## Plugin 1

# sources used to compile this plug-in
libanttest_la_SOURCES = gstmyfilter.cc gstmyfilter.h

# compiler and linker flags used to compile this plugin, set in configure.ac
libanttest_la_CXXFLAGS = $(GST_CFLAGS) `pkg-config --cflags opencv`
libanttest_la_LIBADD = $(GST_LIBS) $(GST_BASE_LIBS) $(GSTCTRL_LIBS)
libanttest_la_LDFLAGS = $(GST_PLUGIN_LDFLAGS) `pkg-config --libs opencv`
libanttest_la_LIBTOOLFLAGS = --tag=disable-static

# headers we need but don't want installed
noinst_HEADERS = gstplugin.h
