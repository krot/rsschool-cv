#Rustem Enikeev

##Contacts

- E-mail: main@csagent.ru (preferred)
- Telegram: @krotx32
- [LinkedIn Profile](https://www.linkedin.com/in/rustem-enikeev/)

##Summary

Middle Fullstack Web Developer, with more than 6 years of production experience
 and more 15 years of common computer science experience.

I worked on different projects and systems, include creating new, refactor, improving and fix current modern and legacy systems.

I do everyday learning and improving for a new as on work, as on my free time. 

Now I want to extend my experience to mobile
development (for example to be able to make Cordova/Capacitor native extensions on Android/iOS).

Also I'm very like to know Rust lang (It's named as me  :-) ) but in next steps.

hobbys: IT, drawing, fitness

##Skills

- Frontend - JavaScript, TypeScript, Redux, TSX, Ionic Framework (Angular2+), Cordova, StencilJS, Apollo, Axios, CSS3, HTML5.

- Backend - PHP (Yii2), GraphQL, Rest API, MySQL, Redis, Sass(Less)

- Env - AWS API and services (Amplify, CloudSearch, Translate API etc), Google API and services 
(tagmanager, analytics, maps, etc), AuthorizeNet API


##Code Examples

```javascript

@Injectable({
  providedIn: "root"
})
export class AuthService {

  public isAuth: boolean = false;

  public isAuth$: Observable<boolean>;
  public isAuthSubject$: Subject<boolean>;

  constructor(
    private userService: UserService,
    private apiService: ApiService,
  ) {
     this.isAuthSubject$ = new Subject<boolean>();
     this.isAuth$ = this.isAuthSubject$.asObservable();
     this.isAuthSubject$.next(this.isAuth);
  }

  isAuthenticated(): Observable<boolean> {
    return this.isAuth$;
  }

  login(email, password): Observable<IUserAuth> {
    return from(
      this.apiService.getUserTokenByCredentials(email, password).pipe(
       tap((data: any) => {
       this.isAuth = true;
       this.isAuthSubject$.next(this.isAuth);
       return data;
     }),
     catchError( err => {
         return throwError(err);
     })));
  }

  logout(): Observable<boolean> {
      this.isAuth = false;
      this.isAuthSubject$.next(this.isAuth);
      return this.isAuth$;
  }
}
```
here code of theAuthService and will better to change Subject to BehaviorSubject to remove isAuth class property
In next commits I will add another examples, sorry most of code under NDA

##Experience

Strong skills on building complex websites and progressive web applications(PWA) from blank 
with fast and responsible design.

Creating, improve and publish cross-platform mobile applications for Android and iOS with using Ionic Framework(Angular2+) 
with publishing to GooglePlay and AppStore  .

Native understanding possible problems and system design issues on processed systems.
Ability to help to solve problems and train colleagues.

Expertise in find and fix issues and bugs in systems so fast and so patience and accuracy.
Experience for explore and use third-party and self-designed APIs


##Education

I'm got a Master CS degree in USATU, Ufa in 2000
but as I said, I'm learn by myself and with api docs

##English

Intermediate, can read, write and discuss with foreign colleagues, but low-level speaking, due to no practice


