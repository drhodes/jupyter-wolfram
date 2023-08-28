SHELL=bash

# -----------------------------------------------------------------------------
# Section: Python

# Ensure the system python is not used, maintain a virtual
# environment.

VENV = source .venv/bin/activate &&

# to run a python script use the following incantation:
#   ${PY} a-python-script.py

PY = ${VENV} python3

.venv: ## establish a virtual environment for python
	python3 -m venv .venv && \
	${VENV} pip install jupyter
	touch .venv

run: .venv
	${VENV} jupyter notebook
