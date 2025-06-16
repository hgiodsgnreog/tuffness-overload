# tuffness-overload import pygame
import time
import random

# Initialize pygame
pygame.init()

# Set up display
width, height = 600, 400
win = pygame.display.set_mode((width, height))
pygame.display.set_caption("Snake Game")

# Colors
black = (0, 0, 0)
white = (255, 255, 255)
red = (213, 50, 80)
green = (0, 255, 0)
blue = (50, 153, 213)

# Snake settings
block_size = 10
clock = pygame.time.Clock()

font = pygame.font.SysFont("comicsans", 25)

def draw_snake(block_size, snake_list):
    for x in snake_list:
        pygame.draw.rect(win, green, [x[0], x[1], block_size, block_size])

def game_loop():
    game_over = False
    game_close = False

    x, y = width // 2, height // 2
    x_change, y_change = 0, 0
    snake_list =
