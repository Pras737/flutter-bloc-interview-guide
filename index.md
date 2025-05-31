
Flutter BLoC Interview Questions & Answers
0-2 Years Experience Candidates (Hinglish)
Flutter Basics (Questions 1-25)
Q1. Flutter kya hai aur ye kaise different hai native development se?
A: Flutter ek cross-platform UI framework hai jo Google ne banaya hai. Ye single codebase se Android aur iOS dono ke liye apps bana sakta hai. Native development mein alag-alag languages use karte hain (Java/Kotlin for Android, Swift/Objective-C for iOS), lekin Flutter mein sirf Dart language use karte hain.

Q2. Dart language ke main features kya hain?
A:

Object-oriented programming support
Strong typing with type inference
Null safety
Asynchronous programming (async/await)
Garbage collection
JIT aur AOT compilation support
Q3. Widget kya hota hai Flutter mein?
A: Widget Flutter mein UI ka basic building block hai. Har cheez Flutter mein widget hoti hai - text, button, layout, etc. Do types ke widgets hote hain:

Stateless Widget: Ek baar create hone ke baad change nahi hota
Stateful Widget: Runtime mein state change ho sakti hai
Q4. StatelessWidget aur StatefulWidget mein difference kya hai?
A:

StatelessWidget: Immutable hota hai, iska state change nahi ho sakta
StatefulWidget: Mutable hota hai, setState() method se state change kar sakte hain
Q5. Widget lifecycle kya hai StatefulWidget mein?
A:

createState() - Widget ka state create karta hai
initState() - Widget initialize hote time call hota hai
build() - UI render karta hai
setState() - State change karne ke liye
dispose() - Widget destroy hote time cleanup ke liye
Q6. BuildContext kya hai?
A: BuildContext widget tree mein current widget ki location batata hai. Ye Navigator, Theme, MediaQuery jaise services access karne ke liye use hota hai.

Q7. Key kya hota hai Flutter mein aur kab use karte hain?
A: Key widget ko uniquely identify karne ke liye use hota hai. Jab widget ki list mein order change hota hai tab Key use karte hain. Types: ValueKey, ObjectKey, UniqueKey, GlobalKey.

Q8. Hot Reload aur Hot Restart mein difference?
A:

Hot Reload: Sirf UI changes reflect karta hai, state preserve rehti hai
Hot Restart: Puri app restart ho jati hai, state reset ho jati hai
Q9. Scaffold kya hai?
A: Scaffold ek basic material design layout structure provide karta hai. Isme AppBar, Body, FloatingActionButton, Drawer jaise components hote hain.

Q10. Container aur SizedBox mein difference?
A:

Container: Decoration, padding, margin, width, height sab set kar sakte hain
SizedBox: Sirf width aur height set kar sakte hain, lightweight hai
Q11. Row aur Column mein MainAxis aur CrossAxis kya hota hai?
A:

Row mein: MainAxis = horizontal, CrossAxis = vertical
Column mein: MainAxis = vertical, CrossAxis = horizontal
Q12. ListView aur GridView kab use karte hain?
A:

ListView: Vertical ya horizontal scrolling list ke liye
GridView: Grid format mein items display karne ke liye
Q13. Navigator kya hai aur page navigation kaise karte hain?
A: Navigator routing handle karta hai. Navigator.push() se new page par jate hain, Navigator.pop() se back aate hain.

Q14. Named routes kya hain?
A: Named routes mein page ko naam se identify karte hain. MaterialApp mein routes define karte hain aur Navigator.pushNamed() se navigate karte hain.

Q15. AppBar customize kaise karte hain?
A: AppBar mein title, backgroundColor, elevation, actions, leading properties set kar sakte hain.

Q16. FloatingActionButton kya hai?
A: Ye ek circular button hota hai jo screen ke corner mein float karta hai, primary action ke liye use hota hai.

Q17. Theme kya hai Flutter mein?
A: Theme app ki overall appearance define karta hai - colors, fonts, button styles, etc. ThemeData class se customize karte hain.

Q18. MediaQuery kya hai?
A: MediaQuery device ki screen information provide karta hai - width, height, orientation, etc.

Q19. Stack widget kya hai?
A: Stack widgets ko overlap karne ke liye use karta hai. Positioned widget se exact position set kar sakte hain.

Q20. Flexible aur Expanded mein difference?
A:

Flexible: Child widget available space use kar sakta hai ya nahi
Expanded: Child widget available space use karna hi padega
Q21. CustomScrollView kya hai?
A: CustomScrollView multiple scrollable widgets ko combine karne ke liye use hota hai. Slivers use karte hain isme.

Q22. Hero animation kya hai?
A: Hero animation ek widget ko ek screen se dusre screen mein smoothly transition karta hai.

Q23. GestureDetector kya hai?
A: GestureDetector touch gestures detect karne ke liye use hota hai - tap, double tap, long press, swipe, etc.

Q24. Form validation kaise karte hain?
A: Form widget aur TextFormField use karte hain. GlobalKey<FormState> se form ko control karte hain.

Q25. SnackBar kya hai?
A: SnackBar bottom mein temporary message show karne ke liye use hota hai.

BLoC Pattern (Questions 26-50)
Q26. BLoC pattern kya hai?
A: BLoC (Business Logic Component) ek architectural pattern hai jo business logic ko UI se separate karta hai. Ye streams aur events use karta hai.

Q27. BLoC pattern ke fayde kya hain?
A:

Separation of concerns
Testable code
Reusable business logic
Predictable state management
Platform independent
Q28. BLoC mein Event, State aur BLoC class ka role kya hai?
A:

Event: User actions ya external triggers
State: UI ki current condition
BLoC: Events ko process karke new state emit karta hai
Q29. BlocProvider kya hai?
A: BlocProvider widget tree mein BLoC instance provide karta hai. Ye InheritedWidget use karta hai.

Q30. BlocBuilder kya hai?
A: BlocBuilder state changes ko listen karta hai aur UI rebuild karta hai.

Q31. BlocListener kya hai?
A: BlocListener state changes ko listen karta hai lekin UI rebuild nahi karta. Side effects ke liye use hota hai.

Q32. BlocConsumer kya hai?
A: BlocConsumer BlocBuilder aur BlocListener dono ka combination hai.

Q33. MultiBlocProvider kya hai?
A: MultiBlocProvider multiple BLoCs ko provide karne ke liye use hota hai.

Q34. Cubit kya hai aur BLoC se kaise different hai?
A: Cubit BLoC ka simplified version hai. Isme events nahi hote, directly methods call karte hain.

Q35. BLoC mein async operations kaise handle karte hain?
A: async/await use karte hain BLoC methods mein. Repository pattern use kar sakte hain.

Q36. BlocObserver kya hai?
A: BlocObserver global level par BLoC state changes ko observe karne ke liye use hota hai.

Q37. Equatable package kya hai aur kyu use karte hain?
A: Equatable objects ko compare karne ke liye use hota hai. BLoC mein state aur events ke liye use karte hain.

Q38. BLoC mein error handling kaise karte hain?
A: Try-catch blocks use karte hain aur error states define karte hain.

Q39. BLoC testing kaise karte hain?
A: blocTest package use karte hain. MockBLoC bana kar unit tests likhte hain.

Q40. Repository pattern kya hai BLoC ke saath?
A: Repository pattern data layer ko abstract karta hai. BLoC ko data source ke bare mein pata nahi hota.

Q41. BLoC mein dependency injection kaise karte hain?
A: get_it package use kar sakte hain ya constructor injection use kar sakte hain.

Q42. Hydrated BLoC kya hai?
A: Hydrated BLoC automatically state ko persist karta hai device storage mein.

Q43. BLoC mein pagination kaise implement karte hain?
A: Load more events create karte hain aur state mein current page track karte hain.

Q44. BLoC mein debouncing kaise karte hain?
A: Stream transformers use karte hain ya transformer parameter use karte hain.

Q45. BLoC architecture mein folder structure kya hona chahiye?
A:

lib/
  blocs/
    auth/
      auth_bloc.dart
      auth_event.dart
      auth_state.dart
  repositories/
  models/
  screens/
Q46. BLoC mein multiple states kaise handle karte hain?
A: Abstract base state class banate hain aur different states extend karte hain.

Q47. BLoC mein navigation kaise handle karte hain?
A: BlocListener use karte hain aur state changes par navigation trigger karte hain.

Q48. Freezed package kya hai BLoC ke saath?
A: Freezed immutable classes generate karta hai. Union types aur copyWith methods provide karta hai.

Q49. BLoC mein API calls kaise manage karte hain?
A: Repository mein API calls karte hain aur BLoC mein repository methods call karte hain.

Q50. BLoC mein loading states kaise handle karte hain?
A: Loading, Success, Error states define karte hain aur UI mein accordingly handle karte hain.

OOP Concepts (Questions 51-70)
Q51. OOP kya hai aur iske main pillars kya hain?
A: Object-Oriented Programming ek programming paradigm hai. Iske 4 main pillars hain:

Encapsulation
Inheritance
Polymorphism
Abstraction
Q52. Class aur Object mein difference kya hai?
A:

Class: Blueprint ya template hota hai
Object: Class ka instance hota hai
Q53. Encapsulation kya hai?
A: Encapsulation data aur methods ko ek hi unit mein wrap karna hai. Private variables use kar ke data hiding karte hain.

Q54. Inheritance kya hai Dart mein?
A: Inheritance ek class ko dusri class se properties aur methods inherit karne ki facility hai. extends keyword use karte hain.

Q55. Polymorphism kya hai?
A: Polymorphism same interface ke through different implementations use karne ki ability hai. Method overriding aur overloading iske examples hain.

Q56. Abstraction kya hai?
A: Abstraction complex implementation details ko hide karna hai. Abstract classes aur interfaces use karte hain.

Q57. Constructor kya hai aur kitne types ke hote hain?
A: Constructor object initialize karne ke liye use hota hai. Types:

Default constructor
Named constructor
Factory constructor
Const constructor
Q58. Static keyword kya hai?
A: Static members class level par belong karte hain, object level par nahi. Direct class name se access karte hain.

Q59. Abstract class kya hai?
A: Abstract class wo class hai jo instantiate nahi ho sakti. Isme abstract methods hote hain jo child classes mein implement karne padte hain.

Q60. Interface kya hai Dart mein?
A: Dart mein har class implicitly interface hai. implements keyword use kar ke interface implement karte hain.

Q61. Mixin kya hai?
A: Mixin ek way hai multiple inheritance achieve karne ka. with keyword use karte hain.

Q62. Super keyword kya hai?
A: Super parent class ke members ko access karne ke liye use hota hai.

Q63. Method overriding kya hai?
A: Child class mein parent class ke method ko redefine karna method overriding hai.

Q64. Final aur const mein difference kya hai?
A:

Final: Runtime mein value set hoti hai, ek baar set hone ke baad change nahi hoti
Const: Compile time mein value set hoti hai
Q65. Getter aur Setter kya hain?
A: Getter property ki value read karne ke liye, Setter property ki value set karne ke liye use hote hain.

Q66. Factory constructor kya hai?
A: Factory constructor same class ka instance return karta hai ya subclass ka instance return kar sakta hai.

Q67. Enum kya hai?
A: Enum named constants ka collection hai. Fixed set of values represent karne ke liye use hota hai.

Q68. Extension methods kya hain?
A: Extension methods existing classes mein new functionality add karne ke liye use hote hain.

Q69. Generics kya hain Dart mein?
A: Generics type-safe collections aur functions banane ke liye use hote hain. <T> syntax use karte hain.

Q70. Callable classes kya hain?
A: Callable classes wo classes hain jo function ki tarah call ho sakti hain. call() method implement karte hain.

Advanced Concepts (Questions 71-85)
Q71. Interceptor kya hai aur kyu use karte hain?
A: Interceptor HTTP requests aur responses ko intercept karne ke liye use hota hai. Dio package mein use karte hain authentication, logging, error handling ke liye.

Q72. Dio interceptor kaise implement karte hain?
A:

dart
class AuthInterceptor extends Interceptor {
  @override
  void onRequest(RequestOptions options, RequestInterceptorHandler handler) {
    options.headers['Authorization'] = 'Bearer $token';
    handler.next(options);
  }
}
Q73. Mixin kya hai aur kaise use karte hain?
A: Mixin code reuse karne ka tarika hai. Multiple mixins use kar sakte hain:

dart
mixin Flyable {
  void fly() => print('Flying');
}

class Bird with Flyable {}
Q74. Stream aur Future mein difference kya hai?
A:

Future: Single asynchronous operation
Stream: Multiple asynchronous values over time
Q75. StreamBuilder kya hai?
A: StreamBuilder stream ko listen karta hai aur data changes par UI rebuild karta hai.

Q76. Isolates kya hain?
A: Isolates Dart mein concurrency achieve karne ka tarika hai. Heavy computations ke liye use karte hain.

Q77. Compute function kya hai?
A: Compute function background isolate mein function run karne ke liye use hota hai.

Q78. Provider package kya hai?
A: Provider state management aur dependency injection ke liye use hota hai. InheritedWidget wrapper hai.

Q79. GetX kya hai?
A: GetX state management, route management aur dependency injection ka complete solution hai.

Q80. Riverpod kya hai?
A: Riverpod Provider ka improved version hai. Better performance aur compile-time safety provide karta hai.

Q81. Local storage options kya hain Flutter mein?
A:

SharedPreferences - simple key-value storage
SQLite - structured data
Hive - NoSQL database
Secure Storage - encrypted storage
Q82. Network calls kaise optimize karte hain?
A:

Caching implement karte hain
Pagination use karte hain
Debouncing karte hain
Connection timeout set karte hain
Q83. App performance kaise improve karte hain?
A:

Lazy loading use karte hain
Image optimization karte hain
Unnecessary rebuilds avoid karte hain
Memory leaks fix karte hain
Q84. Error handling best practices kya hain?
A:

Try-catch blocks use karte hain
Global error handler set karte hain
User-friendly error messages show karte hain
Logging implement karte hain
Q85. Testing types kya hain Flutter mein?
A:

Unit tests - individual functions
Widget tests - UI components
Integration tests - complete app flow
Architecture Patterns (Questions 86-100)
Q86. MVC pattern kya hai?
A: MVC (Model-View-Controller) ek architectural pattern hai:

Model: Data aur business logic
View: User interface
Controller: Model aur View ke beech communication handle karta hai
Q87. MVP pattern kya hai?
A: MVP (Model-View-Presenter) pattern:

Model: Data layer
View: UI layer (passive, sirf display karta hai)
Presenter: Business logic aur View ko control karta hai
Q88. MVVM pattern kya hai?
A: MVVM (Model-View-ViewModel) pattern:

Model: Data aur business logic
View: UI components
ViewModel: View ka state manage karta hai, data binding use karta hai
Q89. MVC, MVP aur MVVM mein difference kya hai?
A:

MVC: Controller View ko directly manipulate karta hai
MVP: Presenter View ka interface implement karta hai
MVVM: ViewModel data binding use karta hai, loose coupling hoti hai
Q90. Flutter mein MVVM kaise implement karte hain?
A:

dart
class UserViewModel extends ChangeNotifier {
  User? _user;
  bool _isLoading = false;
  
  User? get user => _user;
  bool get isLoading => _isLoading;
  
  Future<void> loadUser() async {
    _isLoading = true;
    notifyListeners();
    
    _user = await userRepository.getUser();
    _isLoading = false;
    notifyListeners();
  }
}
Q91. Repository pattern kya hai?
A: Repository pattern data access logic ko encapsulate karta hai. Ye data sources (API, Database) ko abstract karta hai:

dart
abstract class UserRepository {
  Future<User> getUser(String id);
  Future<void> saveUser(User user);
}

class ApiUserRepository implements UserRepository {
  // API implementation
}
Q92. Dependency Injection kya hai aur kyu use karte hain?
A: Dependency Injection dependencies ko externally provide karne ka pattern hai. Benefits:

Loose coupling
Easy testing
Code reusability
Better maintainability
Q93. Clean Architecture kya hai?
A: Clean Architecture mein layers hoti hain:

Presentation Layer: UI aur ViewModels
Domain Layer: Business logic aur entities
Data Layer: Repositories aur data sources
Q94. Singleton pattern kya hai?
A: Singleton pattern ensure karta hai ki class ka sirf ek instance ho:

dart
class ApiService {
  static final ApiService _instance = ApiService._internal();
  factory ApiService() => _instance;
  ApiService._internal();
}
Q95. Observer pattern kya hai?
A: Observer pattern mein object apne dependents ko state changes notify karta hai. Flutter mein ChangeNotifier ye pattern implement karta hai.

REST API & RESTful Services (Questions 96-115)
Q96. REST API kya hai?
A: REST (Representational State Transfer) ek architectural style hai web services banane ke liye. Ye HTTP methods use karta hai aur stateless hota hai.

Q97. RESTful API kya hai?
A: RESTful API wo API hai jo REST principles follow karta hai:

Stateless communication
Client-server architecture
Cacheable responses
Uniform interface
Layered system
Q98. HTTP methods kya hain aur kab use karte hain?
A:

GET: Data retrieve karne ke liye
POST: New resource create karne ke liye
PUT: Resource ko completely update karne ke liye
PATCH: Resource ko partially update karne ke liye
DELETE: Resource delete karne ke liye
Q99. Status codes kya hain aur main ones kya hain?
A:

200 OK: Success
201 Created: Resource successfully created
400 Bad Request: Invalid request
401 Unauthorized: Authentication required
404 Not Found: Resource not found
500 Internal Server Error: Server error
Q100. REST API mein authentication kaise karte hain?
A:

Basic Auth: Username/password encode karte hain
Bearer Token: JWT tokens use karte hain
API Keys: Headers mein API key send karte hain
OAuth: Third-party authentication
Q101. JWT (JSON Web Token) kya hai?
A: JWT ek secure way hai information transmit karne ka. Isme 3 parts hote hain:

Header: Algorithm aur token type
Payload: Claims (data)
Signature: Verification ke liye
Q102. API rate limiting kya hai?
A: Rate limiting API calls ki limit set karta hai per user/per time period. Server overload prevent karne ke liye use hota hai.

Q103. CORS kya hai?
A: CORS (Cross-Origin Resource Sharing) browser security feature hai jo cross-origin requests control karta hai.

Q104. REST API mein pagination kaise implement karte hain?
A:

Offset-based: ?page=1&limit=20
Cursor-based: ?cursor=xyz&limit=20
Time-based: ?since=timestamp&limit=20
Q105. API versioning kaise karte hain?
A:

URL versioning: /api/v1/users
Header versioning: Accept: application/vnd.api+json;version=1
Query parameter: /api/users?version=1
Q106. REST API mein error handling kaise karte hain?
A:

Proper HTTP status codes use karte hain
Error response format consistent rakhte hain
Detailed error messages provide karte hain
json
{
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Invalid email format",
    "details": ["Email field is required"]
  }
}
Q107. API caching kya hai aur kaise implement karte hain?
A: Caching frequently used data store karta hai faster access ke liye:

Client-side caching: Browser cache
Server-side caching: Redis, Memcached
CDN caching: Distributed caching
Q108. REST vs GraphQL mein difference kya hai?
A:

REST: Multiple endpoints, over-fetching/under-fetching issues
GraphQL: Single endpoint, exactly required data fetch karte hain
Q109. API documentation kya hai aur kyu important hai?
A: API documentation developers ko API use karne mein help karta hai. Tools: Swagger/OpenAPI, Postman documentation.

Q110. REST API testing kaise karte hain?
A:

Unit tests: Individual endpoints
Integration tests: Complete API flows
Tools: Postman, Insomnia, Jest, Supertest
Q111. API security best practices kya hain?
A:

HTTPS use karte hain
Authentication/Authorization implement karte hain
Input validation karte hain
Rate limiting karte hain
API keys secure rakhte hain
Q112. Microservices kya hain?
A: Microservices architecture mein application multiple small services mein divide hoti hai. Har service independently deployable hoti hai.

Q113. API Gateway kya hai?
A: API Gateway single entry point hota hai multiple microservices ke liye. Ye routing, authentication, rate limiting handle karta hai.

Q114. REST API mein HATEOAS kya hai?
A: HATEOAS (Hypermedia as the Engine of Application State) response mein related links provide karta hai navigation ke liye.

Q115. API monitoring kaise karte hain?
A:

Response time track karte hain
Error rates monitor karte hain
Uptime check karte hain
Tools: New Relic, DataDog, Pingdom
Project-Related Questions (Questions 116-130)
Q116. Apne project mein kaun sa architecture pattern use kiya hai?
A: Main project mein Clean Architecture ke saath MVVM pattern use kiya hai. BLoC ko ViewModel ki tarah use kiya hai kyunki ye clear separation of concerns provide karta hai aur testing easy hoti hai.

Q117. API integration kaise kiya hai?
A:

Dio package use kiya hai HTTP requests ke liye
Repository pattern implement kiya hai data layer ke liye
Interceptors use kiye hain authentication aur logging ke liye
Error handling aur retry mechanism implement kiya hai
Q118. REST API calls kaise optimize kiye hain?
A:

Caching implement kiya hai frequently used data ke liye
Pagination use kiya hai large datasets ke liye
Debouncing kiya hai search APIs ke liye
Connection pooling use kiya hai better performance ke liye
Q119. Authentication flow kaise design kiya hai?
A:

JWT tokens use kiye hain
Token refresh mechanism implement kiya hai
Biometric authentication add kiya hai
Secure storage use kiya hai tokens ke liye
Q120. API error handling kaise kiya hai project mein?
A:

dart
class ApiException implements Exception {
  final String message;
  final int statusCode;
  
  ApiException(this.message, this.statusCode);
}

// Repository mein
try {
  final response = await dio.get('/api/users');
  return User.fromJson(response.data);
} on DioError catch (e) {
  if (e.response?.statusCode == 401) {
    throw ApiException('Unauthorized', 401);
  }
  throw ApiException('Network error', 500);
}
Q121. Offline-first approach kaise implement kiya hai?
A:

Local database (SQLite/Hive) use kiya hai
Sync mechanism implement kiya hai
Network connectivity check karte hain
Conflict resolution strategy banaya hai
Q122. API versioning kaise handle kiya hai?
A: Base URL mein version include kiya hai (/api/v1/) aur backward compatibility maintain kiya hai older versions ke liye.

Q123. File upload kaise implement kiya hai?
A:

MultipartFile use kiya hai Dio ke saath
Progress tracking implement kiya hai
Compression kiya hai images ka
Background upload implement kiya hai
Q124. Real-time updates kaise handle kiye hain?
A:

WebSocket connection use kiya hai
Server-Sent Events (SSE) implement kiya hai
Push notifications integrate kiye hain
Polling mechanism backup ke liye
Q125. API response caching strategy kya hai?
A:

Dio interceptor use kiya hai caching ke liye
Cache headers respect karte hain
Manual cache invalidation implement kiya hai
Memory aur disk caching dono use kiye hain
Q126. Third-party API integration challenges kya face kiye?
A:

Rate limiting handle kiya hai
Different response formats adapt kiye hain
API keys secure kiye hain
Fallback mechanisms implement kiye hain
Q127. API testing kaise kiya hai?
A:

Mock API responses use kiye hain testing ke liye
Integration tests likhe hain
Postman collections banaye hain
Automated testing pipeline set up kiya hai
Q128. Performance optimization kya kiya hai API calls mein?
A:

Request batching implement kiya hai
Lazy loading use kiya hai
Image optimization kiya hai
Background sync implement kiya hai
Q129. Security measures kya implement kiye hain?
A:

Certificate pinning implement kiya hai
API keys environment variables mein store kiye hain
Input validation kiya hai
Encrypted storage use kiya hai sensitive data ke liye
Q130. Microservices architecture kaise handle kiya hai?
A:

Service discovery implement kiya hai
Circuit breaker pattern use kiya hai
Load balancing configure kiya hai
Health checks implement kiye hain
Advanced Architecture & API Questions (Questions 131-150)
Q131. Clean Architecture ke layers kya hain Flutter mein?
A:

Presentation Layer (UI, BLoC/Cubit)
    ↓
Domain Layer (Use Cases, Entities, Repository Interfaces)
    ↓
Data Layer (Repository Implementation, Data Sources)
Q132. Use Case pattern kya hai?
A: Use Case business logic ka single unit hai. Ye domain layer mein rehta hai:

dart
class GetUserUseCase {
  final UserRepository repository;
  
  GetUserUseCase(this.repository);
  
  Future<Either<Failure, User>> call(String userId) {
    return repository.getUser(userId);
  }
}
Q133. Either type kya hai aur kyu use karte hain?
A: Either type success ya failure represent karta hai. Functional programming concept hai:

dart
Either<Failure, Success> result = await useCase.call();
result.fold(
  (failure) => handleError(failure),
  (success) => handleSuccess(success),
);
Q134. Data Transfer Object (DTO) kya hai?
A: DTO API responses ko represent karta hai aur domain entities se different hota hai:

dart
class UserDto {
  final String id;
  final String name;
  
  User toEntity() => User(id: id, name: name);
}
Q135. Repository vs Data Source mein difference kya hai?
A:

Repository: Abstract interface, business logic
Data Source: Concrete implementation, data fetching logic
Q136. API rate limiting kaise handle karte hain Flutter mein?
A:

dart
class RateLimitInterceptor extends Interceptor {
  @override
  void onError(DioError err, ErrorInterceptorHandler handler) {
    if (err.response?.statusCode == 429) {
      // Implement retry with exponential backoff
    }
    handler.next(err);
  }
}
Q137. Circuit Breaker pattern kya hai?
A: Circuit Breaker failing services ko repeatedly call karne se prevent karta hai. Ye states hote hain: Closed, Open, Half-Open.

Q138. Retry mechanism kaise implement karte hain?
A:

dart
Future<T> retryOperation<T>(Future<T> Function() operation) async {
  int attempts = 0;
  while (attempts < maxRetries) {
    try {
      return await operation();
    } catch (e) {
      attempts++;
      await Future.delayed(Duration(seconds: attempts * 2));
    }
  }
  throw Exception('Max retries exceeded');
}
Q139. API response mapping kaise karte hain complex nested data ke liye?
A:

dart
class UserResponse {
  final String id;
  final ProfileResponse profile;
  
  factory UserResponse.fromJson(Map<String, dynamic> json) {
    return UserResponse(
      id: json['id'],
      profile: ProfileResponse.fromJson(json['profile']),
    );
  }
}
Q140. Bulk operations kaise handle karte hain?
A:

Batch requests use karte hain
Pagination implement karte hain
Background processing use karte hain
Progress tracking karte hain
Q141. API mocking kaise karte hain development mein?
A:

dart
class MockApiService implements ApiService {
  @override
  Future<User> getUser(String id) async {
    await Future.delayed(Duration(seconds: 1));
    return User(id: id, name: 'Mock User');
  }
}
Q142. Content negotiation kya hai REST API mein?
A: Content negotiation client aur server ke beech format decide karne ka process hai. Accept headers use karte hain.

Q143. Idempotency kya hai REST APIs mein?
A: Idempotent operations multiple times call karne par same result dete hain. GET, PUT, DELETE idempotent hain, POST nahi.

Q144. REST API mein HATEOAS implementation kaise karte hain?
A:

json
{
  "user": {
    "id": "123",
    "name": "John",
    "links": {
      "self": "/api/users/123",
      "posts": "/api/users/123/posts"
    }
  }
}
Q145. API Gateway pattern kya hai aur Flutter mein kaise use karte hain?
A: API Gateway single entry point provide karta hai multiple services ke liye. Flutter mein base URL switch kar sakte hain different environments ke liye.

Q146. GraphQL vs REST kab use karte hain?
A:

GraphQL: Complex relationships, flexible queries
REST: Simple CRUD, caching important hai
Q147. Server-side events (SSE) kaise implement karte hain?
A:

dart
Stream<String> serverSentEvents() async* {
  final client = http.Client();
  final request = http.Request('GET', Uri.parse('$baseUrl/events'));
  
  final response = await client.send(request);
  await for (String line in response.stream
      .transform(utf8.decoder)
      .transform(LineSplitter())) {
    yield line;
  }
}
Q148. API analytics aur monitoring kaise implement karte hain?
A:

Request/response logging karte hain
Performance metrics track karte hain
Error rates monitor karte hain
Crashlytics integrate karte hain
Q149. Multi-tenant applications mein API handling kaise karte hain?
A:

Tenant ID headers mein pass karte hain
URL path mein tenant include karte hain
Database level segregation karte hain
Q150. API documentation automation kaise karte hain?
A:

OpenAPI/Swagger specifications use karte hain
Code generation tools use karte hain
Automated testing se documentation sync karte hain
Bonus Tips for Interview
Technical Round Preparation:
Code examples ready rakhiye - Common widgets, BLoC implementation
Project demo prepare kijiye - Screenshots aur functionality explain kar sakte hain
Error handling examples - Try-catch blocks, custom exceptions
Performance optimization - Lazy loading, caching strategies
HR Round Preparation:
Projects ke challenges - Kya problems face kiye aur kaise solve kiye
Learning approach - Naye technologies kaise seekhte hain
Team collaboration - Git workflows, code reviews
Future goals - Career mein kya achieve karna hai
Practical Tips:
Portfolio ready rakhiye - GitHub links, demo videos
Mock interviews practice kijiye
Latest Flutter updates - Null safety, Flutter 3.x features
Clean code principles - SOLID principles, design patterns
All the best for your interview! 🚀

Made with
