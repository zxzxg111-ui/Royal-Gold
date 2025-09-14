import UIKit
import WebKit

class ViewController: UIViewController {
    override func viewDidLoad() {
        super.viewDidLoad()

        let webView = WKWebView(frame: self.view.bounds)
        webView.autoresizingMask = [.flexibleWidth, .flexibleHeight]
        view.addSubview(webView)

        if let url = URL(string: "https://beamish-cannoli-85e806.netlify.app") {
            let request = URLRequest(url: url)
            webView.load(request)
        }
    }
}
