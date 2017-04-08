# Email-signature

![Signature example][Example src]

## Minification

    sed -i 's/^[ \t]*//g; s/[ \t]*$//g;' signature.html
    sed -i ':a;N;$!ba;s/\n/ /g' signature.html

## Customization

    sed -i '
        s/Yancharuk Alexander/Your Name/g;
        s/user@mail.su/your@email.com/g;
        s/Web-developer/Your Position/g;
        s/+7 555 333-22-11/+7 333 222-11-00/g;
        s/https:\/\/www.homepage.info/http:\/\/your-home-page.com/g;
        s/https:\/\/github.com\/username/https:\/\/github.com\/your-username/g;
        s/https:\/\/stackoverflow.com\/users\/3333333\/user-name/https:\/\/stackoverflow.com\/users\/1111111\/your-user-name/g;
        s/https:\/\/hh.ru\/resume\/11111111111111111111111111111111111111/https:\/\/hh.ru\/resume\/222222222222222222222222222222222222222/g;
        s/skype:+75553332211?call/skype:+73332221100?call/g;
        s/https:\/\/t.me/username/https:\/\/t.me/your-username/g;
    ' signature.html

  [Example src]: https://github.com/nafigator/email-signature/raw/master/images/example.png
