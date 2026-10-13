# Cálculo del Sueldo Quincenal

Aplicación web sencilla hecha en PHP que calcula el sueldo quincenal de un trabajador a partir de las horas trabajadas en tres turnos. Para el diseño se usa Bootstrap por CDN.

## Funcionamiento

1. El usuario ingresa su **nombre**, **cédula** y las **horas trabajadas** en los turnos diurno, vespertino y nocturno.
2. Al presionar "Calcular", el formulario se envía por `POST` al mismo archivo (`index.php`).
3. El programa calcula el **sueldo bruto** con las siguientes tarifas por hora:

| Turno      | Tarifa (Bs.) |
|------------|--------------|
| Diurna     | 675          |
| Vespertina | 700          |
| Nocturna   | 956.23       |

4. Según el sueldo bruto, se aplican estos porcentajes de retención:

| Sueldo bruto                    | Ahorro Habitacional | Seguro Social |
|---------------------------------|---------------------|---------------|
| Menor a 85.000 Bs.              | 0.1%                | 0.15%         |
| Entre 85.000 y 150.000 Bs.      | 0.15%               | 0.2%          |
| Mayor a 150.000 Bs.             | 0.3%                | 0.25%         |

5. Se muestra en pantalla:
   - Nombre y cédula del empleado
   - Sueldo bruto
   - Monto descontado por Ahorro Habitacional y por Seguro Social
   - Sueldo quincenal neto (sueldo bruto menos las deducciones)

## Archivos

- `index.php`: contiene el formulario (HTML) y el cálculo (PHP).

## Cómo ejecutarlo

Colocar `index.php` en la carpeta del servidor local (por ejemplo `htdocs` en XAMPP) y abrir `http://localhost/index.php` en el navegador.
