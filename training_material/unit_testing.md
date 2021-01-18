# Unit Testing

Sources

[Local Unit Tests](https://developer.android.com/training/testing/unit-testing/local-unit-tests)

1. Check out `ExampleUnitTest`
 * Run with play button
 * Modify to make it fail, replay
 * Run with `./gradlew app:testDebugUnitTest`
 * Fix the test
 * Add a failing test `subtraction_isCorrect`
 * Run `./gradlew test --tests com.benboral.saucelabstraining.ExampleUnitTest.addition_isCorrect`

1. Testing our ViewModel
 * Write `ScreenInfoViewModelTests`
 
 ```kotlin
 class ScreenInfoViewModelTests {
     @Test
     fun incrementCount_updatesCountByOne() {
         val viewModel = ScreenInfoViewModel()
         assertEquals(0, viewModel.clickCount)
         viewModel.incrementCount()
         assertEquals(1, viewModel.clickCount)
     }
 }
```

 * Run the test: `RuntimeException: Method getMainLooper in android.os.Looper not mocked`
 * Explain the looper and lack of mocking. 