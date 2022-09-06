art_make( BASENAME_ONLY
 LIBRARY_NAME otsdaq-dqm_ArtModules
 SUBDIRS detail
 NO_PLUGINS
 DICT_DICTIONARIES
 ${ART_PERSISTENCY_PROVENANCE}
 ${CANVAS_PERSISTENCY_PROVENANCE}
 LIB_LIBRARIES
) #add libs here if want more mu2e stuff $OFFLINE_LIBS - > get name: libNAME.so

basic_plugin(Occupancy "module"
art_root_io::TFileService_service
otsdaq::NetworkUtilities
${ROOT_BASIC_LIB_LIST}
)

basic_plugin(TriggerDQM "module"
art_root_io::TFileService_service
mu2e_artdaq_core::mu2e-artdaq-core_Overlays
otsdaq_mu2e::otsdaq-mu2e_ArtModules
)


# basic_plugin(BeamMonitor "module"
# art_root_io::TFileService_service
# otsdaq::NetworkUtilities
# ${ROOT_BASIC_LIB_LIST}
# mu2e_Mu2eUtilities
# )

