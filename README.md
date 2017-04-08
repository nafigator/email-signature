# Email-signature
Cool email signature

![Signature example][Example src]

# Minification

    sed -i 's/^[ \t]*//g; s/[ \t]*$//g;' signature.html
    sed -i ':a;N;$!ba;s/\n/ /g' signature.html

  [Example src]: https://github.com/nafigator/email-signature/raw/master/images/example.png
