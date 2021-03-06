cmake_minimum_required(VERSION 3.8)

add_library(main SHARED
            jni_common.cpp
            jni_common.h
            input_manager.cpp
            input_manager.h
            egl_android.cpp
            egl_android.h
            mii_selector.cpp
            mii_selector.h
            keyboard.cpp
            keyboard.h
            main_android.cpp
            mem_region.cpp
            mem_region.h
            multiplayer.cpp
            multiplayer.h
            ndk_motion.cpp
            ndk_motion.h
            png_handler.h
            png_handler.cpp
            camera/camera_base.cpp
            camera/camera_base.h
            camera/camera_util.cpp
            camera/camera_util.h
            camera/still_image_camera.cpp
            camera/still_image_camera.h
            config/config.cpp
            config/config.h
            config/config_info.cpp
            config/config_info.h
            config/ini_file.cpp
            config/ini_file.h
            config/layer.cpp
            config/layer.h
            config/string_util.cpp
            config/string_util.h
            config/main_settings.cpp
            config/main_settings.h
            config/config_loader.cpp
            config/config_loader.h
            )

target_link_libraries(main android EGL log core input_common network)
target_include_directories(main PRIVATE "./" "../../../externals/glad/include/")
