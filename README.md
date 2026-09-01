# Accuknox Django Assignment - Quiz

## What this repo contains
- A Django project that demonstrates Django signals behaviour (synchronous, same thread, transaction)
- Rectangle iterable class demo
- A management command that triggers model creation to show console outputs

## Setup (Linux / macOS / Windows WSL)
1. python -m venv venv
2. source venv/bin/activate   # Windows: venv\Scripts\activate
3. pip install -r requirements.txt
4. python manage.py migrate

## How to run signal demo (console proof)
1. python manage.py create_test
   - This will create a model instance (outside transaction) and one inside an atomic block (rolled back).
   - Watch the console logs — they show signal start/end, thread name, and transactional existence check.

## Rectangle demo
1. python core/demo_rectangle.py

## What to include in submission
- GitHub repo link in the form
- Screenshots of console output:
  - show synchronous sleep in signal
  - show same thread name printed in view/command & signal
  - show transaction rollback behaviour
  - rectangle demo output

## Files of interest
- core/signals.py
- core/management/commands/create_test.py
- core/rectangle.py
