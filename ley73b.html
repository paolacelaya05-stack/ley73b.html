<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ley73-Calc - Grupo 502</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { font-family: system-ui, sans-serif; background: #f4f4f9; padding: 16px; color: #222; }
        .caja { max-width: 520px; margin: auto; background: #fff; padding: 18px; border-radius: 8px; border: 1px solid #ddd; }
        h3 { color: #004085; margin-bottom: 12px; }
        input, button { width: 100%; padding: 9px; margin-bottom: 10px; border-radius: 4px; border: 1px solid #bbb; font-size: 14px; }
        button { background: #004085; color: #fff; border: none; font-weight: bold; cursor: pointer; }
        .btn-sec { background: #198754; }
        .item { background: #f8f9fa; padding: 8px; margin-top: 8px; border-left: 4px solid #004085; font-size: 13px; }
    </style>
</head>
<body>
<div class="caja">
    <h3>📊 Ley73-Calc: Simulador y Reporte</h3>
    <input type="text" id="asegurado" placeholder="Nombre del asegurado">
    <input type="number" id="semanas" placeholder="Semanas cotizadas (ej. 1250)">
    <input type="number" id="salario" placeholder="Salario diario promedio MXN (ej. 550)" step="0.01">
    <button onclick="calcularYGuardar()">Calcular y Guardar</button>
    <button class="btn-sec" onclick="exportarCSV()">Exportar Reporte CSV</button>
    <div id="listaCalculos"></div>
</div>
<script>
    const CLAVE_L73 = "ley73_registros_502";

    function leerRegistros() {
        return JSON.parse(localStorage.getItem(CLAVE_L73)) || [];
    }

    function calcularYGuardar() {
        const nombre = document.getElementById("asegurado").value.trim();
        const semanas = parseInt(document.getElementById("semanas").value, 10);
        const salario = parseFloat(document.getElementById("salario").value);

        if (!nombre || isNaN(semanas) || isNaN(salario) || semanas <= 0 || salario <= 0) {
            alert("Verifica nombre y valores numéricos mayores a 0.");
            return;
        }

        let factor = 0.40;
        if (semanas > 500) {
            factor += (semanas - 500) * 0.00125;
        }
        const pensionMensual = ((salario * 365) * factor) / 12;

        const registros = leerRegistros();
        registros.push({
            nombre,
            semanas,
            pension: pensionMensual.toFixed(2)
        });
        localStorage.setItem(CLAVE_L73, JSON.stringify(registros));

        document.getElementById("asegurado").value = "";
        document.getElementById("semanas").value = "";
        document.getElementById("salario").value = "";
        renderizar();
    }

    function renderizar() {
        const cont = document.getElementById("listaCalculos");
        const datos = leerRegistros();
        cont.innerHTML = datos.map((r, i) =>
            `<div class="item"><strong>#${i + 1} ${r.nombre}</strong> — Semanas: ${r.semanas} | Pensión est.: <strong>$${r.pension} MXN</strong></div>`
        ).join("");
    }

    function exportarCSV() {
        const datos = leerRegistros();
        if (datos.length === 0) {
            alert("No hay cálculos para exportar.");
            return;
        }
        let csv = "Asegurado,Semanas,PensionMensualMXN\n";
        datos.forEach(r => {
            csv += `"${r.nombre}",${r.semanas},${r.pension}\n`;
        });
        const blob = new Blob([csv], { type: "text/csv;charset=utf-8;" });
        const url = URL.createObjectURL(blob);
        const enlace = document.createElement("a");
        enlace.href = url;
        enlace.download = "reporte_ley73.csv";
        enlace.click();
        URL.revokeObjectURL(url);
    }

    document.addEventListener("DOMContentLoaded", renderizar);
</script>
</body>
</html>
