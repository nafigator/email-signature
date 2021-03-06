# Email-signature

![Signature example][Signature img]

## Minification

    perl -p -e 's/^[ \t]*//g;s/[ \t]*$//g;s/\n//g;s/>\s*</></g;s/: /:/g;s/; /;/g' signature.html > minified.html

## Customization

    sed -i '
        s/Yancharuk Alexander/Your Name/g;
        s/user@supermail.su/your@email.com/g;
        s/Web-developer/Your Position/g;
        s/+7 555 333-22-11/+7 333 222-11-00/g;
        s/https:\/\/www.homepage.info/http:\/\/your-home-page.com/g;
        s/https:\/\/github.com\/username/https:\/\/github.com\/your-username/g;
        s/https:\/\/stackoverflow.com\/users\/3333333\/user-name/https:\/\/stackoverflow.com\/users\/1111111\/your-user-name/g;
        s/https:\/\/hh.ru\/resume\/11111111111111111111111111111111111111/https:\/\/hh.ru\/resume\/222222222222222222222222222222222222222/g;
        s/skype:+75553332211?call/skype:+73332221100?call/g;
        s/https:\/\/t.me\/username/https:\/\/t.me\/your-username/g;
    ' minified.html

## Personal data workflow
#### Save converter changes

    # gpg --output convert.gpg --encrypt --recipient <email> convert.sh
    gpg -o convert.gpg -e -r <email> convert.sh
    git commit && git push

#### Load converter changes

    git pull
    # gpg --output convert.sh --decrypt convert.gpg
    gpg -o convert.sh -d convert.gpg

___
[![License][License img]][License src]

  [License img]: https://github.com/nafigator/email-signature/raw/master/images/raw/wtfpl.png
  [License src]: https://tldrlegal.com/license/do-wtf-you-want-to-public-license-v2-(wtfpl-2.0)
  [Signature img]: https://github.com/nafigator/email-signature/raw/master/images/example.png
