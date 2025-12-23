# Valorant Rank Widget  

This project is a **Valorant Rank Widget** that dynamically displays your current rank, rank rating (RR), and rank image. It includes animations for rank changes, such as fading in and out of the rank image and counting up or down the rank rating.

The widget is customizable and designed for use in streaming software like OBS.

---

## Features  

- Real-time updates of Valorant rank, rank rating, shield count & leaderboard placement.
- Smooth animations for rank, rank rating & leaderboard placement changes.
- First-time setup wizard with persistent settings (localStorage & URL parameters).
- Customizable background image via the setup form.
- Easy integration into OBS as a browser source via configured URL.
- Gear icon that appears on hover for quick access to settings.

---

## How to Use  

### 1. **Download Overlay.html**  
1. Click the green **Code** button at the top of the repository.  
2. Select **Download ZIP** and extract the contents to a folder on your computer.  
3. Locate and open `Overlay.html`.

---

### 2. **Open Overlay.html in Your Browser**  
1. Find `Overlay.html` in your Downloads folder (or wherever you extracted it).  
2. Open it in your preferred web browser (Chrome, Firefox, Edge, etc.).  
3. The **First-Time Setup** overlay will automatically appear.

---

### 3. **Fill Out the Setup Form**  
The setup wizard will ask for:

- **API Key** – Get your free API key from the [Henrik Dev Discord](https://discord.gg/X3GaVkX2YN) (check the #get-a-key text channel).  
- **Valorant Username** – Your username before the `#` (e.g., "JstDave" for "JstDave#JST").  
- **Valorant Tag** – Your tag after the `#` (e.g., "JST" for "JstDave#JST").  
- **Region** – Select your region (NA, EU, LATAM, BR, AP, or KR).  
- **Platform** – Select your platform (PC or Console).  
- **Background Image URL (Optional)** – Paste a direct link to a custom background image. Leave blank to use the default background.

![First-Time Setup](https://i.imgur.com/y5rthRu.png)

---

### 4. **Copy the Configured URL**  
1. After filling in your details, click the **"Copy Configured URL"** button.  
2. This copies a URL with all your settings embedded as query parameters.  
3. You can now close the setup overlay or proceed to OBS.

---

### 5. **Create a Browser Source in OBS**  
1. Open OBS Studio.  
2. In your scene, add a new source by clicking the **+** button under **Sources**.  
3. Select **Browser** from the menu.  

![OBS Browser Source Creation](https://i.imgur.com/Pjtv7vt.png)

---

### 6. **Paste the Configured URL**  
1. In the Browser source settings, paste the URL you copied in step 4 into the **URL** field.  
2. Set the following dimensions:
   - **Width:** 1100px  
   - **Height:** 500px  
3. Click **OK**.

![Pasting URL into OBS](https://i.imgur.com/Qw8a1gf.png)

---

### 7. **You're Done!**  
The widget is now live in your OBS scene! It will:
- Automatically update your rank, RR, and leaderboard placement every minute.
- Display smooth animations when your rank or RR changes.
- Show shields or leaderboard placement based on your current rank status.
- Use your custom background image if you provided one.

---

## Settings & Customization  

### Accessing Settings Later  
- **Hover over the widget** – A gear icon (⚙️) will appear in the top-right corner.  
- **Click the gear icon** – This opens the setup form anytime to update or change your settings.  

### Resetting Settings  
- Click the **"Reset saved settings"** link in the setup form to clear all stored information and start fresh.

### Changing the Background Image  

#### Option 1: Via Setup Form (Recommended)
1. Hover over the widget and click the gear icon (⚙️).
2. Paste your background image URL in the **"Background Image URL"** field.
3. Click **"Save & Apply"** or **"Copy Configured URL"**.

#### Option 2: Manual Code Edit
1. Open `Overlay.html` in a text editor (VSCode, Notepad, etc.).  
2. Find the `.rank-box` class in the `<style>` section:  

    ```css
    .rank-box {
        background-image: url('https://i.imgur.com/7LtBNJ3.png');
    }
    ```

3. Replace the URL with your preferred background image link.  
   - For example: `background-image: url('your-image-url-here');`  
   - Or use a local image: `background-image: url('background.jpg');` (place the image file in the same folder as `Overlay.html`).

---

## Storage & Privacy  

- **localStorage** – Your settings are saved locally in your browser for convenience.  
- **URL Parameters** – Settings are embedded in the URL, making it easy to share or back up your configuration.  
- **API Key Security** – If you're concerned about exposing your API key in the URL, rely on localStorage instead. You can optionally remove the `api_key` parameter when sharing the widget link.

---

## Notes  

- The widget updates automatically every 60 seconds.  
- Settings persist across browser sessions when using localStorage or configured URLs.
- Ensure your API key and username/tag are correct to avoid errors.  
- If you encounter issues, check the browser console (F12 → Console tab) for error messages.  
- For support or questions, contact me on my [socials](https://jstdave.com/socials).

---

## Example Pictures & Rankup Animation
<img src="https://i.imgur.com/n0BbsI2.png" height="300"> <img src="https://i.imgur.com/rxL5SU5.png" height="300"> ![Example-Video](https://github.com/user-attachments/assets/a77ed1aa-f2f6-4eb6-b6ce-52e0f2be987f)

## Example Picture of an Account with Leaderboard Placement (Top 15000)
<img src="https://i.imgur.com/uLpKBYg.png" height="300">
