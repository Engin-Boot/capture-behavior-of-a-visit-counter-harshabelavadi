# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given: Server is down, there is a backup server,
  backup server is active.
  When: Server restarts,
  server sends request to backup server to get visitor count data.
  Then: Visitor count data gets retrieved.

Scenario: Reconcile counts if the sensor is offline for a while

  Given: Sensor is not active.
  When: Visitor visits the hospital.
  Then: Count visitors manually.  
