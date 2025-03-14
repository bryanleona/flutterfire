## 2.6.17

 - **REFACTOR**: migrate from hash* to Object.hash* (#8797). ([3dfc0997](https://github.com/firebase/flutterfire/commit/3dfc0997050ee4351207c355b2c22b46885f971f))
 - **REFACTOR**: use "firebase" instead of "FirebaseExtended" as organisation in all links for this repository (#8791). ([d90b8357](https://github.com/firebase/flutterfire/commit/d90b8357db01d65e753021358668f0b129713e6b))

## 2.6.16

 - Update a dependency to the latest release.

## 2.6.15

 - Update a dependency to the latest release.

## 2.6.14

 - Update a dependency to the latest release.

## 2.6.13

 - Update a dependency to the latest release.

## 2.6.12

 - Update a dependency to the latest release.

## 2.6.11

 - Update a dependency to the latest release.

## 2.6.10

 - **FIX**: update all Dart SDK version constraints to Dart >= 2.16.0 (#8184). ([df4a5bab](https://github.com/firebase/flutterfire/commit/df4a5bab3c029399b4f257a5dd658d302efe3908))

## 2.6.9

 - Update a dependency to the latest release.

## 2.6.8

 - Update a dependency to the latest release.

## 2.6.7

 - Update a dependency to the latest release.

## 2.6.6

 - Update a dependency to the latest release.

## 2.6.5

 - **REFACTOR**: fix all `unnecessary_import` analyzer issues introduced with Flutter 2.8. ([7f0e82c9](https://github.com/firebase/flutterfire/commit/7f0e82c978a3f5a707dd95c7e9136a3e106ff75e))

## 2.6.4

 - Update a dependency to the latest release.

## 2.6.3

 - Update a dependency to the latest release.

## 2.6.2

 - Update a dependency to the latest release.

## 2.6.1

 - Update a dependency to the latest release.

## 2.6.0

 - **FEAT**: automatically inject Firebase JS SDKs (#7359).

## 2.5.0

 - **FEAT**: support initializing default `FirebaseApp` instances from Dart (#6549).

## 2.4.5

 - Update a dependency to the latest release.

## 2.4.4

 - Update a dependency to the latest release.

## 2.4.3

 - Update a dependency to the latest release.

## 2.4.2

 - **FIX**: implement missing getter for settings on Firestore web (#6930).
 - **CHORE**: Reduce hash conflicts on objects (#6928).

## 2.4.1

 - Update a dependency to the latest release.

## 2.4.0

 - **STYLE**: enable additional lint rules (#6832).
 - **FIX**: blob was being parsed as geopoint. (#6728).
 - **FEAT**: override ==/hashCode for Firestore Queries (#6797).

## 2.3.0

 - **FIX**: export PersistenceSettings (#6603).
 - **FEAT**: useFirestoreEmulator(host, port) API for firestore (#6428).
 - **CHORE**: publish packages (#6513).

## 2.2.0

 - **FEAT**: useFirestoreEmulator(host, port) API for firestore (#6428).

## 2.1.2

 - Update a dependency to the latest release.

## 2.1.1

 - Update a dependency to the latest release.

## 2.1.0

 - **FIX**: pass GetOptions to web Query.get (#6132).
 - **FEAT**: loadBundle() & namedQueryGet() implementation (#6037).

## 2.0.1

 - **DOCS**: Add missing homepage/repository links (#6054).
 - **CHORE**: publish packages (#6022).
 - **CHORE**: publish packages.

## 2.0.0

 - **FEAT**: Add withConverter function to CollectionReference, DocumentReference and Query (#6015).
    This new method allows interacting with collections/documents in a type-safe way:

    ```dart
    final modelsRef = FirebaseFirestore
        .instance
        .collection('models')
        .withConverter<Model>(
          fromFirestore: (snapshot, _) => Model.fromJson(snapshot.data()!),
          toFirestore: (model, _) => model.toJson(),
        );

    Future<void> main() async {
      // Writes now take a Model as parameter instead of a Map
      await modelsRef.add(Model());
      final Model model = await modelsRef.doc('123').get().then((s) => s.data());
    }
    ```

 - **BREAKING** **REFACTOR**: `DocumentReference`, `CollectionReference`, `Query`, `DocumentSnapshot`,
   `CollectionSnapshot`, `QuerySnapshot`, `Transaction.get`, `Transaction.set` and `WriteBatch.set`
   now take an extra generic parameter.  (#6015).

   See the [migration guide](https://firebase.flutter.dev/docs/firestore/2.0.0_migration) for more
   information on how to update your code.

 - **BREAKING** **FEAT**: convert FieldPath parameters from dynamic to Object (#5997).

## 1.0.7

 - Update a dependency to the latest release.

## 1.0.6

 - **REFACTOR**: Share guard functions accross plugins (#5783).

## 1.0.5

 - **FIX**: conditionally pass options to docChanges (#5751).

## 1.0.4

 - Update a dependency to the latest release.

## 1.0.3

 - **FIX**: cannot store null values in firestore on the web (#5335).
 - **CHORE**: bump min Dart SDK constraint to 2.12.0 (#5430).
 - **CHORE**: publish packages (#5429).

## 1.0.2

 - **FIX**: cannot store null values in firestore on the web (#5335).

## 1.0.1

 - **FIX**: Fix wrong cast (firebase#5050) (#5242).

## 1.0.0

 - Graduate package to a stable release. See pre-releases prior to this version for changelog entries.

## 1.0.0-1.0.nullsafety.0

 - Bump "cloud_firestore_web" to `1.0.0-1.0.nullsafety.0`.

## 0.4.0-1.0.nullsafety.2

 - **FIX**: Fixed crashes due to null `Settings` (#5031).

## 0.4.0-1.0.nullsafety.1

 - Update a dependency to the latest release.

## 0.4.0-1.0.nullsafety.0

> Note: This release has breaking changes.

 - **BREAKING** **REFACTOR**: migrate to NNBD (#4780).

## 0.3.0+1

 - Update a dependency to the latest release.

## 0.3.0

> Note: This release has breaking changes.

 - **FIX**: ensure web FieldValue types are converted (#4247).
 - **BREAKING** **REFACTOR**: remove all currently deprecated APIs (#4594).

## 0.2.1+2

 - Update a dependency to the latest release.

## 0.2.1+1

 - Update a dependency to the latest release.

## 0.2.1

 - **FEAT**: migrate firebase interop files to local repository (#3973).
 - **FEAT** [WEB] `FirebaseFirestore.enablePersistence` now accepts `PersistenceSettings`
 - **FEAT** [WEB] adds `PersistenceSettings` class
 - **FEAT** [WEB] adds support for `FirebaseFirestore.clearPersistence`
 - **FEAT** [WEB] adds support for `FirebaseFirestore.terminate`
 - **FEAT** [WEB] adds support for `FirebaseFirestore.waitForPendingWrites`
 - **FEAT** [WEB] adds support for `SetOptions.mergeFields`
 - **FEAT** [WEB] adds `GetOptions` support for querying against server/cache
 - **FEAT** [WEB] adds support for `Query.limitToLast`
 - **FEAT** [WEB] adds support for `FirebaseFirestore.snapshotsInSync`

## 0.2.0+5

 - Update a dependency to the latest release.

## 0.2.0+4

 - **FIX**: bubble exceptions (#3701).
 - **FIX**: fix returning of transaction result (#3747).
 - **FIX**: ensure isCollectionGroupQuery is initialised (#3772).

## 0.2.0+3

 - **FIX**: dependency issue in pubspec.yaml (#3734).

## 0.2.0+2

 - **FIX**: fix dependency in pubspec.yaml (#3713).

## 0.2.0+1

* Fixed issue #3210 (`Query.orderBy(FieldPath.documentId)` throws exception).
* Bump `cloud_firestore_platform_interface` dependency.

## 0.2.0

* See `cloud_firestore` plugin changelog.

## 0.1.1+2

* Ensure QueryWeb correctly encodes values passed in to `[start|end][At|Before](Document?)` methods.

## 0.1.1+1

* Ensure FieldValueFactoryWeb correctly encodes parameters for arrayRemove/arrayUnion FieldValues.

## 0.1.1

* Support equality comparison of field values.
* `FieldValueWeb` no longer extends `FieldValuePlatform`.
* Updated platform interface dependency.

## 0.1.0+4

* Make the pedantic dev_dependency explicit.

## 0.1.0+3

- Removed unit test that was only testing dart-lang behavior.

## 0.1.0+2

- Update documentation about this package being the endorsed platform for web.

## 0.1.0+1

- Fix `fileName` prop in pubspec.yaml

## 0.1.0

- Initial release
