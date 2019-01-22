cmake_minimum_required(VERSION 3.12)
project(FaceMatch)

set(CMAKE_CXX_STANDARD 14)

include_directories("/usr/local/poco/include")
include_directories("/home/chenhf/Baidu_Face_Offline_SDK_Linux/test-face-api/include")


link_directories("/usr/local/poco/lib")
link_libraries(PocoFoundation PocoNet PocoUtil)


link_directories("/home/chenhf/Baidu_Face_Offline_SDK_Linux/test-face-api/lib3/opencv-linux/lib")
link_libraries(opencv_imgcodecs opencv_core opencv_imgproc opencv_highgui opencv_video opencv_videoio)


link_directories("/home/chenhf/Baidu_Face_Offline_SDK_Linux/test-face-api/facelib")
link_libraries(FaceSDK BaiduFaceApi-ubuntu)

link_directories("/home/chenhf/Baidu_Face_Offline_SDK_Linux/test-face-api/lib3/ffmpeg-linux/lib")
link_libraries(avformat avcodec avutil swscale swresample)

link_directories("/home/chenhf/Baidu_Face_Offline_SDK_Linux/test-face-api/lib3/openblas-linux/lib")
link_libraries(openblas)

link_directories("/home/chenhf/Baidu_Face_Offline_SDK_Linux/test-face-api/lib3/json/lib-ubuntu")
link_libraries(json)

link_directories("/home/chenhf/Baidu_Face_Offline_SDK_Linux/test-face-api/lib3/lib64")
link_libraries(jpeg png12 tiff jasper Imath IlmImf Iex Half IlmThread gtk-x11-2.0 gdk-x11-2.0 atk-1.0 cairo dc1394 fontconfig freetype gdk_pixbuf-2.0 gio-2.0 glib-2.0 gmodule-2.0 gobject-2.0 gstapp-0.10 gstbase-0.10 gstpbutils-0.10 gstreamer-0.10 gstriff-0.10 gstvideo-0.10 gthread-2.0 pango-1.0 pangocairo-1.0 pangoft2-1.0 v4l1 v4l2 bz2 X11 Xfixes Xext Xrender Xinerama Xi Xcomposite Xdamage pixman-1 usb-1.0 selinux Xrandr Xcursor raw1394 gsttag-0.10 xcb v4lconvert gstaudio-0.10 Xau gstinterfaces-0.10)


add_executable(FaceMatch main.cpp)