# Enable Spotlight search on Mac


## Method 1
Navigate to
1. System Preferences
2. Spotlights
3. Privacy
4. Add your local disk to the list 
5. Remove your local disk from the list
The above steps will reindex spotlight on the selected disk

## Method 2
In terminal run:
```
sudo mdutil -E /
sudo mdutil -a -i on
```
Above commands fixed everything for me

