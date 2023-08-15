# Python Pipeline Source Template

Template for a custom Python-based pipeline source that hooks into OVITO and can easily be shared with other users.

This repository contains a template for creating your own [Python script pipeline source](https://www.ovito.org/docs/current/reference/pipelines/data_sources/python_script.html#what-is-a-python-data-source), 
which can be installed into *OVITO Pro* or the [`ovito`](https://pypi.org/project/ovito/) Python module using *pip*. In opposite to using file-based pipeline sources, the python script piplines source allows you to generate ad-hoc contents direclty in OVITO.

## Getting Started

1. Click the "Use this template" button to create your own repository based on this template.
2. Rename `src/PackageName` to reflect the name of your pipeline source.
3. Implement your [custom pipeline source](https://www.ovito.org/docs/current/python/modules/ovito_pipeline.html#ovito.pipeline.PipelineSourceInterface) in [`src/PackageName/__init__.py`](src/PackageName/__init__.py). When you implement only the `create` method, just one static configuration (frame 0) will be generated. To generate a trajectory instead refer to the [`PipelineSourceInterface.compute_trajectory_length`](https://www.ovito.org/docs/current/python/modules/ovito_pipeline.html#ovito.pipeline.PipelineSourceInterface.compute_trajectory_length) method as explained in the OVITO Python docs.
4. Fill in the [`pyproject.toml`](pyproject.toml) file. Fields that need to be replaced with your information are enclosed in descriptive `[[field]]` tags. Please make sure to include ovito>=3.9.2 as a dependency. Depending on your needs, you can add additional fields to the `pyproject.toml` file. Information can be found [here](https://setuptools.pypa.io/en/latest/userguide/index.html).
5. Fill in the [`README_Template.md`](README_Template.md) file. Again, the `[[fields]]` placeholders should guide you. Feel free to add other sections like "Images", "Citation", or "References" as needed.
6. Add meaningful examples and data sample files to the `examples` directory to help others understand the use of your modifier.
7. Pick a license for your project and replace the current (MIT) [`LICENSE`](LICENSE) file with your license. If you keep the MIT license, please update the name and year in the current file.
8. Once you're done, rename `README_Template.md` to `README.md`, replacing this file.
