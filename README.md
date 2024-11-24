import pygame

# กำหนดค่าตัวละคร
player_x = 100
player_y = 100
player_speed = 5

# วนลูปเกม
running = True
while running:
    # ตรวจสอบการกดปุ่ม
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # ตรวจสอบการกดปุ่มลูกศร
    keys = pygame.key.get_pressed()
    if keys[pygame.K_LEFT]:
        player_x -= player_speed
    if keys[pygame.K_RIGHT]:
        player_x += player_speed
    if keys[pygame.K_UP]:
        player_y -= player_speed
    if keys[pygame.K_DOWN]:
        player_y += player_speed

    # อัพเดตหน้าจอ
    pygame.display.flip()

pygame.quit()
