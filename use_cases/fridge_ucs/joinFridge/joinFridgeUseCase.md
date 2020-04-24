# Fridgify

## Use-Case Specification: Join Fridge

## 1. Join Fridge

### 1.1 Brief Description

Fridgify offers the option to have a shared fridge. One user has to create a fridge and offer other users to join the fridge.

## 2. Flow of Events

### 2.1 Basic Flow

The user needs to log into the app. When clicking on the add panel a popup is displayed that offers the option to join or create a fridge. The user has to click on join fridge. The user can now scan a barcode to join an existing fridge. The joined fridge is then immediately displayed on the main page and the user is redirected to the main page. 

### 2.1.1 Activity Diagram

![Activity diagram get fridges](./joinFridgeActivityDiagram.png)

### 2.1.2 Mock Up

![Join Fridge](./fridgesMockUp.png)
![Add Fridge via QR](./AddFridge.png)

### 2.1.3 Feature File
```gherkin
Feature: Overview Screen
  The User is on the Fridge Overview Screen

  Scenario: The User Joins Fridge
    Given I see "overview"
    When I tap the"join" label
    Then I see screen "join"
```

## 3. Special Requirements

### 3.1. Owning an account

In order to join a fridge the user has to have an account. Only if he has one he will be able to join a fridge.

## 4. Preconditions

### 4.1 The user downloaded the app 

The user has to have already downloaded the app.

## 5. Postconditions

### 5.1 The user is a member of a new fridge

The user sees the fridge on the main page and can add items to the fridge.

## 6. Extension Points

**n / a**
