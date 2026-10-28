# Root-Me — Writeups

> Este repositorio es parte de **[sec-proy](https://github.com/hackadvisermx/sec-proy)**, un proyecto más amplio de soluciones a retos de ciberseguridad (CTFs, wargames y máquinas de hacking).

Writeups propios de los desafíos de [Root-Me](https://www.root-me.org/es/Desafios/), una plataforma pública de práctica de ciberseguridad. Los retos se organizan por áreas técnicas y se resuelven únicamente dentro de los entornos autorizados por la plataforma.

> **Sobre las flags:** los writeups documentan el razonamiento, las técnicas y los comandos empleados; no publican flags ni credenciales. Esos datos se conservan únicamente de forma local y están excluidos de git.

## Estado actual

La interfaz en inglés de Root-Me, revisada el **2026-10-28**, muestra **558 retos** en las once categorías. La cuenta `hackadvisermx` ya tiene **43 retos validados (7.7%)**. Este repositorio está revalidando y documentando esos avances de forma incremental: **4/43** writeups ya se verificaron y documentaron.

El detalle que distingue el estado de la plataforma de la documentación local vive en [PROGRESS.md](PROGRESS.md). Una validación existente solo cuenta como documentada cuando se vuelve a reproducir la técnica y se publica su writeup sin la flag.

## Categorías del catálogo

La estructura sigue las once categorías principales del catálogo de desafíos de Root-Me:

| Categoría Root-Me | Directorio |
|---|---|
| App - Script | `challenges/app-script/` |
| App - System | `challenges/app-system/` |
| Cracking | `challenges/cracking/` |
| Cryptanalysis | `challenges/cryptanalysis/` |
| Forensic | `challenges/forensic/` |
| Network | `challenges/network/` |
| Programming | `challenges/programming/` |
| Realist | `challenges/realist/` |
| Steganography | `challenges/steganography/` |
| Web - Client | `challenges/web-client/` |
| Web - Server | `challenges/web-server/` |

## Estructura del repositorio

```
.
├── PROGRESS.md                    # Inventario y seguimiento por categoría
├── challenges/
│   ├── _template/README.md         # Plantilla para cada writeup nuevo
│   ├── app-script/
│   ├── app-system/
│   ├── cracking/
│   ├── cryptanalysis/
│   ├── forensic/
│   ├── network/
│   ├── programming/
│   ├── realist/
│   ├── steganography/
│   ├── web-client/
│   └── web-server/
├── notes/                         # Notas generales no sensibles
└── scripts/                       # Automatizaciones reutilizables
```

Cada reto tendrá su propio directorio bajo `challenges/<categoría>/<slug>/README.md`. El writeup partirá de la [plantilla](challenges/_template/README.md) e incluirá la descripción oficial, metadatos del reto, una explicación reproducible de la técnica, comandos y referencias útiles.

## Metodología

- Resolver solo desafíos públicos y entornos iniciados o autorizados por Root-Me.
- Conservar los recursos descargados que sean necesarios para entender el análisis junto al writeup correspondiente, sin versionar secretos ni material temporal innecesario.
- Documentar una técnica por reto con pasos verificables y contexto suficiente para el aprendizaje, sin incluir flags o credenciales.

## Aviso

Este material tiene fines educativos y de práctica personal en la plataforma Root-Me. No debe extrapolarse a sistemas que no cuenten con autorización explícita.
