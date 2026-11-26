petstore
========

A tiny Python client for the Fixture API (``openapi.yaml``), used to test NOT-IN-SPEC itself.

.. py:module:: petstore

.. py:function:: get_pet(pet_id: int, *, timeout: float = 10.0) -> dict

   Fetch one pet by its ID with ``GET /pets/{petId}``.

   :param pet_id: ID of the pet, an integer.
   :param timeout: Seconds to wait for the server.
   :returns: The pet as a dict with the keys ``id`` and ``name``.
   :raises KeyError: If no pet has this ID.

Example::

   import petstore

   pet = petstore.get_pet(1)
   print(pet["name"])
