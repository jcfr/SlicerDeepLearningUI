cmake_minimum_required(VERSION 3.13.4)

project(DeepLearningWizard)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/mturja-vf-ic-bd/SlicerDeepLearningUI#readme")
set(EXTENSION_CATEGORY "Machine Learning")
set(EXTENSION_CONTRIBUTORS "Md Asadullah Turja (University of North Carolina at Chapel Hill)")
set(EXTENSION_DESCRIPTION "This extension enables the user to run complex deep learning models for medical image classification using a simple UI without the need to understand any code.")
set(EXTENSION_ICONURL "https://raw.githubusercontent.com/mturja-vf-ic-bd/SlicerDeepLearningUI/main/DeepLearningUI.png")
set(EXTENSION_SCREENSHOTURLS
  "https://raw.githubusercontent.com/mturja-vf-ic-bd/SlicerDeepLearningUI/main/screenshot.png"
  "https://raw.githubusercontent.com/mturja-vf-ic-bd/SlicerDeepLearningUI/main/SurfaceLearnerOverviewImage.png"
  "https://raw.githubusercontent.com/mturja-vf-ic-bd/SlicerDeepLearningUI/main/SurfaceLearnerWorkflow.png"
)
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(DeepLearner)
add_subdirectory(Deep)
add_subdirectory(Inference)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
