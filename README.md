# EXPLORING-INTERACTIVE-AI-VIRTUAL-STREAMERS-IN-2D-AND-VR-environments
*By: Sowresh Mecheri-Senthil, Jose Garcia, Terrell Johnson, Korbin Schulz, Abbas Khawaja*

## Introduction
Streaming, particularly with the advent of virtual streamers or VTubers, has gained immense popularity in the entertainment industry. However, the interactivity that popular streaming platforms like Twitch offer is bounded by the constraints of a 2D screen. We introduce Vivi, an AI-powered virtual streamer equipped with machine-learning models for intelligent communication with viewers. Deployed on both Twitch and in a Virtual Reality (VR) environment, Vivi aims to enhance user immersion and interaction while mimicking human streamers.

## Architecture
![architecture](https://github.com/SowreshMS/EXPLORING-INTERACTIVE-AI-VIRTUAL-STREAMERS-IN-2D-AND-VR-environments/assets/132632885/519eeb84-e5bb-418b-8e5d-7975392cc8cd)

The design goal of Vivi is to interact seamlessly with the viewers and stream on both traditional platforms like Twitch and in a VR environment, catering to the preferences of both PC and VR users (Fig. 1).

**PC User**: For PC users, interaction occurs through the Twitch chat, where the user's input is read and contextualized by a Large Language Model (LLM) that generates sentiments and responses tailored to the user's messages. The LLM prompts the avatar to evoke specific facial animations and contextualizes user game requests, influencing the streamer's choice of games. Additionally, the LLM interprets in-game information, enabling the streamer to provide commentary on the ongoing gameplay. Finally, Vivi replies back to the user through the avatar, facilitating a dynamic streaming experience.
    
**VR User**: In the VR environment, users have the ability to communicate through speech and hand gestures directed toward the virtual streamer. These actions are interpreted and contextualized by the Large Language Model (LLM), prompting the avatar to respond accordingly. For example, Vivi can answer questions or engage in interactive gestures such as a handshake, enhancing the immersive experience for VR users.

## Components

**Environment**: We developed four games (Fig. 2) in the Unity Game Engine and added a game menu to facilitate switching between them. Each game was trained using MLAgents, where the agent is rewarded for achieving a goal and penalized for failing to meet certain criteria. The model is activated after the streamer selects a game (Fig. 3).

**Large Language Model (LLM)**: Our LLM is powered by GPT-3.5, a state-of-the-art LLM that can comprehend human language and generate relevant text based on it. To improve Vivi's streamer-like persona, we used prompt engineering to fine-tune the LLM's responses. In the 2D environment, Vivi interacts with viewers by responding to messages in the Twitch chat. In the VR environment, Vivi dynamically responds to user speech.  

**Avatar**: We created Vivi's avatar using VRoid Studio, a 3D humanoid avatar creation application. The avatar's expressions change according to the sentiment from our LLM (Fig. 4). We used Mixamo animations to create haptic interactions the VR users can interact with (Fig. 5). The streamer is able to reply to 2D and VR users using Google Cloud Platform's text-to-speech API.

**Stream**: The stream consists of two main components: Streamlabs and Twitch. We used Streamlabs to create a stream overlay and record the stream. Then, we used a Twitch API key to stream the content from Streamlabs. In the VR Environment, the stream is displayed on the TV (Fig. 6) and the streamer is within the environment.

## Results
While training our agents in various game environments, we observed a consistent pattern. Initially, the agents faced challenges in determining the optimal interactions within their respective environments to maximize rewards. However, as the number of executed steps increased, they exhibited gradual improvement and achieved more consistent higher rewards.

As the number of steps executed increased, the cumulative score's growth accelerated (Fig. 7). This trend shows that the agent was able to improve its performance and become more proficient at learning in its environment.

## Demos


## Conclusion
Experimentation in the "2D" environment illustrates Vivi's interaction capabilities in a standard streaming setting. Placing Vivi in a VR environment cultivates a more connected experience for viewers due to Vivi's ability to dynamically respond to spatial interactions, potentially attracting a larger audience. The immersive nature of VR enhances the possibilities for engagement, making the streaming experience more captivating and appealing to viewers.

[1] Wu, L., Liu, Q., Zhao, J., & Lank, E. (2023). Interactions across displays and space: A study of virtual reality streaming practices on Twitch. Proceedings of the ACM on Human-Computer Interaction, 7(ISS), 242–265. https://doi.org/10.1145/3626473

[2] Hanski, J., & Biçak, K. B. (2021). An Evaluation of the Unity Machine Learning Agents Toolkit in Dense and Sparse Reward Video Game Environments (Dissertation).

[3] Brown, T. B., et al \textit{Language Models are Few-Shot Learners} arXiv:2005.14165v4 [cs.CL] 22 Jul 2020}

