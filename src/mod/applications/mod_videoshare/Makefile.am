include $(top_srcdir)/build/modmake.rulesam
MODNAME=mod_videoshare

mod_LTLIBRARIES = mod_videoshare.la
mod_videoshare_la_SOURCES  = mod_videoshare.c videoshare_api.c videoshare_loop.c videoshare_al.c videoshare_cdr.c videoshare_video.c
mod_videoshare_la_SOURCES += videoshare_event.c videoshare_member.c videoshare_utils.c videoshare_file.c videoshare_record.c
mod_videoshare_la_CFLAGS   = $(AM_CFLAGS) -I.
mod_videoshare_la_LIBADD   = $(switch_builddir)/libfreeswitch.la
mod_videoshare_la_LDFLAGS  = -avoid-version -module -no-undefined -shared

$(am_mod_videoshare_la_OBJECTS):  mod_videoshare.h

if HAVE_OPENAL
mod_videoshare_la_LDFLAGS += -lopenal -lm
mod_videoshare_la_CFLAGS += -DOPENAL_POSITIONING
endif

