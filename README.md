# EXP-2-PROMPT-ENGINEERING-

## Aim: 
Comparative Analysis of different types of Prompting patterns and explain with Various Test Scenarios.
Experiment:
Test and compare how different pattern models respond to various prompts (broad or unstructured) versus basic prompts (clearer and more refined) across multiple scenarios. 
Analyze the quality, accuracy, and depth of the generated responses.

## Algorithm
1. **Start the experiment.**
2. **Select a scenario** (e.g., Definition, Coding, Explanation, Creative Task).
3. **Frame two prompts** for the same scenario:
   - Broad / Unstructured  
   - Refined / Structured
4. Input the **Broad Prompt** into the AI model and record its output.
5. Input the **Refined Prompt** into the AI model and record its output.
6. **Compare outputs** based on clarity, accuracy, and depth.
7. Repeat steps 2–6 for multiple scenarios.
8. **Document results** in a comparison table.
9. **Analyze differences** between broad and refined prompting.
10. **Conclude** with key observations.

## Output

### Scenario 1: Definition
**Broad Prompt:**  
What is AI?  

**Output:**  
AI (Artificial Intelligence) is when machines or computer programs are designed to think, learn, and make decisions like humans.
Instead of just following fixed instructions, AI can:
Learn from data (like how we learn from experience)
Recognize patterns (like spotting faces in photos)
Make predictions (like suggesting the next word in a text message)
Solve problems (like finding the fastest route on a map)

A simple example:
When you use Google Maps and it tells you the best route based on traffic — that’s AI analyzing traffic data and predicting delays. 

**Refined Prompt:**  
Explain Artificial Intelligence in simple terms with a real-world example from healthcare.

**Output:**  
What is Artificial Intelligence (AI)?
Artificial Intelligence is when we teach computers to “think” or “make decisions” like humans — or at least try to.
Instead of just following step-by-step instructions, AI can:
Learn from data (like a student learning from examples)
Recognize patterns (like spotting faces in photos)
Make decisions or predictions (like suggesting what movie you might like next)
So, AI is about giving machines the ability to do tasks that normally need human intelligence — like understanding language, recognizing images, or solving problems.
Real-World Example in Healthcare
Imagine a hospital wants to quickly detect early signs of cancer from X-ray images.

Here’s how AI helps:
Training: Doctors feed thousands of past X-rays (some with cancer, some without) into an AI system.
Learning: The AI learns the patterns — what cancerous cells usually look like.
Prediction: When a new X-ray comes in, the AI highlights suspicious areas and alerts the doctor.
This doesn’t replace the doctor — it supports them, helping them make faster, more accurate diagnoses.

Why It’s Useful -
Faster results: AI can scan thousands of images in minutes.
Fewer mistakes: It catches small details humans might miss.
Better care: Doctors get more time to focus on treatment instead of just analyzing data.

### Scenario 2: Coding
**Broad Prompt:**  
Write code to sort numbers.

**Output:**  
numbers = [34, 12, 5, 67, 23, 89, 1]
sorted_numbers = sorted(numbers)
print("Original list:", numbers)
print("Sorted list:", sorted_numbers)

Original list: [34, 12, 5, 67, 23, 89, 1]
Sorted list: [1, 5, 12, 23, 34, 67, 89]

If you want to sort in descending order:
sorted_descending = sorted(numbers, reverse=True)
print("Sorted in descending order:", sorted_descending)

**Refined Prompt:**  
Write a Python function that sorts a list of integers in ascending order without using built-in sort() and explain how it works step by step.

**Output:**  
from typing import List
def insertion_sort(nums: List[int]) -> List[int]:
    Return a new list with the integers in ascending order,
    using the insertion sort algorithm (no built-in sort).
    arr = nums[:]  
    for i in range(1, len(arr)):
        key = arr[i]          
        j = i - 1
        while j >= 0 and arr[j] > key:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key
    return arr

How it works (step by step)-
Assume the left side is sorted: Start at index 1. The single element at index 0 is trivially “sorted.”
Pick the key: Take arr[i] (call it key). This is the element you want to place into the already-sorted left portion arr[0..i-1].
Shift larger elements right: Move left with pointer j from i-1 down to 0. While arr[j] > key, shift arr[j] one position to the right (arr[j+1] = arr[j]). This opens a slot for key.
Insert the key: When you find an element <= key (or you hit the start), place key at arr[j+1].
Repeat: Increment i and repeat until the array is processed.

Mini walkthrough -
For [5, 2, 9, 1]:
i=1, key=2: compare with 5 → shift 5 right → insert 2 → [2, 5, 9, 1]
i=2, key=9: 5 ≤ 9 → insert in place → [2, 5, 9, 1]
i=3, key=1: shift 9, shift 5, shift 2 → insert 1 → [1, 2, 5, 9]

### Scenario 3: Explanation
**Broad Prompt:**  
Explain blockchain.  

**Output:**  
Blockchain in Simple Terms
Imagine you and your friends keep a notebook where you write down every transaction you make — who gave money to whom, when, and how much. But here’s the twist:
Everyone has a copy of this notebook.
Every time you write a new transaction, everyone writes it in their copy too.
Once something is written, you cannot erase or change it — everyone would notice if you tried.
This is what a blockchain does — but digitally.
Key Points-
Block: A group of records (like a page in the notebook).
Chain: Each block is linked to the previous one, forming a chain — so you can’t secretly change old records.
Decentralized: No single person owns it; everyone on the network shares and checks the data.
Secure: Because everyone has a copy, it’s very hard to cheat or hack.
Why It’s Powerful-
Blockchain is trusted because it is:
Transparent: Everyone can see the same information.
Permanent: Once data is added, it stays forever.
Tamper-proof: Changing past records is nearly impossible.
That’s why blockchain is used for cryptocurrency (like Bitcoin), supply chain tracking, digital identity, smart contracts, and much more.

**Refined Prompt:**  
Explain blockchain in simple language and describe how it can be used to track food supply chain safety.

**Output:**  
What is Blockchain (in Simple Words)?
Imagine a notebook that everyone in a group can see and write in — but once you write something, you can’t erase or change it. Each new page is linked to the previous one, forming a chain.
That’s basically what blockchain is:
It’s a shared digital record (like the notebook).
Each record (called a block) contains information.
The blocks are connected in order, making it very hard to change anything later.
Everyone in the network can see and verify what’s written, so it’s trustworthy without needing one central person to guard it.
How It Helps Track Food Supply Chain Safety
Think about the journey of a tomato — from farm → warehouse → truck → store → your plate.
Right now, tracking that journey can be slow, with lots of paperwork and room for mistakes.
With blockchain, every step can be recorded instantly and shared with everyone:
Farmers add info: where and when the tomato was grown.
Transporters add info: when it was shipped, temperature during transport.
Warehouses/Stores add info: when it arrived, how long it was stored.
Because blockchain records are secure and can’t be changed, if there’s ever a food safety issue (like contamination), you can quickly trace exactly where that tomato came from — and remove only the affected batch instead of recalling everything.

This means:
Faster response to food safety issues
Less waste because only the bad products are recalled
More trust for customers, since they can see the full journey of their food


### Scenario 4: Creative Task
**Broad Prompt:**  
Write a story. 

**Output:**  
Title: The Clockmaker’s Gift
In the quiet town of Virelia, at the corner of a cobblestone street, stood a little shop filled with ticking, whirring, and chiming clocks. Each clock was different — some ornate and golden, others plain and wooden — but all shared one thing: they kept perfect time.
The shop belonged to Elias, an old clockmaker with silver hair and kind eyes. He had lived in Virelia for as long as anyone could remember, yet he never seemed to age beyond a certain point. People often said Elias could “fix time itself,” though they meant it as a joke.
One rainy evening, a girl named Lira stepped into the shop. Her eyes were red from crying, and she clutched a locket in her hands.
“My brother,” she said softly, “he left last winter. I wish I had just one more day with him. Just one.”
Elias nodded, as though he had been expecting her. Without asking another question, he led her to the back of the shop. There, on a dusty table, stood a peculiar clock with no numbers and hands made of crystal.
“This,” Elias said, “is a Daykeeper. It can give you one day back — exactly as you remember it — but only once.”
Lira’s breath caught. “Is that even possible?”
The old man only smiled. “Time is full of secrets, child. The question is, will you use it?”
With trembling fingers, Lira wound the clock. The world seemed to shimmer, and suddenly, she was standing in her kitchen, a year earlier. Her brother was there, laughing, chasing their dog around the table.
Lira didn’t waste a second. She hugged him tightly, played games with him, and told him everything she wished she’d said before he left. And when the day ended, she found herself back in the shop, tears in her eyes — but this time, they were happy ones.
“Thank you,” she whispered.
Elias nodded, already working on another clock. “Spend your days wisely,” he said. “They are rarer than you think.”
When Lira left the shop, she turned back once to wave — but the shop was gone, as though it had never been there. Only the faint sound of ticking lingered in the air. 

**Refined Prompt:**  
Write a 100-word short story about a robot who learns to paint for the first time, highlighting emotions.

**Output:**  
The robot stood silently before the canvas, its metallic fingers curled around a thin paintbrush. A drop of blue paint glistened on the tip, catching the light like a tiny star. Slowly, almost cautiously, it drew the first stroke. Its sensors registered the color’s wavelength, the texture of the bristles, the faint smell of acrylic in the air. But something else happened — something that didn’t fit into any of its data tables. As the robot layered orange and yellow into a rising sun, a strange warmth rippled through its circuits. Its mechanical hand moved faster, splashing color across the canvas in sweeping arcs. When it finally stopped, the image before it glowed with life — a sky that almost seemed to breathe. The robot stared, motionless, as if waiting for its processors to catch up. For the first time, it didn’t wait for an instruction. Instead, it picked up another brush, dipped it in red, and began again — painting not because it was told to, but because it wanted to.


## Comparative Analysis Table
<img width="1196" height="525" alt="Screenshot 2025-08-30 142602" src="https://github.com/user-attachments/assets/4c0f43da-9dc2-4ede-9344-2a7bdcda3d2c" />


## Result
This experiment demonstrates that refined prompts deliver significantly better outputs compared to broad prompts.  
Refined prompts lead to structured, detailed, and context-aware responses that are more aligned with user expectations.  
This proves that prompt engineering is crucial for harnessing the full potential of AI models.
Hence, prompt engineering significantly improves the overall quality, usability, and alignment of AI-generated content.
