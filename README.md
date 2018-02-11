# JView
Minor project to ease the typical scene switching hassle with javafx

# How to use

Adding to project
1. Add JView jar to your build path
2. Use View object to swap current active view in a javafx project

Pre-usage
- JView must know your main stage, thus it's recommended to set mainstage through ViewConfiguration directly upon startup, see example

Example
```java
  //Instantiating a javafx project with a source folder views in the root directory of the build path
	@Override
	public void start(Stage primaryStage) {
		View.getConfiguration().setMainStage(primaryStage);
		View.getConfiguration().setViewSourceFolder("/views");
		View.switchTo("Launcher.fxml");
  }
  
  //Refreshing current active View
  public void updatePage() {
    View.refreshPage();
  }
  
  //Immediately shuts down the current active View
  public void exitWindow() {
    View.closeView();
  }
```

# License
[MIT License](https://github.com/Kavzor/MongoJRepo/blob/master/LICENSE)
