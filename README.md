#########################
# .gitignore file for Xcode4 / OS X Source projects
#
# NB: if you are storing "built" products, this WILL NOT WORK,
#   and you should use a different .gitignore (or none at all)
# This file is for SOURCE projects, where there are many extra
#   files that we want to exclude
#
# For updates, see: http://stackoverflow.com/questions/49478/git-ignore-file-for-xcode-projects
#########################

#####
# OS X temporary files that should never be committed

.DS_Store
*.swp
profile


####
# Xcode temporary files that should never be committed
#
# NB: NIB/XIB files still exist even on Storyboard projects, so we want this...

*~.nib


####
# Xcode build files -
#
# NB: slash on the end, so we only remove the FOLDER, not any files that were badly named "DerivedData"

DerivedData/

# NB: slash on the end, so we only remove the FOLDER, not any files that were badly named "build"

build/


#####
# Xcode private settings (window sizes, bookmarks, breakpoints, custom executables, smart groups)
#
# This is complicated:
#
# SOMETIMES you need to put this file in version control.
# Apple designed it poorly - if you use "custom executables", they are
#  saved in this file.
# 99% of projects do NOT use those, so they do NOT want to version control this file.
#  ..but if you're in the 1%, comment out the line "*.pbxuser"

*.pbxuser
*.mode1v3
*.mode2v3
*.perspectivev3
#    NB: also, whitelist the default ones, some projects need to use these
!default.pbxuser
!default.mode1v3
!default.mode2v3
!default.perspectivev3


####
# Xcode 4 - semi-personal settings, often included in workspaces
#
# You can safely ignore the xcuserdata files - but do NOT ignore the files next to them
#

xcuserdata

####
# XCode 4 workspaces - more detailed
#
# Workspaces are important! They are a core feature of Xcode - don't exclude them :)
#
# Workspace layout is quite spammy. For reference:
#
# (root)/
#   (project-name).xcodeproj/
#     project.pbxproj
#     project.xcworkspace/
#       contents.xcworkspacedata
#       xcuserdata/
#         (your name)/xcuserdatad/
#     xcuserdata/
#       (your name)/xcuserdatad/
#
#
#
# Xcode 4 workspaces - SHARED
#
# This is UNDOCUMENTED (google: "developer.apple.com xcshareddata" - 0 results
# But if you're going to kill personal workspaces, at least keep the shared ones...
#
#
!xcshareddata

####
# XCode 4 build-schemes
#
# PRIVATE ones are stored inside xcuserdata
!xcschemes

####
# Xcode 4 - Deprecated classes
#
# Allegedly, if you manually "deprecate" your classes, they get moved here.
#
# We're using source-control, so this is a "feature" that we do not want!

*.moved-aside

# CocoaPods
/Pods
