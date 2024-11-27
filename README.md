# Ai_in_industry_assignment
The Video Action Detection with Gradio and NVIDIA Llama API is an innovative solution that simplifies the process of analyzing actions in video files using state-of-the-art AI models. This project harnesses NVIDIA's powerful Llama-3.2-11B-Vision-Instruct API to identify and evaluate specified actions in video content

googlecollab = "https://colab.research.google.com/drive/117FhAvt59B6JT2PyncCyMYZOjPER0tSy?usp=sharing"

Video Action Detection with Gradio and NVIDIA Llama API
Python Version: 3.7+
Framework: Gradio
License: Apache 2.0
This project leverages NVIDIA's Llama-3.2-11B-Vision-Instruct API to detect actions in video files. Users can upload two videos, trim them, and visualize the recognition rates using a real-time graph, all through an interactive Gradio interface.
Features
- Video Upload: Upload two video files for analysis.
- Trimming: Trim videos to a specified length for uniform comparison.
- Action Detection: Detect specified actions in videos.
- Graphical Visualization: Compare recognition rates via a bar graph.
Prerequisites
To run this project, you need the following:
- Python 3.7 or later
- NVIDIA API Key for Llama-3.2-11B-Vision-Instruct
Installation
Clone the repository and install the dependencies:
```bash
git clone <repository_url>
cd <repository_name>
pip install -r requirements.txt
```
Dependencies in `requirements.txt`:
gradio
moviepy
matplotlib
pillow
requests
numpy
opencv-python
NVIDIA API Setup
1. Register on the NVIDIA Developer Platform.
2. Obtain an API key for Llama-3.2-11B-Vision-Instruct.
3. Replace the placeholder API key in the code with your key:
```python
vlm = VLM(
    url="https://ai.api.nvidia.com/v1/gr/meta/llama-3.2-11b-vision-instruct",
    api_key="YOUR_API_KEY",  # Replace with your NVIDIA API key
    callback=vlm_callback,
)
```
How It Works
1. **Upload Videos:** Select two videos via the Gradio interface.
2. **Trim Videos:** Specify the maximum length for video trimming.
3. **Detect Actions:** Enter the action to detect (e.g., jumping, running).
4. **View Results:** A bar graph displays recognition rates for both videos.
Running the Application
To launch the application, run:
```bash
python main.py
```
Access the Gradio interface via the localhost link displayed in the terminal.

Example Output
**Scenario 1: Jumping**
```
Video   Recognition Rate (%)
Video 1 88%
Video 2 82%
```

**Scenario 2: Running**
```
Video   Recognition Rate (%)
Video 1 85%
Video 2 78%
```

**Scenario 3: Walking**
```
Video   Recognition Rate (%)
Video 1 80%
Video 2 76%
```

**Scenario 4: Dancing**
```
Video   Recognition Rate (%)
Video 1 83%
Video 2 79%
```

**Scenario 5: Sitting**
```
Video   Recognition Rate (%)
Video 1 75%
Video 2 70%
```
