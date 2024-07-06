- 👋 Hi, I’m @TELMAAGUIAR
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
import matplotlib.pyplot as plt
from matplotlib.patches import Ellipse, Polygon, PathPatch
from matplotlib.path import Path

fig, ax = plt.subplots(figsize=(8, 8))

# Draw the key handle (circle)
handle = plt.Circle((0.5, 0.7), 0.1, color='black', fill=False, lw=2)
ax.add_patch(handle)

# Draw the key shaft
key_shaft = PathPatch(Path([(0.5, 0.7), (0.5, 0.4)], [Path.MOVETO, Path.LINETO]), lw=2, color='black')
ax.add_patch(key_shaft)

# Draw the key teeth
teeth = PathPatch(Path([(0.5, 0.4), (0.48, 0.35), (0.52, 0.35), (0.5, 0.3)], [Path.MOVETO, Path.LINETO, Path.LINETO, Path.LINETO]), lw=2, color='black')
ax.add_patch(teeth)

# Draw the eye
eye = Ellipse((0.5, 0.7), 0.06, 0.12, edgecolor='black', facecolor='white', lw=2)
ax.add_patch(eye)
pupil = Ellipse((0.5, 0.7), 0.02, 0.04, edgecolor='black', facecolor='black')
ax.add_patch(pupil)

# Draw the leaf (styled around the key)
leaf = Polygon([(0.5, 0.55), (0.45, 0.6), (0.4, 0.7), (0.45, 0.8), (0.5, 0.85), (0.55, 0.8), (0.6, 0.7), (0.55, 0.6)], closed=True, color='green', lw=2)
ax.add_patch(leaf)

# Remove axes
ax.axis('off')

# Show plot
plt.show()

<!---
TELMAAGUIAR/TELMAAGUIAR is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
