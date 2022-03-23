{% set is_open_source = cookiecutter.open_source_license != 'Not open source' -%}
{% for _ in cookiecutter.project_name %}={% endfor %}
{{ cookiecutter.project_name }}
{% for _ in cookiecutter.project_name %}={% endfor %}

{% if is_open_source %}

.. image:: https://img.shields.io/pypi/v/{{ cookiecutter.project_slug }}
        :target: https://pypi.python.org/pypi/{{ cookiecutter.project_slug }}
{%- if cookiecutter.use_pytest == 'y' %}

.. image:: https://img.shields.io/travis/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}.svg
        :target: https://travis-ci.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}
{%- endif %}

.. image:: https://readthedocs.org/projects/{{ cookiecutter.project_slug | replace("_", "-") }}/badge/?version=latest
        :target: https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io/en/latest/?version=latest
        :alt: Documentation Status

.. image:: https://img.shields.io/pypi/pyversions/{{ cookiecutter.project_slug }}
        :target: https://pypi.python.org/pypi/{{ cookiecutter.project_slug }}
        :alt: Python Version Support

.. image:: https://img.shields.io/github/issues/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}
        :target: https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/issues
        :alt: GitHub Issues

.. image:: https://img.shields.io/github/followers/{{ cookiecutter.github_username }}?style=social
        :target: https://github.com/{{ cookiecutter.github_username }}
        :alt: GitHub Followers
{%- endif %}
{% if cookiecutter.add_twitter_badge == 'y' %}

.. image:: https://img.shields.io/twitter/follow/hrishikeshrt?style=social
        :target: https://twitter.com/hrishikeshrt
        :alt: Twitter Followers
{% endif %}
{% if cookiecutter.add_pyup_badge == 'y' %}

.. image:: https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/shield.svg
     :target: https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/
     :alt: Updates
{% endif %}

{{ cookiecutter.project_short_description }}

{% if is_open_source %}
* Free software: {{ cookiecutter.open_source_license }}
* Documentation: https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io.
{% endif %}

Features
========

* TODO

Install
=======

To install {{ cookiecutter.project_name }}, run this command in your terminal:

.. code-block:: console

    $ pip install {{ cookiecutter.project_slug }}

Credits
=======

This package was created with Cookiecutter_ and the `hrishikeshrt/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`hrishikeshrt/cookiecutter-pypackage`: https://github.com/hrishikeshrt/cookiecutter-pypackage
