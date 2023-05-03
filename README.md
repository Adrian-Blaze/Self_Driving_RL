# Self_Driving_RL

This codebase is using the Stable Baselines3 library to train a self-driving agent for the CarRacing-v2 environment in OpenAI Gym. It uses the PPO algorithm with a convolutional neural network policy, and trains for a total of some timesteps.

The code starts by importing the necessary libraries and creating the environment. It also creates a VideoRecorder object to record videos of the agent's performance during training.

Then we test run the environment and render it using Gym and the gym.wrappers.monitoring.video_recorder module. The code creates a VideoRecorder object for the environment, which records a video of the environment during each episode.

The loop runs for a specified number of episodes and for each episode, it captures the frame of the environment and renders it. The loop then saves the frame to the VideoRecorder object and calculates the score for the episode.

Once the loop is complete, the VideoRecorder object is closed and the environment is shut down.

The environment is then wrapped in a DummyVecEnv to allow for vectorized training with a single environment. A log path is defined for storing TensorBoard logs.

The PPO model is initialized with the 'CnnPolicy' and the environment, and the model is trained using the learn method for a total of 100000 timesteps.

Finally, the trained model is evaluated using the evaluate_policy function with 10 evaluation episodes and rendering enabled.

