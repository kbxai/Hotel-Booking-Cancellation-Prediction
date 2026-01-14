# Hotel Booking Cancellation Prediction

This notebook documents the complete workflow I used for the Kaggle competition ["Hotel Booking Cancellation"](https://www.kaggle.com/t/acbc86871ce144a197ea032dda27b689). The goal is to predict whether a booking will be cancelled (`booking_status = 1`) using the provided training data and to generate high-quality predictions for the hidden test set.

## Dataset and files

- **train.csv** – 29,500 rows (13 features + target `booking_status`).
- **test.csv** – 7,000 rows without the target (used for Kaggle scoring).
- **sample_submission.csv** – reference format with `id` and `booking_status` columns.

Key feature glossary:
1. `adults`, `children` – party composition.
2. `weekends`, `weekdays` – length of stay split into weekend/weekday nights.
3. `meal_type`, `room_type`, `segment` – categorical booking descriptors.
4. `arrival` – arrival date (string) that we will expand into year/month/day/week features.
5. `lead_time`, `price`, `requests` – continuous business signal features.
6. `repeat` – prior customer flag.
7. `booking_status` – target (1=canceled, 0=honored).
