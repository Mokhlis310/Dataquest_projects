%matplotlib inline
import pandas as pd
import matplotlib.pyplot as plt

women_degrees = pd.read_csv('percent-bachelors-degrees-women-usa.csv')
cb_dark_blue = (0/255,107/255,164/255)
cb_orange = (255/255, 128/255, 14/255)
stem_cats = ['Psychology', 'Biology', 'Math and Statistics', 'Physical Sciences', 'Computer Science', 'Engineering']
lib_arts_cats = ['Foreign Languages', 'English', 'Communications and Journalism', 'Art and Performance', 'Social Sciences and History']
other_cats = ['Health Professions', 'Public Administration', 'Education', 'Agriculture','Business', 'Architecture']
fig = plt.figure(figsize=(13, 21))

# The loop for STEM categories

location = 1
for sp in range(0,6):
    if sp == 0:
        ax = fig.add_subplot(6,3,location)
        ax.text(2002, 87, 'Women')
        ax.text(2002, 8, 'Men')
    else:
        location += 3
        ax = fig.add_subplot(6,3,location)
        
    ax.plot(women_degrees['Year'], women_degrees[stem_cats[sp]], c=cb_dark_blue, label='Women', linewidth=3)
    ax.plot(women_degrees['Year'], 100-women_degrees[stem_cats[sp]], c=cb_orange, label='Men', linewidth=3)
    ax.spines["right"].set_visible(False)    
    ax.spines["left"].set_visible(False)
    ax.spines["top"].set_visible(False)    
    ax.spines["bottom"].set_visible(False)
    ax.set_xlim(1968, 2011)
    ax.set_ylim(0,100)
    ax.set_title(stem_cats[sp])
    ax.tick_params(bottom="off", top="off", left="off", right="off", labelbottom = 'off')
    ax.set_yticks([0,100])
    ax.axhline(50, c=(171/255, 171/255, 171/255), alpha=0.3)
    
    if sp == 5:
        ax.text(2002, 93, 'Men')
        ax.text(2002, 5, 'Women')
        ax.tick_params(labelbottom = 'on')
        
# The loop for lib_ARTS categories
location = 2        
for sp in range(0,5):
    if sp == 0:
        ax = fig.add_subplot(6,3,location)
        ax.text(2002, 78, 'Women')
        ax.text(2002, 20, 'Men')
    else:
        location += 3
        ax = fig.add_subplot(6,3,location)
        
    ax.plot(women_degrees['Year'], women_degrees[lib_arts_cats[sp]], c=cb_dark_blue, label='Women', linewidth=3)
    ax.plot(women_degrees['Year'], 100-women_degrees[lib_arts_cats[sp]], c=cb_orange, label='Men', linewidth=3)
    ax.spines["right"].set_visible(False)    
    ax.spines["left"].set_visible(False)
    ax.spines["top"].set_visible(False)    
    ax.spines["bottom"].set_visible(False)
    ax.set_xlim(1968, 2011)
    ax.set_ylim(0,100)
    ax.set_title(lib_arts_cats[sp])
    ax.tick_params(bottom="off", top="off", left="off", right="off", labelbottom= 'off')
    ax.set_yticks([0,100])
    ax.axhline(50, c=(171/255, 171/255, 171/255), alpha=0.3)
    
    if sp == 4:
        ax.text(2005, 55, 'Men')
        ax.text(2001, 42, 'Women')
        ax.tick_params(labelbottom= 'on')
        
# The loop for Others categories

location = 3

for sp in range(0,6):
    if sp == 0:
        ax = fig.add_subplot(6,3,location)
        ax.text(2005, 5, 'Men')
        ax.text(2002, 90, 'Women')
    else:
        location += 3
        ax = fig.add_subplot(6,3,location)
        
    ax.plot(women_degrees['Year'], women_degrees[other_cats[sp]], c=cb_dark_blue, label='Women', linewidth=3)
    ax.plot(women_degrees['Year'], 100-women_degrees[other_cats[sp]], c=cb_orange, label='Men', linewidth=3)
    ax.spines["right"].set_visible(False)    
    ax.spines["left"].set_visible(False)
    ax.spines["top"].set_visible(False)    
    ax.spines["bottom"].set_visible(False)
    ax.set_xlim(1968, 2011)
    ax.set_ylim(0,100)
    ax.set_title(other_cats[sp])
    ax.tick_params(bottom="off", top="off", left="off", right="off", labelbottom = 'off')
    ax.set_yticks([0,100])
    ax.axhline(50, c=(171/255, 171/255, 171/255), alpha=0.3)
    
    if sp == 5:
        ax.text(2005, 62, 'Men')
        ax.text(2001, 32, 'Women')
        ax.tick_params(labelbottom = 'on')

plt.savefig("gender_degrees.png")        
        
plt.show()
