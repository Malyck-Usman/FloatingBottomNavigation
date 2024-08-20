Floating Bottom Navigation 
>  Add the JitPack repository to your build file
dependencyResolutionManagement {
		repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
		repositories {
			mavenCentral()
			maven { url 'https://jitpack.io' }
		}
	}

>  Add the dependency
dependencies {
   implementation 'com.github.Malyck-Usman:FloatingBottomNavigation:1.0.0'
	}

> Add Floating Bottom Navigation in you layout xml file.
    <com.example.floatingnavigation.FloatingBottomNavigation
            android:layout_width="match_parent"
            android:layout_height="wrap_content"/>
 
> Add menu items in code.
val bottomNavigation = findView(R.id.bottomNavigation)
bottomNavigation.add(FloatingBottomNavigation.Model(1, R.drawable.ic_home))
bottomNavigation.add(FloatingBottomNavigation.Model(2, R.drawable.ic_explore))
bottomNavigation.add(FloatingBottomNavigation.Model(3, R.drawable.ic_message))

> Use setOnShowListener() function to access when a cell has been shown.
bottomNavigation.setOnShowListener {
    // YOUR CODES
}

> Use setOnClickMenuListener() function to access when a cell has been clicked.
bottomNavigation.setOnClickMenuListener {
    // YOUR CODES
}

> Set counter badge on a specific cell by setCount(Int,String).
bottomNavigation.setCount(CELL_ID, YOUR_STRING)

> Clear counter badge on a specific cell by clearCount(Int).
bottomNavigation.clearCount(CELL_ID)

> Clear all counter badges on a specific cell by clearCount(Int).
bottomNavigation.clearAllCounts(TAB_ID)

> To Set Default CELL Use this function :
bottomNavigation.show(CELL_ID)
