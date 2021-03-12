This configuration will improve the security of Firefox.
https://trac.torproject.org/projects/tor/ticket/28168
https://bugzilla.mozilla.org/show_bug.cgi?id=1540618

1- open firefox

2- In the address bar, type about:config and press Return

3- Seach and edit the following settings:


=========== Level 1 - Comfortable Protection ===========

security.pki.distrust_ca_policy;2

security.tls.version.min;3

security.tls.version.max;4

security.mixed_content.block_display_content;true

security.mixed_content.block_object_subrequest;true

security.ssl.require_safe_negotiation;true

security.webauth.u2f;true

network.trr.mode;3

network.trr.uri;https://mozilla.cloudflare-dns.com/dns-query
network.trr.bootstrapAddress;104.16.249.249

security.OCSP.enabled;0

network.security.esni.enabled;true
#network.dns.echconfig.enabled;true
#network.dns.use_https_rr_as_altsvc;true
#network.dns.echconfig.fallback_to_origin;false

network.IDN_show_punycode;true

toolkit.telemetry.enabled;false

security.sandbox.content.level;3

#security.sandbox.socket.process.level

=========== Level 2 - High Protection ===========

security.ssl3.rsa_des_ede3_sha;false

security.ssl3.rsa_aes_128_sha;false

security.ssl3.rsa_aes_256_sha;false

security.OCSP.require;true

security.ssl.treat_unsafe_negotiation_as_broken;true

privacy.resistFingerprinting;true //The backgroung image in the captcha where we need to move a piece of a puzzle to the correct position will not be showed

privacy.firstparty.isolate;true

privacy.trackingprotection.fingerprinting.enabled;true

privacy.trackingprotection.cryptomining.enabled;true

webgl.disabled;true

browser.send_pings;false

browser.cache.offline.enable;false

browser.privatebrowsing.autostart;true


=========== Level 3 - Paranoid Protection ===========

browser.sessionstore.max_tabs_undo;0

dom.event.clipboardevents.enabled;false //Disable copy/paste

dom.serviceWorkers.enabled;false //about:serviceworkers

media.peerconnection.enabled;false

media.navigator.enabled;false

privacy.firstparty.isolate.restrict_opener_access;false

dom.battery.enabled;false

dom.enable_performance;false

dom.enable_resource_timing;false

network.cookie.thirdparty.sessionOnly;true

network.cookie.thirdparty.nonsecureSessionOnly;true

network.cookie.lifetimePolicy;2

network.cookie.cookieBehavior;4 //May also break the functionality of some websites

network.http.referer.spoofSource;true //Some login session with 2FA will fail

network.http.referer.trimmingPolicy;2 //Some websites login will not work anymore

network.http.referer.XOriginPolicy;2 //Some websites login will not work anymore

network.http.referer.XOriginTrimmingPolicy;2 //Some websites login will not work anymore

browser.sessionstore.privacy_level;2

browser.search.suggest.enabled;false

breakpad.reportURL;

geo.enabled;false

network.dnsCacheEntries;0

network.http.redirection-limit;3

beacon.enabled;false

media.video_stats.enabled;false

security.ssl3.dhe_rsa_aes_128_sha;false

security.ssl3.dhe_rsa_aes_256_sha;false

security.ssl3.ecdhe_ecdsa_aes_128_sha;false

security.ssl3.ecdhe_ecdsa_aes_256_sha;false

security.ssl3.ecdhe_rsa_aes_128_sha;false

security.ssl3.ecdhe_rsa_aes_256_sha;false
