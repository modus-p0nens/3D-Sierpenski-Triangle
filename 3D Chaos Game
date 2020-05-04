from mpl_toolkits.mplot3d import Axes3D
import matplotlib
import matplotlib.pyplot as plt
import numpy as np
matplotlib.use("Agg")
from matplotlib.animation import FFMpegWriter

metadata = dict(title='Movie Test', artist='Matplotlib',
                comment='Movie support!')
writer = FFMpegWriter(fps=15, metadata=metadata)

# Fixing random state for reproducibility
np.random.seed(19680801)

fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

x = 0
y = 0
z = 0

for n in range(0,10000):
	k = np.random.randint(0,4)
	if(k==0):
		x = (x+0)/2
		y = (y+0)/2
		z = (z+1)/2   
	elif(k==1):
		x = (x+0)/2
		y = (y+1)/2
		z = (z+0)/2   
	elif(k==2):
		x = (x- (pow(3,1/2)/2) )/2
		y = (y- (1/2))/2
		z = (z+0)/2    
	elif(k==3):
		x = (x + (pow(3,1/2)/2) )/2
		y = (y-(1/2))/2
		z = (z+0)/2   
	ax.scatter(x, y, z, c = 'k', marker = '.')

ax.set_xlabel('X Label')
ax.set_ylabel('Y Label')
ax.set_zlabel('Z Label')

# rotate the axes and update
for angle in range(0, 360):
    ax.view_init(30, angle)
    plt.draw()
    plt.pause(.001)

with writer.saving(fig, "writer_test.mp4", 100):
    for i in range(100):
        x0 += 0.1 * np.random.randn()
        y0 += 0.1 * np.random.randn()
        l.set_data(x0, y0)
        writer.grab_frame()