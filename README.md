<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Matriz Iónica Interactiva</title>
    <style>
        /* Estilo general */
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #f0f4f7, #d9e6f3);
            text-align: center;
            color: #333;
        }

        h1 {
            margin-top: 20px;
            font-size: 2.5rem;
            color: #2c3e50;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }

        p {
            margin: 10px 0 30px;
            font-size: 1.2rem;
        }

        /* Estilo de la tabla */
        table {
            margin: 0 auto;
            border-collapse: collapse;
            width: 90%;
            max-width: 1000px;
            background-color: #ffffff;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
            border-radius: 10px;
            overflow: hidden;
        }

        th, td {
            border: 1px solid #ddd;
            padding: 15px;
            text-align: center;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        th {
            background-color: #2c3e50;
            color: white;
            font-size: 1.2rem;
            text-transform: uppercase;
        }

        td {
            cursor: pointer;
            background-color: #f9f9f9;
        }

        td:hover {
            background-color: #e6f7ff;
            transform: scale(1.05);
        }

        /* Modal estilos */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background: white;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
            width: 90%;
            max-width: 400px;
            animation: fadeIn 0.4s ease-out;
        }

        .modal-content h2 {
            font-size: 2rem;
            margin-bottom: 10px;
            color: #34495e;
        }

        .modal-content p {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: #7f8c8d;
        }

        .close-btn {
            background: #2c3e50;
            color: white;
            padding: 10px 20px;
            font-size: 1rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s ease;
        }

        .close-btn:hover {
            background: #34495e;
        }

        /* Animaciones */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: scale(0.9);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }
    </style>
</head>
<body>
    <h1>Matriz Iónica Equipo 6</h1>
<p align=centre>3IV4</p>
<p align=centre>Alfonso Sanchez Fernanda</p>
<p align=centre>Hernandez Alvarado Christofer Donovan</p>
<p align=centre>Sanchez Baes Cristal Adriana</p>
<p align=centre>Sanchez Carreon Debani Quetzalli</p>
<p align=centre>Sanchez Garcia Daniel</p>
<p align=centre>Yañez Hernandez Kendra Yaham</p>
    <p>Haga clic en una celda para obtener la fórmula y el nombre químico.</p>
    <table>
        <tr>
            <th></th>
            <th>H⁻¹</th>
            <th>O⁻²</th>
            <th>(OH)⁻¹</th>
            <th>(CO₃)⁻²</th>
            <th>(AsO₃)⁻³</th>
            <th>(CN)⁻¹</th>
            <th>(ClO₃)⁻¹</th>
        </tr>
        <tr>
            <td>H⁺¹</td>
            <td onclick="showModal('H₂', 'Hidruro de hidrógeno')"></td>
            <td onclick="showModal('H₂O', 'Agua')"></td>
            <td onclick="showModal('H₂O', 'Agua')"></td>
            <td onclick="showModal('H₂CO₃', 'Ácido carbónico')"></td>
            <td onclick="showModal('H₃AsO₃', 'Ácido arsenioso')"></td>
            <td onclick="showModal('HCN', 'Ácido cianhídrico')"></td>
            <td onclick="showModal('HClO₃', 'Ácido clórico')"></td>
        </tr>
        <tr>
            <td>Li⁺¹</td>
            <td onclick="showModal('LiH', 'Hidruro de litio')"></td>
            <td onclick="showModal('Li₂O', 'Óxido de litio')"></td>
            <td onclick="showModal('LiOH', 'Hidróxido de litio')"></td>
            <td onclick="showModal('Li₂CO₃', 'Carbonato de litio')"></td>
            <td onclick="showModal('Li₃AsO₃', 'Arsenito de litio')"></td>
            <td onclick="showModal('LiCN', 'Cianuro de litio')"></td>
            <td onclick="showModal('LiClO₃', 'Clorato de litio')"></td>
        </tr>
        <tr>
            <td>Ca⁺²</td>
            <td onclick="showModal('CaH₂', 'Hidruro de calcio')"></td>
            <td onclick="showModal('CaO', 'Óxido de calcio')"></td>
            <td onclick="showModal('Ca(OH)₂', 'Hidróxido de calcio')"></td>
            <td onclick="showModal('CaCO₃', 'Carbonato de calcio')"></td>
            <td onclick="showModal('Ca₃(AsO₃)₂', 'Arsenito de calcio')"></td>
            <td onclick="showModal('Ca(CN)₂', 'Cianuro de calcio')"></td>
            <td onclick="showModal('Ca(ClO₃)₂', 'Clorato de calcio')"></td>
        </tr>
        <tr>
            <td>Co⁺³</td>
            <td onclick="showModal('CoH₃', 'Hidruro de cobalto (III)')"></td>
            <td onclick="showModal('Co₂O₃', 'Óxido de cobalto (III)')"></td>
            <td onclick="showModal('Co(OH)₃', 'Hidróxido de cobalto (III)')"></td>
            <td onclick="showModal('Co₂(CO₃)₃', 'Carbonato de cobalto (III)')"></td>
            <td onclick="showModal('CoAsO₃', 'Arsenito de cobalto (III)')"></td>
            <td onclick="showModal('Co(CN)₃', 'Cianuro de cobalto (III)')"></td>
            <td onclick="showModal('Co(ClO₃)₃', 'Clorato de cobalto (III)')"></td>
        </tr>
         <tr>
            <td>V⁺⁴</td>
            <td onclick="showModal('VH₄', 'Hidruro de vanadio (IV)')"></td>
            <td onclick="showModal('VO₂', 'Óxido de vanadio (IV)')"></td>
            <td onclick="showModal('V(OH)₄', 'Hidróxido de vanadio (IV)')"></td>
            <td onclick="showModal('V(CO₃)₂', 'Carbonato de vanadio (IV)')"></td>
            <td onclick="showModal('V(AsO₃)₂', 'Arsenito de vanadio (IV)')"></td>
            <td onclick="showModal('V(CN)₄', 'Cianuro de vanadio (IV)')"></td>
            <td onclick="showModal('V(ClO₃)₄', 'Clorato de vanadio (IV)')"></td>
        </tr>
          <tr>
            <td>Au⁺³</td>
            <td onclick="showModal('AuH₃', 'Hidruro de oro (III)')"></td>
            <td onclick="showModal('Au₂O₃', 'Óxido de oro (III)')"></td>
            <td onclick="showModal('Au(OH)₃', 'Hidróxido de oro (III)')"></td>
            <td onclick="showModal('Au₂(CO₃)₃', 'Carbonato de oro (III)')"></td>
            <td onclick="showModal('AuAsO₃', 'Arsenito de oro (III)')"></td>
            <td onclick="showModal('Au(CN)₃', 'Cianuro de oro (III)')"></td>
            <td onclick="showModal('Au(ClO₃)₃', 'Clorato de oro (III)')"></td>
        </tr>
         <tr>
            <td>Ag⁺¹</td>
            <td onclick="showModal('AgH', 'Hidruro de plata')"></td>
            <td onclick="showModal('Ag₂O', 'Óxido de plata')"></td>
            <td onclick="showModal('AgOH', 'Hidróxido de plata')"></td>
            <td onclick="showModal('Ag₂CO₃', 'Carbonato de plata')"></td>
            <td onclick="showModal('Ag₃AsO₃', 'Arsenito de plata')"></td>
            <td onclick="showModal('AgCN', 'Cianuro de plata')"></td>
            <td onclick="showModal('AgClO₃', 'Clorato de plata')"></td>
        </tr>
    </table>

    <!-- Modal -->
    <div class="modal" id="infoModal">
        <div class="modal-content">
            <h2 id="formula"></h2>
            <p id="name"></p>
            <button class="close-btn" onclick="closeModal()">Cerrar</button>
        </div>
    </div>

    <script>
        // Función para mostrar el modal
        function showModal(formula, name) {
            document.getElementById('formula').textContent = formula;
            document.getElementById('name').textContent = name;
            document.getElementById('infoModal').style.display = 'flex';
        }

        // Función para cerrar el modal
        function closeModal() {
            document.getElementById('infoModal').style.display = 'none';
        }
    </script>
</body>
</html>
