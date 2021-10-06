# MyGuide.city IOS Framework 

## Installation and use

1. Download ```MyGuideCityLib.xcframework```
2. Add framework to project ```Targets > General > Frameworks...```
3. Add import to your view controller class ```import MyGuideCityLib```
4. Set your API key ```MyGuideCityAPI.setKey(message: "api-key")```
5. Prepare MyGuide.city view controller with targt destination ```let vc = MyGuideCityAPI.makeVcWithDestination(destination: "lucerne")```
6. Push MyGuide.city view controller to navigation controller ```self.navigationController?.pushViewController(vc, animated: true)```

## Example



```
import UIKit
import WebKit
import MyGuideCityLib 

class ViewController: UIViewController {
    override func viewDidLoad() {
        super.viewDidLoad()

        MyGuideCityAPI.setKey(message: "api-key") // set your API key
        let vc = MyGuideCityAPI.makeVcWithDestination(destination: "lucerne")
        self.navigationController?.pushViewController(vc, animated: true)
    }
}

```