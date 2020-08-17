# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given: Record of people visiting hospital in a week,
  server is active.
  When: Person is a visitor.
  Then: Display visiting trend of that person for that week.

Scenario: Alert when seating capacity is full

  Given: Person visits the hospital,
  server is active.
  When: Person is a visitor,
  seats are not available.
  Then: Display "seats capacity full" alert message.
