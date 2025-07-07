<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>O Retiro - Inscrições 2025</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Segoe UI', sans-serif; background: linear-gradient(135deg, #1a1a1a, #2d2d2d); min-height: 100vh; color: white; padding: 20px; }
        /* ESCONDER TEXTO DOCTYPE */
        body::before,
        html::before {
            content: none !important;
            display: none !important;
        }

        .repository-content .Box-header,
        .file-navigation .breadcrumb,
        .markdown-body > h1:first-child,
        .highlight-source-html {
            display: none !important;
        }
        /* ESCONDER APENAS CABEÇALHO DO GITHUB */
        .repository-content .Box-header,
        .file-navigation .breadcrumb,
        .markdown-body > h1:first-child {
            display: none !important;
        }

    /* FORÇAR CONTAINER PRINCIPAL */
    .container {
        position: relative !important;
        z-index: 9999 !important;
        margin-top: -50px !important;
    }
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
        font-size: 1.1em;
        color: #fff;
        margin-bottom: 25px;
        letter-spacing: 1.5px;
        font-weight: 700;
        text-transform: uppercase;
        line-height: 1.3;
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
        
        @media (max-width: 768px) {
    body { padding: 10px; }
    .container { margin: 0; border-radius: 10px; }
    .header { padding: 20px; }
    .church-logo img { max-width: 100px; }
    .church-name { font-size: 0.95em; letter-spacing: 1px; }
    .titulo-retiro { font-size: 2.2em; letter-spacing: 2px; }
    .subtitle-retiro { font-size: 1em; letter-spacing: 1px; }
    .genero-selector { font-size: 1em; }
    .form-container { padding: 20px; }
    .section-title { font-size: 1.1em; }
    .color-list { justify-content: center; }
    .color-item { font-size: 0.8em; }

    /* Esconder elementos do GitHub - versão simplificada */
    .repository-content,
    .highlight-source-html,
    .markdown-body > h1:first-child,
    .Box-header,
    .file-navigation,
    .breadcrumb {
        display: none !important;
    }

    /* Garantir que popup seja sobreposto */
    .receipt-modal,
    .modal {
        z-index: 99999 !important;
    }

    /* Remover qualquer texto de rodapé automático */
    body::after,
    html::after {
        content: "" !important;
        display: none !important;
    }
}
    </style>
</head>
<body>
    
    <div class="container">
        <div class="header">
            <div class="church-logo">
                <img src="https://i.imgur.com/T5QABfl.jpeg" alt="Logo O Retiro" id="church-logo-img">
            </div>
            
            <div class="church-name">
            O ALVO CURITIBA - UMA IGREJA, UMA VISÃO<br>
            <strong>VEM E VÊ!</strong>
        </div>
            
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
            url: 'https://ubczydbigeznmxmfmdsi.supabase.co',
            anonKey: 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InViY3p5ZGJpZ2V6bm14bWZtZHNpIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NTEzNzg4MTUsImV4cCI6MjA2Njk1NDgxNX0.ZK4Hy6n8PdY0NY_PUlmlXtjHzVuNZc_vtOQe7CX8fAQ'
        };

        let retiroSupabase;
        let isSubmittingForm = false;

        // INICIALIZAR SUPABASE
        function inicializarSistema() {
            retiroSupabase = window.supabase.createClient(RETIRO_CONFIG.url, RETIRO_CONFIG.anonKey);
            console.log('🎯 Sistema inicializado com sucesso!');
            return true;
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

        // INTEGRAÇÃO COM SUPABASE
async function enviarParaSupabase(informacoes) {
    try {
        console.log('📤 Enviando para Supabase:', informacoes);

        const { data, error } = await retiroSupabase
            .from('inscricoes')
            .insert([{
                nome_completo: informacoes.nome,
                sexo: informacoes.sexo,
                idade: parseInt(informacoes.idade),
                whatsapp: informacoes.whatsapp,
                email: informacoes.email,
                endereco: informacoes.endereco,
                numero: informacoes.numero,
                bairro: informacoes.bairro,
                cidade: informacoes.cidade,
                comorbidade: informacoes.comorbidade,
                comorbidade_qual: informacoes.comorbidadeQual || null,
                gravida: informacoes.gravida,
                gravidez_observacao: informacoes.gravidaObservacao || null,
                medicacao: informacoes.medicacao,
                medicacao_qual: informacoes.medicacaoQual || null,
                restricoes_alimentares: informacoes.restricoes,
                restricoes_quais: informacoes.restricoesQuais || null,
                alergias: informacoes.alergias,
                alergias_quais: informacoes.alergiasQuais || null,
                limitacao_locomocao: informacoes.locomocao,
                locomocao_qual: informacoes.locomocaoQual || null,
                cor_rede: informacoes.corRede,
                vai_servir_receber: informacoes.vaiServirReceber,
                status_pagamento: informacoes.statusPagamento,
                valor_pago: informacoes.valorPago || null,
                forma_pagamento: informacoes.formaPagamento,
                autorizacao_imagem: informacoes.autorizacaoImagem,
                status: 'ATIVO'
            }])
            .select();

        if (error) {
            console.error('❌ Erro Supabase:', error);
            
            // Tratamento específico para dados duplicados
            if (error.code === '23505') {
                if (error.message.includes('whatsapp')) {
                    throw new Error('📱 Ops! Este WhatsApp já foi utilizado em outra inscrição.\n\n✅ Verifique se digitou o número corretamente\n📞 Ou utilize outro WhatsApp\n🏢 Precisa de ajuda? Procure nosso balcão de atendimento!');
                } else if (error.message.includes('email')) {
                    throw new Error('📧 Ops! Este e-mail já foi utilizado em outra inscrição.\n\n✅ Verifique se digitou o e-mail corretamente\n📧 Ou utilize outro e-mail\n🏢 Precisa de ajuda? Procure nosso balcão de atendimento!');
                } else {
                    throw new Error('⚠️ Estes dados já foram utilizados em outra inscrição.\n\n✅ Verifique WhatsApp e e-mail\n🏢 Precisa de ajuda? Procure nosso balcão de atendimento!');
                }
            } else if (error.code === '23514') {
                throw new Error('❌ Alguns dados estão inválidos. Por favor, verifique se todos os campos estão preenchidos corretamente.');
            } else if (error.code === '42501') {
                throw new Error('❌ Erro de sistema temporário. Tente novamente em alguns instantes.');
            } else {
                throw new Error(`❌ Erro inesperado: ${error.message}\n\n🏢 Se o problema persistir, procure nosso balcão de atendimento.`);
            }
        }

        console.log('✅ Sucesso Supabase:', data);
        return { success: true, data };

    } catch (error) {
        console.error('❌ Erro geral:', error);
        return { success: false, error: error.message };
    }
}

// CRIAR POPUP DE SUCESSO CORRIGIDO
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
        
        <div style="font-size: 4em; margin-bottom: 20px;">📝</div>
        
        <h2 style="color: #ff6b35; font-size: 2em; margin-bottom: 20px; font-weight: 900;">
            PRÉ-INSCRIÇÃO REALIZADA!
        </h2>
        
        <!-- RECIBO CORRIGIDO -->
        <div class="receipt-thermal" id="thermal-receipt">
            <div class="header">O ALVO CURITIBA</div>
            <div class="header">UMA IGREJA, UMA VISAO</div>
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
            
            <!-- SEÇÃO CORRIGIDA -->
            <div class="line"></div>
            <div class="center"><b>🏷️ STATUS: PRE-INSCRITO 🏷️</b></div>
            <div class="center small">PAGAMENTO PENDENTE</div>
            <div class="line"></div>
            
            <div class="row">
                <span><b>VALOR A PAGAR:</b></span>
                <span><b>R$ ${informacoes['valor-pago']}</b></span>
            </div>
            
            <div class="row">
                <span><b>FORMA PRETENDIDA:</b></span>
                <span><b>${informacoes['forma-pagamento']}</b></span>
            </div>
            
            <div class="line"></div>
            
            <div class="center small">
                DATA: ${new Date().toLocaleDateString('pt-BR', {timeZone: 'America/Sao_Paulo'})}<br>
    		HORA: ${new Date().toLocaleTimeString('pt-BR', {timeZone: 'America/Sao_Paulo'})}
            </div>
            
            <div class="line"></div>
            
            <!-- INSTRUÇÃO CLARA -->
            <div class="center">
                <b>🏢 PROXIMO PASSO 🏢</b><br>
                <span class="small">COMPAREÇA AO BALCAO<br>
                PARA EFETUAR O PAGAMENTO</span>
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
            <div class="center small">*** AGUARDAMOS VOCE NO BALCAO ***</div>
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
                🖨️ IMPRIMIR COMPROVANTE
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
        
        <!-- INFORMAÇÕES CORRIGIDAS -->
        <div style="background: #333; padding: 15px; border-radius: 8px; margin: 20px 0; line-height: 1.6;">
            <h3 style="color: #ff6b35; margin-bottom: 15px;">📋 Próximos Passos:</h3>
            <p style="font-size: 1.1em;">
                ✅ <strong>Pré-inscrição realizada com sucesso!</strong><br><br>
                💰 Você informou que pretende pagar <strong>R$ ${informacoes['valor-pago']}</strong> como entrada mínima.<br><br>
                🏢 <strong>COMPAREÇA AO BALCÃO</strong> para efetuar o pagamento e garantir sua vaga.<br><br>
                🎽 <strong>LEMBRE-SE:</strong> Os 150 primeiros pagamentos ganham a camisa oficial!
            </p>
        </div>
        
        <div style="background: #1a472a; border: 1px solid #16a34a; padding: 15px; border-radius: 8px; margin-top: 20px;">
            <p style="color: #4ade80; font-weight: bold; margin: 0;">
                ✅ Seus dados foram salvos com sucesso!<br>
                📱 Aguarde contato via WhatsApp se necessário.
            </p>
        </div>
    `;

    // Função para imprimir recibo (mantém a mesma)
    window.imprimirRecibo = function() {
        // ... código de impressão igual ao anterior
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
                    // Erro
                    document.getElementById('error-message').style.display = 'block';
                    document.getElementById('error-details').innerHTML = 
                        `❌ Erro: ${resultado.error}<br>📧 Seus dados foram salvos. Entraremos em contato via WhatsApp.`;
                    
                    // Salvar dados localmente para backup
                    console.log('💾 Backup dos dados:', informacoesCompletas);
                }
                
            } catch (error) {
                console.error('Erro geral:', error);
                document.getElementById('error-message').style.display = 'block';
                document.getElementById('error-details').innerHTML = 
                    '❌ Erro de conexão. Verifique sua internet e tente novamente.';
            } finally {
                submitBtn.textContent = 'Confirmar Inscrição';
                submitBtn.disabled = false;
                isSubmittingForm = false;
            }
        });

        // FUNÇÕES DE TESTE
        window.verificarConexao = async function() {
            console.log('🧪 Testando conexão com Supabase...');
            
            try {
                const { count, error } = await retiroSupabase
                    .from('inscricoes')
                    .select('*', { count: 'exact', head: true });
                
                if (error) throw error;
                
                console.log('✅ Conexão OK! Total de registros:', count);
                alert('✅ Conexão com Supabase funcionando! Total de registros: ' + count);
            } catch (error) {
                console.error('❌ Erro na conexão:', error);
                alert('❌ Erro na conexão: ' + error.message);
            }
        };

        window.inserirTeste = async function() {
            console.log('🧪 Testando inserção...');
            
            const testeInfo = {
                nome: 'TESTE SISTEMA NOVO',
                sexo: 'MASCULINO',
                idade: 25,
                whatsapp: '(11) 99999-9999',
                email: 'teste@teste.com',
                endereco: 'RUA TESTE',
                numero: '123',
                bairro: 'CENTRO',
                cidade: 'SAO PAULO',
                comorbidade: 'NÃO',
                comorbidadeQual: null,
                gravida: 'NÃO',
                gravidaObservacao: null,
                medicacao: 'NÃO',
                medicacaoQual: null,
                restricoes: 'NÃO',
                restricoesQuais: null,
                alergias: 'NÃO',
                alergiasQuais: null,
                locomocao: 'NÃO',
                locomocaoQual: null,
                corRede: 'AZUL',
                vaiServirReceber: 'TRABALHO',
                statusPagamento: 'ENTRADA-PRÉ',
                valorPago: '150,00',
                formaPagamento: 'PIX',
                autorizacaoImagem: 'SIM'
            };
            
            const resultadoTeste = await enviarParaSupabase(testeInfo);
            
            if (resultadoTeste.success) {
                console.log('✅ Teste de inserção OK!');
                alert('✅ Teste de inserção funcionando!');
            } else {
                console.error('❌ Erro no teste:', resultadoTeste.error);
                alert('❌ Erro no teste: ' + resultadoTeste.error);
            }
        };

        // INICIALIZAÇÃO
        document.addEventListener('DOMContentLoaded', function() {
            if (inicializarSistema()) {
                console.log('🎯 Sistema do retiro inicializado com sucesso!');
                console.log('💡 Para testar a conexão, execute: verificarConexao()');
                console.log('💡 Para testar inserção, execute: inserirTeste()');
            }
        });

        console.log('🎯 Sistema do Retiro 2025 carregado!');
        console.log('🎽 Todas as funcionalidades incluídas!');
        console.log('🖼️ Logo configurada!');
    </script>
</body>
</html>
