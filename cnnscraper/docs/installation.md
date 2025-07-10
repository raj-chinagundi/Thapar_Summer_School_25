# Installation

This project requires Python 3.x.

## Dependencies

The project dependencies are listed in `requirement.txt`.

To install them, navigate to the project root directory in your terminal and run:

```bash
pip install -r requirement.txt
```

This will install:
- `beautifulsoup4`: For parsing HTML and XML documents.
- `requests`: For making HTTP requests.
- `regex`: A regular expression module for more advanced pattern matching.

!!! note "Virtual Environment Recommended"
    It is highly recommended to use a virtual environment to manage project dependencies to avoid conflicts with other Python projects.
    ```bash
    # Create a virtual environment
    python -m venv .venv
    # Activate the virtual environment
    source .venv/bin/activate # On Windows: .venv\Scripts\activate
    # Install dependencies within the active environment
    pip install -r requirement.txt
    ```
    Remember to activate the environment each time you work on the project.