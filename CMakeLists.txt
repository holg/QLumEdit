cmake_minimum_required(VERSION 3.22)
project(QLumEdit)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${USE_FLAGS} -sERROR_ON_UNDEFINED_SYMBOLS=0")
set(CMAKE_LINKER_FLAGS "${CMAKE_LINKER_FLAGS} ${USE_FLAGS} -sERROR_ON_UNDEFINED_SYMBOLS=0" -sASYNCIFY -Os)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_AUTOMOC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTORCC ON)
set(DCMAKE_BUILD_TYPE=Release)
set(PROJECT_BINARY_DIR "wasm")
set(EXECUTABLE_OUTPUT_PATH "wasm")
#set(CMAKE_EXECUTABLE_SUFFIX ".html")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "wasm")
set(QT_EMSCRIPTEN_ASYNCIFY=1)
find_package(Qt6 COMPONENTS
        Core
        Gui
        Widgets
        REQUIRED)
include_directories(sources, /opt/qt6/qtbase/lib/)

qt_add_executable(QLumEdit
        sources/application.qrc
        sources/configtabdialog.cpp
        sources/configtabdialog.h
        sources/eulumdat.cpp
        sources/eulumdat.h
        sources/eulumdatcalculate.cpp
        sources/eulumdatimage.cpp
        sources/eulumdattablewidget.cpp
        sources/eulumdattablewidget.h
        sources/eulumdatwidget.cpp
        sources/eulumdatwidget.h
        sources/eulumdatwidget2.cpp
        sources/eulumdatwidget2.h
        sources/eulumdatwidget3.cpp
        sources/eulumdatwidget3.h
        sources/eulumdatwidget4.cpp
        sources/eulumdatwidget4.h
        sources/exportto.cpp
        sources/main.cpp
        sources/maintabwidget.cpp
        sources/maintabwidget.h
        sources/mainwindow.cpp
        sources/mainwindow.h
#        sources/moc_configtabdialog.cpp
#        sources/moc_eulumdat.cpp
#        sources/moc_eulumdattablewidget.cpp
#        sources/moc_eulumdatwidget.cpp
#        sources/moc_eulumdatwidget2.cpp
#        sources/moc_eulumdatwidget3.cpp
#        sources/moc_eulumdatwidget4.cpp
#        sources/moc_maintabwidget.cpp
#        sources/moc_mainwindow.cpp
#        sources/moc_newdialog.cpp
#        sources/moc_predefs.h
#        sources/moc_renderwidget.cpp
#        sources/moc_validator.cpp
        sources/newdialog.cpp
        sources/newdialog.h
#        sources/qrc_application.cpp
        sources/renderwidget.cpp
        sources/renderwidget.h
        sources/validator.cpp
        sources/validator.h
        sources/vars.cpp
        sources/vars.h)

target_compile_options(QLumEdit PRIVATE -fPIC)        
        
target_link_libraries(QLumEdit PRIVATE
        Qt::Core
        Qt::Gui
        Qt::Widgets
        )
#install(
#
#)