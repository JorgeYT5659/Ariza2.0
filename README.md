<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Plataforma del Colegio Adventista de Granada</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }
        h1 {
            text-align: center;
            color: #333;
            margin-top: 20px;
        }
        form {
            width: 50%;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        label {
            display: block;
            margin-bottom: 10px;
            font-weight: bold;
        }
        input[type="text"],
        input[type="number"],
        select,
        button {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-sizing: border-box;
            font-size: 16px;
        }
        button {
            background-color: #0c71e4;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #0c71e4;
        }
        table {
            width: 70%;
            margin: 20px auto;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid #dddddd;
            padding: 8px;
            text-align: left;
        }
        th {
            background-color: #f2f2f2;
        }
        .logo {
            text-align: center;
            margin-bottom: 20px;
        }
        .logo img {
            width: 200px;
            height: auto;
        }
    </style>
</head>
<body>
    <div class="logo">
        <img src="https://static.wixstatic.com/media/188a9a_a12105ee2b06440db227c107b36e59ab~mv2.png/v1/fill/w_320,h_180,q_90/188a9a_a12105ee2b06440db227c107b36e59ab~mv2.png" alt="Logo del Colegio Adventista de Granada">
    </div>
    <h1>Plataforma del Colegio Adventista de Granada</h1>

    <form>
        <label for="nombreEstudiante">Nombre del Estudiante:</label>
        <input type="text" id="nombreEstudiante" required>

        <label for="grado">Grado:</label>
        <select id="grado" required>
            <option value="" disabled selected>Seleccione el grado</option>
            <option value="Transición">Transición</option>
            <option value="Primero">Primero</option>
            <option value="Segundo">Segundo</option>
            <option value="Tercero">Tercero</option>
            <option value="Cuarto">Cuarto</option>
            <option value="Quinto">Quinto</option>
            <option value="Sexto">Sexto</option>
            <option value="Septimo">Septimo</option>
            <option value="Octavo">Octavo</option>
            <option value="Noveno">Noveno</option>
            <option value="Decimo">Decimo</option>
            <option value="Once">Once</option>
            <!-- Agregar más opciones según los grados disponibles -->
        </select>

        <label for="materia">Materia:</label>
        <select id="materia" required>
            <option value="" disabled selected>Seleccione una materia</option>
            <option value="Trigonometria">Trigonometria</option>
            <option value="Estadistica">Estadistica</option>
            <option value="Competencias Ciuadadanas">Competencias Ciudadanas</option>
            <option value="Ciencias Politicas">Ciencias Politicas</option>
            <option value="Lenguaje">Lenguaje</option>
            <option value="Filosofia">Filosofia</option>
            <option value="Quimica">Quimica</option>
            <option value="Fisica">Fisica</option>
            <option value="Ingles">Ingles</option>
            <option value="Contabilidad">Contabilidad</option>
            <option value="Religion">Religion</option>
            <!-- Agregar más materias según sea necesario -->
        </select>

        <label for="nota">Nota:</label>
        <input type="number" id="nota" min="1" max="5" step="0.1" required>

        <button type="button" onclick="guardarNota()">Guardar Nota</button>
    </form>

    <h2>Registro Academico</h2>
    <table>
        <thead>
            <tr>
                <th>Nombre del Estudiante</th>
                <th>Grado</th>
                <th>Materia</th>
                <th>Nota</th>
            </tr>
        </thead>
        <tbody id="cuerpoTabla">
            <!-- Aquí se agregarán las filas de la tabla dinámicamente -->
        </tbody>
    </table>

    <script>
        function guardarNota() {
            var nombreEstudiante = document.getElementById("nombreEstudiante").value;
            var grado = document.getElementById("grado").value;
            var materia = document.getElementById("materia").value;
            var nota = document.getElementById("nota").value;

            // Crear una nueva fila de tabla para mostrar la nota guardada
            var fila = document.createElement("tr");
            var celdaNombre = document.createElement("td");
            celdaNombre.textContent = nombreEstudiante;
            var celdaGrado = document.createElement("td");
            celdaGrado.textContent = grado;
            var celdaMateria = document.createElement("td");
            celdaMateria.textContent = materia;
            var celdaNota = document.createElement("td");
            celdaNota.textContent = nota;

            // Agregar las celdas a la fila
            fila.appendChild(celdaNombre);
            fila.appendChild(celdaGrado);
            fila.appendChild(celdaMateria);
            fila.appendChild(celdaNota);

            // Agregar la fila a la tabla
            document.getElementById("cuerpoTabla").appendChild(fila);
        }
    </script>
</body>
