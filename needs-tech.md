# Visit-counter technical needs

Scenario: Recover across restarts of the server that runs the visit-counter

	Given server is down
	And there is a backup server
	And backup server is active

	When the server restarts
	And server sends request to backup server to get visitor count data

	Then "visitor count" data is retrieved 

Scenario: Reconcile counts if the sensor is offline for a while

	Given sensor is not active

	When a visitor visits the hospital

	Then count visitors manually 
