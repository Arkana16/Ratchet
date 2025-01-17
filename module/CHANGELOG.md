CHANGELOG
=========

###Legend

* "BC": Backwards compatibility break (from public component APIs)
* "BF": Bug fix

---

* 0.3.0 (2013-xx-xx)

 * Added the `App` class to help making Ratchet so easy to use it's silly
 * BC: Require hostname to do HTTP Host header match and do Origin HTTP header check, verify same name by default, helping prevent CSRF attacks
 * Added Symfony/2.2 based HTTP Router component to allowing for a single Ratchet server to handle multiple apps -> Ratchet\Http\Router
 * BC: Decoupled HTTP from WebSocket component -> Ratchet\Http\HttpServer
 * Updated dependency to React/0.3
 * BF: Single sub-protocol selection to conform with RFC6455
 * BF: Sanity checks on WAMP protocol to prevent errors

* 0.2.7 (2013-06-09)

 * BF: Sub-protocol negotation with Guzzle 3.6

* 0.2.6 (2013-06-01)

 * Guzzle 3.6 support

* 0.2.5 (2013-04-01)

 * Fixed Hixie-76 handshake bug

* 0.2.4 (2013-03-09)

 * Support for Symfony 2.2 and Guzzle 2.3
 * Minor bug fixes when handling errors

* 0.2.3 (2012-11-21)

 * Bumped dep: Guzzle to v3, React to v0.2.4
 * More tests

* 0.2.2 (2012-10-20)

 * Bumped deps to use React v0.2

* 0.2.1 (2012-10-13)

 * BF: No more UTF-8 warnings in browsers (no longer sending empty sub-protocol string)
 * Documentation corrections
 * Using new composer structure

* 0.2 (2012-09-07)

 * Ratchet passes every non-binary-frame test from the Autobahn Testsuite
 * Major performance improvements
 * BC: Renamed "WampServer" to "ServerProtocol"
 * BC: New "WampServer" component passes Topic container objects of subscribed Connections
 * Option to turn off UTF-8 checks in order to increase performance
 * Switched dependency guzzle/guzzle to guzzle/http (no API changes)
 * mbstring no longer required

* 0.1.5 (2012-07-12)

 * BF: Error where service wouldn't run on PHP <= 5.3.8
 * Dependency library updates

* 0.1.4 (2012-06-17)

 * Fixed dozens of failing AB tests
 * BF: Proper socket buffer handling

* 0.1.3 (2012-06-15)

 * Major refactor inside WebSocket protocol handling, more loosley coupled
 * BF: Proper error handling on failed WebSocket connections
 * BF: Handle TCP message concatenation
 * Inclusion of the AutobahnTestSuite checking WebSocket protocol compliance
 * mb_string now a requirement

* 0.1.2 (2012-05-19)

 * BC/BF: Updated WAMP API to coincide with the official spec
 * Tweaks to improve running as a long lived process

* 0.1.1 (2012-05-14)

 * Separated interfaces allowing WebSockets to support multiple sub protocols
 * BF: remoteAddress variable on connections returns proper value

* 0.1 (2012-05-11)

 * First release with components: IoServer, WsServer, SessionProvider, WampServer, FlashPolicy, IpBlackList
 * I/O now handled by React, making Ratchet fully asynchronous

