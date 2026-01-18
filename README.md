
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Solicitação de Análise de Crédito</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        .spinner {
            border: 3px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top: 3px solid #ffffff;
            width: 20px;
            height: 20px;
            -webkit-animation: spin 1s linear infinite;
            animation: spin 1s linear infinite;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        /* Custom scrollbar for selects if needed on some browsers */
        select::-ms-expand {
            display: none;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-700 font-sans min-h-screen flex items-center justify-center p-4">

    <div class="w-full max-w-2xl bg-white rounded-xl shadow-2xl overflow-hidden border border-gray-100">
        
        <!-- Cabeçalho -->
        <div class="bg-[#5DBAA6] p-6 text-white text-center">
            <h2 class="text-2xl font-bold">Crédito Para Investimentos</h2>
            <p class="text-sm opacity-90 mt-1">Preencha os dados abaixo para solicitar a análise de crédito.</p>
        </div>

        <div class="p-8">
            <form id="form_integracao_crm" class="space-y-5">

                <!-- Dados Pessoais -->
                <div class="grid grid-cols-1 md:grid-cols-2 gap-5">
                    <!-- Nome -->
                    <div class="col-span-1 md:col-span-2">
                        <label class="block text-sm font-medium text-gray-700 mb-1">Seu nome completo*</label>
                        <div class="relative">
                            <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-user"></i>
                            </div>
                            <input type="text" name="Nome" class="w-full pl-10 pr-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#5DBAA6] focus:border-[#5DBAA6] outline-none transition" maxlength="80" placeholder="Ex: João da Silva" required>
                        </div>
                    </div>

                    <!-- Telefone -->
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Telefone com DDD*</label>
                        <div class="relative">
                            <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-phone"></i>
                            </div>
                            <input type="tel" name="Telefone" class="w-full pl-10 pr-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#5DBAA6] focus:border-[#5DBAA6] outline-none transition" maxlength="20" placeholder="(00) 00000-0000" required>
                        </div>
                    </div>

                    <!-- Cidade -->
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Cidade*</label>
                        <div class="relative">
                            <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <!-- Nota: O name 'Cidade;' com ponto e vírgula foi mantido conforme o original para compatibilidade -->
                            <input type="text" name="Cidade;" class="w-full pl-10 pr-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#5DBAA6] focus:border-[#5DBAA6] outline-none transition" maxlength="1000" placeholder="Ex: São Paulo" required>
                        </div>
                    </div>
                </div>

                <hr class="border-gray-100 my-4">

                <!-- Dados do Investimento -->
                <div class="grid grid-cols-1 md:grid-cols-2 gap-5">
                    
                    <!-- Área de Investimento -->
                    <div class="col-span-1 md:col-span-2">
                        <label class="block text-sm font-medium text-gray-700 mb-1">Área de investimento*</label>
                        <div class="relative">
                            <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-chart-line"></i>
                            </div>
                            <select class="w-full pl-10 pr-10 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#5DBAA6] focus:border-[#5DBAA6] outline-none transition bg-white appearance-none cursor-pointer" required name="Área de investimento:">
                                <option value="" disabled selected>Selecione uma opção</option>
                                <option value="Imóvel/Construção/Reforma">Imóvel/Construção/Reforma</option>
                                <option value="Veículos">Veículos</option>
                                <option value="Rural/Maquinários/Terras/Fazenda">Rural/Maquinários/Terras/Fazenda</option>
                                <option value="Empresarial">Empresarial</option>
                            </select>
                            <div class="absolute inset-y-0 right-0 pr-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-chevron-down text-xs"></i>
                            </div>
                        </div>
                    </div>

                    <!-- Valor do Crédito -->
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Valor do crédito*</label>
                        <div class="relative">
                            <select class="w-full px-4 pr-10 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#5DBAA6] focus:border-[#5DBAA6] outline-none transition bg-white appearance-none cursor-pointer" required name="Valor do crédito:">
                                <option value="" disabled selected>Selecione</option>
                                <option value="100 MIL">100 MIL</option>
                                <option value="200 MIL">200 MIL</option>
                                <option value="350 MIL">350 MIL</option>
                                <option value="450 MIL">450 MIL</option>
                                <option value="500 MIL">500 MIL</option>
                                <option value="800 MIL">800 MIL</option>
                                <option value="1 MILHÃO">1 MILHÃO</option>
                                <option value="+ De 3 MILHÕES">+ De 3 MILHÕES</option>
                            </select>
                            <div class="absolute inset-y-0 right-0 pr-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-chevron-down text-xs"></i>
                            </div>
                        </div>
                    </div>

                    <!-- Valor de Parcela -->
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Valor de Parcela*</label>
                        <div class="relative">
                            <select class="w-full px-4 pr-10 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#5DBAA6] focus:border-[#5DBAA6] outline-none transition bg-white appearance-none cursor-pointer" required name="Valor de Parcela:">
                                <option value="" disabled selected>Selecione</option>
                                <option value="800 R$">800 R$</option>
                                <option value="950 R$">950 R$</option>
                                <option value="1.200 R$">1.200 R$</option>
                                <option value="2.400 R$">2.400 R$</option>
                                <option value="3.500 R$">3.500 R$</option>
                                <option value="4.300 R$">4.300 R$</option>
                                <option value="5.000 R$">5.000 R$</option>
                                <option value="6.000 R$">6.000 R$</option>
                                <option value="+ De 10.000 R$">+ De 10.000 R$</option>
                            </select>
                            <div class="absolute inset-y-0 right-0 pr-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-chevron-down text-xs"></i>
                            </div>
                        </div>
                    </div>

                    <!-- Possui Entrada -->
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Possui entrada?*</label>
                        <div class="relative">
                            <select class="w-full px-4 pr-10 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#5DBAA6] focus:border-[#5DBAA6] outline-none transition bg-white appearance-none cursor-pointer" required name="Possui entrada?">
                                <option value="" disabled selected>Selecione</option>
                                <option value="Sim">Sim</option>
                                <option value="Não">Não</option>
                            </select>
                            <div class="absolute inset-y-0 right-0 pr-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-chevron-down text-xs"></i>
                            </div>
                        </div>
                    </div>

                    <!-- Valor Entrada (Se tiver) -->
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Valor entrada (Se tiver)</label>
                        <div class="relative">
                            <select class="w-full px-4 pr-10 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#5DBAA6] focus:border-[#5DBAA6] outline-none transition bg-white appearance-none cursor-pointer" name="Valor entrada (Se tiver)">
                                <option value="" disabled selected>Selecione</option>
                                <option value="2.000">2.000</option>
                                <option value="3.500">3.500</option>
                                <option value="4.000">4.000</option>
                                <option value="5.000">5.000</option>
                                <option value="6.300">6.300</option>
                                <option value="8.000">8.000</option>
                                <option value="+ De 10.000">+ De 10.000</option>
                            </select>
                            <div class="absolute inset-y-0 right-0 pr-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-chevron-down text-xs"></i>
                            </div>
                        </div>
                    </div>

                    <!-- Renda Mensal -->
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Renda mensal*</label>
                        <div class="relative">
                             <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-wallet"></i>
                            </div>
                            <select class="w-full pl-10 pr-10 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#5DBAA6] focus:border-[#5DBAA6] outline-none transition bg-white appearance-none cursor-pointer" required name="Renda mensal:">
                                <option value="" disabled selected>Selecione</option>
                                <option value="1.500">1.500</option>
                                <option value="2.300">2.300</option>
                                <option value="3.400">3.400</option>
                                <option value="4.200">4.200</option>
                                <option value="5.500">5.500</option>
                                <option value="+ De 10.000">+ De 10.000</option>
                            </select>
                            <div class="absolute inset-y-0 right-0 pr-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-chevron-down text-xs"></i>
                            </div>
                        </div>
                    </div>

                    <!-- Previsão -->
                    <div>
                        <label class="block text-sm font-medium text-gray-700 mb-1">Previsão para investir*</label>
                        <div class="relative">
                            <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-calendar-alt"></i>
                            </div>
                            <select class="w-full pl-10 pr-10 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#5DBAA6] focus:border-[#5DBAA6] outline-none transition bg-white appearance-none cursor-pointer" required name="Previsão para investir:">
                                <option value="" disabled selected>Selecione</option>
                                <option value="Imediato">Imediato</option>
                                <option value="Até 30 dias">Até 30 dias</option>
                                <option value="Em 2 meses">Em 2 meses</option>
                                <option value="Em até 3 Meses">Em até 3 Meses</option>
                            </select>
                            <div class="absolute inset-y-0 right-0 pr-3 flex items-center pointer-events-none text-gray-400">
                                <i class="fas fa-chevron-down text-xs"></i>
                            </div>
                        </div>
                    </div>

                </div>

                <!-- Status Messages -->
                <div id="status-message" class="hidden rounded-lg p-4 text-sm mt-4"></div>

                <!-- Submit Button -->
                <button id="btnEnviar" type="submit" class="w-full bg-[#5DBAA6] hover:bg-[#4aa390] text-white font-bold py-3 px-4 rounded-lg shadow-md transition duration-300 flex items-center justify-center gap-2 mt-6">
                    <span id="btnText">Enviar Solicitação</span>
                    <div id="btnSpinner" class="spinner hidden"></div>
                </button>

            </form>
        </div>
        
        <!-- Footer -->
        <div class="bg-gray-50 px-8 py-4 text-center text-xs text-gray-400 border-t border-gray-100">
            <i class="fas fa-lock mr-1"></i> Ambiente seguro e criptografado.
        </div>
    </div>

    <script type="text/javascript">
        document.addEventListener('DOMContentLoaded', function(e) {
            const form = document.getElementById('form_integracao_crm');
            const statusDiv = document.getElementById('status-message');
            const btn = document.querySelector('#btnEnviar');
            const btnText = document.getElementById('btnText');
            const btnSpinner = document.getElementById('btnSpinner');

            function showStatus(type, message) {
                statusDiv.classList.remove('hidden', 'bg-green-100', 'text-green-800', 'bg-red-100', 'text-red-800');
                if (type === 'success') {
                    statusDiv.classList.add('bg-green-100', 'text-green-800');
                    statusDiv.innerHTML = `<div class="flex items-center"><i class="fas fa-check-circle mr-2"></i> ${message}</div>`;
                } else {
                    statusDiv.classList.add('bg-red-100', 'text-red-800');
                     statusDiv.innerHTML = `<div class="flex items-center"><i class="fas fa-exclamation-circle mr-2"></i> ${message}</div>`;
                }
                statusDiv.classList.remove('hidden');
            }

            form.addEventListener('submit', async (e) => {
                e.preventDefault();
                statusDiv.classList.add('hidden');
                
                // Get URL Parameters (UTM)
                const params = new Proxy(new URLSearchParams(window.location.search), {
                    get: (searchParams, prop) => searchParams.get(prop),
                });

                const formData = new FormData(form);
                if (params.utm_source) formData.append('UTMSource', params.utm_source);
                if (params.utm_medium) formData.append('UTMMedium', params.utm_medium);
                if (params.utm_campaign) formData.append('UTMCampaing', params.utm_campaign);

                try {
                    // Loading State
                    btnText.innerText = 'Enviando...';
                    btnSpinner.classList.remove('hidden');
                    btn.disabled = true;
                    btn.classList.add('opacity-75', 'cursor-not-allowed');

                    const inputs = document.querySelectorAll('#form_integracao_crm input, #form_integracao_crm select');
                    inputs.forEach(input => input.disabled = true);

                    // API Call
                    const response = await fetch('https://app.crmdeconsorcio.com.br/api/v1/Integracao/Formulario', {
                        method: 'POST',
                        mode: 'cors',
                        headers: {
                            // Token Atualizado
                            'Authorization': 'Bearer MmIwNDg0MDYtMzUwYi00YTU1LThlZjQtOGZkYWU1YmE3MjExOjE3Njg3NDIxNzQ=',
                            'Access-Control-Allow-Origin': '*' 
                        },
                        body: formData
                    });

                    if (response.ok) {
                        const redirectTo = ''; // Define URL to redirect if needed
                        if (redirectTo) {
                            window.location.href = redirectTo;
                        } else {
                            showStatus('success', 'Obrigado! Recebemos seus dados com sucesso.');
                            form.reset();
                        }
                    } else {
                        throw response;
                    }
                } catch (error) {
                    console.error(error);
                    showStatus('error', 'Não foi possível enviar. Tente novamente mais tarde.');
                } finally {
                    // Reset State
                    btnText.innerText = 'Enviar Solicitação';
                    btnSpinner.classList.add('hidden');
                    btn.disabled = false;
                    btn.classList.remove('opacity-75', 'cursor-not-allowed');

                    const inputs = document.querySelectorAll('#form_integracao_crm input, #form_integracao_crm select');
                    inputs.forEach(input => input.disabled = false);
                }
            });
        });
    </script>
</body>
</html>

