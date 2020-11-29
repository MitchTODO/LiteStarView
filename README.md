#  LiteStarView ⭐️⭐️⭐️⭐️⭐️

## Desciption

A light weight star ⭐️ rating UI component for iOS written in Swift.

## Installation 

### Manually 

You can download or copy the following files 

- StarView.swift
- StarGestures.swift
- StarBezier.swift

### CocoaPods

Currently not on CocoaPods 

## Setup

1. Create and drop a UIView then set the class to StarView.

![alt text](ReadmePic/className.png "Title")

2. Set your constraints
- Top
- Trailing
- Leading 
- Height

![alt text](ReadmePic/constraints.png "Constraints")

The view can be set up in one of two ways.

- Show Rating (Non-interactive)
![alt text](ReadmePic/userEnabled.png "User Interaction Enabled")
![alt text](ReadmePic/starFloat.gif "Float")
![alt text](ReadmePic/starInt.gif "Int")

- User provide rating (interactive)
![alt text](ReadmePic/userDisabled.png "User Interaction Disabled")
![alt text](ReadmePic/screenShot.png "User Interaction Enabled")

## Design

The design is minimalist, with a few customizations. 

**Note**: *This view is not currently IBDesignable*

### Features 

- Can be used to show ratings followed by number of ratings.
- If `isUserInteractionEnabled` user can provied a rating by panning or tapping on stars, rating will be shown.
- Gives haptic Feedback when user selects/deselect one full star
- Round stars to the nears whole 

### Modifiers / Customization

- `starCount` :`Int`              : Number of stars in view  
- `ratingCount`:`Int`           : Amount of ratings for item
- `rating`: `CGFloat`            : Rating for item
- `roundRating`:`Bool`         : Keeps rating in whole numbers
- `fillColor` :`UIColor`      : Star fill color
- `stokeColor` :`UIColor`    : Star outline (strokeColor) color 


## Behavior

### Updating the view

Stars are automaticity update when when the `rating` or `ratingCount` changes. 
Also calling `starView.updateStar()` will force a update. So make your changes before calling!


### Calculating user set star rating by width and pan gesture


