# email-signature
Cool email signature

# Minification

    sed -i 's/^[ \t]*//g; s/[ \t]*$//g;' signature.html
    sed -i ':a;N;$!ba;s/\n/ /g' signature.html

![Signature example][Example src]

  [Example src]: https://github.com/nafigator/email-signature/raw/master/images/example.png
