cmake_minimum_required(VERSION 3.0)

project(balaev_a_a)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Find includes in corresponding build directories
set(CMAKE_INCLUDE_CURRENT_DIR ON)
# Instruct CMake to run moc automatically when needed
set(CMAKE_AUTOMOC ON)
# Create code from a list of Qt designer ui files
set(CMAKE_AUTOUIC ON)

# Find the QtWidgets library
find_package(Qt5 COMPONENTS Widgets REQUIRED)
find_package(Qt5PrintSupport)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)
set_property(GLOBAL PROPERTY PREDEFINED_TARGETS_FOLDER "cmake")


set(balaev_a_a
      invest_trader/main.cpp
      invest_trader/mainwindow.cpp
      invest_trader/mainwindow.h
      invest_trader/BoughtCollection.cpp
      invest_trader/BoughtCollection.h
      invest_trader/changeinformation.cpp
      invest_trader/changeinformation.h
      invest_trader/client.cpp
      invest_trader/client.h
      invest_trader/graphics.cpp
      invest_trader/graphics.h
      invest_trader/Investment.cpp
      invest_trader/Investment.h
      invest_trader/myinvestment.cpp
      invest_trader/myinvestment.h
      invest_trader/PaperCollection.cpp
      invest_trader/PaperCollection.h
      invest_trader/qcustomplot.cpp
      invest_trader/qcustomplot.h
      invest_trader/SecurityPaper.cpp
      invest_trader/SecurityPaper.h
      invest_trader/User.cpp
      invest_trader/User.h
      invest_trader/utils.cpp
      invest_trader/utils.h
    ${QRCS}
)

add_executable(${PROJECT_NAME} ${balaev_a_a})
target_link_libraries(${PROJECT_NAME} PRIVATE Qt5::Widgets Qt5::PrintSupport)