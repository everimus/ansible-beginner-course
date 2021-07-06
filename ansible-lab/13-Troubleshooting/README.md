# Ansible Troubleshooting

- Use `debug` module
- Use verbosity levels
- Include comments and proper names for tasks
- `--check` and `--diff` option
- `--syntax-check`
- `fail` and `uri` module
- Use name and `ansible_host` to identify nodes
- Check with adhoc commands 
- 

## Task: Check and Fail

- Check the url `http://node` and fail the task if the return content doesnt contain the word `version`