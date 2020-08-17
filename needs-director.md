# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given: Person visits the hospital on a particular day (working or holiday),
  server is active, visitor information gets stored in database.
  When: Person visiting hospital is a patient.
  Then: Displays patient visits with date and time.

Scenario: Compute parking slots to reserve for visiting specialists

  Given: Person visits the hospital,
  server is active, visitor information gets stored in database,
  visitor has a car.
  When: Person is a visiting specialist,
  parking system collects the specialist data,
  parking slots are available.
  Then: Parking slot reserved for that specialist,
  number of available parking slots updated.
  
