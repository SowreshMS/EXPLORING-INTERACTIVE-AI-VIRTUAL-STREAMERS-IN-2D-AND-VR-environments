# EXPLORING-INTERACTIVE-AI-VIRTUAL-STREAMERS-IN-2D-AND-VR-environments
By: Sowresh Mecheri-Senthil, Jose Garcia, Terrell Johnson, Korbin Schulz, Abbas Khawaja

# Introduction
  Streaming, particularly with the advent of virtual streamers or VTubers, has gained immense popularity in the entertainment industry. However, the interactivity that popular streaming platforms like Twitch offer is bounded by the constraints of a 2D screen $^{[1]}$. We introduce Vivi, an AI-powered virtual streamer equipped with machine learning models for intelligent communication with viewers. Deployed on both Twitch and in a Virtual Reality (VR) environment, Vivi aims to enhance user immersion and interaction while mimicking human streamers.

# Architecture
  The design goal of Vivi is to interact seamlessly with the viewers and stream on both traditional platforms like Twitch and in a VR environment, catering to the preferences of both PC and VR users (Fig. 1).

  PC User: For PC users, interaction occurs through the Twitch chat, where the user's input is read and contextualized by a Large Language Model (LLM) that generates sentiments and responses tailored to the user's messages. The LLM prompts the avatar to evoke specific facial animations and contextualizes user game requests, influencing the streamer's choice of games. Additionally, the LLM interprets in-game information, enabling the streamer to provide commentary on the ongoing gameplay. Finally, Vivi replies back to the user through the avatar, facilitating a dynamic streaming experience.
    
  VR User: In the VR environment, users have the ability to communicate through speech and hand gestures directed towards the virtual streamer. These actions are interpreted and contextualized by the Large Language Model (LLM), prompting the avatar to respond accordingly. For example, Vivi can answer questions or engage in interactive gestures such as a hand shake, enhancing the immersive experience for VR users.

# Environment
  We developed four games (Fig. 2) in the Unity Game Engine and added a game menu to facilitate switching between them. Each game was trained using MLAgents, where the agent is rewarded for achieving a goal and penalized for failing to meet certain criteria$^{[2]}$. The model is activated after the streamer selects a game (Fig. 3).
