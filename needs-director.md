# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

	Given a person visits the hospital on a particular day (working or holiday)
	And the server is active
	And the visitor information is stored in database
	
	When the person visiting hospital is a patient
	
	Then the "patient visits with date and time" is displayed

Scenario: Compute parking slots to reserve for visiting specialists

	Given a person visits the hospital 
	And the server is active
	And the visitor information is stored in database
	And the visitor owns a car
	
	When the person is a visiting specialist
	And the parking system collects the specialist data
	And parking slots are available
	
	Then reservation of parking slot is done for that specialist
	And number of available parking slots updated
