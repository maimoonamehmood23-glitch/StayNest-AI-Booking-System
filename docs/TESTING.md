# Testing: Booking Validation (KAN-5)

Manual test cases to verify the implementation of booking validation and error handling.

| Test | Steps | Expected result |
| :--- | :--- | :--- |
| **Empty Form** | Leave all fields empty and click "Confirm Booking" | All required fields show "is required" error messages; form is not submitted. |
| **Check-out before Check-in** | Set check-out date to a date before the check-in date and click "Confirm Booking" | Check-out field shows "Check-out must be after check-in" error. |
| **Valid Booking** | Fill all fields correctly and click "Confirm Booking" | No validation errors; system proceeds to confirmation screen. |
| **Submit Failure** | Trigger a network failure or database error during submission (e.g., by disabling network or using a faulty Supabase key) | A user-friendly "Booking failed" or "An unexpected error occurred" banner appears at the top of the form. |
