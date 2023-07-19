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
- Android Ripple Effect
- Platform API: Platform.OS
- Implementig Navigation Between two screens:
  - React Navigation: navigation prop and route prop
- Styling:
  - flex: 1, take all available space
