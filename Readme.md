# Flight Data Generator and Analyzer

This Python script generates a large number of JSON files containing randomly generated flight data, and then analyzes this data to provide various statistics.

## Description

The script performs two main tasks:

1. **Generation Phase**: Creates 5000 JSON files, each containing 50-100 randomly generated flight records. Each record includes information such as date, origin city, destination city, flight duration, and number of passengers.

2. **Analysis Phase**: Processes all generated files to produce statistics including:
   - Total number of records processed
   - Number of "dirty" records (records with NULL values)
   - Average and 95th percentile of flight duration for the top 25 destination cities
   - Cities with the maximum number of passengers arrived and departed

## Requirements

- Python 3.7 or higher

## How to Run

1. Save the script to a file, e.g., `flight_data_analyzer.py`

2. Open a terminal or command prompt

3. Navigate to the directory containing the script:
   ```
   cd path/to/script/directory
   ```

4. Run the script using Python:
   ```
   python flight_data_analyzer.py
   ```

5. Set
   ```
   OUTPUT_DIR = os.getcwd()+"/tmp/flights"
   ```
   The script will generate files in the `/tmp/flights/`sub  directory. Ensure you have write permissions for this directory.

7. Wait for the script to complete. It will print progress updates and final results to the console.

## Output

The script will generate two types of output:

1. JSON files in the `/tmp/flights/` directory (or the directory specified by `OUTPUT_DIR`)
2. Console output showing:
   - Total records processed
   - Number of dirty records
   - Total run duration
   - Average and 95th percentile flight duration for top 25 destination cities
   - Cities with maximum passengers arrived and departed

## Customization

You can modify the following constants at the top of the script to customize its behavior:

- `N`: Number of JSON files to generate
- `M_MIN`, `M_MAX`: Range for number of flight records per file
- `K`: Number of cities
- `L`: Probability for NULL values
- `OUTPUT_DIR`: Directory where JSON files will be saved
