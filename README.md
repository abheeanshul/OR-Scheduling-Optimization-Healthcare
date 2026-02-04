# OR-Scheduling-Optimization-Healthcare
**Operating Room Scheduling Optimization**
--Applied Healthcare Operations Analytics--

Overview
This project analyzes operating room scheduling performance at a hospital using real world inspired data. The goal is to understand how scheduling decisions impact idle time, delays, and overtime, and to evaluate how small adjustments to scheduled case durations affect overall operational cost.

The analysis emphasizes operational insight over model complexity, aligning with how analytics is applied in healthcare operations.

Key Questions Addressed
•	How effectively are operating rooms utilized?
•	Where does idle time, delay, and overtime occur?
•	Can adjusting scheduled case durations reduce total system cost?
•	What scheduling buffer minimizes operational inefficiency?

Data Description
The dataset represents scheduled and actual surgical case durations across:
•	Multiple operating rooms
•	Multiple operating days
•	Fixed operating hours (7 AM – 5 PM)
Key variables include:
•	Scheduled start times and durations
•	Actual surgery durations
•	Operating room and day identifiers
(Raw data is not included due to course restrictions.)

Methodology
1.	Timeline Reconstruction
  o	Reconstructed actual start and end times using scheduled starts and realized durations
  o	Propagated delays across consecutive cases
2.	Operational Definitions
  o	Idle Time: Unused OR capacity when cases finish early
  o	Delay: Spillover of one case into the next scheduled slot
  o	Overtime: Surgeries extending past normal operating hours
3.	Cost Model
  o	Idle cost: $1 per minute
  o	Delay cost: $2 per minute
  o	Overtime cost: $3 per minute
4.	Scheduling Optimization
  o	Scheduled durations scaled using a multiplier (alpha)
  o	Alpha optimized via sensitivity analysis across all room day combinations
  o	Objective: minimize total operational cost

Outputs
•	Room day level OR timeline visualizations
•	Cost vs scheduling buffer sensitivity curves
•	Identification of operational bottlenecks and inefficiencies

Tools Used
•	R
•	Base graphics for custom visualizations
•	Data driven simulation and sensitivity analysis

Key Takeaways
•	Small scheduling adjustments can materially impact downstream delays and overtime
•	Distinguishing buffer time from idle time is critical in healthcare settings
•	Overly aggressive compression of schedules can increase system wide costs
