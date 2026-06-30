# Phone-Number-Tracker
# 📍 Phone Number Location Tracker

A Python project that retrieves the geographical region and telecom carrier information of a phone number and generates an interactive map showing the approximate location using Folium.

> **Note:** This project provides the **registered region** of a phone number, **not the live GPS location** of the device.

---

## Features

- Detects the geographical region of a phone number.
- Identifies the telecom service provider.
- Converts the region into latitude and longitude using OpenCage Geocoding API.
- Creates an interactive HTML map with a marker.
- Saves the map as `mylocation.html`.

---

## Technologies Used

- Python 3.x
- phonenumbers
- OpenCage Geocoder API
- Folium

---

## Project Structure

```
Phone-Number-Tracker/
│
├── main.py              # Main Python script
├── myphone.py           # Stores the phone number
├── mylocation.html      # Generated map
├── README.md
```

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/Phone-Number-Tracker.git
cd Phone-Number-Tracker
```

### 2. Create a virtual environment (Optional)

Windows

```bash
python -m venv .venv
.venv\Scripts\activate
```

Linux/Mac

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install phonenumbers folium opencage
```

Or

```bash
pip install -r requirements.txt
```

---

## Create `myphone.py`

Create a file named **myphone.py**

Example:

```python
number = "+919876543210"
```

Replace the number with the phone number you want to analyze in international format.

---

## OpenCage API Key

1. Visit https://opencagedata.com/
2. Create a free account.
3. Generate an API key.
4. Replace the key in the code:

```python
key = "YOUR_API_KEY"
```

---

## Running the Project

```bash
python main.py
```

---

## Sample Output

```
Maharashtra
Airtel
19.7515 75.7139
```

After execution, an HTML file named

```
mylocation.html
```

will be created.

Open it in any web browser to view the map.

---

## Example Workflow

```
Phone Number
      │
      ▼
phonenumbers Library
      │
      ├── Region
      └── Carrier
      │
      ▼
OpenCage API
      │
      ▼
Latitude & Longitude
      │
      ▼
Folium
      │
      ▼
Interactive HTML Map
```

---

## Limitations

- Does **not** track a person's real-time or live location.
- Displays only the approximate geographical region where the phone number is registered.
- Accuracy depends on the phone number database and OpenCage Geocoder.
- Some numbers may return only the country or state instead of an exact city.

---

## Dependencies

- phonenumbers
- folium
- opencage

---

## Install All Dependencies

```bash
pip install phonenumbers folium opencage
```

---

## Future Improvements

- GUI using Tkinter or PyQt.
- Real-time map interface.
- Export results to PDF or CSV.
- Support for batch phone number lookup.
- Better error handling for invalid numbers and API failures.

---

## Disclaimer

This project is intended for educational purposes only. It does not provide live location tracking and should not be used to violate privacy or for unauthorized surveillance.

---

## Author

**Rudra Jawale**

Computer Science Engineering (Data Science)
