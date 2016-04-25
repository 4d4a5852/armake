add_executable(armake binarize.c build.c docopt.c filesystem.c main.c model_config.c p3d.c preprocess.c rapify.c utils.c)

target_link_libraries(armake minilzo sha1 m)
