<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>O Retiro - Inscrições 2025</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Segoe UI', sans-serif; background: linear-gradient(135deg, #1a1a1a, #2d2d2d); min-height: 100vh; color: white; padding: 20px; }
        .container { max-width: 600px; margin: 0 auto; background: #000; border-radius: 15px; box-shadow: 0 20px 40px rgba(0,0,0,0.5); overflow: hidden; border: 1px solid #333; }
        
        .header { 
            background: #000; 
            padding: 30px 30px 40px 30px; 
            text-align: center; 
            border-bottom: 2px solid #333;
        }
        
        .church-logo {
            margin-bottom: 20px;
        }
        
        .church-logo img {
            max-width: 120px;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(255, 107, 53, 0.3);
            transition: transform 0.3s ease;
        }
        
        .church-logo img:hover {
            transform: scale(1.05);
        }
        
        .church-name {
            font-size: 1.4em;
            color: #fff;
            margin-bottom: 25px;
            letter-spacing: 2px;
            font-weight: 700;
            text-transform: uppercase;
            line-height: 1.2;
        }
        
        .genero-selector {
            font-size: 1.1em; 
            color: #ff6b35; 
            font-weight: 600; 
            margin-bottom: 15px;
            letter-spacing: 1px;
            text-transform: uppercase;
        }
        
        .titulo-retiro { 
            font-size: 3em; 
            margin-bottom: 15px; 
            color: #fff; 
            font-weight: 900;
            letter-spacing: 3px;
            text-transform: uppercase;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .subtitle-retiro { 
            font-size: 1.2em; 
            color: #ccc;
            letter-spacing: 2px;
            font-weight: 500;
            text-transform: uppercase;
        }

        .form-container { padding: 40px; background: #111; }
        .section-title { color: #ff6b35; font-size: 1.3em; font-weight: bold; margin: 30px 0 20px 0; padding-bottom: 10px; border-bottom: 2px solid #333; }
        .form-group { margin-bottom: 25px; }
        .conditional-field { margin-top: 15px; padding-left: 20px; border-left: 3px solid #ff6b35; display: none; }
        label { display: block; margin-bottom: 8px; font-weight: 600; color: #fff; font-size: 1.1em; }
        .required { color: #ff6b35; }
        input, select, textarea { width: 100%; padding: 15px; border: 2px solid #333; border-radius: 8px; font-size: 16px; transition: all 0.3s ease; background: #222; color: #fff; text-transform: uppercase; }
        input[type="number"], input[type="tel"], input[type="email"] { text-transform: none; }
        input:focus, select:focus, textarea:focus { outline: none; border-color: #ff6b35; background: #333; box-shadow: 0 0 0 3px rgba(255, 107, 53, 0.1); }
        input::placeholder { color: #999; }
        textarea { resize: vertical; min-height: 80px; }
        select { cursor: pointer; appearance: none; background-image: url("data:image/svg+xml;charset=US-ASCII,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 4 5'><path fill='%23999' d='M2 0L0 2h4zm0 5L0 3h4z'/></svg>"); background-repeat: no-repeat; background-position: right 15px center; background-size: 12px; padding-right: 45px; }
        select option { background: #222; color: #fff; }
        .submit-btn { background: linear-gradient(45deg, #ff6b35 0%, #ff8a5b 100%); color: white; border: none; padding: 18px 40px; border-radius: 50px; font-size: 1.2em; font-weight: 600; cursor: pointer; width: 100%; transition: all 0.3s ease; text-transform: uppercase; letter-spacing: 1px; }
        .submit-btn:hover { transform: translateY(-2px); box-shadow: 0 10px 25px rgba(255, 107, 53, 0.3); }
        .submit-btn:disabled { opacity: 0.7; cursor: not-allowed; transform: none; }
        .success-message { display: none; background: #1a472a; color: #4ade80; border: 1px solid #16a34a; padding: 20px; border-radius: 8px; margin-bottom: 20px; text-align: center; }
        .error-message { display: none; background: #660000; color: #ff6666; border: 1px solid #cc0000; padding: 20px; border-radius: 8px; margin-bottom: 20px; text-align: center; }
        .info-box { background: #1a1a2e; border-left: 4px solid #ff6b35; padding: 15px; margin-bottom: 25px; border-radius: 4px; color: #ccc; }
        .color-legend { background: #222; padding: 15px; border-radius: 8px; margin-bottom: 20px; border: 1px solid #333; }
        .color-legend h4 { color: #ff6b35; margin-bottom: 10px; }
        .color-list { display: flex; flex-wrap: wrap; gap: 10px; }
        .color-item { display: flex; align-items: center; gap: 5px; font-size: 0.9em; }
        .color-dot { width: 12px; height: 12px; border-radius: 50%; border: 1px solid #555; }
        .color-dot.branca { background: #fff; }
        .color-dot.azul { background: #3b82f6; }
        .color-dot.amarela { background: #eab308; }
        .color-dot.vermelha { background: #ef4444; }
        .color-dot.verde { background: #22c55e; }
        
        /* Debug panel styles */
        .debug-panel {
            position: fixed;
            top: 20px;
            right: 20px;
            background: #111;
            border: 2px solid #ff6b35;
            border-radius: 10px;
            padding: 15px;
            max-width: 300px;
            font-size: 0.9em;
            z-index: 1000;
            display: none;
        }
        
        .debug-panel.active {
            display: block;
        }
        
        .debug-btn {
            background: #333;
            color: #fff;
            border: 1px solid #ff6b35;
            padding: 8px 12px;
            border-radius: 5px;
            cursor: pointer;
            margin: 5px;
            font-size: 0.8em;
        }
        
        .debug-btn:hover {
            background: #ff6b35;
        }
        
        @media (max-width: 768px) {
            body { padding: 10px; }
            .container { margin: 0; border-radius: 10px; }
            .header { padding: 20px; }
            .church-logo img { max-width: 100px; }
            .church-name { font-size: 1.1em; }
            .titulo-retiro { font-size: 2.2em; letter-spacing: 2px; }
            .subtitle-retiro { font-size: 1em; letter-spacing: 1px; }
            .genero-selector { font-size: 1em; }
            .form-container { padding: 20px; }
            .section-title { font-size: 1.1em; }
            .color-list { justify-content: center; }
            .color-item { font-size: 0.8em; }
            .debug-panel { right: 10px; top: 10px; max-width: 250px; }
        }
    </style>
</head>
<body>
    <!-- Debug Panel -->
    <div class="debug-panel" id="debug-panel">
        <h4 style="color: #ff6b35; margin-bottom: 10px;">🔧 Debug Panel</h4>
        <button class="debug-btn" onclick="toggleDebug()">Fechar</button>
        <button class="debug-btn" onclick="verificarConexao()">Testar Conexão</button>
        <button class="debug-btn" onclick="inserirTeste()">Testar Inserção</button>
        <button class="debug-btn" onclick="listarRegistros()">Listar Registros</button>
        <div id="debug-output" style="margin-top: 10px; font-size: 0.8em; color: #ccc;"></div>
    </div>

    <div class="container">
        <div class="header">
            <div class="church-logo">
                <img src="https://i.imgur.com/T5QABfl.jpeg" alt="Logo O Retiro" id="church-logo-img">
            </div>
            
            <div class="church-name">
                ALVO - UMA IGREJA, UMA VISÃO,<br>
                <strong>VEM E VÊ!</strong>
            </div>
            
            <!-- Debug toggle button -->
            <button onclick="toggleDebug()" style="position: absolute; top: 10px; right: 10px; background: #333; color: #fff; border: none; padding: 5px 10px; border-radius: 5px; font-size: 0.8em; cursor: pointer;">🔧</button>
            
            <div class="genero-selector" id="date-display">PROGRAMAÇÃO - O RETIRO</div>
            
            <div class="subtitle-retiro">VISÃO • MISSÃO • PRESSÃO</div>
        </div>

        <div class="form-container">
            <div class="info-box">
                <strong>🎯 Inscrição Rápida:</strong> Preencha os dados essenciais para sua pré inscrição. O pagamento deverá ser realizado presencialmente.
            </div>

            <div class="info-box">
                <strong>💰 Informações de Pagamento:</strong><br>
                • <strong>Entrada Mínima para Pré-Inscrição:</strong> R$ 150,00
            </div>

            <div class="info-box">
                <strong>🎽 PROMOÇÃO ESPECIAL - CAMISA DO RETIRO:</strong><br>
                • <strong>Os 150 primeiros pagamentos ganham a camisa oficial do RETIRO!</strong><br>
                • <strong>Como garantir:</strong> Compareça ao balcão e pague o valor mínimo de R$ 150,00
            </div>

            <div class="success-message" id="success-message">
                🙌 <strong>Tenha um excelente Retiro!</strong><br>
                <div id="payment-instructions" style="margin-top: 10px; padding: 10px; background: #333; border-radius: 5px;">
                    <strong>📋 Próximos Passos:</strong><br>
                    <span id="next-steps"></span>
                    <div style="margin-top: 15px; padding: 10px; background: #444; border-radius: 5px; font-size: 0.9em; color: #ccc;">
                        ⚠️ <strong>Importante:</strong> Não devolvemos ou transferimos o valor da inscrição
                    </div>
                </div>
            </div>

            <div class="error-message" id="error-message">
                ❌ <strong>Erro temporário no sistema.</strong><br>
                <span id="error-details">Tente novamente em alguns segundos.</span>
            </div>

            <form id="inscricao-form">
                <!-- IDENTIFICAÇÃO E CONTATO -->
                <div class="section-title">✅ Identificação e Contato</div>
                
                <div class="form-group">
                    <label for="nome">Nome Completo <span class="required">*</span></label>
                    <input type="text" id="nome" name="nome" required placeholder="DIGITE SEU NOME COMPLETO">
                    <div style="font-size: 0.9em; color: #ccc; margin-top: 5px;">
                        ⚠️ Digite o nome exatamente como está no documento (RG/CPF)
                    </div>
                </div>

                <div class="form-group">
                    <label for="sexo">Sexo <span class="required">*</span></label>
                    <select id="sexo" name="sexo" required>
                        <option value="">Selecione seu sexo</option>
                        <option value="MASCULINO">👨 Masculino</option>
                        <option value="FEMININO">👩 Feminino</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="idade">Idade <span class="required">*</span></label>
                    <input type="number" id="idade" name="idade" required placeholder="DIGITE SUA IDADE" min="12" max="100">
                </div>

                <div class="form-group">
                    <label for="whatsapp">WhatsApp <span class="required">*</span></label>
                    <input type="tel" id="whatsapp" name="whatsapp" placeholder="(11) 99999-9999" required>
                </div>

                <div class="form-group">
                    <label for="email">Email <span class="required">*</span></label>
                    <input type="email" id="email" name="email" placeholder="SEU@EMAIL.COM" required style="text-transform: lowercase;">
                </div>

                <div class="form-group">
                    <label for="endereco">Endereço <span class="required">*</span></label>
                    <input type="text" id="endereco" name="endereco" placeholder="RUA, AVENIDA..." required>
                </div>

                <div class="form-group">
                    <label for="numero">Número <span class="required">*</span></label>
                    <input type="text" id="numero" name="numero" placeholder="123" required>
                </div>

                <div class="form-group">
                    <label for="bairro">Bairro <span class="required">*</span></label>
                    <input type="text" id="bairro" name="bairro" placeholder="NOME DO BAIRRO" required>
                </div>

                <div class="form-group">
                    <label for="cidade">Cidade <span class="required">*</span></label>
                    <input type="text" id="cidade" name="cidade" placeholder="NOME DA CIDADE" required>
                </div>

                <!-- INFORMAÇÕES DE SAÚDE E ACESSIBILIDADE -->
                <div class="section-title">🏥 Informações de Saúde e Acessibilidade</div>

                <div class="form-group">
                    <label for="comorbidade">Possui alguma comorbidade? <span class="required">*</span></label>
                    <select id="comorbidade" name="comorbidade" required>
                        <option value="">Selecione uma opção</option>
                        <option value="NÃO">❌ Não</option>
                        <option value="SIM">✅ Sim</option>
                    </select>
                    <div id="comorbidade-detalhes" class="conditional-field">
                        <label for="comorbidade-qual">Qual comorbidade?</label>
                        <textarea id="comorbidade-qual" name="comorbidade-qual" placeholder="DESCREVA A COMORBIDADE..."></textarea>
                    </div>
                </div>

                <div class="form-group">
                    <label for="gravida">Está grávida? <span class="required">*</span></label>
                    <select id="gravida" name="gravida" required>
                        <option value="">Selecione uma opção</option>
                        <option value="NÃO">❌ Não</option>
                        <option value="SIM">✅ Sim</option>
                    </select>
                    <div id="gravida-detalhes" class="conditional-field">
                        <label for="gravida-observacao">Tem alguma observação sobre a gravidez?</label>
                        <textarea id="gravida-observacao" name="gravida-observacao" placeholder="OBSERVAÇÕES SOBRE A GRAVIDEZ..."></textarea>
                    </div>
                </div>

                <div class="form-group">
                    <label for="medicacao">Usa medicação contínua? <span class="required">*</span></label>
                    <select id="medicacao" name="medicacao" required>
                        <option value="">Selecione uma opção</option>
                        <option value="NÃO">❌ Não</option>
                        <option value="SIM">✅ Sim</option>
                    </select>
                    <div id="medicacao-detalhes" class="conditional-field">
                        <label for="medicacao-qual">Qual medicação?</label>
                        <textarea id="medicacao-qual" name="medicacao-qual" placeholder="DESCREVA AS MEDICAÇÕES..."></textarea>
                    </div>
                </div>

                <div class="form-group">
                    <label for="restricoes">Tem restrições alimentares? <span class="required">*</span></label>
                    <select id="restricoes" name="restricoes" required>
                        <option value="">Selecione uma opção</option>
                        <option value="NÃO">❌ Não</option>
                        <option value="SIM">✅ Sim</option>
                    </select>
                    <div id="restricoes-detalhes" class="conditional-field">
                        <label for="restricoes-quais">Quais restrições alimentares?</label>
                        <textarea id="restricoes-quais" name="restricoes-quais" placeholder="DESCREVA AS RESTRIÇÕES ALIMENTARES..."></textarea>
                    </div>
                </div>

                <div class="form-group">
                    <label for="alergias">Tem alergias? <span class="required">*</span></label>
                    <select id="alergias" name="alergias" required>
                        <option value="">Selecione uma opção</option>
                        <option value="NÃO">❌ Não</option>
                        <option value="SIM">✅ Sim</option>
                    </select>
                    <div id="alergias-detalhes" class="conditional-field">
                        <label for="alergias-quais">Quais alergias?</label>
                        <textarea id="alergias-quais" name="alergias-quais" placeholder="DESCREVA AS ALERGIAS..."></textarea>
                    </div>
                </div>

                <div class="form-group">
                    <label for="locomocao">Tem alguma limitação de locomoção? <span class="required">*</span></label>
                    <select id="locomocao" name="locomocao" required>
                        <option value="">Selecione uma opção</option>
                        <option value="NÃO">❌ Não</option>
                        <option value="SIM">✅ Sim</option>
                    </select>
                    <div id="locomocao-detalhes" class="conditional-field">
                        <label for="locomocao-qual">Qual limitação de locomoção?</label>
                        <textarea id="locomocao-qual" name="locomocao-qual" placeholder="DESCREVA A LIMITAÇÃO DE LOCOMOÇÃO..."></textarea>
                    </div>
                </div>

                <!-- INFORMAÇÕES DE VÍNCULO COM ALVO -->
                <div class="section-title">🎯 Informações de vínculos</div>

                <div class="form-group">
                    <div class="color-legend">
                        <h4>Referência das Cores das Redes:</h4>
                        <div class="color-list">
                            <div class="color-item">
                                <div class="color-dot branca"></div>
                                <span>Branca</span>
                            </div>
                            <div class="color-item">
                                <div class="color-dot azul"></div>
                                <span>Azul</span>
                            </div>
                            <div class="color-item">
                                <div class="color-dot amarela"></div>
                                <span>Amarela</span>
                            </div>
                            <div class="color-item">
                                <div class="color-dot vermelha"></div>
                                <span>Vermelha</span>
                            </div>
                            <div class="color-item">
                                <div class="color-dot verde"></div>
                                <span>Verde</span>
                            </div>
                        </div>
                    </div>
                    
                    <label for="cor-rede">Cor da Rede <span class="required">*</span></label>
                    <select id="cor-rede" name="cor-rede" required>
                        <option value="">Selecione a cor da sua rede</option>
                        <option value="BRANCA">🤍 Rede Branca</option>
                        <option value="AZUL">💙 Rede Azul</option>
                        <option value="AMARELA">💛 Rede Amarela</option>
                        <option value="VERMELHA">❤️ Rede Vermelha</option>
                        <option value="VERDE">💚 Rede Verde</option>
                        <option value="NÃO-POSSUO">🆕 Não possuo rede ainda</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="vai-servir-receber">Trabalho ou Encontrista? <span class="required">*</span></label>
                    <select id="vai-servir-receber" name="vai-servir-receber" required>
                        <option value="">Selecione uma opção</option>
                        <option value="TRABALHO">💼 Trabalho</option>
                        <option value="ENCONTRISTA">🎯 Encontrista</option>
                    </select>
                </div>

                <!-- INFORMAÇÕES DE PAGAMENTO -->
                <div class="section-title">💰 Informações de Pagamento</div>

                <div class="form-group">
                    <label for="pagamento">Status do Pagamento do retiro <span class="required">*</span></label>
                    <select id="pagamento" name="pagamento" required>
                        <option value="">Selecione o status do pagamento</option>
                        <option value="ENTRADA-PRÉ">💰 Entrada Pré Inscrição (R$ 150,00+)</option>
                        <option value="RETIRO-INTEGRAL">🎯 Retiro Integral</option>
                        <option value="PAGAR-DIFERENÇA">📅 Pagar Diferença</option>
                    </select>
                </div>

                <div class="form-group" id="valor-group" style="display: none;">
                    <label for="valor-pago">Valor que será pago <span class="required">*</span></label>
                    <div style="position: relative;">
                        <input type="text" id="valor-pago" name="valor-pago" placeholder="150,00" style="padding-left: 40px;">
                        <span style="position: absolute; left: 15px; top: 50%; transform: translateY(-50%); color: #ccc; font-weight: bold;">R$</span>
                    </div>
                    <div id="valor-warning" style="display: none; background: #660000; border: 1px solid #cc0000; color: #ff6666; padding: 10px; border-radius: 5px; margin-top: 10px;">
                        ⚠️ <strong>Atenção:</strong> O valor mínimo da pré-inscrição é R$ 150,00
                    </div>
                </div>

                <div class="form-group">
                    <label for="forma-pagamento">Como prefere pagar o retiro? <span class="required">*</span></label>
                    <select id="forma-pagamento" name="forma-pagamento" required>
                        <option value="">Selecione a forma de pagamento</option>
                        <option value="PIX">🏦 Pix</option>
                        <option value="DINHEIRO">💵 Dinheiro</option>
                        <option value="CT-DÉBITO">💳 Cartão Débito</option>
                        <option value="CT-CRÉDITO">💳 Cartão Crédito</option>
                    </select>
                </div>

                <!-- AUTORIZAÇÃO DE IMAGEM -->
                <div class="section-title">📸 Autorização de Imagem</div>

                <div class="form-group">
                    <div style="background: #1a1a2e; border: 2px solid #ff6b35; padding: 20px; border-radius: 8px; margin-bottom: 15px;">
                        <p style="color: #fff; font-size: 1.1em; line-height: 1.6; margin-bottom: 15px;">
                            <strong>📹 AUTORIZAÇÃO DE USO DE IMAGEM:</strong><br>
                            O retiro será gravado e fotografado para fins de registro, divulgação e memória do evento. 
                            As imagens poderão ser utilizadas em redes sociais, site da igreja, materiais promocionais e outros meios de comunicação da ALVO.
                        </p>
                    </div>
                    
                    <label for="autorizacao-imagem">
                        <input type="checkbox" id="autorizacao-imagem" name="autorizacao-imagem" required style="width: auto; margin-right: 10px; transform: scale(1.5);">
                        <span style="color: #ff6b35; font-weight: bold;">*</span> Eu autorizo o uso da minha imagem conforme descrito acima
                    </label>
                </div>

                <button type="submit" class="submit-btn" id="submit-btn">
                    Confirmar Inscrição
                </button>
            </form>
        </div>
    </div>

    <!-- Supabase CDN -->
    <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
    
    <script>
        // CONFIGURAÇÕES SUPABASE
        const RETIRO_CONFIG = {
            url: 'https://yuikwufjkdzgdzvlotaq.supabase.co',
            anonKey: 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Inl1aWt3dWZqa2R6Z2R6dmxvdGFxIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NTA5ODcwMzcsImV4cCI6MjA2NjU2MzAzN30.UGW0AHHSsIv842Z92F6RjI930fgS-5FmPX0i7kumgYo'
        };

        let retiroSupabase;
        let isSubmittingForm = false;

        // DEBUG FUNCTIONS
        function debugLog(message, data = null) {
            const debugOutput = document.getElementById('debug-output');
            const timestamp = new Date().toLocaleTimeString();
            const logEntry = `[${timestamp}] ${message}`;
            
            console.log(logEntry, data);
            
            if (debugOutput) {
                debugOutput.innerHTML += `<div style="margin: 2px 0; padding: 2px; background: #222; border-radius: 3px;">${logEntry}</div>`;
                debugOutput.scrollTop = debugOutput.scrollHeight;
            }
        }

        function toggleDebug() {
            const debugPanel = document.getElementById('debug-panel');
            debugPanel.classList.toggle('active');
        }

        // INICIALIZAR SUPABASE
        function inicializarSistema() {
            try {
                retiroSupabase = window.supabase.createClient(RETIRO_CONFIG.url, RETIRO_CONFIG.anonKey);
                debugLog('✅ Sistema inicializado com sucesso!');
                return true;
            } catch (error) {
                debugLog('❌ Erro ao inicializar:', error.message);
                return false;
            }
        }

        // FORMATAÇÃO
        function formatarWhatsApp(input) {
            let value = input.value.replace(/\D/g, '');
            if (value.length >= 11) {
                value = value.replace(/(\d{2})(\d{5})(\d{4})/, '($1) $2-$3');
            } else if (value.length >= 7) {
                value = value.replace(/(\d{2})(\d{4})(\d{0,4})/, '($1) $2-$3');
            } else if (value.length >= 3) {
                value = value.replace(/(\d{2})(\d{0,5})/, '($1) $2');
            }
            input.value = value;
        }

        function formatarValor(input) {
            let value = input.value.replace(/\D/g, '');
            if (value.length >= 3) {
                value = value.replace(/(\d+)(\d{2})$/, '$1,$2');
            }
            input.value = value;
        }

        function validarValorMinimo() {
            const pagamento = document.getElementById('pagamento').value;
            const valorInput = document.getElementById('valor-pago');
            const warning = document.getElementById('valor-warning');
            
            if (valorInput.value) {
                const valor = parseFloat(valorInput.value.replace(',', '.'));
                
                if (pagamento === 'ENTRADA-PRÉ' && valor < 150) {
                    warning.style.display = 'block';
                    warning.innerHTML = '⚠️ <strong>Atenção:</strong> O valor mínimo da pré-inscrição é R$ 150,00';
                } else {
                    warning.style.display = 'none';
                }
            } else {
                warning.style.display = 'none';
            }
        }

        // ATUALIZAR DATA BASEADA NO SEXO
        function atualizarDataRetiro() {
            const sexo = document.getElementById('sexo').value;
            const dateDisplay = document.getElementById('date-display');
            
            if (sexo === 'MASCULINO') {
                dateDisplay.textContent = 'MASCULINO: 8, 9 E 10 DE AGOSTO';
                dateDisplay.style.color = '#4ade80';
            } else if (sexo === 'FEMININO') {
                dateDisplay.textContent = 'FEMININO: 15, 16 E 17 DE AGOSTO';
                dateDisplay.style.color = '#ff6b9d';
            } else {
                dateDisplay.textContent = 'SELECIONE SEU SEXO';
                dateDisplay.style.color = '#ff6b35';
            }
        }

        // CAMPOS CONDICIONAIS
        function configurarCampoCondicional(selectId, detailsId) {
            const select = document.getElementById(selectId);
            const details = document.getElementById(detailsId);
            const textarea = details.querySelector('textarea');
            
            select.addEventListener('change', function() {
                if (this.value === 'SIM') {
                    details.style.display = 'block';
                    textarea.required = true;
                } else {
                    details.style.display = 'none';
                    textarea.required = false;
                    textarea.value = '';
                }
            });
        }

        // FUNÇÕES DE TESTE E DEBUG
        async function verificarConexao() {
            debugLog('🧪 Testando conexão com Supabase...');
            
            try {
                // Tentar uma consulta simples primeiro
                const { data, error } = await retiroSupabase
                    .from('inscricoes')
                    .select('id', { count: 'exact', head: true });
                
                if (error) {
                    debugLog('❌ Erro na consulta:', error.message);
                    
                    // Se houver erro de RLS, testar inserção anônima
                    if (error.code === '42501') {
                        debugLog('⚠️ Detectado erro de RLS. Testando inserção anônima...');
                        return await testarInsercaoAnonima();
                    }
                    
                    throw error;
                }
                
                debugLog('✅ Conexão OK!');
                return { success: true, message: 'Conexão funcionando!' };
                
            } catch (error) {
                debugLog('❌ Erro na conexão:', error.message);
                return { success: false, error: error.message };
            }
        }

        async function testarInsercaoAnonima() {
            try {
                debugLog('🔓 Testando inserção com dados mínimos...');
                
                const dadosMinimos = {
                    nome_completo: 'TESTE ANONIMO',
                    sexo: 'MASCULINO',
                    idade: 25,
                    whatsapp: '(11) 99999-9999',
                    email: 'teste@anonimo.com',
                    endereco: 'RUA TESTE',
                    numero: '123',
                    bairro: 'CENTRO',
                    cidade: 'SAO PAULO',
                    comorbidade: 'NÃO',
                    gravida: 'NÃO',
                    medicacao: 'NÃO',
                    restricoes_alimentares: 'NÃO',
                    alergias: 'NÃO',
                    limitacao_locomocao: 'NÃO',
                    cor_rede: 'AZUL',
                    vai_servir_receber: 'TRABALHO',
                    status_pagamento: 'ENTRADA-PRÉ',
                    valor_pago: '150,00',
                    forma_pagamento: 'PIX',
                    autorizacao_imagem: 'SIM',
                    data_inscricao: new Date().toISOString(),
                    status: 'ATIVO'
                };

                const { data, error } = await retiroSupabase
                    .from('inscricoes')
                    .insert([dadosMinimos])
                    .select();

                if (error) {
                    debugLog('❌ Erro na inserção anônima:', error.message);
                    throw error;
                }

                debugLog('✅ Inserção anônima bem-sucedida!', data);
                return { success: true, message: 'Sistema funcionando!' };
                
            } catch (error) {
                debugLog('❌ Falha na inserção anônima:', error.message);
                return { success: false, error: error.message };
            }
        }

        async function inserirTeste() {
            debugLog('🧪 Testando inserção completa...');
            
            const testeInfo = {
                nome: 'TESTE SISTEMA COMPLETO',
                sexo: 'MASCULINO',
                idade: 25,
                whatsapp: '(11) 99999-9999',
                email: 'teste@sistema.com',
                endereco: 'RUA TESTE COMPLETO',
                numero: '456',
                bairro: 'CENTRO',
                cidade: 'SAO PAULO',
                comorbidade: 'NÃO',
                comorbidadeQual: '',
                gravida: 'NÃO',
                gravidaObservacao: '',
                medicacao: 'NÃO',
                medicacaoQual: '',
                restricoes: 'NÃO',
                restricoesQuais: '',
                alergias: 'NÃO',
                alergiasQuais: '',
                locomocao: 'NÃO',
                locomocaoQual: '',
                corRede: 'AZUL',
                vaiServirReceber: 'TRABALHO',
                statusPagamento: 'ENTRADA-PRÉ',
                valorPago: '150,00',
                formaPagamento: 'PIX',
                autorizacaoImagem: 'SIM'
            };
            
            const resultado = await enviarParaSupabase(testeInfo);
            
            if (resultado.success) {
                debugLog('✅ Teste de inserção completa OK!');
                alert('✅ Teste de inserção funcionando!');
            } else {
                debugLog('❌ Erro no teste completo:', resultado.error);
                alert('❌ Erro no teste: ' + resultado.error);
            }
        }

        async function listarRegistros() {
            debugLog('📋 Listando registros...');
            
            try {
                const { data, error, count } = await retiroSupabase
                    .from('inscricoes')
                    .select('nome_completo, sexo, data_inscricao', { count: 'exact' })
                    .order('data_inscricao', { ascending: false })
                    .limit(5);
                
                if (error) throw error;
                
                debugLog(`📊 Total de registros: ${count}`);
                
                if (data && data.length > 0) {
                    debugLog('📝 Últimos 5 registros:');
                    data.forEach((registro, index) => {
                        debugLog(`${index + 1}. ${registro.nome_completo} (${registro.sexo})`);
                    });
                } else {
                    debugLog('📭 Nenhum registro encontrado');
                }
                
            } catch (error) {
                debugLog('❌ Erro ao listar registros:', error.message);
            }
        }

        // INTEGRAÇÃO COM SUPABASE MELHORADA
        async function enviarParaSupabase(informacoes) {
            try {
                debugLog('📤 Enviando para Supabase...', informacoes.nome);

                // Preparar dados com validação
                const dadosParaInserir = {
                    nome_completo: informacoes.nome || '',
                    sexo: informacoes.sexo || '',
                    idade: parseInt(informacoes.idade) || 0,
                    whatsapp: informacoes.whatsapp || '',
                    email: informacoes.email || '',
                    endereco: informacoes.endereco || '',
                    numero: informacoes.numero || '',
                    bairro: informacoes.bairro || '',
                    cidade: informacoes.cidade || '',
                    comorbidade: informacoes.comorbidade || 'NÃO',
                    comorbidade_qual: informacoes.comorbidadeQual || null,
                    gravida: informacoes.gravida || 'NÃO',
                    gravidez_observacao: informacoes.gravidaObservacao || null,
                    medicacao: informacoes.medicacao || 'NÃO',
                    medicacao_qual: informacoes.medicacaoQual || null,
                    restricoes_alimentares: informacoes.restricoes || 'NÃO',
                    restricoes_quais: informacoes.restricoesQuais || null,
                    alergias: informacoes.alergias || 'NÃO',
                    alergias_quais: informacoes.alergiasQuais || null,
                    limitacao_locomocao: informacoes.locomocao || 'NÃO',
                    locomocao_qual: informacoes.locomocaoQual || null,
                    cor_rede: informacoes.corRede || '',
                    vai_servir_receber: informacoes.vaiServirReceber || '',
                    status_pagamento: informacoes.statusPagamento || '',
                    valor_pago: informacoes.valorPago || null,
                    forma_pagamento: informacoes.formaPagamento || '',
                    autorizacao_imagem: informacoes.autorizacaoImagem || 'NÃO',
                    data_inscricao: new Date().toISOString(),
                    data_confirmacao_pagamento: null,
                    status: 'ATIVO'
                };

                debugLog('📦 Dados preparados:', dadosParaInserir.nome_completo);

                const { data, error } = await retiroSupabase
                    .from('inscricoes')
                    .insert([dadosParaInserir])
                    .select();

                if (error) {
                    debugLog('❌ Erro Supabase:', error.message);
                    
                    // Tratamento específico para erros comuns
                    if (error.code === '42501') {
                        return { 
                            success: false, 
                            error: 'Erro de permissão no banco de dados. Verifique as configurações RLS.' 
                        };
                    } else if (error.code === '23505') {
                        return { 
                            success: false, 
                            error: 'Registro duplicado. Esta pessoa já pode estar inscrita.' 
                        };
                    }
                    
                    throw error;
                }

                debugLog('✅ Sucesso Supabase:', data[0]?.nome_completo);
                return { success: true, data };

            } catch (error) {
                debugLog('❌ Erro geral:', error.message);
                return { success: false, error: error.message };
            }
        }

        // CRIAR POPUP DE SUCESSO
        function criarPopupSucesso(informacoes) {
            const overlay = document.createElement('div');
            overlay.style.cssText = `
                position: fixed;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                background: rgba(0, 0, 0, 0.8);
                z-index: 10000;
                display: flex;
                justify-content: center;
                align-items: center;
                backdrop-filter: blur(5px);
            `;

            const popup = document.createElement('div');
            popup.style.cssText = `
                background: linear-gradient(135deg, #1a1a1a, #2d2d2d);
                border: 2px solid #ff6b35;
                border-radius: 15px;
                padding: 40px;
                max-width: 500px;
                width: 90%;
                text-align: center;
                color: white;
                box-shadow: 0 20px 40px rgba(255, 107, 53, 0.3);
                animation: popupSlideIn 0.3s ease-out;
            `;

            popup.innerHTML = `
                <style>
                    @keyframes popupSlideIn {
                        from { transform: scale(0.7); opacity: 0; }
                        to { transform: scale(1); opacity: 1; }
                    }
                    .receipt-thermal {
                        font-family: 'Courier New', monospace;
                        font-size: 12px;
                        line-height: 1.2;
                        width: 280px;
                        margin: 20px auto;
                        background: white;
                        color: black;
                        padding: 10px;
                        border: 1px solid #ccc;
                        text-align: center;
                    }
                    .receipt-thermal .header {
                        font-weight: bold;
                        font-size: 14px;
                        margin-bottom: 5px;
                    }
                    .receipt-thermal .line {
                        border-bottom: 1px dashed #000;
                        margin: 5px 0;
                    }
                    .receipt-thermal .row {
                        display: flex;
                        justify-content: space-between;
                        margin: 2px 0;
                    }
                    .receipt-thermal .center {
                        text-align: center;
                        font-weight: bold;
                    }
                    .receipt-thermal .small {
                        font-size: 10px;
                    }
                </style>
                
                <div style="font-size: 4em; margin-bottom: 20px;">🎉</div>
                
                <h2 style="color: #ff6b35; font-size: 2em; margin-bottom: 20px; font-weight: 900;">
                    TENHA UM EXCELENTE RETIRO!
                </h2>
                
                <!-- RECIBO PARA IMPRESSÃO TÉRMICA -->
                <div class="receipt-thermal" id="thermal-receipt">
                    <div class="header">ALVO - UMA IGREJA, UMA VISAO</div>
                    <div class="header">VEM E VE!</div>
                    <div class="line"></div>
                    
                    <div class="center">*** COMPROVANTE PRE-INSCRICAO ***</div>
                    <div class="center">O RETIRO 2025</div>
                    <div class="line"></div>
                    
                    <div class="row">
                        <span><b>NOME:</b></span>
                    </div>
                    <div style="text-align: left; margin-bottom: 5px; font-weight: bold;">
                        ${informacoes.nome.substring(0, 32)}
                    </div>
                    
                    <div class="row">
                        <span><b>SEXO:</b></span>
                        <span><b>${informacoes.sexo}</b></span>
                    </div>
                    
                    <div class="row">
                        <span><b>WHATSAPP:</b></span>
                        <span><b>${informacoes.whatsapp}</b></span>
                    </div>
                    
                    <div class="row">
                        <span><b>VALOR PAGO:</b></span>
                        <span><b>R$ ${informacoes['valor-pago']}</b></span>
                    </div>
                    
                    <div class="line"></div>
                    
                    <div class="center small">
                        DATA: ${new Date().toLocaleDateString('pt-BR')}<br>
                        HORA: ${new Date().toLocaleTimeString('pt-BR')}
                    </div>
                    
                    <div class="line"></div>
                    
                    <div class="center">
                        <b>🎽 PROMOCAO CAMISA 🎽</b><br>
                        <span class="small">150 PRIMEIROS PAGAMENTOS<br>
                        GANHAM A CAMISA OFICIAL!</span>
                    </div>
                    
                    <div class="line"></div>
                    
                    <div class="center small">
                        <b>IMPORTANTE:</b><br>
                        NAO DEVOLVEMOS OU<br>
                        TRANSFERIMOS O VALOR<br>
                        DA INSCRICAO
                    </div>
                    
                    <div class="line"></div>
                    
                    <div class="center small">
                        RETIRO MASCULINO:<br>
                        8, 9 E 10 DE AGOSTO<br><br>
                        RETIRO FEMININO:<br>
                        15, 16 E 17 DE AGOSTO
                    </div>
                    
                    <div class="line"></div>
                    <div class="center small">*** TENHA UM EXCELENTE RETIRO ***</div>
                </div>
                
                <div style="margin: 20px 0;">
                    <button onclick="imprimirRecibo()" 
                            style="
                                background: #4ade80;
                                color: white;
                                border: none;
                                padding: 12px 30px;
                                border-radius: 8px;
                                font-size: 1.1em;
                                font-weight: 600;
                                cursor: pointer;
                                margin-right: 10px;
                            ">
                        🖨️ IMPRIMIR RECIBO
                    </button>
                    
                    <button onclick="this.parentElement.parentElement.parentElement.remove()" 
                            style="
                                background: linear-gradient(45deg, #ff6b35 0%, #ff8a5b 100%);
                                color: white;
                                border: none;
                                padding: 12px 30px;
                                border-radius: 8px;
                                font-size: 1.1em;
                                font-weight: 600;
                                cursor: pointer;
                            ">
                        FECHAR
                    </button>
                </div>
                
                <div style="background: #333; padding: 15px; border-radius: 8px; margin: 20px 0; line-height: 1.6;">
                    <h3 style="color: #ff6b35; margin-bottom: 15px;">📋 Próximos Passos:</h3>
                    <p style="font-size: 1.1em;">
                        💰 Você informou que pagará <strong>R$ ${informacoes['valor-pago']}</strong> como entrada mínima.<br><br>
                        🎽 <strong>LEMBRE-SE:</strong> Os 150 primeiros pagamentos ganham a camisa oficial do retiro!<br><br>
                        🏢 <strong>Compareça ao balcão e pague o valor mínimo de R$ 150,00</strong>
                    </p>
                </div>
            `;

            // Função para imprimir recibo
            window.imprimirRecibo = function() {
                const recibo = document.getElementById('thermal-receipt').outerHTML;
                const printWindow = window.open('', '_blank');
                printWindow.document.write(`
                    <html>
                        <head>
                            <title>Recibo - O Retiro 2025</title>
                            <style>
                                body { 
                                    margin: 0; 
                                    padding: 20px; 
                                    font-family: 'Courier New', monospace; 
                                }
                                .receipt-thermal {
                                    font-family: 'Courier New', monospace;
                                    font-size: 14px;
                                    line-height: 1.3;
                                    width: 300px;
                                    margin: 0 auto;
                                    background: white;
                                    color: black;
                                    padding: 10px;
                                    text-align: center;
                                }
                                .receipt-thermal .header {
                                    font-weight: bold;
                                    font-size: 16px;
                                    margin-bottom: 5px;
                                }
                                .receipt-thermal .line {
                                    border-bottom: 1px dashed #000;
                                    margin: 8px 0;
                                }
                                .receipt-thermal .row {
                                    display: flex;
                                    justify-content: space-between;
                                    margin: 3px 0;
                                }
                                .receipt-thermal .center {
                                    text-align: center;
                                    font-weight: bold;
                                }
                                .receipt-thermal .small {
                                    font-size: 12px;
                                }
                                @media print {
                                    body { margin: 0; padding: 5px; }
                                    .receipt-thermal { width: 280px; font-size: 12px; }
                                }
                            </style>
                        </head>
                        <body>
                            ${recibo}
                        </body>
                    </html>
                `);
                printWindow.document.close();
                printWindow.print();
            };

            overlay.appendChild(popup);
            document.body.appendChild(overlay);

            // Remover popup ao clicar no overlay
            overlay.addEventListener('click', function(e) {
                if (e.target === overlay) {
                    overlay.remove();
                }
            });
        }

        // EVENT LISTENERS
        document.getElementById('sexo').addEventListener('change', atualizarDataRetiro);

        // Configurar campos condicionais
        configurarCampoCondicional('comorbidade', 'comorbidade-detalhes');
        configurarCampoCondicional('gravida', 'gravida-detalhes');
        configurarCampoCondicional('medicacao', 'medicacao-detalhes');
        configurarCampoCondicional('restricoes', 'restricoes-detalhes');
        configurarCampoCondicional('alergias', 'alergias-detalhes');
        configurarCampoCondicional('locomocao', 'locomocao-detalhes');

        // Configurar pagamento
        document.getElementById('pagamento').addEventListener('change', function() {
            const valorGroup = document.getElementById('valor-group');
            const valorInput = document.getElementById('valor-pago');
            
            if (this.value) {
                valorGroup.style.display = 'block';
                valorInput.required = true;
                
                if (this.value === 'ENTRADA-PRÉ') {
                    valorInput.placeholder = '150,00';
                    valorInput.value = '';
                } else if (this.value === 'PAGAR-DIFERENÇA') {
                    valorInput.placeholder = 'valor';
                    valorInput.value = '';
                } else if (this.value === 'RETIRO-INTEGRAL') {
                    valorInput.placeholder = 'valor integral';
                    valorInput.value = '';
                }
            } else {
                valorGroup.style.display = 'none';
                valorInput.required = false;
            }
            
            validarValorMinimo();
        });

        document.getElementById('valor-pago').addEventListener('input', function() {
            formatarValor(this);
            validarValorMinimo();
        });

        document.getElementById('whatsapp').addEventListener('input', function() {
            formatarWhatsApp(this);
        });

        // Converter para MAIÚSCULA (exceto email)
        document.querySelectorAll('input[type="text"], textarea').forEach(input => {
            if (input.id !== 'email') {
                input.addEventListener('input', function() {
                    this.value = this.value.toUpperCase();
                });
            }
        });

        // Manter email em minúscula
        document.getElementById('email').addEventListener('input', function() {
            this.value = this.value.toLowerCase();
        });

        // SUBMIT DO FORMULÁRIO
        document.getElementById('inscricao-form').addEventListener('submit', async function(e) {
            e.preventDefault();
            
            if (isSubmittingForm) return;
            isSubmittingForm = true;
            
            debugLog('📝 Iniciando envio do formulário...');
            
            const formData = new FormData(this);
            const informacoes = Object.fromEntries(formData);
            
            // Validação básica
            if (informacoes.pagamento === 'ENTRADA-PRÉ') {
                const valor = parseFloat(informacoes['valor-pago'].replace(',', '.'));
                if (valor < 150) {
                    alert('O valor mínimo da pré-inscrição é R$ 150,00');
                    isSubmittingForm = false;
                    return;
                }
            }

            const submitBtn = document.getElementById('submit-btn');
            submitBtn.textContent = 'Enviando...';
            submitBtn.disabled = true;

            // Esconder mensagens anteriores
            document.getElementById('success-message').style.display = 'none';
            document.getElementById('error-message').style.display = 'none';

            // Preparar dados para Supabase
            const informacoesCompletas = {
                nome: informacoes.nome,
                sexo: informacoes.sexo,
                idade: informacoes.idade,
                whatsapp: informacoes.whatsapp,
                email: informacoes.email,
                endereco: informacoes.endereco,
                numero: informacoes.numero,
                bairro: informacoes.bairro,
                cidade: informacoes.cidade,
                comorbidade: informacoes.comorbidade,
                comorbidadeQual: informacoes['comorbidade-qual'] || '',
                gravida: informacoes.gravida,
                gravidaObservacao: informacoes['gravida-observacao'] || '',
                medicacao: informacoes.medicacao,
                medicacaoQual: informacoes['medicacao-qual'] || '',
                restricoes: informacoes.restricoes,
                restricoesQuais: informacoes['restricoes-quais'] || '',
                alergias: informacoes.alergias,
                alergiasQuais: informacoes['alergias-quais'] || '',
                locomocao: informacoes.locomocao,
                locomocaoQual: informacoes['locomocao-qual'] || '',
                corRede: informacoes['cor-rede'],
                vaiServirReceber: informacoes['vai-servir-receber'],
                statusPagamento: informacoes.pagamento,
                valorPago: informacoes['valor-pago'] || '',
                formaPagamento: informacoes['forma-pagamento'],
                autorizacaoImagem: informacoes['autorizacao-imagem'] ? 'SIM' : 'NÃO'
            };

            try {
                const resultado = await enviarParaSupabase(informacoesCompletas);
                
                if (resultado.success) {
                    debugLog('✅ Formulário enviado com sucesso!');
                    
                    // Criar popup de sucesso
                    criarPopupSucesso(informacoes);
                    
                    // Reset do formulário
                    this.reset();
                    document.querySelectorAll('.conditional-field').forEach(field => {
                        field.style.display = 'none';
                    });
                    document.getElementById('valor-group').style.display = 'none';
                    
                    // Reset da data display
                    document.getElementById('date-display').textContent = 'SELECIONE SEU SEXO';
                    document.getElementById('date-display').style.color = '#ff6b35';

                } else {
                    debugLog('❌ Erro no envio:', resultado.error);
                    
                    // Erro
                    document.getElementById('error-message').style.display = 'block';
                    document.getElementById('error-details').innerHTML = 
                        `❌ Erro: ${resultado.error}<br>📧 Entre em contato conosco para completar sua inscrição.`;
                }
                
            } catch (error) {
                debugLog('❌ Erro geral no formulário:', error.message);
                document.getElementById('error-message').style.display = 'block';
                document.getElementById('error-details').innerHTML = 
                    '❌ Erro de conexão. Verifique sua internet e tente novamente.';
            } finally {
                submitBtn.textContent = 'Confirmar Inscrição';
                submitBtn.disabled = false;
                isSubmittingForm = false;
            }
        });

        // INICIALIZAÇÃO
        document.addEventListener('DOMContentLoaded', function() {
            if (inicializarSistema()) {
                debugLog('🎯 Sistema inicializado com sucesso!');
                debugLog('💡 Use o painel de debug para testar funções');
                
                // Teste automático de conexão
                setTimeout(async () => {
                    const resultado = await verificarConexao();
                    if (resultado.success) {
                        debugLog('🚀 Sistema pronto para uso!');
                    } else {
                        debugLog('⚠️ Possíveis problemas de configuração detectados');
                    }
                }, 1000);
            }
        });

        // EXPOSIÇÃO DE FUNÇÕES PARA DEBUG
        window.verificarConexao = verificarConexao;
        window.inserirTeste = inserirTeste;
        window.listarRegistros = listarRegistros;
        window.toggleDebug = toggleDebug;

        debugLog('🎯 Sistema do Retiro 2025 carregado!');
        debugLog('🎽 Todas as funcionalidades incluídas!');
        debugLog('🔧 Painel de debug disponível!');
    </script>
</body>
</html>
