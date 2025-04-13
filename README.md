## Install

### 1. Upload the template file to the server

Choose the version and run the corresponding command.

```
sudo wget -O /var/lib/marzban/templates/subscription/index.html https://raw.githubusercontent.com/justteddy/marzban-template/index.html
```

### 2. Configure the subscription page path

**Automatically**

Run these commands to set the path:
```
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/marzban/.env
```

**Manually**

Edit the Marzban `.env` file and add the following lines:
```
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"
```

### 3. Restart Marzban

Apply the changes by restarting Marzban:
```
marzban restart
```

## Personalization

To personalize, edit the `index.html` file.

### Main Values

Find and replace these default values with your own.

| Name         | Value                                                                               |
|--------------|-------------------------------------------------------------------------------------|
| Description  | `Simple, beautiful, and user-friendly HTML template for Marzban subscription page.` |
| Title        | `Marzbanify Template`                                                               |
| Favicons     | `apple-touch-icon.png`, `favicon-16x16.png`, `favicon-32x32.png`                    |
| Logo         | `logo.png`                                                                          |
| Support link | `https://t.me/`                                                                     |

### Optional Variables

These variables allow further personalization.

| Variable          | Description                                                 |
|-------------------|-------------------------------------------------------------|
| `DEFAULT_THEME`   | Default website theme (`system`, `light`, `dark`)           |
| `SUB_URL_SCHEMES` | URL schemes for quick subscription import                   |
| `DEFAULT_LOCALE`  | Default locale for content display (`en`, `ru`, `zh`, `fa`) |
| `MESSAGES`        | Translation data for multi-language support                 |
