CREATE PROCEDURE `ManageBooking`(
    IN BookingID INT,
    IN NewCustomerID INT,
    IN NewTableNumber INT,
    IN NewBookingDate DATE
)
BEGIN
    IF EXISTS (SELECT 1 FROM booking WHERE booking_id = BookingID) THEN
          UPDATE booking
        SET
            customerid = NewCustomerID,
            tablenumber = NewTableNumber,
            date = NewBookingDate
        WHERE booking_id = BookingID;
        SELECT 'Booking updated successfully' AS Result;
    ELSE
        SELECT 'Booking not found' AS Result;
    END IF;
END;
