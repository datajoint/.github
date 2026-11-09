# Welcome to DataJoint!

The **DataJoint Library** is a Python framework for scientific data pipelines built on the **Relational Workflow Model**, a paradigm in which your database schema is an executable specification of your workflow.

- **Tables represent workflow steps**: each table is a step in your pipeline.
- **Foreign keys encode dependencies**: parent tables are populated before their children.
- **Computations are declarative**: you define *what* to compute, and DataJoint handles *when*.
- **Results are immutable**: every result traces back to its declared inputs.

This organization hosts the DataJoint Library ([datajoint-python](https://github.com/datajoint/datajoint-python)), its [documentation](https://github.com/datajoint/datajoint-docs), codec plugins, and example pipelines.

## Example pipeline

![Example DataJoint pipeline](https://raw.githubusercontent.com/datajoint/datajoint-python/master/images/pipeline.svg)

**Cite DataJoint:** [Yatsenko et al., 2026, *DataJoint 2.0: A Computational Substrate for Agentic Scientific Workflows*](https://arxiv.org/abs/2602.16585). RRID: [SCR_014543](https://scicrunch.org/resolver/SCR_014543)

## Getting started

```bash
pip install datajoint
```

or with Conda:

```bash
conda install -c conda-forge datajoint
```

- **[Documentation](https://docs.datajoint.com)**: tutorials, how-to guides, explanations and API reference
  - [Installation](https://docs.datajoint.com/how-to/installation/)
  - [Tutorials](https://docs.datajoint.com/tutorials/)
  - [Migration Guide](https://docs.datajoint.com/how-to/migrate-to-v20/): upgrading pipelines from DataJoint before 2.0
- **[DataJoint Elements](https://docs.datajoint.com/elements/)**: example pipelines for neuroscience experiments
- **[GitHub Discussions](https://github.com/datajoint/datajoint-python/discussions)**: questions and community support
