# 🫨 Funny Faces

**Funny Faces** is a fun and interactive iOS app that uses Apple’s Vision framework along with SwiftUI to detect faces in real time using the front-facing camera — and decorate them live with animated googly eyes, cartoon sunglasses, and a playful red mouth.

It’s a hands-on project to explore:

- `AVFoundation` for real-time video capture  
- `Vision` for facial detection and landmark tracking  
- `CALayer` for drawing AR-style overlays directly on the camera feed  

---

## ✨ Features

- 📸 Face detection using the **front camera**
- 👀 Bouncy **googly eyes** that follow your face
- 🕶️ Animated **sunglasses** positioned over your eyes
- 👄 A dynamic **cartoon mouth** that tracks your lips
- 🔁 Built with **SwiftUI** via `UIViewControllerRepresentable`
- ⚙️ Powered by `AVCaptureSession` and `VNDetectFaceLandmarksRequest`

---

## 🔧 How It Works

Here’s the flow behind the scenes:

1. Captures frames continuously using `AVCaptureSession`
2. Sends each frame to the Vision framework with the `.leftMirrored` orientation (for front cam mirroring)
3. Vision detects the face and its landmarks (eyes, mouth)
4. Normalized coordinates from Vision are converted into screen space
5. Custom `CALayer`s are used to draw overlays on top of the live feed

---

## 📱 Requirements

- Xcode 15 or newer
- iOS 17+
- A real iOS device (camera access isn’t available in Simulator)

---

## 🚀 Getting Started

1. Clone this repository or copy the `LiveCameraView` and `CameraViewController` files into your SwiftUI project.
2. Embed the camera view in your app like so:

   ```swift
   struct ContentView: View {
       var body: some View {
           LiveCameraView()
               .ignoresSafeArea()
       }
   }



---
<br />


## Authors & contributors

The original setup of this repository is by [Santo Gaglione](https://github.com/Santein).
This is the branch for reviews

<br />
