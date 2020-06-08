---
title: '\[Summary / title goes here\]'
---

**Investigation driver: Hector LeMans**

**Investigation contributors:**

**Last Update:** 2020-06-09\
**Status: Reviewed\
Start time: 2018-01-10 00:30\
End time: 2018-01-10 08:50**

**Duration: 08:20**

**TTR SLA: 2H**

**Severity Index: 1.11675**

**Severity: Critical**

**Table of contents**

1 History 1

2 Impact 1

3 Root Cause(s) 1

4 Trigger 1

5 Resolution 2

6 Detection 2

7 Affected Business Units 2

8 Affected Services 2

9 Timeline 2

10 Action Items 2

11 Glossary 3

12 Appendix 3

History
=======

  ------------- ------------ -------------------- -------------
  **Version**   **Date**     **Author**           **Comment**
  0.1           2018-01-11   **Merche Colomar**   Draft
  0.2           2018-01-12   **Manny Calavera**   Review
  ------------- ------------ -------------------- -------------

Impact
======

  **Type**       **Yes / No**   **Estimated loss**
  -------------- -------------- --------------------------
  Operational                   500K queries to database
  Financial                     \$2 000 000,00
  Reputational                  

Root Cause(s)
=============

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
occaecat cupidatat non proident, sunt in culpa qui officia deserunt
mollit anim id est laborum.

Trigger
=======

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
velit esse cillum dolore eu fugiat nulla pariatur

Resolution
==========

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
occaecat cupidatat non proident, sunt in culpa qui officia deserunt
mollit anim id est laborum.

Detection
=========

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
commodo consequat.

Affected Business Units
=======================

  **Name**         **Yes / No**
  ---------------- --------------
  Product          
  Operations       
  Finance          
  Engineering      
  Infrastructure   
  IT               
  ...              

Affected Services
=================

  **Name**        **CMDB IC**          **SLI**   **SLO**   **Burned SL**   **Degraded**   **Unavailable**
  --------------- -------------------- --------- --------- --------------- -------------- -----------------
  Application X   8a610aa0-6347-40d3   0.0%      99.80%    **99.80%**                     
  Database Y      735c0f0b-88ba-422d   98.30%    99.80%    **1.50%**                      
  ...                                                                                     

Timeline
========

  **Timestamp**      **Event description**
  ------------------ -------------------------------------------------------------------
  2018-01-10 00:30   Lorem ipsum dolor sit amet, consectetur adipiscing elit
  2018-01-10 00:34   sed do eiusmod tempor incididunt ut labore et dolore magna aliqua
  2018-01-10 00:48   Ut enim ad minim veniam, quis nostrud exercitation ullamco
  ...                

Action Items
============

  **Item**                                      **Type**   **Owner**          **Tracking Issue**   **Pre-emptive Priority**
  --------------------------------------------- ---------- ------------------ -------------------- --------------------------
  Lorem ipsum dolor sit amet                    Mitigate   Merche Colomar     APP-1234             Urgent
  tempor incididunt ut labore et dolore magna   Prevent    Don Copal          APP-5678             Urgent
  Ut enim ad minim veniam                       Process    Salvador Limones   DB-1234              Urgent
  consectetur adipiscing elit                   Process    Manny Calavera     N / A                Urgent
  ...                                                                                              

Glossary
========

CMDB IC: Configuration Management Database Identification Code

SL: Service Level

SLI: Service Level Indicator (one that can reflect uptime or
availability)

SLO: Service Level Objective (one that can reflect uptime or
availability)

SLA: Service Level Agreement

TTR: Time to Recovery

Burned SL: Difference between the SLO and the SLI

Severity Index: The calculated value used to establish the incident's
Severity

Pre-emptive Priority: The follow-up action items' priority established
from the resulting Severity

Appendix
========

Severity Index / Severity / Priority matrix:

  **Severity Index**   **Severity**   **Pre-emptive Priority**
  -------------------- -------------- --------------------------
  \> 0.8               Critical       Urgent
  \> 0.6 and \<= 0.8   High           High
  \> 0.4 and \<= 0.6   Medium         Medium
  \> 0 and \<= 0.4     Low            Low

Severity Index calculation:

-   Duration index: 0.1 x Duration (minutes) / TTR SLA (minutes)

-   Financial impact index:

    -   (Financial impact Estimated loss \> 0 ? 0.4 : 0.0) + (Financial
        impact Estimated loss x 0,0000001)

-   Reputational impact index: Reputational impact Estimated loss \> 0 ?
    1.0 : 0.0

-   Affected Services index (add, per each service):

    -   (Unavailable == True ? 0.1 : 0.0) + ((Degraded == True AND
        Burned SL \> 0) ? 0.05 x Burned SL : 0.0)

Severity Index for this post-mortem case:

-   Duration index: 0.1 x 500 / 120 == 0.416

-   Financial impact index: 0.4 + 0.2 == 0.6

-   Affected Services index:

    -   For service Application X: 0.1 + 0.0 == 0.1

    -   For service Database Y: 0.0 + 0.00075 == 0.00075

-   Total Severity Index: Duration index + Financial impact index +
    Affected Services index(N)

    -   0.416 + 0.6 + 0.1 + 0.00075 == 1.11675

Which, according to the Severity Index / Severity / Priority matrix,
establishes a Severity of **Critical** and a Pre-emptive Priority of
**Urgent**
