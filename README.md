# PGDPertemuan5

1. Part A - Part E - Part C - Part G - Part B - Part M - Part I - Part H - Part J - Part D - Part F - Part L - Part K

2. class Opponent(Block):
	def __init__(self,path,x_pos,y_pos,speed):
		super().__init__(path,x_pos,y_pos)
		self.speed = speed

	def update(self,ball_group):
		if self.rect.top < ball_group.sprite.rect.y:
			self.rect.y += self.speed
		if self.rect.bottom > ball_group.sprite.rect.y:
			self.rect.y -= self.speed
		self.constrain()

	def constrain(self):
		if self.rect.top <= 0: self.rect.top = 0
		if self.rect.bottom >= screen_height: self.rect.bottom = screen_height
    
    Program tersebut merupakan implementasi AI karena pada script tersebut mengatur paddle yang berada di sebelah kiri bergerak secara otomatis ke atas dan ke bawah bersamaan mengikuti pergerakan bola
    
3. Ball akan bergerak atau memantul ke arah paddle pemain dan computer secara berulang ulang. Paddle kiri bergerak secara otomatis sedangkan paddle kanan bergerak sesuai keyboard    yang ditekan yaitu ke atas atau ke bawah. Score dihitung dari ball yang masuk ke gawang lawan.
