# Order Service Troubleshooting

If the website says:

```text
The order service could not be reached.
```

it means the website could not load the Google Apps Script Web App URL from `config.js`.

## Most Common Fixes

1. Make sure `config.js` has the Web App URL.

```js
backendUrl: "https://script.google.com/macros/s/YOUR_DEPLOYMENT_ID/exec",
```

2. The URL must end with:

```text
/exec
```

Do not use the Apps Script editor URL.

3. In Apps Script, deploy it as:

- Type: **Web app**
- Execute as: **Me**
- Who has access: **Anyone**

4. After changing the Apps Script code, redeploy:

```text
Deploy > Manage deployments > Edit > New version > Deploy
```

5. Make sure your admin key in `admin.html` matches:

```js
var ADMIN_KEY="..."
```

inside Apps Script.

## Test It

Upload `backend-test.html` to GitHub with the rest of the site.

Then open:

```text
https://YOUR-GITHUB-USERNAME.github.io/YOUR-REPO-NAME/backend-test.html
```

Paste your backend URL and admin key.

Good result:

```json
{
  "ok": true,
  "orders": []
}
```

Bad result:

- If it says it could not load the script, the deployment URL or access setting is wrong.
- If it says `Invalid admin key`, the backend works but the key is wrong.
- If it shows a Google login page when opened directly, the deployment access is not set to **Anyone**.
