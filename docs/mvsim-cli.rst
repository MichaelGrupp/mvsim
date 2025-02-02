mvsim cli
===================

The command-line interface (cli) application ``mvsim`` is the main
entry-point to run, query, or modify a running simulation from a 
command line terminal. It can be used to launch standalone simulations (without ROS), 
or to modify, manipulate, or query a running simulation within a ROS system.

.. note::
   The ROS node is a different cli application, named ``mvsim_node`` instead.
   The ROS package ``mvsim`` ships **both** executables: ``mvsim`` and ``mvsim_node``.
   See :ref:`mvsim ROS node`.

Invoking ``mvsim``
------------------------
Make sure you have compiled or installed MVSim, and that the executable named ``mvsim`` is 
in your ``PATH``. If you installed it as a ROS package, activating the ROS environment (``setup.bash``) is enough.

If this command works, you can go on with the next commands:

.. code-block:: console

   $ mvsim --version

You can get a list of available commands with:

.. code-block:: console

   $ mvsim --help
   mvsim v0.7.2: A lightweight multivehicle simulation environment.

   Available commands:
      mvsim launch <WORLD.xml>  Start a comm. server and simulates a world.
      mvsim server              Start a standalone communication server.
      mvsim node                List connected nodes, etc.
      mvsim topic               Inspect, publish, etc. topics.
      mvsim --version           Shows program version.
      mvsim --help              Shows this information.

   Or use `mvsim <COMMAND> --help` for further options


Command ``mvsim launch``
--------------------------

.. code-block:: console

   $ mvsim launch --help
   Usage: mvsim launch <WORLD_MODEL.xml> [options]

   Available options:
   --headless              Launch without GUI (e.g. suitable for dockerized envs.)
   --full-profiler         Enable full profiling (generates file with all timings)
   --realtime-factor <1.0> Run slower (<1) or faster (>1) than real time if !=1.0
   -v, --verbosity         Set verbosity level: DEBUG, INFO (default), WARN, ERROR


Write me!


Command ``mvsim server``
--------------------------

.. code-block:: console

   $ mvsim server --help
   Usage: mvsim server

   Available options:
   -p 23700, --port 23700   Listen on given TCP port.
   -v, --verbosity      Set verbosity level: DEBUG, INFO (default), WARN, ERROR


Write me!


Command ``mvsim node``
--------------------------

.. code-block:: console

   $ mvsim node --help
   Usage:

      mvsim node --help     Show this help
      mvsim node list       List all nodes connected to the server.

Write me!


Command ``mvsim topic``
--------------------------

.. code-block:: console

   $ mvsim topic --help
   Usage:

      mvsim topic --help            Show this help
      mvsim topic list [--details]  List all advertised topics in the server
      mvsim topic echo <topicName>  Subscribe and print a topic
      mvsim topic hz <topicName>    Estimate topic publication rate (in Hz)

Write me!


