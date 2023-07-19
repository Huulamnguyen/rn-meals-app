## React Native MEALS APP:

- A simple application by React Native to navigate to Food Categories

## Topics:

- Navigation in React Native
- Displaying items in Grids
- Learn more about styling

## Documentation:

- Flatlist - an example of using Flatlist

  ```javascript
  const MealsOverviewScreen = ({ route }) => {
    const catId = route.params.categoryId;

    const displayedMeals = MEALS.filter((meal) => {
      return meal.categoryIds.indexOf(catId) >= 0;
    });

    const renderMealItem = (itemData) => {
      return <MealsDetail title={itemData.item.title} />;
    };

    return (
      <View style={styles.container}>
        <FlatList
          data={displayedMeals}
          keyExtractor={(item) => item.id}
          renderItem={renderMealItem}
        />
      </View>
    );
  };
  ```

- Grid Styles
- Shadows: shadowColor, shadowOpacity, shadowRadius, shadowOffset
  ```javascript
  elevation: 4,
  shadowColor: "black",
  shadowOpacity: 0.5,
  shadowRadius: 8,
  shadowOffset: { width: 0, height: 6 },
  overflow: Platform.OS === "android" ? "hidden" : "visible",
  ```
- Android Ripple Effect and opacity for IOS

  ```javascript
  <Pressable
    android_ripple={{ color: "#ccc" }}
    style={({ pressed }) => (pressed ? styles.buttonPressed : null)}
  >
    //code
  </Pressable>

  // then

  buttonPressed: {
    opacity: 0.75,
  },
  ```

- Platform API: Platform.OS
- React Navigation: navigation prop and route prop
- Styling:
  - flex: 1, take all available space
