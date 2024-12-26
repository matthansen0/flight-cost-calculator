# GA vs. Airline Cost & Time Calculator

## Visit the page
**https://matthansen0.github.io/flight-cost-calculator/**

---

This project is a single-page **HTML + JavaScript** tool that compares the **cost** and **travel time** of flying a general aviation (GA) airplane versus taking a commercial airline. It includes various advanced features:

- **Multiple Airplane Profiles** (built-in or user-created)
- **Customizable Aircraft Data** (wet rate, cruise speed, fuel burn)
- **Iterative Fuel Stops Calculation** (3 gallons used per additional takeoff/climb)
- **Minimum Hobbs (Overnight Rental) Logic** (fully customizable)
- **FBO Fees, Overhead Times, and Airline Costs/Times** comparisons
- **Modal Pop-ups** to edit plane data, add new planes, or adjust the minimum Hobbs rules

---

## Features

1. **Add or Customize Airplanes**
   - **Built-in:** DA40 XLS, Cirrus SR20  
   - **Add** your own airplane (name, rate, speed, fuel burn)  
   - **Customize** existing airplane data on-the-fly  

2. **Fuel & Stop Calculations**
   - **Iterative** approach to factor in an extra 3 gallons burned per fuel stop (for run-up, taxi, climb)
   - Subtract **1 hour of reserve** from total usable fuel to ensure safe landing fuel

3. **Minimum Hobbs Logic**
   - Edit the default overnight/minimum block times (e.g., 6-hour blocks, base 2 hrs, +1 hr each block)
   - The tool calculates a “minimum billable hours” if the reservation length exceeds your chosen thresholds

4. **Cost Comparison**
   - **Airline**: Number of passengers × ticket cost, plus overhead time for check-in/security
   - **GA**: (billable flight hours × wet rate) + FBO fees + overhead times (preflight, fueling stops, etc.)

5. **Time Comparison**
   - **Door-to-door** GA time: flight time + overhead (fuel stops, pre/post-flight)  
   - **Door-to-door** airline time: in-flight + overhead (arriving early, security lines)

6. **Flexible HTML & JavaScript**
   - No external frameworks required
   - Everything stored in JavaScript objects and updated via modals

---

## Usage

1. **Input Basic Info**
   - # of Passengers
   - Airline Ticket Price
   - Trip Distance (one-way, in nautical miles)
   - Reservation Length (total hours from check-out to check-in, affecting min Hobbs)

2. **Select (or Add) an Airplane**
   - Pick from built-in planes (DA40, SR20) or click **"Add New Airplane"** to define your own.

3. **Adjust Additional Fields**
   - **Fuel** (usable gallons after weight & balance)
   - **Fuel Stop Overhead** (time on the ground each stop)
   - **Extra Hobbs per Stop** (default 0.5 hr for run-up, takeoff, climb)
   - **FBO Fees** (for each fuel stop + destination ramp fee)
   - **GA Overhead** (preflight/postflight time)
   - **Airline Overhead** (arrival time, security)

4. **Customize**
   - **Customize Plane Data**: Edit the wet rate, speed, and GPH for the currently selected plane.
   - **Edit Min Hobbs Logic**: Change how many hours get billed for overnight/long rentals (block size, base hours, extra hours/block).

5. **Click "Calculate"**
   - The calculator shows:
     - **GA Cost** vs. **Airline Cost**
     - **GA Total Time** vs. **Airline Total Time**
     - Detailed breakdown of flight time, fuel stops, FBO fees, and minimum Hobbs calculations

---

## Customizing

- **`CLIMB_GALS_PER_STOP`**: Inside the JavaScript code, you can change how many gallons are assumed to be used per additional takeoff/climb. It is set to **3** gallons by default.
- **Minimum Hobbs Logic**: Accessed by **"Edit Min Hobbs Logic"** button. The default is 6-hour blocks, with a base 2 hours minimum after the first block, and +1 hour for each additional block.

---

## License

This project is provided under the **MIT License**. You’re free to use, modify, and distribute it, but there is no warranty or guarantee of fitness for any particular purpose. See [LICENSE](LICENSE) for details.

---

**Questions, feedback, or feature requests?**  
Feel free to open an issue or submit a pull request. Enjoy optimizing your GA trips with real-world cost and time estimates!
