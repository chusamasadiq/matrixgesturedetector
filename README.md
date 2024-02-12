# matrix_gesture_detector

`MatrixGestureDetector` detects translation, scale and rotation gestures
and combines them into `Matrix4` object that can be used by `Transform` widget
or by low level `CustomPainter` code. You can customize types of reported
gestures by passing `shouldTranslate`, `shouldScale` and `shouldRotate`
parameters.

## Getting Started

The usage is as follows:

```dart
  MatrixGestureDetector(
    onMatrixUpdate: (Matrix4 m, Matrix4 tm, Matrix4 sm, Matrix4 rm) {
      setState(() {
        matrix = m;
      });
    },
    child: SomeWidgetThatUsesMatrix(
      matrix: matrix,
      ...
    )
  )
```
