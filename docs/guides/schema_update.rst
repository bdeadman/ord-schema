// a guide to docuemnt ORD best practice in making changes to the schema, and propagating these through to dependent ORD packages.

*************************************************************
Procedures for Making Additions or Updates to the ORD Schema
*************************************************************
The ORD Schema is an evolving standard. This guide documents best practices for making changes to the schema.


********************************************
Step 1: Preparations
********************************************

Consider the following:

* How is the data currently structured in the ORD Schema?
* How do synthesis chemists or ML scientists expect the data to be labelled?
* Will existing ORD records be updated accordingly?


Please do the following preparation:

1. Please discuss your proposed edits with the ORD team first.
2. Please work on a fork of the ord-schema.
3. For complex changes it is advisable to work in a branch of your fork.


********************************************
Step 2: Make Changes to the Proto Files
********************************************

to be added

********************************************
Step 3: Rebuild the Protocol Buffer Wrappers
********************************************

If you make changes to the protocol buffer definitions then you need to re-compile the proto wrappers and run the format tests. Ensure that you have protoc, protobuf-javascript and go installed (`installation notes <editable_schema_install_notes.html>` `Overview of the ORD <editable_schema_install_notes.html>`_). Then run the following from your ord-schema directory:

.. code-block::

    ./compile-proto-wrappers.sh
    ./format.sh

This should update the following files:

* js/ord-schema/proto/dataset_pb.js
* js/ord-schema/proto/reaction_pb.js
* js/ord-schema/proto/test_pb.js
* ord_schema/proto/dataset_pb2.py
* ord_schema/proto/reaction_pb2.py
* ord_schema/proto/test_pb2.py

From Git changes can be committed to your branch and then pushed to the branch on origin.


********************************************
Step 4: Push Update to ord-schema
********************************************

to be added

********************************************
Step 5: Update ord-interface?
********************************************

to be added

********************************************
Step 6: Update existing ord records?
********************************************

to be added
