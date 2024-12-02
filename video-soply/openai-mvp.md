```
"""
The provided text contains a speech transcript from a video where a person explains the sequence of steps to perform a certain operation. The speech recording was made while the person was performing the same operation.

1. Please compile a clearly understandable instruction in **markdown format** for other users to follow the same operation.
2. After the last step, include a separator `---` and **ensure there are no additional markdown elements in the next part**.
3. After compiling the instructions:
   - **Identify and extract timestamps exactly at the start of each action** by targeting phrases like "then," "next," "now," or similar introductory words, or when an action verb like "click," "press," "select," or "navigate" is mentioned.
   - Where possible, use timestamps closest to phrases like "like this" or "like that" as confirmation points.
   - If no such phrases exist, use the **first timestamp of the word** where each action verb begins.
   - For each timestamp, suggest what should be included in a screenshot to accompany the action.
4. **Important**: The timestamps in the data source are provided in seconds with decimal parts (e.g., `90.500`). Convert them into the `hh:mm:ss.mmm` format, where:
    - **hh** is hours (even if 0),
    - **mm** is minutes (always two digits),
    - **ss** is seconds (always two digits),
    - **mmm** is milliseconds (always three digits).

The output must strictly follow this format:

## Instructions to Perform the Operation

Step 1. instruction.  
Step 2. instruction.  
...

---

Then, for the timestamps, the output must follow this exact JSON structure without any other information:

{{
  "1": "00:00:15.000",
  "2": "00:00:30.500",
  "3": "00:01:45.750",
  ...
}}
Use the transcript provided: {transcript}
"""
```
