# discord-music
discord-music
import requests

data = {
    "name": "testuser",
    "password": "testpassword",
    "ip": "127.0.0.1"
}

response = requests.post("http://localhost:5000/user", json=data)
import requests

response = requests.get("http://localhost:5000/user")

print(response.json())
import os
import pygame

class MusicBot:
    def __init__(self):
        pygame.mixer.init()

    def add_song(self, file_path):
        pygame.mixer.music.load(file_path)

    def play_song(self):
        pygame.mixer.music.play()

    def stop_song(self):
        pygame.mixer.music.stop()

# Example usage
music_bot = MusicBot()
music_bot.add_song("/path/to/your/song.mp3")
music_bot.play_song()
