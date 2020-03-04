#
#  Dangerfile
#
#  Copyright (c) 2019 Netguru Sp. z o.o. All rights reserved.
#

# Running SwiftLint
swiftlint.config_file = '.swiftlint.yml'
swiftlint.lint_files
the_coding_love.random
# xcode_outdated.warn_on_mondays

warn("lol")

app_implementation_changed = !git.modified_files.grep(/XcodeOutdatedExample/).empty?
app_tests_implementation_changed = !git.modified_files.grep(/XcodeOutdatedExampleTests/).empty?

if app_implementation_changed && !app_tests_implementation_changed
  warn("App target has changed. Relevant test target has not been updated", sticky: false)
end
