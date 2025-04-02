

# 🖼️ Free Style Image Generator  

## 🔍 Overview  
Free Style Image Generator is a **Gradio-based** web application that leverages **Hugging Face's Inference API** to generate and analyze images. It offers two main features:  

✅ **Text to Image** – Converts text descriptions into AI-generated images  
✅ **Image to Prompt** – Analyzes uploaded images to generate detailed text prompts  

---

## 🚀 Features  
🎭 Text-to-Image Generation  
🖼 Image Analysis  
🎨 Style Presets  
🖥 User-Friendly Interface  
💰 Free Tier Compatible  

---

## 🛠 Getting Started  

### 📌 Prerequisites  
- Python 3.7 or higher  
- Hugging Face API token ([Get one here](https://huggingface.co/settings/tokens))  
- Required Packages: `gradio`, `requests`, `pillow`, `numpy`  

### ⚙️ Installation  
1. Clone the repository or download the code  
2. Install required packages:  
```bash
pip install gradio requests pillow numpy
```  
3. Run the application:  
```bash
python main.py
```  

---

## 🎭 How to Use  

### ✨ Text to Image  
1. Enter Hugging Face API token  
2. Write a detailed description  
3. (Optional) Select a style preset  
4. Click "Generate Image"  
5. Wait for the image to generate  

### 🖼 Image to Prompt  
1. Enter Hugging Face API token  
2. Upload an image or provide an image URL  
3. Click "Analyze Image & Generate Prompt"  
4. View the generated prompt  
5. (Optional) Generate a new image from the prompt  

---

## 🛠 Code Explanation  

### 🖌 Image Generation Function  
```python
def generate_image_huggingface(api_token, prompt, style="none"):
```  
- Uses multiple AI models  
- Implements retry logic for API rate limits  

### 📷 Image Analysis Function  
```python
def analyze_image_and_generate_prompt(api_token, input_image):
```  
- Uses AI to generate captions  
- Provides fallback analysis  

### 📝 Prompt Enhancement  
```python
def enhance_prompt(caption):
```  
- Improves prompt quality with extra details  

### 🔄 Fallback Prompt Generation  
```python
def generate_fallback_prompt(image):
```  
- Analyzes colors, brightness, and aspect ratio  

### 🌐 URL Image Download  
```python
def download_image_from_url(url):
```  
- Fetches images from provided URLs  

### 🖥 Gradio Interface  
- Easy-to-use tabbed interface with multiple components  

---

## 🎭 Style Presets  
- Anime  
- Ghibli  
- Photographic  
- Digital Art  
- Comic Book  
- Fantasy Art  
- Line Art  
- Cinematic  

---

## ⚠️ Error Handling  
- Rate limit detection and retry logic  
- Fallback to alternative models  
- Local analysis when API fails  
- Input validation for empty submissions  

---

## 📊 Technical Details  

### 🔗 API Usage  
- Uses Hugging Face’s Inference API  

### 🖼 Image Processing  
- Converts formats, analyzes colors, and optimizes brightness  

---

## ⚠️ Limitations  
- Rate limits apply for free-tier users  
- Free models may not match paid services  
- Image generation can take 10-30 seconds  

---

## 🛠 Extending the Application  
- Add more style presets  
- Integrate additional AI models  
- Implement image editing tools  
- Save image generation history  

---

## 📞 Contact  
📧 **Email**: aryankaminwar@gmail.com 


---

## 🎖 Credits  
- **Gradio** – Web interface framework  
- **Hugging Face Inference API** – AI models  
- **Pillow** – Image processing  
- **Stable Diffusion & Captioning Models**  
