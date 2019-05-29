# Prerequisites:

To build the code you'll need Tick42 DLLs (namely DOT.AGM.dll and its dependencies). To obtain those DLLs, please contact us at <add mail here>.

# How to deploy GlueSymphonyRfqBridge

## 1. Contents:

This package includes 3 components:

	- GlueSymphonyRfqBridge
	- CounterRFQ.xlsm and RequestRFQ.xlsm
	- Javascript web apps

## 2. Dependencies not included in this repo:
- GlueXL (so that xlsm files can talk to one another)
- AGM Bridge (if you want to use the web apps)
- HTML Server (to host the JS apps)
- Tick42 libs referenced by GlueSymphonyRfqBridge (DOT.AGM and its dependencies)
- PricePublisher (to populate the JS Server web app with mock market data, so it can autoreply on RFQ inquiries)

## 3. How to build the code:
Get in touch with Tick42 <Add email here> so that you can get an installer for the Tick42 DLL dependencies referenced by the RFQ Bridge. The installer also contains the support applications required by the JS web apps.

## 4. How to run the demo
- Start the bridge using StartBot.cmd (assuming you've built it in Release mode) or from VisualStudio.
- At this point you should be able to use the two XLSM files to post RFQ queries from one to the other as well as chat messages. Integration to Symphony should also be available at this point.
- If you want to use the web apps, you'd have to get a copy of the ServerBridge. It's included in the installer for the DLL dependencies.
- Host the JS apps using a HTTP server. Built versions of the apps, a http-server and Node are included in the installer (JavaScript)
- At this point you should be able to send chat messages from the apps to Excel/Symphony and vice versa.
- If you want to use the autorespond JS server feature, you'd have to start the PricePublisher.

## Contributing

1. Fork it (<https://github.com/symphonyoss/glue-symphony-rfq/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Read our [contribution guidelines](.github/CONTRIBUTING.md) and [Community Code of Conduct](https://www.finos.org/code-of-conduct)
4. Commit your changes (`git commit -am 'Add some fooBar'`)
5. Push to the branch (`git push origin feature/fooBar`)
6. Create a new Pull Request

## License

The code in this repository is distributed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).

Copyright (c) 2016-2019 Tick42