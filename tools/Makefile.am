tool_programs =  \
  fuzz_torrent

if ENABLE_EXAMPLES
bin_PROGRAMS = $(tool_programs)
endif

EXTRA_PROGRAMS = $(tool_programs)
EXTRA_DIST = Jamfile     \
  parse_bandwidth_log.py \
  parse_buffer_log.py    \
  parse_dht_log.py       \
  parse_dht_rtt.py       \
  parse_dht_stats.py     \
  parse_disk_buffer_log.py\
  parse_memory_log.py    \
  parse_peer_log.py      \
  parse_sample.py        \
  parse_session_stats.py \
  parse_utp_log.py

fuzz_torrent_SOURCES = fuzz_torrent.cpp

LDADD = $(top_builddir)/src/libtorrent-rasterbar.la

AM_CPPFLAGS = -ftemplate-depth-50 -I$(top_srcdir)/include @DEBUGFLAGS@

AM_LDFLAGS = @BOOST_SYSTEM_LIB@
#AM_LDFLAGS = $(LDFLAGS) @BOOST_SYSTEM_LIB@ @OPENSSL_LDFLAGS@ @OPENSSL_LIBS@
#AM_LDFLAGS = @OPENSSL_LDFLAGS@
