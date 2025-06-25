# Copilot Instructions

Please generate Python code that always satisfies Pylance **strict** mode (`python.analysis.typeCheckingMode = "strict"`). Ensure all functions, variables, and generics are fully annotated and no type errors remain.

- Always check the 'from typing import ...' line for unused imports and remove them.
- Always use logging instead of print statements for debugging and information output. Use the `logging` module's functions like `logging.debug()`, `logging.info()`, etc. Set appropriate logging levels and ensure log messages are clear and actionable.
- All code must include comprehensive error checking and exception handling. Catch specific exceptions, never use bare `except` clauses, and always log errors using the `logging` module. Where appropriate, re-raise exceptions after logging or handle them gracefully to ensure program stability.
- All functions and classes must include detailed docstrings explaining their purpose, parameters, return values, exceptions raised, and usage examples if relevant. Use type hints for all function parameters and return types.
- When writing tests, ensure they are comprehensive and cover edge cases, normal cases, and failure scenarios. Use `unittest` or `pytest` frameworks, and always include assertions to verify expected outcomes. Tests must be self-contained, repeatable, and should not rely on external state unless explicitly required.
- For any new feature or code modification, automatically generate or update corresponding tests to fully verify the new or changed functionality. Ensure that all code paths, including error and edge cases, are tested.
- When working with databases, files, or external resources, always handle exceptions gracefully, log errors, and ensure resources are properly closed or cleaned up (using context managers where possible).
- When writing scripts that interact with the command line or user input, always validate inputs, handle potential errors, and provide helpful error messages. Use `argparse` or similar libraries for command-line argument parsing.
- After making any code changes, always determine if the README.md or other documentation files need to be updated to reflect the changes made in the code. Update usage examples and API documentation as needed.
- Ensure that all code is modular, readable, and follows PEP 8 style guidelines. Refactor duplicated or complex code into reusable functions or classes.
- For any configuration, secrets, or credentials, never hard-code values in the codebase. Use environment variables or configuration files, and document their usage.
- When adding new dependencies, update the requirements.txt or pyproject.toml file accordingly and document any installation or setup steps required.
- For public APIs or libraries, ensure that versioning and backward compatibility are considered and documented.
- Before finalizing changes, run all tests and static analysis tools (e.g., mypy, flake8, pylint) to ensure code quality and correctness.