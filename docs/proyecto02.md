# Proyecto 02: cálculo del sueldo

## 1. Formulario HTML

El archivo `ut02_p02a.html` contiene un formulario para introducir el sueldo base y seleccionar el puesto del trabajador. El sueldo mínimo permitido es de 1000 €.

```html
<form action="ut02_p02.php" method="post">
	<label for="sueldo">Sueldo:</label>
	<input type="number" id="sueldo" name="sueldo" required min="1000">

	<label for="puesto">Puesto</label>
	<select name="puesto" id="puesto">
		<option value="1">Base</option>
		<option value="2">Directivo</option>
		<option value="3">Alto Cargo</option>
	</select>

	<input type="submit" value="Submit">
</form>
```

El formulario envía los datos al archivo `ut02_p02.php` mediante el método `POST`.

## 2. Complemento según el puesto

El programa recibe el sueldo y el puesto seleccionados usando `$_POST`. Si no se reciben datos, utiliza un sueldo de 1000 € y el puesto base como valores predeterminados.

El porcentaje del complemento se determina con una estructura condicional:

```php
if ($puesto == 1) {
	$porcentaje = 10;
} elseif ($puesto == 2) {
	$porcentaje = 15;
} elseif ($puesto == 3) {
	$porcentaje = 20;
} else {
	$porcentaje = 0;
}
```

Los complementos establecidos son:

- **Base:** 10 %.
- **Directivo:** 15 %.
- **Alto Cargo:** 20 %.

## 3. Cálculo del sueldo final

Primero se calcula el importe del aumento y después se suma al sueldo base:

```php
$aumento = $sueldo * ($porcentaje / 100);
$sueldofinal = $sueldo + $aumento;
```

## 4. Resultado

El programa muestra el sueldo base, el porcentaje del complemento y el sueldo final:

```php
echo "El sueldo base es de " . $sueldo . "€<br>";
echo "El complemento es del " . $porcentaje . "%<br>";
echo "El sueldo final es de " . $sueldofinal . "€";
```

Por ejemplo, para un sueldo de 1500 € y un puesto directivo, el resultado es:

```text
El sueldo base es de 1500€
El complemento es del 15%
El sueldo final es de 1725€
```

## Resumen

Este proyecto utiliza un formulario HTML y un script PHP para calcular el sueldo final de un trabajador. Los datos se envían mediante `POST`, se aplica un complemento según el puesto y se muestra el resultado en una página web.
