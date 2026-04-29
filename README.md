# OJS Project Setup by Togzhan Oral  (Open Journal Systems)

## What is included

This project contains:

* `ojs-3.5.0-3.zip` — main OJS website files
* `files.zip` — uploaded journal files (articles, etc.)
* `ojs_db.sql` — database dump

---

## Requirements

Before starting, install:

* MAMP (for Windows or Mac)
  https://www.mamp.info/en/downloads/

---

## Step-by-step Setup

### 1. Install and run MAMP

* Open MAMP
* Click **Start Servers**

---

### 2. Extract project files

Extract archives to:

```
C:\MAMP\htdocs\
```

You should get:

```
C:\MAMP\htdocs\ojs-3.5.0-3
```

---

### 3. Move "files" folder

Extract `files.zip` and place it here:

```
C:\MAMP\files
```

If folder does not exist — create it manually.

---

### 4. Create database

Open in browser:

```
http://localhost/phpMyAdmin
```

Steps:

1. Click **New**
2. Create database:

```
ojs_db
```

---

### 5. Import database

1. Open `ojs_db`
2. Go to **Import**
3. Upload file:

```
ojs_db.sql
```

4. Click **Go**

---

### 6. Configure OJS

Open file:

```
C:\MAMP\htdocs\ojs-3.5.0-3\config.inc.php
```

Set:

```
base_url = "http://localhost/ojs-3.5.0-3"
```

And database settings:

```
host = localhost
username = root
password = root
name = ojs_db
```

---

### 7. Open website

Go to:

```
http://localhost/ojs-3.5.0-3
```

---

## Troubleshooting

### If site does not load:

* Make sure MAMP is running
* Check port (use http://localhost:8888 if needed)
* Check config.inc.php settings

### If styles are broken:

* Clear browser cache
* Check correct base_url

### If database error:

* Re-import ojs_db.sql
* Check database credentials


