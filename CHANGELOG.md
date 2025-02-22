CHANGELOG
=========

0.3.1 - 2023-09-26
------------------

Make sure async session is still open when we call .all()

Contributed by [mattalbr](https://github.com/mattalbr) via [PR #55](https://github.com/strawberry-graphql/strawberry-sqlalchemy/pull/55/)


0.3.0 - 2023-09-26
------------------

Adds support for async sessions. To use:

```python
from sqlalchemy.ext.asyncio import async_sessionmaker, create_async_engine
from strawberry_sqlalchemy_mapper import StrawberrySQLAlchemyLoader

url = "postgresql://..."
engine = create_async_engine(url)
sessionmaker = async_sessionmaker(engine)

loader = StrawberrySQLAlchemyLoader(async_bind_factory=sessionmaker)
```

Contributed by [mattalbr](https://github.com/mattalbr) via [PR #53](https://github.com/strawberry-graphql/strawberry-sqlalchemy/pull/53/)


0.2.1 - 2023-09-21
------------------

Fix typo in pyproject.toml for poetry build.

Contributed by [Dan Sully](https://github.com/dsully) via [PR #52](https://github.com/strawberry-graphql/strawberry-sqlalchemy/pull/52/)


0.2.0 - 2023-09-15
------------------

Native SQLAlchemy JSON Conversion Support. Added native support for SQLAlchemy JSON conversions. Now, you'll find that `sqlalchemy.JSON` is converted to `strawberry.scalars.JSON` for enhanced compatibility.

Contributed by [Luis Gustavo](https://github.com/Ckk3) via [PR #40](https://github.com/strawberry-graphql/strawberry-sqlalchemy/pull/40/)


0.1.4 - 2023-09-11
------------------

Makes a series of minor changes to fix lint errors between MyPy and Ruff.

Contributed by [mattalbr](https://github.com/mattalbr) via [PR #38](https://github.com/strawberry-graphql/strawberry-sqlalchemy/pull/38/)


0.1.3 - 2023-09-11
------------------

Fixes a bug where an Interface is not properly registered, resulting in an infinite-loop for mapping Interfaces to polymorphic Models.

Contributed by [Layton Wedgeworth](https://github.com/asimov-layton) via [PR #24](https://github.com/strawberry-graphql/strawberry-sqlalchemy/pull/24/)


0.1.2 - 2023-09-08
------------------

Dependency version changes needed for python 3.12 compatibility.

Contributed by [mattalbr](https://github.com/mattalbr) via [PR #35](https://github.com/strawberry-graphql/strawberry-sqlalchemy/pull/35/)


