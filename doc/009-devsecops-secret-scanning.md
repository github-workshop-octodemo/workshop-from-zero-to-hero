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



> Note : if your repositoruy is Public the behavior is different as you can see in the [documentation](https://docs.github.com/en/enterprise-cloud@latest/code-security/secret-scanning/about-secret-scanning#about-secret-scanning-for-public-repositories).


## Conclusion

In this lab you have learned how to:

- 👏 use GitHub Secret Scanning 

---

Next : 
  - **[DevOps: Deploy to Kubernetes](010-devops-deploy-to-kubernetes.md)**
