# adalib examples

This repository contains Jupyter Notebooks demonstrating how to use `adalib`. Each Notebook contains a detailed explanation of how to use one specific function. Thus, they can be readily used to explore `adalib` functionalities or as a starting point for your own creations.

## For regular users

Functions accessible to regular users, such as interacting with cards and apps, can be found under [user/](user/).

## For administrators and curators

On top of what regular users can do, AdaLab platform administrators and curators can take actions related to platform management. Examples for these can be found under [admin/](admin/).

## Requirements

In order to use these examples, you will need to have `adalib` and `adalib-auth` installed. Note that you should always use the version (tag) of this repository which matches your `adalib` version.

If your code is executed outside AdaLab (e.g., your local computer, a CI/CD pipeline), you first need to obtain the JupyterHub secret from your user Lab. To do so, execute the following script in your Lab:

```python
from adalib_auth.config import get_config
adalib_config = get_config()
print(adalib_config.KEYCLOAK_CLIENTS['jupyterhub_secret'])
```

Then, in the machine where `adalib` is used, export it to an environment variable called `ADALAB_CLIENT_SECRET`.
