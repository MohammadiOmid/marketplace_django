# Puddle - Online Marketplace

Puddle is a simple online marketplace web application built with Django, following the [freeCodeCamp Django tutorial](https://www.youtube.com/watch?v=ZxMB6Njs3ck). Users can sign up, log in, create listings for items, browse items, and manage their own dashboard.

---

## Features

- User authentication (sign up, log in, log out)
- Create, view, and delete item listings
- Dashboard for managing your own items
- Category browsing (structure in place)
- Media upload for item images
- Responsive UI with Tailwind CSS

---

## Project Structure

```
puddle/
├── core/         # Main app: homepage, auth, base templates
├── item/         # Item listings: models, forms, views, templates
├── dashboard/    # User dashboard: manage own items
├── media/        # Uploaded images
├── manage.py     # Django management script
└── puddle/       # Project settings, URLs, WSGI/ASGI
```

---

## Setup Instructions

### 1. Clone the Repository

```sh
git clone <your-repo-url>
cd puddle
```

### 2. Create a Virtual Environment

```sh
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```sh
pip install -r requirements.txt
```

### 4. Apply Migrations

```sh
python manage.py migrate
```

### 5. Create a Superuser (Admin)

```sh
python manage.py createsuperuser
```

### 6. Run the Development Server

```sh
python manage.py runserver
```

Visit [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser.

---

## Usage

- **Homepage:** Lists newest items and categories.
- **Sign Up / Log In:** Use the navigation bar to register or log in.
- **New Item:** Authenticated users can create new listings.
- **Dashboard:** View and manage your own items.
- **Item Detail:** View item details, related items, and contact seller (future feature).
- **Admin:** Visit `/admin/` to manage categories and items as an admin.

---

## File Overview

- [`core`](puddle/core/): Homepage, authentication, base templates.
- [`item`](puddle/item/): Models for `Category` and `Item`, item forms, item views, and templates.
- [`dashboard`](puddle/dashboard/): User dashboard for managing items.
- [`media/`](puddle/media/): Uploaded item images.
- [`puddle/settings.py`](puddle/puddle/settings.py): Project settings (media, static, installed apps, etc.).
- [`puddle/urls.py`](puddle/puddle/urls.py): Main URL routing.

---

## Customization

- **Styling:** Uses [Tailwind CSS](https://tailwindcss.com/) via CDN in `base.html`.
- **Templates:** All HTML templates are in their respective app's `templates/` directories.
- **Media:** Uploaded images are stored in the `media/` directory.

---

## Extending the Project

- Add item editing functionality.
- Implement messaging between buyers and sellers.
- Add search and filtering for items.
- Improve category browsing.
- Add user profile pages.

---

## Troubleshooting

- If images do not display, ensure `MEDIA_URL` and `MEDIA_ROOT` are set in [`settings.py`](puddle/puddle/settings.py) and your server is running in development mode.
- For any issues with authentication, check the `LOGIN_URL`, `LOGIN_REDIRECT_URL`, and `LOGOUT_REDIRECT_URL` settings.

---

## License

This project is for educational purposes, based on the [freeCodeCamp Django tutorial](https://www.youtube.com/watch?v=ZxMB6Njs3ck).

---

## Credits

- [freeCodeCamp.org](https://www.freecodecamp.org/)
- [Django Documentation](https://docs.djangoproject.com/)

---

## Screenshots

