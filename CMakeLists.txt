cmake_minimum_required(VERSION 2.8)
project( manga-text-detection )
find_package( OpenCV REQUIRED )
add_compile_options(-std=c++11)

add_executable( main main.cpp )
target_link_libraries( main ${OpenCV_LIBS} )

add_executable( img2cc img2cc.cpp )
target_link_libraries( img2cc ${OpenCV_LIBS} )

add_executable( img2ccr img2ccr.cpp )
target_link_libraries( img2ccr ${OpenCV_LIBS} )

add_executable( img2label img2label.cpp )
target_link_libraries( img2label ${OpenCV_LIBS} )

add_executable( svmtrain svmtrain.cpp )
target_link_libraries( svmtrain ${OpenCV_LIBS} )