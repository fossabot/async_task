## 1.0.9-dev

- `README.md`:
  - Fix type.
  - Improve channel usage description.

## 1.0.8

- Fix isolate message of a task without `SharedData`.
- Improved tests scenarios.

## 1.0.7

- Small fix in README.
- Small fix in example.

## 1.0.6

- Added `AsyncTaskChannel` for messages communication with tasks during execution.
- Added `AsyncExecutorStatus`.
- `AsyncExecutor`: optimize to avoid creating of futures while executing/processing a task.
- Improved README. 

## 1.0.5

- Added `AsyncTaskPlatform` and `AsyncTaskPlatformType`.
- `AsyncTask`:
  - Optimize `taskType`
  - Optimize `execute` to use less `async` operations.
- Added `AsyncExecutorSharedDataInfo` to report `SharedData` information.
- `AsyncExecutor`:
  - New constructor parameter `parallelismPercentage`. 
  - Optimize `execute`, `executeAll` and `executeAllAndWaitResults` to dispatch less asyn operations.
  - Added `disposeSharedData` and `disposeSharedDataInfo`.
- Extensions:
  - Added `IterableFutureOrExtension` and `IterableFutureExtension`.
- `_AsyncExecutorMultiThread`:
  - Optimized to use less `async` operations.
  - Using `_RawReceivePortPool` to optimize ports.
  - Optimized to pre send `SharedData`.
- Added `_RawReceivePortPool`: pool of reusable `_ReceivePort`.
- Added `_ReceivePort`: an optimized `RawReceivePort`.

## 1.0.4

- `AsyncTask`:
  - Allow multiple `SharedData`: Optional method `sharedData`
    now returns a `Map<String,SharedData>`.

## 1.0.3

- `AsyncExecutor`:
  - Fix `close` operation while tasks are being executed.

## 1.0.2

- Added `SharedData`, to optimize data sharing between
  tasks and threads/isolates.
- `AsyncExecutor`: added `close` to stop and finalize an executor.
- Added collections extensions:
  `ListExtension`, `MapExtension`, `SetExtension`, `IterableExtension`.

## 1.0.1

- Fix `pubspec.yaml` description length.
- Improve `README.md` description. 

## 1.0.0

- Implemented `AsyncTask` with `status`, `result` and `executionTime`. 
- `AsyncExecutor` with implementations based on `dart:isolate` and `dart:async`. 
- Initial version.
