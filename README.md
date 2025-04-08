# YouTube Live Chat Custom CSS 🎨

This repository contains a custom CSS stylesheet designed to modify and improve the visual appearance of the YouTube Live Chat. It focuses on creating a cleaner, minimalistic, and more user-friendly chat interface by hiding unnecessary elements and enhancing the readability and aesthetics of chat messages.

## Preview:
![Preview](https://i.imgur.com/ghggL7P.png)

## Features:

- **Modern Design**: Streamlines the YouTube Live Chat with a transparent background and custom chat message bubbles for a more modern and visually appealing interface. ✨
- **Customizable**: Easily modify the CSS to adjust colors, font sizes, and background styles to fit your personal preferences. 🎨
- **Color-Coded User Roles**: Differentiates users by their roles (e.g., channel owner, moderator, members) using distinct colors for their names. 🌈

## Installation: ⚙️

Follow these steps to apply the custom CSS to your YouTube Live Chat:

1. **Copy the CSS Code**  
   Go to the [CSS file on GitHub](https://github.com/Finzxy/costum_css_for_youtube_livechat_V1/blob/main/livechatV1.css) and copy the entire CSS code. 📋

2. **Open OBS Studio**  
   Launch OBS Studio on your computer. 🎥

3. **Add Browser Source**  
   In OBS, click the **"+"** button under the "Sources" box and select **"Browser"**. ➕

4. **Enter Your Live Chat URL**  
   In the **"Create/Select Source"** window, name your source (e.g., "YouTube Live Chat") and click **"OK"**.  
   In the **"URL"** field, enter your live chat URL (e.g., `https://studio.youtube.com/your_live_chat_id`). 🌐

5. **Add Custom CSS**  
   Scroll down to the **"Custom CSS"** field in the Browser Source settings.  
   Paste the CSS code you copied in step 1 into this field. 📑

6. **Click "OK"**  
   Once the custom CSS is applied, click **"OK"** to save your changes. ✅

7. **Enjoy Your New Live Chat Style**  
   Your YouTube Live Chat should now have a cleaner and more stylish appearance in OBS! 🎉

## Customization: 🔧

Feel free to modify the CSS to suit your personal preferences, including adjusting colors, font sizes, and background styles. You can tweak it to make the chat interface exactly how you like it! 🎨

Here's a breakdown of the CSS code and what each section does:

## Hide Unnecessary Elements:
yt-live-chat-mode-change-message-renderer,
yt-live-chat-viewer-engagement-message-renderer,
yt-live-chat-restricted-participation-renderer,
yt-live-chat-banner-manager,
yt-live-chat-action-panel-renderer,
yt-live-chat-renderer #action-panel,
yt-reaction-control-panel-overlay,
yt-reaction-control-panel-overlay-view-model,
yt-reaction-control-panel-view-model,
yt-live-chat-viewer-engagement-message-renderer,
yt-live-chat-ticker-renderer,
yt-live-chat-text-message-renderer[is-deleted],
yt-live-chat-legacy-paid-message-renderer[is-deleted],
yt-live-chat-header-renderer,
yt-live-chat-moderation-message-renderer,
yt-live-chat-message-input-renderer {
    display: none !important;
}

## Set Transparent Background for Chat:
yt-live-chat-renderer,
yt-live-chat-item-list-renderer {
    background: transparent !important;
}

## Custom Chat Message Design:
yt-live-chat-text-message-renderer {
    padding: 12px;
    background: #17202a !important;
    border-radius: 8px !important;
    margin-bottom: 18px !important;
    box-shadow: 0px 10px 5px 0px rgba(0, 0, 0, 1);
}

## Increase Font Size for Chat Messages:
yt-live-chat-text-message-renderer #message {
    font-size: 20px !important;
}

## Increase Font Size and Bold Usernames:
yt-live-chat-text-message-renderer #author-name {
    font-size: 18px !important;
    font-weight: bold !important;
}
## Add Colon After Username;
yt-live-chat-text-message-renderer #author-name::after {
    content: " :";
    font-weight: bold !important;
    color: #fff !important;
    margin-left: 3px !important;
}

## Color-Coding Based on User Role:
yt-live-chat-text-message-renderer[author-type="owner"] #author-name {
    color: red !important;
}

yt-live-chat-text-message-renderer[author-type="moderator"] #author-name {
    color: blue !important;
}

yt-live-chat-text-message-renderer[author-type="member"] #author-name {
    color: #239b56 !important;
}

yt-live-chat-text-message-renderer #author-name {
    color: #ff9c33 !important;
}
Purpose: Differentiates users by their roles:

- Owner: Red

- Moderator: Blue

- Member: Green (#239b56)

- Regular User: Orange (#ff9c33)

Modify the color values to use any color you prefer.

## Hide User Avatars
yt-live-chat-text-message-renderer #author-photo,
yt-live-chat-paid-message-renderer #author-photo,
yt-live-chat-legacy-paid-message-renderer #author-photo {
    display: none !important;
}

## Remove Scrollbars
yt-live-chat-item-list-renderer #items,
yt-live-chat-item-list-renderer #item-scroller {
    overflow: hidden !important;
}

## Remove Underlines from Links
yt-live-chat-text-message-renderer a,
yt-live-chat-legacy-paid-message-renderer a {
    text-decoration: none !important;
}

## License: 📜
This project is licensed under the MIT License.
