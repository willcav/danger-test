MAX_LINES_CHANGED = 1

def check_lines_changed
  total_lines_changed = git.lines_of_code
  if total_lines_changed > MAX_LINES_CHANGED
    warn("Seu PR excede o número máximo de linhas (#{MAX_LINES_CHANGED}). Por favor, considere dividí-lo em PRs menores.")
  end
end

check_lines_changed
