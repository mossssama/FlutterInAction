# Flutter In Action
A concise illustration of Flutter In Action in bullets

**Chapter 1**

- Flutter is a mobile SDK written in Dart that empowers everyone to build beautiful, performant mobile apps. 
- Dart is a language made by Google that can compile to JavaScript. It’s fast, strictly typed, and easy to learn.
- The advantages of using Flutter are that it compiles to native device code, making it more performant than other cross-platform options. It also has the best developer experience around, thanks to Dart’s JIT and Flutter’s hot reload.
- Flutter is ideal for anyone who wants to make a highly performant Cross platform app quickly. It’s probably not the best choice for a large company with existing native teams.
- In Flutter, everything is a widget. Widgets are simply Dart classes that describe their view. A UI is created by composing several small widgets into complete widget trees.
- Widgets come in two main Flavors: stateless and stateful.
- Flutter provides state management tools, such as widget life-cycle methods and special State objects.


**Chapter 2**

- Dart’s syntax is familiar if you know any C-like language.
- Dart is an object-oriented, strictly typed language.
- All Dart programs begin with a main function as the entry point to the application.
- Types are used to ensure that code is using the correct values at the correct time. They can seem cumbersome, but they’re helpful for reducing bugs.
- Functions must return types or void.
- Most operators in Dart are like operators in other languages, but there are a few special operators, such as ~/, is, and as.
- Null-aware operators are useful for performing null checks, which ensure that values are not null.
- For control flow, Dart supports if/else statements, as well as switch statements and ternary operators.
- Using an Enum with a switch statement enforces accounting for all possible cases.
- Loops in Dart should be familiar if you come from most other languages. There are for loops, for-in loops, while loops, and do while loops.
- Dart functions are objects and can be passed around like any other value. This is called a higher-order function in many languages.
- Dart is a true object-oriented programming language, and your code will make heavy use of classes, constructors, and inheritance.
- There are multiple types of constructors: the default constructor, factory constructors, and named constructors.
- An Enum is a special kind of class that gives additional type safety when there is a predetermined number of options for a property or variable.


**Chapter 3**

- In Flutter, everything is a widget, and widgets are just Dart classes that know how to describe their view.
- A widget can define any aspect of an application’s view. Some widgets, such as Row, define aspects of layout. Some are less abstract and define structural elements, like Button and TextField.
- Flutter Favors composition over inheritance. Composition defines a “has a” relationship, and inheritance defines an “is a” relationship.
- Every widget must contain a build method, and that method must return a widget.
- Widgets should be immutable in Flutter, but state objects shouldn’t.
- Widgets have const constructors in most cases. You can, and should, omit the new and const keywords when creating widgets in Flutter.
- A StatefulWidget tracks its own internal state, via an associated state object. A StatelessWidget is “dumb” and is destroyed entirely when Flutter removes it from the widget tree.
- setState is used to tell Flutter to update some state and then repaint. It should not be given any async work to do.
- initState and other lifecycle methods are powerful tools on the state object.
- BuildContext is a reference to a widget’s location in the widget tree. In practice, this means your widget can gather information about its place in the tree.
- The element tree is the smart one. It manages widgets, which are just blueprints for elements that are in use.
- In Flutter, widgets are rendered by their associated RenderBox objects. These render boxes are responsible for the telling the widget its actual, physical size. These objects receive constraints from their parent, and then use those to determine their actual size.
- The Container widget is a “convenience” widget that provides a whole slew of properties that you would otherwise get from individual widgets.
- Flutter Row and Column widgets use the concept of flex layouts, much like FlexBox in CSS


**Chapter 4**

- Flutter includes a ton of convenient, structural widgets, like MaterialApp, Scaffold, and AppBar. These widgets give you an incredible amount for free: navigation, menu drawers, theming, and more.
- Use the SystemChrome class to manipulate features of the device itself, such as forcing the app to be in landscape or portrait mode.
- Use MediaQuery to get information about the screen size. This is useful if you want to size widgets in a way that ensures they scale by screen size.
- Use Theme to set style properties that will effect nearly every widget in your app.
- Use the stack widget to overlap widgets anywhere on the screen.
- Use the Table widget to lay out widgets in a table.
- The ListView and its builder constructor give you a fast, performant way to create lists with infinite items.


**Chapter 5**

- User interaction in flutter is handled via two kinds of widgets: inputs and gesture detectors.
- Flutter handles gestures and user interaction events via GestureDetector widgets.
- If you want to programmatically give focus to any text field, you have to use a FocusNode widget and request focus for it.
- A gesture detector can listen for many gestures via its various callbacks. These are only 5 of about 30: – onTap – onLongPress – onDoubleTap – onVerticalDragDown – onPanDown
- Built-in widgets listen for these gestures as well: Dismissible, Button, FormField, and many more.
- Flutter forms are convenient wrappers around several input widgets that make managing complex forms easier.
- A form’s state can be managed with a GlobalKey, which is a reference to a FormState object.
- Forms are aware of widgets below them in the widget tree that are wrapped in FormField widgets, and can take advantage of this relationship.
- Form fields provide several methods: onChange, onSave, and validator. These methods are used to respond to user actions and wire up to the FormState.
- Forms have two valuable methods: onChange and onWillPop.


**Chapter 6**

- Many Material Design widgets have built-in animations. If you’re using the Material library, you’ll want to make sure the widgets you’re using aren’t already animated. You can override any built-in widgets, but doing so may be a waste of time if the animations are built-in.
- Animations require the developer to implement three pieces at a minimum: a controller, a tween, and a ticker. Flutter will take care of the curve for you, if you don’t want to customize it.
- Tweens map values of an animatable property to a number scale.
- Tickers are what give life to animations, calling their callback on every frame change.
- Classes that have AnimationController objects as properties should extend SingleTickerProviderStateMixin or TickerProviderStateMixin.
- All widgets that extend AnimatedWidget require an animation as a parameter, which provides the value of whichever property you’re animating.
- You can paint exactly what you want, pixel by pixel, using the CustomPaint widget.
- The CustomPaint widget takes a child that extends CustomPainter and has a paint method.
- Painting to the canvas generally consists of drawing a series of shapes and lines using the Canvas class.
- The TweenSequence class is extremely useful for making staggered animations


**Chapter 7**

- Flutter uses dynamic routing, which makes routing much more flexible and fluid.
- Flutter’s Navigator allows you to create routes “on the fly” in your code, just as some user interaction takes place or the app receives new data.
- Flutter supports (practically) static routing using named routes. (Although these routes are still technically created as the app is running.)
- Define your named routes in your MaterialApp widget or whichever top-level App widget you’re using.
- The Navigator manages all the routes in a stack manner.
- Navigating to routes is done by calling variations of Navigator.push and Navigator.pop.
- Navigator.push calls return a Future that awaits a value which is to be passed back by the new route. 
- Creating a full Material-style menu drawer in Flutter involves several incredibly generous widgets: Drawer, ListView, ListTile, AboutListTile, and DrawerHeader.
- You can anticipate changes in routing by setting up a RouteObserver and subscribing to it on any widget’s state object.
- Several UI elements are managed with the Navigator and are technically routes, though they aren’t pages, such as snackbars, bottom sheets, drawers, and menus.
- You can listen for user interactions using the GestureDetector widget.
- Implementing custom page transitions is done by extending Route classes.
- A stateful widget lifecycle gives fine-grain control over rebuilding widgets in Flutter using the methods: – initState – didChangeDependencies – build – widgetDidUpdate – setState – dispose.
- State objects are long-lived and can even be reused.
- Using only stateful widgets, you can implement a management pattern called “lifting state up.” 
- InheritedWidgets are special widgets optimized to pass data down the tree. Access InheritedWidgets anywhere in its subtree with an of method that calls inheritFromWidgetOfExactType.
- Combining an InheritedWidget and a StatefulWidget gives you a cleaner way to lift state up.
- The bloc pattern is a state management pattern that encourages a simple API and reusable business logic components.
- Blocs inputs and outputs should only be sinks and streams, respectively. 
- Streams, also know as observables, are first-class citizens in Dart and are used for reactive, asynchronous programming.
- Streams emit events to listeners, which are always waiting patiently for an update from streams.


**Chapter 8**

- A stateful widget lifecycle gives fine-grain control over rebuilding widgets in Flutter using the methods: – initState – didChangeDependencies – build – widgetDidUpdate – setState – dispose.
- State objects are long-lived and can even be reused.
- Using only stateful widgets, you can implement a management pattern called “lifting state up.”
- InheritedWidgets are special widgets optimized to pass data down the tree. Access InheritedWidgets anywhere in its subtree with an of method that calls inheritFromWidgetOfExactType.
- Combining an InheritedWidget and a StatefulWidget gives you a cleaner way to lift state up.
- The bloc pattern is a state management pattern that encourages a simple API and reusable business logic components.
- Blocs inputs and outputs should only be sinks and streams, respectively.
- Streams, also known as observables, are first-class citizens in Dart and are used for reactive, asynchronous programming.
- Streams emit events to listeners, which are always waiting patiently for an update from streams.


**Chapter 9**

- Asynchronous programming is difficult, but hugely important in UI development.
- Futures provide values that don’t yet exist but will soon.
- async and await make async programming easier because they’re more readable than using futures. Functionally, they accomplish the same task.
- StreamController objects are used to define streams and sinks.
- A Sink is the entry point of data for a stream.
- A Stream is what other pieces of code listen to in order to get data from streams as it becomes available. Streams can be transformed, and functions that take in streams and output a stream of transformed data are called higher-order streams.
- A bloc is a business logic component that relies on streams to build inputs and outputs your widgets can interact with as the state management logic in your widget.
- Flutter provides async widgets via the StreamBuilder class, which make an async UI much cleaner.
- Stream builders are often, but not necessarily, used to build infinite and dynamic scroll views. These are usually built with CustomScrollView widgets.
- A Sliver is a special widget that’s smart about rebuilding, making scrollables more efficient.
- A Sliver builds its children with functions called delegates.


**Chapter 10**

- Google has provided packages for HTTP if you want to use a traditional backend.
- There’s also Firebase packages, which let you use Firebase as a backend with ease. Firebase provides a reactive, NoSQL database called Firestore, which is a great combination to use with Flutter.
- Breaking the controller logic out of your UI and making it a middleman between the UI and services makes your logic layer highly reusable.
- You can share code between a web app and mobile app using dependency injection.
- Regardless of the backend you’re using, JSON serialization lets you gather data from external sources and turn it into proper Dart objects.
- JSON serialization can be done manually or with packages that generate code automatically.


**Chapter 11**

- There are three ways to test Flutter code: Dart unit tests, widget tests, and integration tests.
- Unit tests are great for testing classes and functions.
- You can “mock” classes, especially useful for classes that make service calls, with the Mockito library. Widget tests are best used to test specific widgets.
- Widget tests use Matcher and Finder objects to compare what you expect to happen and what actually happened.
- Integration tests can test how all the moving pieces of a feature work together. Integration tests in Flutter are done with the flutter\_driver package.
- You can profile the performance of your app with integration tests.
- Tests written with flutter\_driver are similar to widget tests. Both use the concept of “pumping” widgets to simulate an app being run.
- Accessibility is important in production apps. ¡ Flutter helps you write more accessible apps via the Semantics widget. Use it!


Eng. _Mohamed Osama_  <br>
Mobile Developer
