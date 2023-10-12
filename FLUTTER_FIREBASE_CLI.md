#### Install CLI first if not exist
Link: https://firebase.google.com/docs/cli#setup_update_cli


# Step 1: Logout account

```
firebase logout
```

# Step 2: Login account

```
firebase login
```
# Step 3: Install the FlutterFire CLI by running the following command from any directory:

```
dart pub global activate flutterfire_cli
```

# Step 4: Configure your apps to use Firebase:

your flutter project $:  
```
flutterfire configure
```

# Step 5: Initialization#

Next the generated options need to be provided to the initializeApp method. Since this is an asynchronous operation, the main function can be modified to ensure initialization is complete before running the application.

First import the firebase_core plugin and generated firebase_options.dart file:


File: lib/main.dart

```
import 'package:firebase_core/firebase_core.dart';
import 'firebase_options.dart';
```
Next, within the main function, ensure WidgetsFlutterBinding is initialized and then initialize Firebase:

```
void main() async {
  WidgetsFlutterBinding.ensureInitialized();
  await Firebase.initializeApp(
    options: DefaultFirebaseOptions.currentPlatform,
  );
  runApp(MyApp());
}
```
