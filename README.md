# Hospital Managment System Based On Priority Scheduling

# Overview Of The Project:
 The Hospital Management System is designed to streamline patient care by efficiently managing patient intake, room allocation, and priority-based treatment. It uses a dynamic scheduling system where patients are assigned priorities based on their medical conditions, ensuring that critical cases receive prompt attention. The system employs a Tkinter-based GUI for easy interaction, a MySQL database for storing patient details, and integrates real-time clock updates and priority adjustments. By automating room assignments and enhancing patient management, the system improves hospital workflow and overall patient experience.
 # Programming Language Used:
     Python
     
 # Libraries Used:
  
   tkinter: Used to create the graphical user interface (GUI) for the system, including forms, buttons, labels, and other interactive elements.
  
   messagebox (from tkinter): Displays pop-up dialogs to inform users about errors, confirmations, and other important messages.
  
   difflib: Used to find close matches for disease names by comparing text inputs with predefined disease lists.
 
  random: Used for randomly assigning available rooms to patients.
  
  time: Used to record the waiting time of patients and provide real-time clock updates.
  
  mysql.connector: Enables interaction with the MySQL database, allowing the system to store and retrieve patient data from the database.

 # keyconcepts:
 Priority Scheduling:
Patients are treated based on the severity of their condition. More critical diseases are assigned higher priority (lower numerical value), ensuring that patients with life-threatening issues (e.g., heart attack, stroke) are treated before less severe cases (e.g., common cold).

Starvation:
Starvation occurs when low-priority patients wait indefinitely because higher-priority patients keep arriving. In this system, starvation could happen if critical patients continue to be added, leaving non-critical patients waiting for long periods.

Aging:
Aging is implemented to prevent starvation by gradually increasing the priority of patients who have been waiting for a long time. If a patient waits longer than a specified period (e.g., 1 minute), their priority is boosted, ensuring they eventually receive treatment, even if their initial priority was low.

Dynamic Priority Adjustment:
The system automatically adjusts patient priority over time using the aging technique. This ensures fair treatment by allowing patients with less critical conditions to eventually get attention if they've been waiting for a long time.

Room Allocation:
Rooms are assigned to patients dynamically based on availability. The system ensures that critical patients are prioritized for room allocation, making sure they receive care promptly.
# Dataflow And Methodology:
Patient Registration:
The system takes input for patient details like name, age, and disease through a user-friendly interface.
The disease entered is matched to predefined conditions using a priority system.

Priority Assignment:
Each disease is assigned a priority number based on severity (lower number = higher priority).
If no exact match is found for the disease, a default low priority is assigned.

Room Allocation:
The system checks available rooms and randomly assigns one to each patient.
If no rooms are available, the patient is added to a waiting list.

Patient Queue Management:
Patients are sorted in a queue based on their assigned priority.
The system periodically checks waiting times and adjusts the priority using an aging mechanism to prevent long wait times.

Room Assignment & Database Storage:
Once a room is available, the patient is moved from the waiting list to the assigned room.
All patient details and room assignments are stored in a MySQL database for easy access and record-keeping.

Monitoring & Updates:
The system continuously updates patient information and the status of room allocations in real-time, ensuring efficient hospital management.

# Conclusion :
In conclusion, the Hospital Management System effectively prioritizes patient care using dynamic priority scheduling, preventing starvation through aging techniques. It ensures that critical patients receive timely treatment, while also addressing the needs of those with less severe conditions over time. The system efficiently allocates resources and optimizes hospital operations, improving patient management.
