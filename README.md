# Little Lemon Restaurant - Django Project

Sebuah website restoran yang dibangun dengan Django untuk menampilkan menu, informasi tentang restoran, dan sistem booking.

## Fitur

- Menu makanan dengan gambar dan deskripsi
- Sistem booking meja
- Halaman about dengan informasi restoran
- Responsive design
- Admin Django untuk mengelola konten

## Teknologi

- **Backend**: Django 5.2.5
- **Frontend**: HTML, CSS, JavaScript
- **Database**: SQLite (development), PostgreSQL (production ready)
- **Template**: Django Templates

## Setup Development

### Prerequisites

- Python 3.10+
- Pipenv (optional)
- Git

### Installation

1. Clone repository:
```bash
git clone <repository-url>
cd littlelemon
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Setup environment variables:
```bash
cp .env.example .env
# Edit .env file dengan konfigurasi yang sesuai
```

4. Jalankan migrations:
```bash
python manage.py migrate
```

5. Jalankan development server:
```bash
python manage.py runserver
```

6. Buka http://localhost:8000 di browser

## Environment Variables

Buat file `.env` dengan variabel berikut:

```
SECRET_KEY=your-secret-key-here
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
```

## Production Deployment

Untuk deployment production, pastikan:

1. Set `DEBUG=False`
2. Gunakan database production (PostgreSQL/MySQL)
3. Setup static files serving
4. Setup proper ALLOWED_HOSTS
5. Gunakan web server seperti Gunicorn + Nginx

## Struktur Project

```
littlelemon/
├── littlelemon/          # Project settings
├── restaurant/           # Main app
│   ├── models.py
│   ├── views.py
│   ├── templates/
│   └── static/
├── db.sqlite3           # Database (jangan di-commit)
├── manage.py
└── requirements.txt
```

## Contributing

1. Fork repository
2. Buat feature branch
3. Commit changes
4. Push ke branch
5. Buat Pull Request

## License

MIT License
