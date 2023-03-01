require 'danger'

MAX_LINES_CHANGED = 1

added_lines = git.lines_of_code.added
deleted_lines = git.lines_of_code.deleted

total_lines_changed = added_lines + deleted_lines

if total_lines_changed > MAX_LINES_CHANGED
  warn("Your changes exceed the maximum allowed number of lines (100). Please consider splitting them into smaller changesets.")
end