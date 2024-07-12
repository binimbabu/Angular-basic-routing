Routing

Routing is handling a set of pages with url’s, when the url’s changes automatically the route component will change. All the routing can be handled only by one component thats why angular is called single page application.

<router-outlet></router-oulet>

router-outlet is a placeholder it is used when it hits a particular url in the browser which is registered in the app.routing,module.ts it goes to component mentioned in the url. All the component deatils will be loaded when hitting a url in the browser (where the url is registered in  app.routing,module.ts ) by giving router-outlet.

In the app-routing.module.ts if we give the below code in the routes

{ path: '**', component: NotfoundComponent }


If a url is entered in the browser that does not match any url registered in  app-routing.module.ts then the above code will give  render NotfoundComponent since the path is given ‘**’.


{ path: '', redirectTo: '/login', pathMatch: 'full' },

When path is given ‘’ then when we just enter localhost:4200 with out any url mentioned int the app.routing.module.ts then it will redirect to login and the pathMatch is full because it has to exactly match to the redirect value ( i.e  redirectTo: '/login'  ) that is /login.
