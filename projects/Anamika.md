# Anamika - Interactive Ouija Board Experience

## Project Overview

Anamika is an innovative project aimed at recreating the ghostly character from the Malayalam movie "Romancham" using modern technologies. The project leverages Language Learning Models (LLMs), Speech-to-Text APIs, and 3D graphics to create an immersive experience where users can interact with Anamika through a virtual Ouija board.

<div>
   <b>YouTube: </b>
   </br>
   <a href="https://www.youtube.com/watch?v=Pk_6XVoo61A">
     <img src="http://img.youtube.com/vi/Pk_6XVoo61A/0.jpg" alt="Video 1" style="width: 48%;">
   </a>
</div>

![Romancham Carrom Board](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fd32qys9a6wm9no.cloudfront.net%2Fimages%2Fmovies%2Fbackdrop%2F8e%2F24b31a46d4d5eb846e869bf5a3b02e93_706x397.jpg%3Ft%3D1675802362&f=1&nofb=1&ipt=7d5f3d1394aa849938824ba457fa9e3e5abd7756ca356fadda2b1d35fe3ed972&ipo=images)

## Key Features

1. **Speech-to-Text Conversion:**
   - Users can speak to Anamika in Malayalam.
   - Speech input is converted to text using a Speech-to-Text API.

2. **Language Understanding:**
   - A 7B LLaMA-2 Indic model, fine-tuned on Malayalam tokens, processes the input text.
   - The model generates responses in English based on the user's input.

3. **Interactive Ouija Board:**
   - A React application renders the Ouija board using Three.js.
   - The Ouija board simulates the movement of a glass piece, representing Anamika's responses.
   - Audio effects enhance the ghostly atmosphere.

## Implementation Concepts

### 1. Speech-to-Text API Integration

- **API Choice:** Use Google Cloud Speech-to-Text API or Microsoft Azure Cognitive Services.
- **Functionality:**
  - Capture audio input from the user.
  - Convert audio to Malayalam text.

### 2. Language Model (LLM)

- **Model:** 7B LLaMA-2 Indic model.
- **Training:** Continuously fine-tune using LoRA on a dataset containing Malayalam tokens.
- **Processing:**
  - Input: Malayalam text from the Speech-to-Text API.
  - Output: Response in English text.

### 3. React Application

- **Framework:** React for building the user interface.
- **3D Graphics:** Three.js for rendering the interactive Ouija board.
- **Features:**
  - Display a virtual Ouija board similar to the provided image.
  - Animate the movement of a glass piece based on the model's response.
  - Integrate sound effects to mimic the ambiance of a real Ouija board session.

### 4. Backend Server

- **Purpose:** Handle the communication between the frontend React app, the Speech-to-Text API, and the LLM.
- **Technology:** Node.js/Express.
- **Functionality:**
  - Receive audio input from the frontend.
  - Send audio to the Speech-to-Text API and receive transcribed text.
  - Send transcribed text to the LLM and receive the response.
  - Return the response to the frontend for display and animation.

## Workflow

1. **User Interaction:**
   - The user speaks to Anamika in Malayalam using a microphone.
   - The audio input is captured by the React app.

2. **Speech-to-Text Conversion:**
   - The captured audio is sent to the Speech-to-Text API.
   - The API converts the audio to Malayalam text.

3. **Language Processing:**
   - The Malayalam text is sent to the backend server.
   - The backend server processes the text using the 7B LLaMA-2 Indic model.
   - The model generates an English response.

4. **Ouija Board Interaction:**
   - The English response is sent back to the React app.
   - The app animates the movement of the glass piece on the Ouija board to spell out the response.
   - Sound effects are played to enhance the experience.

## Conclusion

This project combines advanced technologies to create a unique and interactive experience. Users can communicate with Anamika through speech, and the virtual Ouija board brings the ghostly responses to life. This README provides a high-level overview and implementation concepts for the project.

For detailed instructions and code examples, refer to the respective directories and documentation within the repository.

## Relevant Links:

- [React Ouija Board](https://medium.com/@meirgotroot/the-spooky-side-of-ai-building-an-animated-ouija-board-app-fbe4485aa336)
- [Indic LLMs](https://huggingface.co/abhinand/malayalam-llama-7b-instruct-v0.1)
- [MallayaLLM](https://github.com/VishnuPJ/MalayaLLM)
