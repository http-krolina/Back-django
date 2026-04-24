# Projeto Django — Keys

Este README ajuda a iniciar um projeto `Keys` usando Django. Ele cobre os passos básicos para configurar o ambiente, criar o projeto e rodar o servidor de desenvolvimento.

## Pré-requisitos

- Python 3.10+ (recomendado)
- `pip`
- `venv` (já incluído no Python)

## 1) Criar e ativar ambiente virtual

```bash
python -m venv .venv
```

### macOS/Linux
```bash
source .venv/bin/activate
```

### Windows (PowerShell)
```powershell
.venv\Scripts\Activate.ps1
```

## 2) Instalar dependências

```bash
pip install django
```

Opcional (salvar dependências):
```bash
pip freeze > requirements.txt
```

## 3) Criar projeto Django

> Execute no diretório raiz do repositório.

```bash
django-admin startproject config .
```

## 4) Executar migrações iniciais

```bash
python manage.py migrate
```

## 5) Criar usuário administrador (opcional)

```bash
python manage.py createsuperuser
```

## 6) Iniciar servidor de desenvolvimento

```bash
python manage.py runserver
```

Acesse:
- Aplicação: http://127.0.0.1:8000
- Admin: http://127.0.0.1:8000/admin

---

## Estrutura inicial esperada

```text
.
├── manage.py
├── config/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
└── README.md
```

## Comandos úteis

Criar uma app:
```bash
python manage.py startapp core
```

Gerar migrações após alterar models:
```bash
python manage.py makemigrations
python manage.py migrate
```

## Próximos passos sugeridos

- Adicionar `requirements.txt`
- Configurar `.gitignore` para Python/Django
- Separar configurações por ambiente (`dev`, `prod`)
- Configurar variáveis de ambiente (ex.: `python-decouple`)
