### A bar for navigator.

install by **npm i react-native-custom-nav-bar**

add it into navigationBar when init navigator, just like :

		`  <Navigator
            ....
            navigationBar={NavigationBar.render()}
            sceneStyle ={styles.sub_navi_page}  />`

 custom style of bar by this:

 		`NavigationBar.render({backgroundColor: 'red'})`


 then, when pushing page, can define title by:

 		` navigator.push({
	        title:'PageOne',
	        name: 'PageOne',
	        component: PageOne,
	        rightButton: {
	          action: 'CUSTOM',
	          express: 'more',
	          handle: () => {},
	        },
	        leftButton: {
	          action: 'BACK'
	        },
      	 })`

 there are two kinds of buttons , 'BACK' and 'CUSTOM'. when use 'BACK', the handle is auto defined as poping. when use 'CUSTOM', express can be defined as string or function, when is function, should return view,like:

    	`express: () => <View />,`