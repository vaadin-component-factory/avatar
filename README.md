# Incubator Avatar for Vaadin 10+

[Live Demo ↗](https://incubator.app.fi/avatar-demo/index.html)

[&lt;vcf-avatar&gt;](https://vaadin.com/directory/component/vcf-avatar) is a Web Component for displaying an avatar for a user, his name initials, or a placeholder icon.

# What does the component do?

Avatar displays an image or abbreviation that represents a user.

# How is it used?

An avatar is visual identifier that represents user by showing image or name abbreviation (in case image is not set). 
A tooltip (enabled by default) can be enabled or disabled to display the name of the avatar when hovering over it.

The abbreviation is generated from the name initials. E.g. John Smith becomes JS.

### Vaadin Prime
This component is part of Vaadin Prime. Still, open source you need to have a valid CVAL license in order to use it. Read more at: vaadin.com/pricing

## Avatar - Image (URL)
```java
Avatar avatar = new Avatar();
avatar.setImage("https://banner2.kisspng.com/20171216/6c0/google-png-5a3554027e9924.3682726615134443545186.jpg");
```

## Avatar - Image (resources)

```java
Avatar avatar = new Avatar();
String path = IMAGE_PATH;
avatar.setImage(path,"image/png");
```

## Avatar - Name and tooltip

```java
Avatar avatar = new Avatar("John Smith");
avatar.setTooltipPosition(TooltipPosition.RIGHT);
avatar.setTooltipAlignment(TooltipAlignment.BOTTOM);
```

or

```java
Avatar avatar = new Avatar("John Smith", TooltipPosition.RIGHT, TooltipAlignment.BOTTOM);
```

## Avatar - Click listener
```java
Avatar avatar = new Avatar();
avatar.setName("Second Example abbreviation");
avatar.setTooltipPosition(TooltipPosition.BOTTOM);
avatar.setTooltipAlignment(TooltipAlignment.RIGHT);

avatar.addClickListener(clickEvent -> {
    Notification notification = new Notification(
            "You clicked on the avatar", 3000);
    notification.open();
});
```

## Avatar - Enabling and Disabling tooltip
```java
Avatar avatar = new Avatar("Sophia Wilson");

Button actionButton = new Button("enable/disable", event -> {
    avatar.setToolTipEnabled(!avatar.isToolTipEnabled());
});

```

# How to run the demo?

The Demo can be run by going to the project incubator-avatar-flow-vaadincom-demo and executing the maven goal:

```mvn jetty:run```

After server startup, you'll be able find the demo at[http://localhost:8080/avatar](http://localhost:8080/avatar)


## License & Author

This Add-on is distributed under [Commercial Vaadin Add-on License version 3](http://vaadin.com/license/cval-3) (CVALv3). For license terms, see LICENSE.txt.

Incubator avatar is written by Vaadin Ltd.


## Setting up for development:

Clone the project in GitHub (or fork it if you plan on contributing)

```
git clone git@github.com/vaadin/incubator-avatar-flow.git
```

to install project to your maven repository run
 
```mvn install```