MAX_LINES_CHANGED = 5
added_lines = diff.added_lines
deleted_lines = diff.deleted_lines

warn(added_lines)
warn(deleted_lines)

def check_lines_changed
  lines_changed = added_lines + deleted_lines
  if lines_changed > MAX_LINES_CHANGED
      warn("Seu PR excede o limite de #{MAX_LINES_CHANGED} linhas alteradas. Considere dividi-lo PRs menores.")
  end
end