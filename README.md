# CE.SDK CocoaPods Specs

This is the CocoaPods spec repository for the iOS pods of [CE.SDK](https://img.ly/products/creative-sdk) by IMG.LY.

CocoaPods trunk stops accepting new pod versions on December 2, 2026 ([announcement](https://blog.cocoapods.org/CocoaPods-Specs-Repo/)). New CE.SDK versions are published here instead. React Native and Flutter apps install the native CE.SDK pods through CocoaPods, so they need this repository to get new releases.

## Usage

Add these two lines at the top of your `Podfile`:

```ruby
source 'https://github.com/imgly/cesdk-specs.git'
source 'https://cdn.cocoapods.org/'
```

Keep both lines. A Podfile with a `source` line uses only the sources it lists. The second line keeps all your other pods resolving from trunk.

Then install the pods again:

```bash
pod install --repo-update
```

The [CE.SDK documentation](https://img.ly/docs/cesdk/) has step-by-step guides for React Native, Expo and Flutter.

## Pods

| Pod | Contents |
|---|---|
| `IMGLYEngine` | The CE.SDK engine, as an xcframework |
| `IMGLYUI` | The prebuilt editors, with one subspec per editor |
| `IMGLYCamera` | The camera |
| `IMGLYPlugin*` | Optional plugins, such as background removal |

This repository holds only the podspecs. When you install, CocoaPods downloads the source code from [imgly/IMGLYUI-swift](https://github.com/imgly/IMGLYUI-swift) and the engine binary from the IMG.LY CDN.

Versions released before December 2, 2026 are also on trunk and stay installable from there.

## Native iOS Apps

For a native iOS, macOS or Mac Catalyst app, use Swift Package Manager instead of CocoaPods: [IMGLYUI-swift](https://github.com/imgly/IMGLYUI-swift) and [IMGLYEngine-swift](https://github.com/imgly/IMGLYEngine-swift).

## Contributing

Every CE.SDK release updates this repository automatically. Please do not open pull requests here. Report problems at [img.ly/support](https://img.ly/support).

## License

The podspecs are published under the license of the matching CE.SDK release. Using CE.SDK requires a license. See [img.ly/pricing](https://img.ly/pricing).
