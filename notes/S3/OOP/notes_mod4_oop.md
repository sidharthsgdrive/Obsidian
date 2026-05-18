## Events
- An *event* is an object that describes a state change in a source.
- A *source* is an object that generates an `event`.
- A *registration method* is a method for an event,  used to link an event listener object with an event source.
	- EG: `addKeyListener()`, `addMouseListener()`
***
## Casting Events
- *multicasting*: When an event occurs, all registered listeners are notified, and receive a copy of the `event` object.
	- Notifications are sent only to listeners that are registered to receive them.
- *unicasting*:  Sources that only allow one listener to register.
	- ```java
		public void addTypeListener(TypeListener el) throws java.util.TooManyListenersException;
		```
	- The source must also provide a method that allows a listener to *unregister* an interest in a specific type of event.
	- ```java
	  public void removeTypeListener(TypeListener el);
	  ```
***
## Event Listeners
A *listener* is an object that is notified when an event occurs.
Requirements: 
1. It must have been registered with one or more sources to receive notifications about specific types of events.
2. It must implement methods to receive and process these notifications.
```java
Button b = new Button("Click here: ");
b.addActionListener(new MyListener()); // register myListener with button
***
class myListener implements ActionListener {
public void actionPerformed(ActionEvent ae) {
	...
	}
}
```
***
## Event Classes
- These are the classes that represent events.
- We will be seeing events defined by AWT *(Abstract Window Toolkit)*.
- Inheritance structure:
	└── `java.util.EventObject`
	    └── `java.awt.AWTEvent`
	        └── (all AWT events handled by delegation event model)
- event object has two methods:
	- `getSource()` returns source of event
	- `toString()` returns string equivalent of event

| Event Class     | Occurs When:                                      |
| --------------- | ------------------------------------------------- |
| ActionEvent     | Button pressed / Menu item selected               |
| AdjustmentEvent | Scrollbar manipulated                             |
| ComponentEvent  | Component is hidden/moved/resized/made visible    |
| ContainerEvent  | Component is added to or removed from a container |
| FocusEvent      | Component gains or loses keyboard focus           |
| InputEvent      | Superclass for all component input event classes  |
| ItemEvent       | Checkbox/List item toggled                        |
| KeyEvent        | Input received from keyboard                      |
| MouseEvent      | Mouse dragged/moved/clicked/pressed/released      |
| MouseWheelEvent | Scrollwheel moved                                 |
| TextEvent       | Value of text field changed                       |
| WindowEvent     | Window activated/deactivated/opened/closed        |
