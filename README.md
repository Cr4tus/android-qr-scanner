# Android QR Scanner

## What does the app do?
Once it is running the app is able to scan QR codes that contains a simple text and display it on the screen. The app uses camera permission.

## Programming Languages:
- Kotlin

## Frameworks & Libraries:
- Android Jetpack Suite (including Jetpack Compose for UI) - https://developer.android.com/jetpack
- Gradle - https://developer.android.com/build/releases/gradle-plugin
- Google
    - zxing - https://github.com/zxing/zxing
    - accompanist (for permissions handling) - https://github.com/google/accompanist/tree/main/permissions

## Implementation:
The important steps are:
- creating an image analyzer which is able to analyze objects of type *ImageProxy*
- creating a *@Composable* function that handles the camera view
- define the constants for the supported image & bar code formats:
```kotlin
import android.graphics.ImageFormat
import com.google.zxing.BarcodeFormat

val supportedImageFormats = listOf(
    ImageFormat.YUV_420_888,
    ImageFormat.YUV_422_888,
    ImageFormat.YUV_444_888,
)

val supportedBarCodeFormats = listOf(
    BarcodeFormat.QR_CODE,
)
```
