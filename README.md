# 2do projects

2do is an ecosystem of tools allowing to manage events in an OpenSimulator.
It is composed of several elements, depending of the way you want to implement it.

This repository contains no code, only the information about the related projects.

## 1. 2do-board

This is were it all began. A scripted object in-world, displaying ongoing and upcoming 
events, allowing teleport. By default, it is set to use 2do.directory service, but it can
be customize with the tools below. It can be used on any region, regardless of the
implementation of search or not on the grid, but requires OSSL draw functions to be function.

- https://github.com/GuduleLapointe/2do-board

## 2. 2do.directory

The easiest way to enable in-world search (including events) is to configure the simulators
to use 2do.directory services. It only requires the addition of OpenSimSearch.dll in OpenSimulator
bin folder and a few configuration lines in OpenSim.ini. Search is provided by 2do.directory
website and allow sharing of hypergrid destinations. It avoids the need to install helpers.

- https://2do.directory/

## 3. OpenSim Helpers

Installing your own helpers allow to use your own databases for search and events. It is 
relevant for private or associated grids, or to setup and alternate shared directory.
Currently, due to OpenSimulator and/or viewer limitations, searching classifieds require
a direct access to the Robust database, so to enable them, installing helpers specific to
the grid is necessary.

A local installation of OpenSimulator helpers can be combined with the use of an external
events provider like 2do.directory.

- https://opensim-helpers.dev/ standalone helpers
- https://w4os.org/ full OpenSimulator web interface, including helpers

## 4. 2do-aggregator

To providde your own events server. Collects events from different sources and made
them available to the search engine and in-world boards. It is usually not necessary
to install your own implementation, the service is offered by 2do.directory.

- https://github.com/GuduleLapointe/2do-aggregator

## Deprecated

- 2do-server: the previous aggregator, written in python 2.7 and forked from Tom Frost's
HypEvents abandonned project, replaced by 2do-aggreagator
- 2do-search: another implementation of search engine, focused on events. Replaced
by opensim-helpers
