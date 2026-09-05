Project 1 — Data Cleaning & Preparation

Cleaned a raw 1,201-row order dataset (14 columns: OrderID, Date, CustomerID, Product, Quantity, UnitPrice, 
ShippingAddress, PaymentMethod, OrderStatus, TrackingNumber, ItemsInCart, CouponCode, ReferralSource, TotalPrice).
No duplicate records were found. Identified 309 blank entries in the CouponCode column and determined these represent transactions where no coupon was used, 
rather than missing data — labeled explicitly as "No Coupon" to remove ambiguity for downstream analysis.
Standardized inconsistent number formatting in the UnitPrice and TotalPrice columns. 
Investigated an unusual pattern where UnitPrice varied significantly across transactions for the same product (e.g., "Monitor"); 
confirmed via distinct-value analysis that UnitPrice carries a near-unique value per transaction across the dataset (163 distinct prices across 163 Monitor orders), 
ruling out coupon usage, customer tier,
and time-based pricing as explanations, and documenting this as a dataset characteristic rather than a data quality error.

Tools and skills: Excel, Power Query, Data cleaning, Profiling, Data validation & Quality.
