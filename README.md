## Topic "Apache Airflow"

I have successfully completed the homework assignment on the topic "Apache Airflow." Below are the details of the tasks I have implemented:

---

### Step-by-Step Implementation

1. **Table Creation**  
   I created a table using `IF NOT EXISTS` with the following fields:
   - `id` (auto-increment, primary key)
   - `medal_type`
   - `count`
   - `created_at`

2. **Random Value Generation**  
   I implemented a task to randomly select one of three values: `['Bronze', 'Silver', 'Gold']`.

3. **Branching Logic**  
   Based on the randomly selected value, I executed one of the three tasks using branching logic in the DAG.

4. **Task Descriptions**  
   I implemented the following three tasks:
   - **Task 1**: Counted the number of records in the `olympic_dataset.athlete_event_results` table where the `medal` field contains `Bronze` and inserted the result into the table created in Step 1, along with the medal type and creation time.  
   - **Task 2**: Counted the number of records where the `medal` field contains `Silver` and inserted the result into the same table.  
   - **Task 3**: Counted the number of records where the `medal` field contains `Gold` and inserted the result into the same table.

5. **Task Execution Delay**  
   Using the `PythonOperator` with the `time.sleep(n)` function, I introduced a delay before proceeding to the next task, ensuring the previous task was successfully executed.

6. **Sensor Check**  
   I implemented a sensor to verify that the most recent record in the table created in Step 1 is not older than 30 seconds compared to the current time.  
   - Additionally, I simulated scenarios where the delay exceeded 30 seconds to demonstrate the sensor's "failed" behavior.

---
