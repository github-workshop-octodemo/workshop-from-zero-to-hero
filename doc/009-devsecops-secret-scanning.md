# 9 - DevSecOps with GitHub : Secret Scanning

GitHub scans repositories for known types of secrets, to prevent fraudulent use of secrets that were committed accidentally.

- [List of supported secrets for private repositories](https://docs.github.com/en/enterprise-cloud@latest/code-security/secret-scanning/secret-scanning-partners#list-of-supported-secrets-for-private-repositories)


A secret/key should never be stored in the repository, but for this lab you will do it to see how GitHub is protecting you.


## 1 - Add a secret in your project

Suppose you need to use some Google API, you will have a key that looks like `AIzaSyC8hreAohtwY647W85qTfE_4LP7ObTdD_c`


1. Update the `index.js` file (or any other one)

2. Add the following definition
    ```js
      const g = "AIzaSyC8hreAohtwY647W85qTfE_4LP7ObTdD_c";
    ```


3. Commit your changes.

## 2- Secret Scanning Alert

GitHub is automatically scanning your commit, and will discover the new API key.

1. Click on **Security**.

2. Click on **Secret scanning alerts** in the left menu.
![](../images/img-043.png)
GitHub has recognized the Google API Key

3. Click on the alert, and mark the alert as **Close as** - **Revoked**



4. You should also have received an email with the alert
![](../images/img-042.png)


## 3- Push Protection

You can use secret scanning to prevent supported secrets from being pushed into your organization or repository by enabling push protection.

Go in the `Settings` tab of your project in the `Code security and analysis` page and enable "Push protection"  under the "Secret scanning" section.

Add the following string to your code, commit and push this commit:

```js
const af = "aio_MtXK444XX8zwjZ13vXbAoJ4vmJxh";
```

Your push should be refused as it contains a recognized secret pattern ( [Supported secrets for push protection](https://docs.github.com/en/enterprise-cloud@latest/code-security/secret-scanning/secret-scanning-patterns#supported-secrets-for-push-protection))

## Conclusion

> Note : if your repositoruy is Public the behavior is different as you can see in the [documentation](https://docs.github.com/en/enterprise-cloud@latest/code-security/secret-scanning/about-secret-scanning#about-secret-scanning-for-public-repositories).


In this lab you have learned how to:

- 👏 use GitHub Secret Scanning 

---

Next : 
  - **[Deploy to Kubernetes with GitHub Actions](010-devops-deploy-to-kubernetes.md)**
