if(QT_KNOWN_POLICY_QTP0001)
    qt_policy(SET QTP0001 NEW)
    # the RESOURCE_PREFIX argument for qt_add_qml_module() defaults to ":/qt/qml/"
endif()
if(POLICY CMP0071)
    # https://cmake.org/cmake/help/latest/policy/CMP0071.html
    cmake_policy(SET CMP0071 NEW)
endif()




find_package(Dtk6 REQUIRED COMPONENTS Core Declarative SystemSettings Tools)
