
# Code Conventions

These are some code conventions to follow when coding using Laravel framework. You are welcome to suggest more.

1. Use snake case for variable naming eg: ``` $snake_case = "correct"; ```
1. Use plural pascal case for Controller names. Eg: CourtCasesController
1. Method Ordering In Models:<br> When ordering the attributes and methods in a model, follow the below convention
    1. Attributes
    2. Boot Method
    3. Relations
    4. Scopes
    5. Mutators (when writing separately, prioritize set over get)
    6. Custom Functions
1. Action classes must be suffixed with "Action". Eg: UpdateOrCreateUserAction
1. Action classes should be in singular pascal case. Eg: UpdateOrCreateUserAction
1. Request classes must be in plural pascal case. Eg: AddressesRequest
1. Policy classes must be in singular pascal case. Eg: CourtCasePolicy
1. Service classes must be in singular pascal case and must be suffixed with "Service". Eg: CourtCaseService
1. Seeder classes must be in plural pascal case. Eg: DefaultUsersSeeder

**Note:** 
1. You may use custom query builder classes to extract scopes out of the model.
2. You may use Presenter classes to extract mutators out of the model.
3. Use Actions to extract out custom functions (if extraction serves a purpose).
4. You may use a single request class for both update and store if the there is not much difference in the rules and conditionally add or remove classes. You may use ``` $this->route('model-route-parameter'); ``` to get the currently editing model.
   
**TODO:** Views, routes and test conventions