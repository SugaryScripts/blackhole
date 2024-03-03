

### Creating a Virtual Environment

Bash

```
python3 -m venv my_venv  # Replace "my_venv" with your desired name
```

Use code [with caution.](https://gemini.google.com/faq#coding)

content_copy

This command creates a new virtual environment named "my_venv" in the current directory using the standard library module `venv`.

**Explanation:**

- `python3` specifies the Python interpreter to use (replace with `python` if you only have Python 2).
- `-m venv` tells Python to execute the `venv` module.
- `"my_venv"` is the name you choose for your virtual environment directory.

### Activating the Virtual Environment

**Windows:**

Bash

```
my_venv\Scripts\activate.bat
```

Use code [with caution.](https://gemini.google.com/faq#coding)

content_copy

**macOS/Linux:**

Bash

```
source my_venv/bin/activate
```

Use code [with caution.](https://gemini.google.com/faq#coding)

content_copy

This command activates your virtual environment. The specific command depends on your operating system.

**Explanation:**

- Activates the virtual environment, making its installed packages available within your shell session.
- The path to the activation script will vary depending on your OS.

**Note:** After activation, your shell prompt will typically change to indicate you're in the virtual environment (e.g., `(my_venv)user@machine:`).

### Installing Packages

Bash

```
pip install <package_name>
```

Use code [with caution.](https://gemini.google.com/faq#coding)

content_copy

This command installs a specific Python package into your virtual environment's isolated directory.

**Explanation:**

- `<package_name>` is the name of the package you want to install (e.g., `requests`, `numpy`).
- `pip` is the package installer included with Python.
- Packages are installed within the virtual environment, keeping them separate from system-wide installations.

### Deactivating the Virtual Environment

Bash

```
deactivate
```

Use code [with caution.](https://gemini.google.com/faq#coding)

content_copy

This command deactivates the virtual environment, returning you to your system's default Python environment.

**Explanation:**

- Deactivate the environment when you're finished working on your project to avoid using the virtual environment's packages unintentionally.

**Tip:** Consider creating a bash script or alias to automate the activation and deactivation process for your virtual environment.