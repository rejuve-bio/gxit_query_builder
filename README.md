# Planemo Galaxy Tool: Visual Query Builder Wrapper

This repository contains a Galaxy wrapper for Rejuve's Visual Query Builder for Human BioAtomspace, designed to be tested and deployed using [Planemo](https://planemo.readthedocs.io/) and the Galaxy ToolShed.

---

## 📦 Setup: Create `.venv` and Install Dependencies

### 1. Create a virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate
````

### 2. Install Planemo and required tools

```bash
pip install planemo
```

To verify installation:

```bash
planemo --version
```

---

---

## 🚀 Uploading to the ToolShed

### Tool Shed Targets

* **Test Tool Shed**: `https://testtoolshed.g2.bx.psu.edu/`
* **Main Tool Shed**: `https://toolshed.g2.bx.psu.edu/`

### Upload to the Test Tool Shed

```bash
make upload-test
```

Or update an existing tool:

```bash
make update-test
```

### Upload to the Main Tool Shed

```bash
make upload-shed
```

Or update an existing tool:

```bash
make update-shed
```

---

## 📁 Project Structure

```
.
├── planemo.xml               # Your Galaxy tool definition
├── shed.yml               # Metadata for Tool Shed
├── scripts/
│   ├── test_tools.sh      # Script to test the tool
│   ├── upload_shed.sh     # Script to upload to Tool Shed
│   └── update_shed.sh     # Script to update Tool Shed
├── Makefile               # Task runner for test/upload
└── README.md              # This file
```

---

## 🧰 Makefile Variables

You can adjust the following variables in the `Makefile`:

```make
TEST_SHED = testtoolshed      # Upload/update target for testing
MAIN_SHED = toolshed          # Upload/update target for production
GALAXY_ROOT = $(shell pwd)/scripts/
VERSION = 0.0.1
```

---

## ✅ Requirements

* Python 3.7+
* Bash (for shell scripts)
* [Planemo](https://planemo.readthedocs.io/en/latest/)
* Galaxy installation (for advanced testing, optional)

---
