add_executable(
  ActsExampleGeantinoRecordingGdml
  GdmlGeantinoRecording.cpp)
target_link_libraries(
  ActsExampleGeantinoRecordingGdml
  PRIVATE
    ActsExamplesCommon
    ActsExamplesDetectorDD4hep
    ActsExamplesFramework
    ActsExamplesGeant4
    ActsExamplesIoRoot
    Boost::program_options)

install(
  TARGETS ActsExampleGeantinoRecordingGdml
  RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})

add_subdirectory_if(DD4hep ACTS_BUILD_EXAMPLES_DD4HEP)
