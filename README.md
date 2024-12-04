# Valorant Rank Widget  

This project is a **Valorant Rank Widget** that dynamically displays your current rank, rank rating (RR), and rank image. It includes animations for rank changes, such as fading in and out of the rank image and counting up or down the rank rating.

The widget is customizable and designed for use in streaming software like OBS.

---

## Features  

- Real-time updates of Valorant rank and rank rating.
- Smooth animations for rank and rank rating changes.
- Customizable background image, API key, username, and tag.
- Easy integration into OBS as a local browser source.

---

## How to Use  

### 1. **Download the Widget**  
1. Click the green **Code** button at the top of the repository.  
2. Select **Download ZIP** and extract the contents to a folder on your computer.  

---

### 2. **Set Up Your API Key, Username, and Tag**  
1. Open the `index.html` file in any text editor (e.g., Notepad, VSCode).  
2. Locate the following section in the `<script>` tag:  

    ```javascript
    // Please add your information here
    const API_KEY = "YOUR_API_KEY"; // Replace with your API key
    const USERNAME = "YOUR_USERNAME";   // Replace with your Valorant username
    const TAG = "YOUR_TAG";             // Replace with your Valorant tag
    ```

3. Replace the placeholders with:  
   - Your **API key** from [Henrik Dev API]([https://henrikdev.xyz/valorant](https://discord.gg/henrikdev-systems-704231681309278228)).
   - Your **Valorant username** (in quotes) (For example "JstDave" for the name "JstDave#JST").  
   - Your **Valorant tag** (in quotes) (For example "JST" for the name "JstDave#JST").  

---

### 3. **Change the Background Image**  
1. Locate the `.rank-box` class in the `<style>` tag:  

    ```css
    .rank-box {
        background-image: url('https://i.imgur.com/VW2vLbY.png');
    }
    ```

2. Replace the URL with the link to your preferred background image.  
   - For example: `background-image: url('your-image-url-here');`  

   Alternatively, you can use a local image by placing it in the same folder as `index.html` and changing the URL to the file name.  
   - Example: `background-image: url('background.jpg');`  

---

### 4. **Add the Widget to OBS**  
1. Open OBS Studio.  
2. Add a new **Browser Source**.  
3. Set the following:
   - **Local File:** Check the checkbox **"Local File"**.
   - **Browse:** Click the **Browse** button and select your `index.html` file.  
   - **Width:** 1100px  
   - **Height:** 400px  
5. Adjust the size and position of the widget in your OBS scene as needed.

---

## Notes  

- The widget updates automatically every 2 minutes.  
- Ensure your API key and username/tag are correct to avoid errors.  
- If you encounter issues, check the browser console for error messages.  

