[![](https://jitpack.io/v/LucasFebatis/gdx-controllers.svg)](https://jitpack.io/#LucasFebatis/gdx-controllers)

# 🤔 Why does this fork exist?

Fork made only for use with version 2.0.12.0 of Jamepad, while version 2.0.12.1 with player selection support is not released and the main repository uses it

## How to use

1. Use the libGDX project builder available in: https://libgdx.badlogicgames.com/download.html

2. Change dependencies

```
api "com.badlogicgames.gdx:gdx-controllers-desktop:$gdxVersion"
api "com.badlogicgames.gdx:gdx-controllers-platform:$gdxVersion:natives-desktop"
```

by:

```
api 'com.github.LucasFebatis.gdx-controllers:gdx-controllers-desktop:1.0'
```

## For Mappings

[📖️ Go to Wiki](https://github.com/LucasFebatis/gdx-controllers/wiki)


# 🎮️ Game Controller Extension for libGDX, Version 2

Use game controllers with ease in your libGDX games.

[📖️ Documentation](https://github.com/libgdx/gdx-controllers/wiki) - [🎁️ Feature overview](https://github.com/libgdx/gdx-controllers/wiki/Features)

Release version not yet available. If you need a released version, take a look at
[gdx-controllers v1](https://github.com/libgdx/libgdx/wiki/Controllers). However, you are
welcome to use the new v2 in work here.

[🚀️ Migration guide from v1](https://github.com/libgdx/gdx-controllers/wiki/Migrate-from-v1)

## 💾️ Installation

The recommended way to use gdx-pay is via dependency management with Gradle or Maven. Artifacts are available in
[Snapshot Repository](https://oss.sonatype.org/content/repositories/snapshots/com/badlogicgames/gdx-controllers/).

*project-root/build.gradle:*

    ext {
        gdxControllersVersion = '2.0.0-SNAPSHOT'
    }

Add the following dependencies:

#### core:
```
implementation "com.badlogicgames.gdx-controllers:gdx-controllers-core:$gdxControllersVersion"
```

#### desktop:

##### Original
```
implementation "com.badlogicgames.gdx-controllers:gdx-controllers-desktop:$gdxControllersVersion"
```

##### This Git
```
api 'com.github.LucasFebatis.gdx-controllers:gdx-controllers-desktop:master-SNAPSHOT'
```

#### android:
```
implementation "com.badlogicgames.gdx-controllers:gdx-controllers-android:$gdxControllersVersion"
```
Proguard setting:
```
-keep class com.badlogic.gdx.controllers.android.AndroidControllers { *; }
```

#### ios:
```
implementation "com.badlogicgames.gdx-controllers:gdx-controllers-ios:$gdxControllersVersion"
```
`robovml.xml` needs the following line added to `forceLinkClasses`:
```
<pattern>com.badlogic.gdx.controllers.IosControllerManager</pattern> 
```
#### html:
```
implementation "com.badlogicgames.gdx-controllers:gdx-controllers-core:$gdxControllersVersion:sources"
implementation "com.badlogicgames.gdx-controllers:gdx-controllers-gwt:$gdxControllersVersion:sources"
```
You also need to add the following file to your GdxDefinition.gwt.xml in your html project:
```
<inherits name="com.badlogic.gdx.controllers" />
<inherits name="com.badlogic.gdx.controllers.controllers-gwt"/>
```

### Building from source
To build from source, clone or download this repository, then open it in Android Studio. Perform the following command to compile and upload the library in your local repository:

    gradlew clean uploadArchives -PLOCAL=true
    
See `build.gradle` file for current version to use in your dependencies.

## 🤝️ News & Community

You can get help on the [libgdx discord](https://discord.gg/6pgDK9F).

## License

The project is licensed under the Apache 2 License, meaning you can use it free of charge, without strings attached in commercial and non-commercial projects. We love to get (non-mandatory) credit in case you release a game or app using this project!
