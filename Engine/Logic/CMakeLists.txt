set(LOGIC_SOURCES
    src/Entity.cpp
    src/TransformComponent.cpp
    src/RenderComponent.cpp
    src/Scene.cpp
    src/SceneManager.cpp
    src/DemoScene.cpp
    src/PhysicsTestScene.cpp
    src/SimplePhysicsComponent.cpp
    src/CollisionComponent.cpp
    src/CollisionSystem.cpp
    src/ParticleScene.cpp
)

set(LOGIC_HEADERS
    include/Component.h
    include/Entity.h
    include/TransformComponent.h
    include/RenderComponent.h
    include/Scene.h
    include/SceneManager.h
    include/DemoScene.h
    include/PhysicsTestScene.h
    include/SimplePhysicsComponent.h
    include/CollisionComponent.h
    include/CollisionSystem.h
    include/ParticleScene.h
)

add_library(Logic STATIC ${LOGIC_SOURCES} ${LOGIC_HEADERS})

target_include_directories(Logic
    PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

target_link_libraries(Logic
    PUBLIC
        Common
)
