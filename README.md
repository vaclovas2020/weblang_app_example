# Example Weblang web application for testing Weblang CLI 

This is Weblang program for testing weblang programming language and Weblang CLI
Please use for testing purposes only.

1. Add GPG public key:
```sh
curl -fsSL https://weblang.dev/deb-repo/pgp-key.public | sudo gpg --dearmor -o /usr/share/keyrings/weblang.gpg
```

2. Add deb package to package list:
```sh
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/weblang.gpg] https://weblang.dev/deb-repo stable main" | sudo tee /etc/apt/sources.list.d/weblang.list  > /dev/null
```

3. Update apt list and install weblang package:
```sh
sudo apt update && sudo apt install weblang
```

4. Run application with command:
```sh
weblang run web/src web/generated
```
