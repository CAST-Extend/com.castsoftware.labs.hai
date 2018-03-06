# _com.castsoftware.labs.hai_ Description

This extension provides computation of the following new assessment indicator\(s\)

* the _High Availability index_
* supporting Technical Criteria

## Problem Statement

Assessing the risks of software downtime based on its structural quality. Software is obviously only part of the whole High Availability topic but it's a key element. Most hardware-based failover solutions are here to recover from a downtime. This assessment is about preventing such downtime.

## Research Labs proposal

The Research Labs offer a solution based on CAST AIP Assessment Model, following a Goal-Question-Metric approach.

* The _High Availability Index_ goal, modeled as a Business Criterion, is based on the answers to the following four questions:
* The _HA - detect and handle failures_ question: is the software detecting and handling errors and exceptions ?
* The _HA - external threats mitigation_ question: is the software protecting itself agains malevolent actions from external actors ?
* The _HA - unexpected workload mitigation_ question: is the software ready to accomodate unexpected surge in workload ?
* The _HA - internal failure mitigation_ question: is the software using structural coding patterns that are known to cause functional failures ? 
  
The Research Labs released this first version of the High Availability Index to leverage the expertise and experience of customers in order to fine-tune its exact composition and collect feedback.

## Formula

The High Availability Index is based on the following Technical Criteria

* HA - detect and handle failures
* HA - external threats mitigation
* HA - unexpected workload mitigation
* HA - internal failure mitigation


# In what situation should you install this extension?

If you are interested in getting a preview of what the High Availability Index would be and are willing to share the results to help the CAST Research Labs validate them.

# Release notes

## 1.0.0
Initial release.

# _com.castsoftware.labs.hai_ technology support

All technologies supported out-of-the-box by CAST AIP are supported.
In case of technologies supported by some AIP extensions, the selection of Quality Rules to contribute to the dedicated new Technical Criteria will have to take place.

# Function Point, Quality and Sizing support

This extension is designed to bring new quality indicators aside existing ones.

# CAST AIP compatibility

This extension is compatible with:

* 8.2.x out-of-the-box \(AIP release 8.2.0 used for the tests\)

# Supported DBMS servers

This extension is currently supported on any CAST databases \(CAST Storage Service used for the tests\).

# Prerequisites

* An installation of any compatible release of CAST AIP \(see support information above\)

# Bug Fix List

N\/A

# Download and installation instructions

Please see:  [Extension Link Installation](http://doc.castsoftware.com/display/DOCEXT/Extension+download+and+installation)

The installation steps are the following:

* download the extension through the CAST Extend server (https://extend.castsoftware.com) or the CAST Extension Downloader using the https://extend.castsoftware.com:443/labs download server
* open Server Manager 8.2+
* select the existing set of databases to update \/ install a new set of databases
* manage extensions of the existing set of database \/ follow the installation wizard up to the manage extension pane
* select _com.castsoftware.labs.hai_ version _1.0.0_
* run the update \/ the installation  
* open CAST Management Studio
* import the Assessment Model from the Dashboard Service processed in steps \#3 to \#6 above; this is a _Mandatory_ step to start computing the new indicator, one MUST import and use the Assessment Model from the Dashboard that was updated with the extension
* to allow investigation along the High Availability Index findings in CAST AED, you need to change the "filterHealthFactor" parameter from the ..\\engineering\\resources\\ced.json web application configuration file to "false" from "true"
* to offer a direct access to High Availability Index analytics in CAST AAD, you need to add "QualityIndicatorResult" and "QualityIndicatorResults" tiles targeting the ID 2027005 in ..\\portal\\resources\\app.json and ..\\portal\\resources\\cmp.json web application configuration files

# Packaging, delivering and analyzing your source code

Packaging, delivering and analyzing your source code is performed the same way as usual.

To get results:

* run a new snapshot \/ consolidate existing snapshot(s) 

To avoid computing the High Availability Index for applications whose continuous availability is not required:

* open CAST Management Studio
* edit the Dashboard Service\(s\) you are publishing the Snapshots of the N\/A application\(s\)
* select the Assessment Model tab
* create an exclusion for the High Availability index and the N\/A application\(s\)

# What results can you expect?

## Objects

N\/A

## Links

N\/A

## Quality rules

N\/A

## Technical Criteria

List of new Technical Criteria

* HA - detect and handle failures
* HA - external threats mitigation
* HA - unexpected workload mitigation
* HA - internal failure mitigation

## Business Criteria

List of new Business Criteria

* High Availability index

# Limitations

N\/A
