<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reportes de Producto Mal Estado</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/sweetalert2@11/dist/sweetalert2.min.css">
    <script src="https://www.gstatic.com/firebasejs/9.6.0/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.6.0/firebase-firestore-compat.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf-autotable/3.5.28/jspdf.plugin.autotable.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>
    <style>
        :root {
            --primary: #4361ee;
            --primary-hover: #3a56d4;
            --secondary: #3f37c9;
            --accent: #4895ef;
            --dark: #1b263b;
            --light: #f8f9fa;
            --card-bg: #ffffff;
            --text: #2b2d42;
            --text-light: #8d99ae;
            --danger: #fc0303;
            --warning: #fc7703;
            --success: #03fc41;
            --border-radius: 8px;
            --shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            --transition: all 0.2s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--light);
            color: var(--text);
            padding: 1rem;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            width: 100%;
        }

        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid rgba(0, 0, 0, 0.1);
        }

        .header-title {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .header-title h1 {
            font-size: 1.5rem;
            color: var(--dark);
        }

        .header-actions {
            display: flex;
            gap: 0.5rem;
        }

        .search-container {
            margin-bottom: 1.5rem;
            display: flex;
            gap: 1rem;
        }

        .search-input {
            flex: 1;
            padding: 0.75rem;
            border: 1px solid rgba(0, 0, 0, 0.1);
            border-radius: var(--border-radius);
            font-size: 0.95rem;
        }

        .search-btn {
            background: var(--primary);
            color: white;
            border: none;
            padding: 0 1.5rem;
            border-radius: var(--border-radius);
            cursor: pointer;
            transition: var(--transition);
        }

        .search-btn:hover {
            background: var(--primary-hover);
        }

        .btn {
            background: var(--primary);
            color: white;
            border: none;
            padding: 0.8rem 1rem;
            border-radius: var(--border-radius);
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: var(--transition);
            font-size: 0.9rem;
        }

        .btn:hover {
            background: var(--primary-hover);
        }

        .btn-danger {
            background: var(--danger);
        }

        .btn-success {
            background: var(--primary);
        }

        .btn-pdf {
            background: #e74c3c;
        }

        .btn-warning {
            background: var(--warning);
        }

        .btn-secondary {
            background: var(--secondary);
        }

        .return-form {
            background: var(--card-bg);
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            padding: 1.5rem;
            margin-bottom: 2rem;
            display: none;
        }

        .form-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .form-header h2 {
            font-size: 1.3rem;
            color: var(--dark);
        }

        .form-header-actions {
            display: flex;
            gap: 0.8rem;
            align-items: center;
        }

        .form-row {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.2rem;
            margin-bottom: 1.2rem;
        }

        .invoice-fields {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.2rem;
            margin-bottom: 1.2rem;
        }
        
        .invoice-fields .form-group label {
            font-size: 0.9rem;
            color: var(--text-light);
        }
        
        .invoice-fields .form-control {
            font-size: 0.95rem;
            padding: 0.7rem;
        }

        .form-group {
            margin-bottom: 1.2rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.6rem;
            font-weight: 500;
            font-size: 0.95rem;
        }

        .form-control {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid rgba(0, 0, 0, 0.1);
            border-radius: var(--border-radius);
            font-size: 1rem;
            text-transform: uppercase;
        }

        textarea.form-control {
            min-height: 50px;
            resize: vertical;
            font-size: 0.95rem;
            text-transform: none;
        }

        .products-table {
            width: 100%;
            border-collapse: collapse;
            margin: 1.2rem 0;
            background: var(--card-bg);
            box-shadow: var(--shadow);
            border-radius: var(--border-radius);
            overflow: hidden;
        }

        .products-table th {
            background-color: var(--primary);
            color: white;
            padding: 0.9rem;
            text-align: left;
            font-size: 0.95rem;
        }

        .products-table td {
            padding: 0.7rem;
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            font-size: 0.95rem;
        }

        .products-table tr:last-child td {
            border-bottom: none;
        }

        .products-table input[type="text"] {
            width: 100%;
            padding: 0.7rem;
            border: 1px solid rgba(0, 0, 0, 0.1);
            border-radius: 4px;
            font-size: 1rem;
            text-transform: uppercase;
        }

        .products-table input[type="number"] {
            width: 100%;
            padding: 0.7rem;
            border: 1px solid rgba(0, 0, 0, 0.1);
            border-radius: 4px;
            font-size: 1rem;
        }

        .products-table input.code-input {
            width: 100px;
            font-family: monospace;
            letter-spacing: 1px;
            padding: 0.7rem;
        }

        .product-status {
            width: 15px;
            height: 15px;
            border-radius: 50%;
            display: inline-block;
            margin-right: 5px;
            cursor: pointer;
        }

        .status-pending {
            background-color: var(--warning);
        }

        .status-received {
            background-color: var(--success);
        }

        .status-cancelled {
            background-color: var(--danger);
        }

        .status-date {
            font-size: 0.8rem;
            color: var(--text-light);
            display: block;
            margin-top: 2px;
        }

        .status-cell {
            cursor: pointer;
            position: relative;
        }

        .add-row-btn {
            margin-top: 0.8rem;
            background: var(--accent);
            font-size: 0.9rem;
            padding: 0.7rem 1rem;
        }

        .reports-list {
            display: grid;
            gap: 1.2rem;
        }

        .report-card {
            background: var(--card-bg);
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            padding: 1.5rem;
        }

        .report-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.2rem;
            padding-bottom: 0.8rem;
            border-bottom: 1px solid rgba(0, 0, 0, 0.1);
        }

        .report-id {
            font-weight: 700;
            color: var(--primary);
            background: rgba(67, 97, 238, 0.1);
            padding: 0.4rem 0.8rem;
            border-radius: 4px;
            font-size: 0.95rem;
        }

        .report-date {
            color: var(--text-light);
            font-size: 0.9rem;
        }

        .report-supplier {
            font-weight: 600;
            margin-bottom: 0.7rem;
            font-size: 1rem;
        }

        .report-notes {
            color: var(--text-light);
            margin-bottom: 1.2rem;
            font-size: 0.95rem;
            max-height: 60px;
            overflow-y: auto;
        }

        .report-products {
            width: 100%;
            border-collapse: collapse;
            margin-top: 0.8rem;
            font-size: 0.95rem;
        }

        .report-products th {
            background-color: rgba(0, 0, 0, 0.05);
            padding: 0.7rem;
            text-align: left;
            font-weight: 500;
            font-size: 0.9rem;
        }

        .report-products td {
            padding: 0.7rem;
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            font-size: 0.9rem;
        }

        .report-products tr:last-child td {
            border-bottom: none;
        }

        .report-actions {
            display: flex;
            gap: 0.8rem;
            margin-top: 1.2rem;
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            z-index: 1000;
            justify-content: center;
            align-items: center;
            padding: 1.5rem;
        }

        .modal-content {
            background: white;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            width: 100%;
            max-width: 850px;
            max-height: 90vh;
            overflow-y: auto;
            padding: 1.5rem;
            position: relative;
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.2rem;
        }

        .modal-header h2 {
            font-size: 1.4rem;
        }

        .modal-body .form-group {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
        }

        .modal-body .form-group label {
            min-width: 140px;
            margin-bottom: 0;
            font-size: 0.95rem;
        }

        .modal-body .form-control {
            flex: 1;
            padding: 0.7rem;
            font-size: 0.95rem;
        }

        @media (max-width: 768px) {
            .form-row, .invoice-fields {
                grid-template-columns: 1fr;
            }
            
            .products-table {
                display: block;
                overflow-x: auto;
            }
            
            .report-header {
                flex-direction: column;
                align-items: flex-start;
                gap: 0.8rem;
            }
            
            .report-actions {
                flex-direction: column;
                gap: 0.8rem;
            }

            .form-header {
                flex-direction: column;
                align-items: flex-start;
                gap: 0.8rem;
            }

            .form-header-actions {
                width: 100%;
                justify-content: flex-end;
            }

            .search-container {
                flex-direction: column;
            }

            .search-btn {
                padding: 0.8rem;
            }

            .modal-body .form-group {
                flex-direction: column;
                align-items: flex-start;
            }

            .modal-body .form-group label {
                min-width: auto;
                margin-bottom: 0.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="header-title">
                <i class="fas fa-exclamation-triangle"></i>
                <h1>Reportes de Producto Mal Estado</h1>
            </div>
            <div class="header-actions">
                <button class="btn" id="newReportBtn">
                    <i class="fas fa-plus"></i>
                    Nueva Devolución
                </button>
            </div>
        </header>

        <!-- Buscador -->
        <div class="search-container" id="searchContainer">
            <input type="text" class="search-input" id="searchInput" placeholder="Buscar por número de reporte o fecha...">
            <button class="search-btn" id="searchBtn">
                <i class="fas fa-search"></i>
            </button>
        </div>

        <!-- Formulario de nueva devolución -->
        <div class="return-form" id="returnForm">
            <div class="form-header">
                <h2><i class="fas fa-file-alt"></i> Nueva Devolución</h2>
                <div class="form-header-actions">
                    <button class="btn btn-danger" id="cancelReportBtn">
                        <i class="fas fa-times"></i>
                        Cancelar
                    </button>
                    <button class="btn btn-success" id="saveReportBtn">
                        <i class="fas fa-save"></i>
                        Guardar
                    </button>
                    <div class="report-id">Registro <span id="reportNumber">--</span></div>
                </div>
            </div>
            
            <div class="form-row">
                <div class="form-group">
                    <label for="supplier">Proveedor</label>
                    <input type="text" class="form-control" id="supplier" required>
                </div>
                <div class="form-group">
                    <label for="reportDate">Fecha</label>
                    <input type="date" class="form-control" id="reportDate" required>
                </div>
            </div>
            
            <div class="invoice-fields">
                <div class="form-group">
                    <label for="invoiceNumber">Número de Factura (Opcional)</label>
                    <input type="text" class="form-control" id="invoiceNumber" placeholder="Ingrese número">
                </div>
                <div class="form-group">
                    <label for="invoiceSeries">Serie de Factura (Opcional)</label>
                    <input type="text" class="form-control" id="invoiceSeries" placeholder="Ingrese serie">
                </div>
            </div>
            
            <div class="form-group">
                <label for="notes">Observaciones (Opcional)</label>
                <textarea class="form-control" id="notes" style="min-height: 50px;"></textarea>
            </div>
            
            <h3 style="margin: 1.2rem 0 0.8rem; font-size: 1.15rem;">Productos en mal estado</h3>
            
            <table class="products-table" id="productsTable">
                <thead>
                    <tr>
                        <th>Sku</th>
                        <th>Cód. Fábrica</th>
                        <th>Descripción</th>
                        <th style="width: 90px;">Cantidad</th>
                        <th style="width: 140px;">Motivo</th>
                        <th style="width: 60px;"></th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><input type="text" class="code-input" placeholder="Sku" maxlength="9"></td>
                        <td><input type="text" placeholder="Cód. Fábrica"></td>
                        <td><input type="text" placeholder="Descripción"></td>
                        <td><input type="number" placeholder="0" min="1"></td>
                        <td><input type="text" placeholder="Ej: Quebrado"></td>
                        <td style="text-align: center;"><i class="fas fa-trash-alt" style="color: var(--danger); cursor: pointer;"></i></td>
                    </tr>
                </tbody>
            </table>
            
            <button class="btn add-row-btn" id="addRowBtn">
                <i class="fas fa-plus"></i>
                Agregar Producto
            </button>
        </div>

        <!-- Lista de reportes -->
        <div class="reports-list" id="reportsList">
            <div class="no-reports" style="text-align: center; padding: 2.5rem; color: var(--text-light);">
                <i class="fas fa-box-open" style="font-size: 2.5rem; margin-bottom: 1.2rem; opacity: 0.5;"></i>
                <h3>No hay reportes registrados</h3>
                <p>Haz clic en "Nueva Devolución" para crear tu primer reporte</p>
            </div>
        </div>
    </div>

    <!-- Modal para ver reporte completo -->
    <div class="modal" id="reportModal">
        <div class="modal-content">
            <div class="modal-header">
                <h2><i class="fas fa-file-alt"></i> Detalle de Reporte</h2>
                <button onclick="window.closeModal()" style="background: none; border: none; cursor: pointer; font-size: 1.5rem;">&times;</button>
            </div>
            <div class="modal-body" id="modalReportContent">
                <!-- Contenido del reporte se cargará aquí -->
            </div>
            <div class="report-actions" id="modalReportActions">
                <!-- Acciones del reporte se cargarán aquí -->
            </div>
        </div>
    </div>

    <script>
        // Configuración de Firebase
        const firebaseConfig = {
            apiKey: "AIzaSyCefeYE1rHVxumOYyi311IMIg4vuqujC00",
            authDomain: "inventario-productos-fal-dfb1d.firebaseapp.com",
            projectId: "inventario-productos-fal-dfb1d",
            storageBucket: "inventario-productos-fal-dfb1d.appspot.com",
            messagingSenderId: "164587710116",
            appId: "1:164587710116:web:c1a1e3bb8327dbadf76831",
            measurementId: "G-JGVLWTF44G"
        };

        // Inicializa Firebase
        firebase.initializeApp(firebaseConfig);
        const db = firebase.firestore();
        const { jsPDF } = window.jspdf;

        // Datos de la aplicación
        let reports = [];
        let currentReportId = null;
        let reportCounter = 0;
        let isCreatingNewReport = false;
        const companyName = "MACAAL S.A";
        const companyLogo = new Image();
        companyLogo.src = 'images/logo/logo.png';

        // Función para cerrar modal (ahora está en el ámbito global)
        window.closeModal = function() {
            document.getElementById('reportModal').style.display = 'none';
            document.body.style.overflow = '';
        };

        document.addEventListener('DOMContentLoaded', () => {
            // Elementos del DOM
            const newReportBtn = document.getElementById('newReportBtn');
            const returnForm = document.getElementById('returnForm');
            const cancelReportBtn = document.getElementById('cancelReportBtn');
            const saveReportBtn = document.getElementById('saveReportBtn');
            const addRowBtn = document.getElementById('addRowBtn');
            const productsTable = document.getElementById('productsTable');
            const reportsList = document.getElementById('reportsList');
            const reportModal = document.getElementById('reportModal');
            const modalReportContent = document.getElementById('modalReportContent');
            const modalReportActions = document.getElementById('modalReportActions');
            const reportNumberSpan = document.getElementById('reportNumber');
            const supplierInput = document.getElementById('supplier');
            const reportDateInput = document.getElementById('reportDate');
            const invoiceNumberInput = document.getElementById('invoiceNumber');
            const invoiceSeriesInput = document.getElementById('invoiceSeries');
            const notesInput = document.getElementById('notes');
            const searchInput = document.getElementById('searchInput');
            const searchBtn = document.getElementById('searchBtn');
            const searchContainer = document.getElementById('searchContainer');
            const headerActions = document.querySelector('.header-actions');

            // Mostrar alerta de confirmación con SweetAlert
            function showConfirmAlert(title, text, confirmButtonText) {
                return Swal.fire({
                    title: title,
                    text: text,
                    icon: 'warning',
                    showCancelButton: true,
                    confirmButtonColor: '#3085d6',
                    cancelButtonColor: '#d33',
                    confirmButtonText: confirmButtonText || 'Confirmar',
                    cancelButtonText: 'Cancelar'
                });
            }

            // Mostrar alerta de éxito
            function showSuccessAlert(title, text) {
                return Swal.fire({
                    title: title,
                    text: text,
                    icon: 'success',
                    confirmButtonColor: '#3085d6'
                });
            }

            // Mostrar alerta de error
            function showErrorAlert(title, text) {
                return Swal.fire({
                    title: title,
                    text: text,
                    icon: 'error',
                    confirmButtonColor: '#3085d6'
                });
            }

            // Mostrar alerta de validación
            function showValidationAlert(message) {
                return Swal.fire({
                    title: 'Validación requerida',
                    text: message,
                    icon: 'info',
                    confirmButtonColor: '#3085d6'
                });
            }

            // Convertir texto a mayúsculas
            function toUpperCase(text) {
                return text ? text.toUpperCase() : '';
            }

            // Generar número de reporte consecutivo basado en el último existente
            async function generateReportNumber() {
                try {
                    const snapshot = await db.collection("reportesMalEstado")
                        .orderBy("reportNumber", "desc")
                        .limit(1)
                        .get();
                    
                    if (!snapshot.empty) {
                        const lastReport = snapshot.docs[0].data();
                        reportCounter = lastReport.reportNumber;
                    }
                    
                    reportCounter++;
                    return reportCounter.toString(); // Solo el número, sin #
                } catch (error) {
                    console.error("Error al obtener último reporte:", error);
                    reportCounter++;
                    return reportCounter.toString(); // Solo el número, sin #
                }
            }

            // Mostrar formulario de nueva devolución
            async function showNewReportForm() {
                if (isCreatingNewReport) {
                    showErrorAlert('Operación en curso', 'Ya tienes una devolución en proceso. Termina o cancela la actual antes de crear una nueva.');
                    return;
                }

                currentReportId = await generateReportNumber();
                reportNumberSpan.textContent = currentReportId;
                
                // Establecer fecha actual
                const today = new Date().toISOString().split('T')[0];
                reportDateInput.value = today;
                
                // Limpiar campos
                supplierInput.value = '';
                invoiceNumberInput.value = '';
                invoiceSeriesInput.value = '';
                notesInput.value = '';
                
                // Limpiar tabla de productos (dejar solo una fila vacía)
                const tbody = productsTable.querySelector('tbody');
                tbody.innerHTML = `
                    <tr>
                        <td><input type="text" class="code-input" placeholder="Sku" maxlength="9"></td>
                        <td><input type="text" placeholder="Cód. Fábrica"></td>
                        <td><input type="text" placeholder="Descripción"></td>
                        <td><input type="number" placeholder="0" min="1"></td>
                        <td><input type="text" placeholder="Ej: Quebrado"></td>
                        <td style="text-align: center;"><i class="fas fa-trash-alt" style="color: var(--danger); cursor: pointer;"></i></td>
                    </tr>
                `;
                
                // Restaurar texto del botón de guardar
                saveReportBtn.innerHTML = '<i class="fas fa-save"></i> Guardar';
                
                // Agregar event listeners a los botones de eliminar
                addDeleteRowListeners();
                
                // Ocultar elementos
                reportsList.style.display = 'none';
                searchContainer.style.display = 'none';
                headerActions.style.display = 'none';
                
                // Mostrar el formulario
                returnForm.style.display = 'block';
                
                // Marcar que estamos creando un nuevo reporte
                isCreatingNewReport = true;
            }

            // Ocultar formulario de devolución
            function hideReturnForm() {
                returnForm.style.display = 'none';
                reportsList.style.display = 'grid';
                searchContainer.style.display = 'flex';
                headerActions.style.display = 'flex';
                isCreatingNewReport = false;
            }

            // Agregar nueva fila a la tabla de productos
            function addProductRow() {
                const tbody = productsTable.querySelector('tbody');
                const newRow = document.createElement('tr');
                newRow.innerHTML = `
                    <td><input type="text" class="code-input" placeholder="Sku" maxlength="9"></td>
                    <td><input type="text" placeholder="Cód. Fábrica"></td>
                    <td><input type="text" placeholder="Descripción"></td>
                    <td><input type="number" placeholder="0" min="1"></td>
                    <td><input type="text" placeholder="Ej: Quebrado"></td>
                    <td style="text-align: center;"><i class="fas fa-trash-alt" style="color: var(--danger); cursor: pointer;"></i></td>
                `;
                tbody.appendChild(newRow);
                
                // Agregar event listener al botón de eliminar
                const deleteBtn = newRow.querySelector('.fa-trash-alt');
                deleteBtn.addEventListener('click', () => {
                    if (tbody.childElementCount > 1) {
                        tbody.removeChild(newRow);
                    } else {
                        // Si es la última fila, limpiar los campos
                        const inputs = newRow.querySelectorAll('input');
                        inputs.forEach(input => input.value = '');
                    }
                });
            }

            // Agregar event listeners a los botones de eliminar fila
            function addDeleteRowListeners() {
                const deleteBtns = productsTable.querySelectorAll('.fa-trash-alt');
                const tbody = productsTable.querySelector('tbody');
                
                deleteBtns.forEach(btn => {
                    btn.addEventListener('click', (e) => {
                        const row = e.target.closest('tr');
                        if (tbody.childElementCount > 1) {
                            tbody.removeChild(row);
                        } else {
                            // Si es la última fila, limpiar los campos
                            const inputs = row.querySelectorAll('input');
                            inputs.forEach(input => input.value = '');
                        }
                    });
                });
            }

            // Obtener productos de la tabla
            function getProductsFromTable() {
                const products = [];
                const rows = productsTable.querySelectorAll('tbody tr');
                
                rows.forEach(row => {
                    const inputs = row.querySelectorAll('input');
                    const sku = toUpperCase(inputs[0].value.trim());
                    const factoryCode = toUpperCase(inputs[1].value.trim()) || '-';
                    const description = toUpperCase(inputs[2].value.trim());
                    const quantity = inputs[3].value.trim();
                    const reason = toUpperCase(inputs[4].value.trim());
                    
                    if (sku && description && quantity && reason) {
                        products.push({
                            sku: sku,
                            factoryCode: factoryCode,
                            description: description,
                            quantity: parseInt(quantity),
                            reason: reason,
                            status: 'pending',
                            receivedDate: null
                        });
                    }
                });
                
                return products;
            }

            // Validar formulario
            function validateForm() {
                if (!supplierInput.value.trim()) {
                    showValidationAlert('Por favor ingresa el nombre del proveedor');
                    return false;
                }
                
                const products = getProductsFromTable();
                if (products.length === 0) {
                    showValidationAlert('Debes agregar al menos un producto');
                    return false;
                }
                
                return true;
            }

            // Guardar reporte en Firebase
            async function saveReport() {
                if (!validateForm()) return;
                
                const reportData = {
                    id: currentReportId,
                    supplier: toUpperCase(supplierInput.value.trim()),
                    date: reportDateInput.value,
                    invoiceNumber: invoiceNumberInput.value.trim() || 'XXXXX',
                    invoiceSeries: invoiceSeriesInput.value.trim() || 'XXXXX',
                    notes: notesInput.value.trim(), // Notas se mantienen como se escriben
                    products: getProductsFromTable(),
                    updatedAt: firebase.firestore.FieldValue.serverTimestamp(),
                    reportNumber: parseInt(currentReportId) // Guardamos como número
                };
                
                // Verificar si estamos editando o creando nuevo
                const isEditing = saveReportBtn.innerHTML.includes('Actualizar');
                
                if (isEditing) {
                    // Mantener los datos existentes que no se editan
                    const originalReport = reports.find(r => r.id === currentReportId);
                    if (originalReport) {
                        reportData.status = originalReport.status;
                        reportData.createdAt = originalReport.createdAt;
                        reportData.reportNumber = originalReport.reportNumber;
                        
                        // Mantener el estado de los productos
                        reportData.products.forEach((product, index) => {
                            if (originalReport.products && originalReport.products[index]) {
                                product.status = originalReport.products[index].status;
                                product.receivedDate = originalReport.products[index].receivedDate;
                            } else {
                                product.status = 'pending';
                                product.receivedDate = null;
                            }
                        });
                    }
                    
                    db.collection("reportesMalEstado").doc(currentReportId)
                        .update(reportData)
                        .then(() => {
                            showSuccessAlert('Reporte actualizado', 'El reporte se ha actualizado correctamente')
                                .then(() => {
                                    hideReturnForm();
                                    loadReports();
                                });
                        })
                        .catch(error => {
                            console.error("Error al actualizar el reporte:", error);
                            showErrorAlert('Error', 'Ocurrió un error al actualizar el reporte');
                        });
                } else {
                    // Es un nuevo reporte
                    reportData.createdAt = firebase.firestore.FieldValue.serverTimestamp();
                    reportData.status = 'active';
                    
                    // Establecer estado inicial de los productos
                    reportData.products.forEach(product => {
                        product.status = 'pending';
                        product.receivedDate = null;
                    });
                    
                    db.collection("reportesMalEstado").doc(currentReportId)
                        .set(reportData)
                        .then(() => {
                            showSuccessAlert('Reporte guardado', 'El reporte se ha guardado correctamente')
                                .then(() => {
                                    hideReturnForm();
                                    loadReports();
                                });
                        })
                        .catch(error => {
                            console.error("Error al guardar el reporte:", error);
                            showErrorAlert('Error', 'Ocurrió un error al guardar el reporte');
                        });
                }
            }

            // Buscar reportes
            function searchReports() {
                const searchTerm = searchInput.value.trim().toLowerCase();
                
                if (searchTerm === '') {
                    loadReports();
                    return;
                }
                
                // Buscar por número de reporte o fecha
                const filteredReports = reports.filter(report => {
                    return report.id.toLowerCase().includes(searchTerm) || 
                           formatDate(report.date).toLowerCase().includes(searchTerm);
                });
                
                renderReportsList(filteredReports);
            }

            // Cargar reportes desde Firebase
            function loadReports() {
                db.collection("reportesMalEstado")
                    .orderBy("createdAt", "desc")
                    .get()
                    .then(querySnapshot => {
                        reports = [];
                        querySnapshot.forEach(doc => {
                            const data = doc.data();
                            // Asegurarse de que todos los productos tengan status
                            if (data.products) {
                                data.products.forEach(product => {
                                    if (!product.status) {
                                        product.status = 'pending';
                                    }
                                    if (!product.receivedDate && product.status === 'received') {
                                        product.receivedDate = new Date().toISOString();
                                    }
                                    // Asegurar que todos los productos tengan código
                                    if (!product.sku) {
                                        product.sku = '';
                                    }
                                    if (!product.factoryCode) {
                                        product.factoryCode = '-';
                                    }
                                });
                            }
                            // Asegurar que existan los campos de factura
                            if (!data.invoiceNumber) {
                                data.invoiceNumber = 'XXXXX';
                            }
                            if (!data.invoiceSeries) {
                                data.invoiceSeries = 'XXXXX';
                            }
                            reports.push(data);
                        });
                        
                        renderReportsList(reports);
                    })
                    .catch(error => {
                        console.error("Error al cargar reportes:", error);
                        showErrorAlert('Error', 'Ocurrió un error al cargar los reportes');
                    });
            }

            // Mostrar lista de reportes
            function renderReportsList(reportsToRender = reports) {
                if (reportsToRender.length === 0) {
                    reportsList.innerHTML = `
                        <div class="no-reports" style="text-align: center; padding: 2.5rem; color: var(--text-light);">
                            <i class="fas fa-box-open" style="font-size: 2.5rem; margin-bottom: 1.2rem; opacity: 0.5;"></i>
                            <h3>No se encontraron reportes</h3>
                            <p>No hay reportes que coincidan con tu búsqueda</p>
                        </div>
                    `;
                    return;
                }
                
                reportsList.innerHTML = '';
                
                reportsToRender.forEach(report => {
                    const reportCard = document.createElement('div');
                    reportCard.className = 'report-card';
                    
                    // Contar productos recibidos
                    const receivedCount = report.products ? report.products.filter(p => p.status === 'received').length : 0;
                    const totalCount = report.products ? report.products.length : 0;
                    
                    reportCard.innerHTML = `
                        <div class="report-header">
                            <div>
                                <span class="report-id">${report.id}</span>
                                <span class="report-date">${formatDate(report.date)}</span>
                                <div style="margin-top: 0.3rem; font-size: 0.9rem; color: ${report.status === 'cancelled' ? 'var(--danger)' : receivedCount === totalCount ? 'var(--success)' : 'var(--warning)'}">
                                    ${report.status === 'cancelled' ? 'ANULADO' : `${receivedCount}/${totalCount} productos recibidos`}
                                </div>
                            </div>
                            <div style="display: flex; gap: 0.8rem;">
                                <button class="btn" onclick="viewReport('${report.id}')">
                                    <i class="fas fa-eye"></i> Ver
                                </button>
                                <button class="btn btn-pdf" onclick="generatePDF('${report.id}')">
                                    <i class="fas fa-file-pdf"></i> PDF
                                </button>
                                ${report.status === 'active' ? `
                                <button class="btn btn-danger" onclick="cancelReport('${report.id}')">
                                    <i class="fas fa-ban"></i> Anular
                                </button>
                                ` : ''}
                                ${report.status === 'active' ? `
                                <button class="btn btn-secondary" onclick="editReport('${report.id}')">
                                    <i class="fas fa-edit"></i> Editar
                                </button>
                                ` : ''}
                            </div>
                        </div>
                        <div class="report-supplier">Proveedor: ${report.supplier}</div>
                        ${report.notes ? `<div class="report-notes">Observaciones: ${report.notes}</div>` : ''}
                        <table class="report-products">
                            <thead>
                                <tr>
                                    <th>Sku</th>
                                    <th>Cód. Fábrica</th>
                                    <th>Descripción</th>
                                    <th style="width: 70px;">Cantidad</th>
                                    <th style="width: 120px;">Motivo</th>
                                    <th style="width: 110px;">Estado</th>
                                </tr>
                            </thead>
                            <tbody>
                                ${report.products ? report.products.map(product => `
                                    <tr>
                                        <td>${product.sku || ''}</td>
                                        <td>${product.factoryCode || '-'}</td>
                                        <td>${product.description}</td>
                                        <td>${product.quantity}</td>
                                        <td>${product.reason}</td>
                                        <td>
                                            <span class="product-status status-${product.status}"></span>
                                            ${product.status === 'pending' ? 'Pendiente' : product.status === 'received' ? 'Recibido' : 'Anulado'}
                                        </td>
                                    </tr>
                                `).join('') : ''}
                            </tbody>
                        </table>
                    `;
                    
                    reportsList.appendChild(reportCard);
                });
            }

            // Formatear fecha
            function formatDate(dateString) {
                const options = { year: 'numeric', month: 'long', day: 'numeric' };
                return new Date(dateString).toLocaleDateString('es-ES', options);
            }

            // Formatear fecha y hora
            function formatDateTime(dateString) {
                if (!dateString) return 'No especificada';
                const options = { 
                    year: 'numeric', 
                    month: 'long', 
                    day: 'numeric',
                    hour: '2-digit',
                    minute: '2-digit'
                };
                return new Date(dateString).toLocaleDateString('es-ES', options);
            }

            // Anular reporte
            window.cancelReport = function(reportId) {
                showConfirmAlert('¿Anular reporte?', '¿Estás seguro que deseas anular este reporte?', 'Sí, anular')
                    .then((result) => {
                        if (result.isConfirmed) {
                            db.collection("reportesMalEstado").doc(reportId)
                                .update({
                                    status: 'cancelled',
                                    cancelledAt: firebase.firestore.FieldValue.serverTimestamp()
                                })
                                .then(() => {
                                    // Actualizar el estado de todos los productos a 'cancelled'
                                    const report = reports.find(r => r.id === reportId);
                                    if (report && report.products) {
                                        report.products.forEach(product => {
                                            product.status = 'cancelled';
                                        });
                                        return db.collection("reportesMalEstado").doc(reportId)
                                            .update({
                                                products: report.products
                                            });
                                    }
                                    return Promise.resolve();
                                })
                                .then(() => {
                                    showSuccessAlert('Reporte anulado', 'El reporte ha sido anulado correctamente')
                                        .then(() => {
                                            loadReports();
                                            window.closeModal();
                                        });
                                })
                                .catch(error => {
                                    console.error("Error al anular el reporte:", error);
                                    showErrorAlert('Error', 'Ocurrió un error al anular el reporte');
                                });
                        }
                    });
            };

            // Editar reporte
            window.editReport = function(reportId) {
                const report = reports.find(r => r.id === reportId);
                if (!report) return;
                
                if (report.status !== 'active') {
                    showErrorAlert('Error', 'Solo se pueden editar reportes activos');
                    return;
                }

                currentReportId = report.id;
                reportNumberSpan.textContent = report.id;
                
                // Cambiar el texto del botón de guardar
                saveReportBtn.innerHTML = '<i class="fas fa-save"></i> Actualizar';
                
                // Llenar campos del formulario
                supplierInput.value = report.supplier;
                reportDateInput.value = report.date.split('T')[0];
                invoiceNumberInput.value = report.invoiceNumber === 'XXXXX' ? '' : report.invoiceNumber;
                invoiceSeriesInput.value = report.invoiceSeries === 'XXXXX' ? '' : report.invoiceSeries;
                notesInput.value = report.notes || '';
                
                // Llenar tabla de productos
                const tbody = productsTable.querySelector('tbody');
                tbody.innerHTML = '';
                
                report.products.forEach(product => {
                    const newRow = document.createElement('tr');
                    newRow.innerHTML = `
                        <td><input type="text" class="code-input" value="${product.sku || ''}" placeholder="Sku" maxlength="9"></td>
                        <td><input type="text" value="${product.factoryCode || ''}" placeholder="Cód. Fábrica"></td>
                        <td><input type="text" value="${product.description}" placeholder="Descripción"></td>
                        <td><input type="number" value="${product.quantity}" placeholder="0" min="1"></td>
                        <td><input type="text" value="${product.reason}" placeholder="Ej: Quebrado"></td>
                        <td style="text-align: center;"><i class="fas fa-trash-alt" style="color: var(--danger); cursor: pointer;"></i></td>
                    `;
                    tbody.appendChild(newRow);
                });
                
                // Agregar event listeners a los botones de eliminar
                addDeleteRowListeners();
                
                // Ocultar elementos
                reportsList.style.display = 'none';
                searchContainer.style.display = 'none';
                headerActions.style.display = 'none';
                
                // Mostrar el formulario
                returnForm.style.display = 'block';
                
                // Marcar que estamos editando un reporte
                isCreatingNewReport = true;
                
                // Cerrar el modal si está abierto
                window.closeModal();
                
                // Desplazar hasta el formulario
                returnForm.scrollIntoView({ behavior: 'smooth' });
            };

            // Cambiar estado del producto
            window.toggleProductStatus = function(reportId, productIndex, event) {
                if (event) event.stopPropagation(); // Evitar que se propague el evento
                
                const report = reports.find(r => r.id === reportId);
                if (!report || !report.products || !report.products[productIndex] || report.status !== 'active') return;
                
                const product = report.products[productIndex];
                const newStatus = product.status === 'pending' ? 'received' : 'pending';
                
                // Actualizar estado del producto
                product.status = newStatus;
                if (newStatus === 'received') {
                    product.receivedDate = new Date().toISOString();
                } else {
                    product.receivedDate = null;
                }
                
                // Actualizar en Firebase
                db.collection("reportesMalEstado").doc(reportId)
                    .update({
                        products: report.products
                    })
                    .then(() => {
                        // Verificar si todos los productos están recibidos
                        const allReceived = report.products.every(p => p.status === 'received');
                        if (allReceived) {
                            return db.collection("reportesMalEstado").doc(reportId)
                                .update({
                                    status: 'completed',
                                    completedAt: firebase.firestore.FieldValue.serverTimestamp()
                                });
                        } else if (report.status === 'completed') {
                            // Si ya estaba completado pero ahora no todos están recibidos
                            return db.collection("reportesMalEstado").doc(reportId)
                                .update({
                                    status: 'active',
                                    completedAt: firebase.firestore.FieldValue.delete()
                                });
                        }
                        return Promise.resolve();
                    })
                    .then(() => {
                        loadReports();
                        // Volver a abrir el modal para ver los cambios
                        const currentModalReport = reports.find(r => r.id === reportId);
                        if (currentModalReport) {
                            viewReport(reportId);
                        }
                    })
                    .catch(error => {
                        console.error("Error al actualizar el producto:", error);
                        showErrorAlert('Error', 'Ocurrió un error al actualizar el producto');
                    });
            };

            // Ver reporte completo en modal
            window.viewReport = function(reportId) {
                const report = reports.find(r => r.id === reportId);
                if (!report) return;
                
                modalReportContent.innerHTML = `
                    <div class="report-header">
                        <div>
                            <span class="report-id">${report.id}</span>
                            <span class="report-date">${formatDate(report.date)}</span>
                            <div style="margin-top: 0.3rem; font-size: 0.95rem; color: ${report.status === 'cancelled' ? 'var(--danger)' : report.status === 'completed' ? 'var(--success)' : 'var(--warning)'}">
                                Estado: ${report.status === 'active' ? 'Activo' : report.status === 'cancelled' ? 'ANULADO' : 'Completado'}
                                ${report.cancelledAt ? `<span class="status-date">Anulado el: ${formatDateTime(report.cancelledAt.toDate ? report.cancelledAt.toDate().toISOString() : report.cancelledAt)}</span>` : ''}
                                ${report.completedAt ? `<span class="status-date">Completado el: ${formatDateTime(report.completedAt.toDate ? report.completedAt.toDate().toISOString() : report.completedAt)}</span>` : ''}
                            </div>
                        </div>
                    </div>
                    <div class="form-group">
                        <label>Proveedor</label>
                        <div class="form-control" style="background: #f8f9fa;">${report.supplier}</div>
                    </div>
                    <div class="form-group">
                        <label>Fecha de Reporte</label>
                        <div class="form-control" style="background: #f8f9fa;">${formatDate(report.date)}</div>
                    </div>
                    <div class="form-group">
                        <label>Número de Factura</label>
                        <div class="form-control" style="background: #f8f9fa;">${report.invoiceNumber}</div>
                    </div>
                    <div class="form-group">
                        <label>Serie de Factura</label>
                        <div class="form-control" style="background: #f8f9fa;">${report.invoiceSeries}</div>
                    </div>
                    ${report.notes ? `
                    <div class="form-group">
                        <label>Observaciones</label>
                        <div class="form-control" style="background: #f8f9fa; min-height: auto;">${report.notes}</div>
                    </div>
                    ` : ''}
                    <div class="form-group">
                        <label>Productos en mal estado</label>
                        <table class="report-products" style="width: 100%; margin-top: 0;">
                            <thead>
                                <tr>
                                    <th>Sku</th>
                                    <th>Cód. Fábrica</th>
                                    <th>Descripción</th>
                                    <th style="width: 70px;">Cantidad</th>
                                    <th style="width: 120px;">Motivo</th>
                                    <th style="width: 120px;">Estado</th>
                                    ${report.status === 'active' ? '<th style="width: 90px;">Acción</th>' : ''}
                                </tr>
                            </thead>
                            <tbody>
                                ${report.products ? report.products.map((product, index) => `
                                    <tr>
                                        <td>${product.sku || ''}</td>
                                        <td>${product.factoryCode || '-'}</td>
                                        <td>${product.description}</td>
                                        <td>${product.quantity}</td>
                                        <td>${product.reason}</td>
                                        <td class="status-cell" onclick="toggleProductStatus('${report.id}', ${index}, event)">
                                            <span class="product-status status-${product.status}"></span>
                                            ${product.status === 'pending' ? 'Pendiente' : product.status === 'received' ? 'Recibido' : 'Anulado'}
                                            ${product.receivedDate ? `<span class="status-date">Recibido el: ${formatDateTime(product.receivedDate)}</span>` : ''}
                                        </td>
                                        ${report.status === 'active' ? `
                                        <td>
                                            <button class="btn btn-success" style="padding: 0.3rem 0.6rem; font-size: 0.85rem;" 
                                                onclick="toggleProductStatus('${report.id}', ${index}, event)">
                                                <i class="fas fa-check"></i> ${product.status === 'pending' ? 'Recibido' : 'Pendiente'}
                                            </button>
                                        </td>
                                        ` : ''}
                                    </tr>
                                `).join('') : ''}
                            </tbody>
                        </table>
                    </div>
                `;
                
                modalReportActions.innerHTML = `
                    <button class="btn btn-pdf" onclick="generatePDF('${report.id}')">
                        <i class="fas fa-file-pdf"></i>
                        Generar PDF
                    </button>
                    ${report.status === 'active' ? `
                    <button class="btn btn-secondary" onclick="editReport('${report.id}')">
                        <i class="fas fa-edit"></i> Editar
                    </button>
                    <button class="btn btn-danger" onclick="cancelReport('${report.id}')">
                        <i class="fas fa-ban"></i> Anular
                    </button>
                    ` : ''}
                    <button class="btn" onclick="window.closeModal()">
                        <i class="fas fa-times"></i>
                        Cerrar
                    </button>
                `;
                
                reportModal.style.display = 'flex';
                document.body.style.overflow = 'hidden';
            };

            // Generar PDF del reporte
            window.generatePDF = function(reportId) {
                const report = reports.find(r => r.id === reportId);
                if (!report) return;
                
                const doc = new jsPDF();
                
                // Configuración de márgenes
                const marginLeft = 15;
                const marginRight = 15;
                const pageWidth = doc.internal.pageSize.getWidth();
                const contentWidth = pageWidth - marginLeft - marginRight;
                
                // Logo de la empresa y nombre
                doc.addImage(companyLogo, 'PNG', marginLeft, 10, 40, 15);
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.text(companyName, pageWidth / 2, 20, { align: 'center' });
                
                // Título del documento
                doc.setFontSize(12);
                doc.setFont('helvetica', 'normal');
                doc.text('Reporte de Productos en Mal Estado', pageWidth / 2, 30, { align: 'center' });
                
                // Línea separadora
                doc.setDrawColor(200, 200, 200);
                doc.line(marginLeft, 35, pageWidth - marginRight, 35);
                
                // Información del reporte
                doc.setFontSize(10);
                let yPosition = 45;
                
                // Textos alineados a la izquierda
                const leftTexts = [
                    `Proveedor: ${report.supplier}`,
                    `Número de Factura: ${report.invoiceNumber}`,
                    `Serie de Factura: ${report.invoiceSeries}`
                ];
                
                // Textos alineados a la derecha
                const rightTexts = [
                    `Número de Reporte: ${report.id}`,
                    `Fecha de Reporte: ${formatDate(report.date)}`
                ];
                
                // Calcular posición vertical para alinear ambos lados
                const lineHeight = 7;
                const maxLines = Math.max(leftTexts.length, rightTexts.length);
                
                for (let i = 0; i < maxLines; i++) {
                    if (i < leftTexts.length) {
                        doc.text(leftTexts[i], marginLeft, yPosition + (i * lineHeight));
                    }
                    
                    if (i < rightTexts.length) {
                        const text = rightTexts[i];
                        const textWidth = doc.getStringUnitWidth(text) * doc.internal.getFontSize() / doc.internal.scaleFactor;
                        doc.text(text, pageWidth - marginRight - textWidth, yPosition + (i * lineHeight));
                    }
                }
                
                yPosition += (maxLines * lineHeight) + 10;
                
                if (report.notes) {
                    const splitNotes = doc.splitTextToSize(`Observaciones: ${report.notes}`, contentWidth);
                    doc.text(splitNotes, marginLeft, yPosition);
                    yPosition += splitNotes.length * 5 + 10;
                } else {
                    yPosition += 10;
                }
                
                // Tabla de productos con bordes
                const tableData = report.products ? report.products.map(product => [
                    product.sku || '',
                    product.factoryCode || '-',
                    product.description,
                    product.quantity.toString(),
                    product.reason,
                    product.status === 'pending' ? 'Pendiente' : product.status === 'received' ? `Recibido\n${formatDateTime(product.receivedDate)}` : 'Anulado'
                ]) : [];
                
                doc.autoTable({
                    startY: yPosition,
                    head: [['Sku', 'Cód. Fábrica', 'Descripción', 'Cantidad', 'Motivo', 'Estado']],
                    body: tableData,
                    margin: { left: marginLeft, right: marginRight },
                    styles: {
                        fontSize: 9,
                        cellPadding: 3,
                        valign: 'middle',
                        lineWidth: 0.2,
                        lineColor: 50
                    },
                    headStyles: {
                        fillColor: [67, 97, 238],
                        textColor: 255,
                        fontStyle: 'bold',
                        lineWidth: 0.2
                    },
                    bodyStyles: {
                        lineWidth: 0.2
                    },
                    columnStyles: {
                        0: { cellWidth: 25 },
                        1: { cellWidth: 25 },
                        2: { cellWidth: 'auto' },
                        3: { cellWidth: 20 },
                        4: { cellWidth: 30 },
                        5: { cellWidth: 30 }
                    }
                });
                
                // Firmas más separadas y con letra más grande
                const lastY = doc.lastAutoTable.finalY + 30;
                
                doc.setFontSize(14);
                doc.text('Fecha de Entrega: ________________________', marginLeft, lastY);
                doc.text('Recibe: _________________________________', marginLeft, lastY + 20);
                doc.text('Entrega: ________________________________', marginLeft, lastY + 40);
                
                // Guardar PDF
                doc.save(`Reporte_${report.id}.pdf`);
            };

            // Event listeners
            newReportBtn.addEventListener('click', showNewReportForm);
            cancelReportBtn.addEventListener('click', hideReturnForm);
            saveReportBtn.addEventListener('click', saveReport);
            addRowBtn.addEventListener('click', addProductRow);
            reportModal.addEventListener('click', (e) => {
                if (e.target === reportModal) window.closeModal();
            });
            searchBtn.addEventListener('click', searchReports);
            searchInput.addEventListener('keypress', (e) => {
                if (e.key === 'Enter') searchReports();
            });

            // Convertir automáticamente a mayúsculas mientras se escribe
            document.addEventListener('input', function(e) {
                if (e.target.matches('#supplier, #productsTable input[type="text"]:not(.code-input), #invoiceNumber, #invoiceSeries')) {
                    e.target.value = e.target.value.toUpperCase();
                }
            });

            // Cargar reportes al iniciar
            loadReports();
        });
    </script>
</body>
</html>
