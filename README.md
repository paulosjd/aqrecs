
Source code for a prototype API which supports GraphQL operations as well as REST.
It is written in Python and libraries used include Pyramid and graphene-sqlalchemy.
Schema revolves around hourly recorded measurements taken sites 
within an automated air pollution monitoring network.

# todo add equivalent REST endpoints


For database setup, run alembic -c development.ini init alembic
In the env.py file that get after , update like:

# add your model's MetaData object here
# for 'autogenerate' support
from pyratest.models.meta import Base
target_metadata = Base.metadata

alembic -c development.ini revision --autogenerate -m "some message"   and upgrade head
