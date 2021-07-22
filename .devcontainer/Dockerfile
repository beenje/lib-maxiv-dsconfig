FROM condaforge/mambaforge

# Python 3.6 environment
RUN mamba create -y -p /py36 \
  python=3.6 \
  pytango \
  jsonpatch>=1.13 \
  jsonschema \
  six \
  xlrd \
  pytest \
  pytest-cov \
  faker \
  mock \
  && conda clean -ay

# Python 2.7 environment
# tango-controls is required for Python 2.7
RUN mamba create -y -c conda-forge -c tango-controls -p /py27 \
  python=2.7 \
  pytango \
  jsonpatch>=1.13 \
  jsonschema \
  six \
  xlrd \
  pytest \
  pytest-cov \
  faker \
  mock \
  && conda clean -ay
