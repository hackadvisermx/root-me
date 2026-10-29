# Web - Server — API - Mass Assignment

## Descripción

- **Puntos:** 20
- **Reto:** [Root-Me — API - Mass Assignment](https://www.root-me.org/en/Challenges/Web-Server/API-Mass-Assignment)

La API acepta propiedades no previstas al actualizar el objeto del usuario. Un campo de rol controlado por el cliente permite elevar privilegios.

## Solución

1. Crear una cuenta efímera e iniciar sesión en la instancia de CTF.
2. Consultar Swagger y probar los métodos HTTP permitidos; el recurso de usuario también acepta `PUT`.
3. Enviar un atributo de rol no expuesto por el flujo normal:

   ```json
   {"status":"admin"}
   ```

4. Con el rol elevado, consultar el endpoint de administración y usar el resultado únicamente en Root-Me.

La respuesta fue validada y el «Like» quedó registrado.

## Notas adicionales

- Las APIs deben permitir explícitamente cada campo modificable; nunca hacer *binding* masivo sobre objetos sensibles.
- La cuenta creada existió solo en la instancia aislada.

## Referencias

- [Reto oficial](https://www.root-me.org/en/Challenges/Web-Server/API-Mass-Assignment)
- [OWASP API3:2023 — Broken Object Property Level Authorization](https://owasp.org/API-Security/editions/2023/en/0xa3-broken-object-property-level-authorization/)
