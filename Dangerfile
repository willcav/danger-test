require 'danger/changeset'

MAX_LINES_CHANGED = 5
changeset = Danger::Changeset.new


def check_lines_changed()
  added_lines = changeset.added_lines
  deleted_lines = changeset.deleted_lines
  message(added_lines)
  message(deleted_lines)
  lines_changed = added_lines + deleted_lines
  if lines_changed > MAX_LINES_CHANGED
      warn("Seu PR excede o limite de #{MAX_LINES_CHANGED} linhas alteradas. Considere dividi-lo PRs menores.")
  end
end

check_lines_changed()