# Indian Bazaar & Desi Bites Website

Upload everything in this folder to a new GitHub repository.

## Main Pages

- `index.html` is the customer website.
- `admin.html` links staff to the live Google Apps Script order manager.
- `backend-test.html` shows the live order manager link from `config.js`.

## Required Files

Keep these files in the main/root area of the GitHub repo:

- `.nojekyll`
- `index.html`
- `admin.html`
- `backend-test.html`
- `config.js`
- `styles.css`
- `script.js`
- `admin.css`
- `admin.js`
- `README.md`
- `ORDER_BACKEND_SETUP.md`
- `ORDER_SERVICE_TROUBLESHOOTING.md`
- `GOOGLE_APPS_SCRIPT_CODE.txt`

Keep this folder too:

- `assets`

## Google Apps Script

Paste the contents of `GOOGLE_APPS_SCRIPT_CODE.txt` into Google Apps Script. This version contains the real live staff order manager.

The website already has the current backend URL in `config.js`.

## Staff Login

The staff page uses the admin key you set inside Google Apps Script.

For live orders, open:

```text
backend-test.html
```

Then click **Open staff order manager** and enter the admin key.
