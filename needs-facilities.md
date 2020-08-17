# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

	Given record of people visiting hospital in a week
	And server is active
	
	When the person is a visitor
	
	Then the "visiting trend" of that person for that week is displayed

Scenario: Alert when seating capacity is full

	Given the person visits the hospital
	And server is active

	When the person is a visitor
	And the seats are not available

	Then "seating capacity full" alert message is displayed
