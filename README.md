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
        
        /* HEADER REDESENHADO COM LOGO */
        .header { 
            background: #000; 
            padding: 30px 30px 40px 30px; 
            text-align: center; 
            border-bottom: 2px solid #333;
        }
        
        /* LOGO DA IGREJA */
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
        
        /* Texto da Igreja */
        .church-name {
            font-size: 1.4em;
            color: #fff;
            margin-bottom: 25px;
            letter-spacing: 2px;
            font-weight: 700;
            text-transform: uppercase;
            line-height: 1.2;
        }
        
        /* Seletor de gênero */
        .genero-selector {
            font-size: 1.1em; 
            color: #ff6b35; 
            font-weight: 600; 
            margin-bottom: 15px;
            letter-spacing: 1px;
            text-transform: uppercase;
        }
        
        /* Título principal */
        .titulo-retiro { 
            font-size: 3em; 
            margin-bottom: 15px; 
            color: #fff; 
            font-weight: 900;
            letter-spacing: 3px;
            text-transform: uppercase;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        /* Subtítulo */
        .subtitle-retiro { 
            font-size: 1.2em; 
            color: #ccc;
            letter-spacing: 2px;
            font-weight: 500;
            text-transform: uppercase;
        }

        .form-container { padding: 40px; background: #111; }
        .counter { text-align: center; font-size: 1.4em; margin-bottom: 30px; padding: 15px; background: #222; border-radius: 10px; border: 1px solid #333; }
        .counter-number { color: #ff6b35; font-weight: bold; font-size: 1.5em; }
        .section-title { color: #ff6b35; font-size: 1.3em; font-weight: bold; margin: 30px 0 20px 0; padding-bottom: 10px; border-bottom: 2px solid #333; }
        .form-group { margin-bottom: 25px; }
        .conditional-field { margin-top: 15px; padding-left: 20px; border-left: 3px solid #ff6b35; display: none; }
        label { display: block; margin-bottom: 8px; font-weight: 600; color: #fff; font-size: 1.1em; }
        .required { color: #ff6b35; }
        input, select, textarea { width: 100%; padding: 15px; border: 2px solid #333; border-radius: 8px; font-size: 16px; transition: all 0.3s ease; background: #222; color: #fff; text-transform: uppercase; }
        input[type="number"], input[type="tel"] { text-transform: none; }
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
        .supabase-info { background: #0f1419; border: 1px solid #00d4aa; color: #00d4aa; padding: 15px; border-radius: 8px; margin-bottom: 20px; text-align: center; font-size: 0.9em; }
        .config-warning { background: #cc0000; color: white; padding: 10px; text-align: center; font-weight: bold; margin-bottom: 20px; border-radius: 8px; }
        
        /* RESPONSIVO */
        @media (max-width: 768px) {
            body { padding: 10px; }
            .container { margin: 0; border-radius: 10px; }
            .header { padding: 20px; }
            
            /* Logo responsivo */
            .church-logo img {
                max-width: 100px;
            }
            
            .church-name { font-size: 1.1em; }
            .titulo-retiro { 
                font-size: 2.2em;
                letter-spacing: 2px;
            }
            .subtitle-retiro { 
                font-size: 1em;
                letter-spacing: 1px;
            }
            .genero-selector {
                font-size: 1em;
            }
            .form-container { padding: 20px; }
            .section-title { font-size: 1.1em; }
            .color-list { justify-content: center; }
            .color-item { font-size: 0.8em; }
        }
        
        /* Caso a imagem não carregue */
        .church-logo img {
            background: #333;
            border: 2px dashed #666;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <!-- LOGO DA IGREJA - TROQUE APENAS O ENDEREÇO AQUI! -->
            <div class="church-logo">
                <img src="https://i.imgur.com/T5QABfl.jpeg" alt="Logo O Retiro" id="church-logo-img">
            </div>
            
            <!-- Texto da Igreja centralizado -->
            <div class="church-name">
                ALVO - UMA IGREJA, UMA VISÃO,<br>
                <strong>VEM E VÊ!</strong>
            </div>
            
            <!-- Texto "PROGRAMAÇÃO - O RETIRO" em laranja -->
            <div class="genero-selector" id="date-display">PROGRAMAÇÃO - O RETIRO</div>
            
            <!-- Subtítulo -->
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

            <div class="config-warning" id="config-warning">
                ⚠️ CONFIGURE AS CHAVES DO SUPABASE NO CÓDIGO ANTES DE USAR!
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

                <div class="form-group" id="gravida-group" style="display: none;">
                    <label for="gravida">Está grávida? <span class="required">*</span></label>
                    <select id="gravida" name="gravida">
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
        // ===================================
        // CONFIGURAÇÕES SUPABASE
        // ===================================
        
        // 🔧 CONFIGURAÇÕES DO SEU NOVO SUPABASE - ATUALIZADO!
        const SUPABASE_CONFIG = {
            url: 'https://yuikwufjkdzgdzvlotaq.supabase.co', // URL do novo projeto
            anonKey: 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Inl1aWt3dWZqa2R6Z2R6dmxvdGFxIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NTA5ODcwMzcsImV4cCI6MjA2NjU2MzAzN30.UGW0AHHSsIv842Z92F6RjI930fgS-5FmPX0i7kumgYo' // Nova chave
        };

        // Inicializar cliente Supabase
        let supabase;
        
        function initializeSupabase() {
            if (SUPABASE_CONFIG.url.includes('SEU-PROJETO') || SUPABASE_CONFIG.anonKey.includes('SUA-ANON')) {
                console.warn('⚠️ Configure as chaves do Supabase!');
                return false;
            }
            
            supabase = window.supabase.createClient(SUPABASE_CONFIG.url, SUPABASE_CONFIG.anonKey);
            document.getElementById('config-warning').style.display = 'none';
            return true;
        }

        let inscricaoCount = 0;
        let isSubmitting = false;

        // ===================================
        // CONFIGURAÇÃO DA LOGO
        // ===================================
        
        // Tratamento de erro para logo
        document.addEventListener('DOMContentLoaded', function() {
            const logoImg = document.getElementById('church-logo-img');
            
            logoImg.addEventListener('error', function() {
                console.warn('⚠️ Logo não encontrada. Verifique o endereço da imagem.');
                // Oculta a logo se não carregar
                this.style.display = 'none';
            });
            
            logoImg.addEventListener('load', function() {
                console.log('✅ Logo carregada com sucesso!');
            });
        });

        // ===================================
        // FUNÇÕES DE FORMATAÇÃO
        // ===================================
        
        function formatWhatsApp(input) {
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

        function formatValor(input) {
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
                
                if (pagamento === 'ENTRADA-PRÉ' && valor < 200) {
                    warning.style.display = 'block';
                    warning.innerHTML = '⚠️ <strong>Atenção:</strong> O valor mínimo da pré-inscrição é R$ 200,00';
                } else if (pagamento === 'RETIRO-INTEGRAL' && valor !== 520) {
                    warning.style.display = 'block';
                    warning.innerHTML = '⚠️ <strong>Atenção:</strong> O valor do retiro integral deve ser exatamente R$ 520,00';
                    valorInput.value = '520,00';
                } else {
                    warning.style.display = 'none';
                }
            } else {
                warning.style.display = 'none';
            }
        }

        // ===================================
        // CONFIGURAR CAMPOS CONDICIONAIS
        // ===================================
        
        function setupConditionalField(selectId, detailsId) {
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

        // ===================================
        // ATUALIZAR DATA BASEADA NO GÊNERO
        // ===================================
        
        function atualizarDataRetiro() {
            const genero = document.getElementById('genero').value;
            const dateDisplay = document.getElementById('date-display');
            
            if (genero === 'HOMEM') {
                dateDisplay.textContent = 'HOMENS: 8, 9 E 10 DE AGOSTO';
                dateDisplay.style.color = '#4ade80';
            } else if (genero === 'MULHER') {
                dateDisplay.textContent = 'MULHERES: 15, 16 E 17 DE AGOSTO';
                dateDisplay.style.color = '#ff6b9d';
            } else {
                dateDisplay.textContent = 'SELECIONE SEU GÊNERO';
                dateDisplay.style.color = '#ff6b35';
            }
        }

        // ===================================
        // INTEGRAÇÃO COM SUPABASE API
        // ===================================
        
        async function submitToSupabase(dados) {
            try {
                console.log('📤 Enviando para Supabase:', dados);

                const { data, error } = await supabase
                    .from('inscricoes')
                    .insert([{
                        nome_completo: dados.nome,
                        sexo: dados.sexo,
                        idade: parseInt(dados.idade),
                        whatsapp: dados.whatsapp,
                        email: dados.email,
                        endereco: dados.endereco,
                        numero: dados.numero,
                        bairro: dados.bairro,
                        cidade: dados.cidade,
                        comorbidade: dados.comorbidade,
                        comorbidade_qual: dados.comorbidadeQual || null,
                        gravida: dados.gravida,
                        gravidez_observacao: dados.gravidaObservacao || null,
                        medicacao: dados.medicacao,
                        medicacao_qual: dados.medicacaoQual || null,
                        restricoes_alimentares: dados.restricoes,
                        restricoes_quais: dados.restricoesQuais || null,
                        alergias: dados.alergias,
                        alergias_quais: dados.alergiasQuais || null,
                        limitacao_locomocao: dados.locomocao,
                        locomocao_qual: dados.locomocaoQual || null,
                        cor_rede: dados.corRede,
                        vai_servir_receber: dados.vaiServirReceber,
                        status_pagamento: dados.statusPagamento,
                        valor_pago: dados.valorPago || null,
                        forma_pagamento: dados.formaPagamento,
                        autorizacao_imagem: dados.autorizacaoImagem,
                        data_inscricao: new Date().toISOString(),
                        data_confirmacao_pagamento: null,
                        status: 'ATIVO'
                    }])
                    .select();

                if (error) throw error;

                console.log('✅ Sucesso Supabase:', data);
                return { success: true, data };

            } catch (error) {
                console.error('❌ Erro Supabase:', error);
                return { success: false, error: error.message };
            }
        }

        // ===================================
        // BUSCAR CONTADOR DE INSCRIÇÕES
        // ===================================
        
        async function buscarContadorInscricoes() {
            try {
                if (!supabase) return;

                const { count, error } = await supabase
                    .from('inscricoes')
                    .select('*', { count: 'exact', head: true });

                if (error) throw error;

                inscricaoCount = count || 0;
                console.log('Total de inscrições:', inscricaoCount);
                
            } catch (error) {
                console.log('Não foi possível buscar contador:', error);
            }
        }

        // ===================================
        // EVENT LISTENERS
        // ===================================
        
        document.getElementById('sexo').addEventListener('change', atualizarDataRetiro);

        // Configurar campos condicionais
        setupConditionalField('comorbidade', 'comorbidade-detalhes');
        setupConditionalField('gravida', 'gravida-detalhes');
        setupConditionalField('medicacao', 'medicacao-detalhes');
        setupConditionalField('restricoes', 'restricoes-detalhes');
        setupConditionalField('alergias', 'alergias-detalhes');
        setupConditionalField('locomocao', 'locomocao-detalhes');

        // Configurar pagamento
        document.getElementById('pagamento').addEventListener('change', function() {
            const valorGroup = document.getElementById('valor-group');
            const valorInput = document.getElementById('valor-pago');
            const valorWarning = document.getElementById('valor-warning');
            
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
            formatValor(this);
            validarValorMinimo();
        });

        document.getElementById('whatsapp').addEventListener('input', function() {
            formatWhatsApp(this);
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

        // ===================================
        // SUBMIT DO FORMULÁRIO
        // ===================================
        
        document.getElementById('inscricao-form').addEventListener('submit', async function(e) {
            e.preventDefault();
            
            if (isSubmitting) return;
            isSubmitting = true;
            
            const formData = new FormData(this);
            const dados = Object.fromEntries(formData);
            
        // ===================================
        // CRIAR POPUP DE SUCESSO
        // ===================================
        
        function criarPopupSucesso(dados) {
            // Criar overlay
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

            // Criar popup
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

            const valorPago = dados['valor-pago'] ? parseFloat(dados['valor-pago'].replace(',', '.')) : 0;

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
                        ${dados.nome.substring(0, 32)}
                    </div>
                    
                    <div class="row">
                        <span><b>SEXO:</b></span>
                        <span><b>${dados.sexo}</b></span>
                    </div>
                    
                    <div class="row">
                        <span><b>WHATSAPP:</b></span>
                        <span><b>${dados.whatsapp}</b></span>
                    </div>
                    
                    <div class="row">
                        <span><b>VALOR PAGO:</b></span>
                        <span><b>R$ ${dados['valor-pago']}</b></span>
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
                        💰 Você informou que pagará <strong>R$ ${dados['valor-pago']}</strong> como entrada mínima.<br><br>
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

        // ===================================
        // VALIDAÇÃO BÁSICA
            if (dados.pagamento === 'ENTRADA-PRÉ') {
                const valor = parseFloat(dados['valor-pago'].replace(',', '.'));
                if (valor < 150) {
                    alert('O valor mínimo da pré-inscrição é R$ 150,00');
                    isSubmitting = false;
                    return;
                }
            }

            // Preparar dados para Supabase
            const dadosSupabase = {
                nome: dados.nome,
                sexo: dados.sexo,
                idade: dados.idade,
                whatsapp: dados.whatsapp,
                email: dados.email,
                endereco: dados.endereco,
                numero: dados.numero,
                bairro: dados.bairro,
                cidade: dados.cidade,
                comorbidade: dados.comorbidade,
                comorbidadeQual: dados['comorbidade-qual'] || '',
                gravida: dados.gravida,
                gravidaObservacao: dados['gravida-observacao'] || '',
                medicacao: dados.medicacao,
                medicacaoQual: dados['medicacao-qual'] || '',
                restricoes: dados.restricoes,
                restricoesQuais: dados['restricoes-quais'] || '',
                alergias: dados.alergias,
                alergiasQuais: dados['alergias-quais'] || '',
                locomocao: dados.locomocao,
                locomocaoQual: dados['locomocao-qual'] || '',
                corRede: dados['cor-rede'],
                vaiServirReceber: dados['vai-servir-receber'],
                statusPagamento: dados.pagamento,
                valorPago: dados['valor-pago'] || '',
                formaPagamento: dados['forma-pagamento'],
                autorizacaoImagem: dados['autorizacao-imagem'] ? 'SIM' : 'NÃO'
            }; básica
            if (dados.pagamento === 'ENTRADA-PRÉ') {
                const valor = parseFloat(dados['valor-pago'].replace(',', '.'));
                if (valor < 200) {
                    alert('O valor mínimo da pré-inscrição é R$ 200,00');
                    isSubmitting = false;
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
            const dadosSupabase = {
                nome: dados.nome,
                genero: dados.genero,
                idade: dados.idade,
                whatsapp: dados.whatsapp,
                comorbidade: dados.comorbidade,
                comorbidadeQual: dados['comorbidade-qual'] || '',
                gravida: dados.gravida,
                gravidaObservacao: dados['gravida-observacao'] || '',
                medicacao: dados.medicacao,
                medicacaoQual: dados['medicacao-qual'] || '',
                restricoes: dados.restricoes,
                restricoesQuais: dados['restricoes-quais'] || '',
                alergias: dados.alergias,
                alergiasQuais: dados['alergias-quais'] || '',
                locomocao: dados.locomocao,
                locomocaoQual: dados['locomocao-qual'] || '',
                corRede: dados['cor-rede'],
                vaiServirReceber: dados['vai-servir-receber'],
                statusPagamento: dados.pagamento,
                valorPago: dados['valor-pago'] || '',
                formaPagamento: dados['forma-pagamento']
            };

            try {
                const result = await submitToSupabase(dadosSupabase);
                
                if (result.success) {
                    // Criar popup de sucesso
                    criarPopupSucesso(dados);
                    
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
                        `❌ Erro: ${result.error}<br>📧 Seus dados foram salvos. Entraremos em contato via WhatsApp.`;
                    
                    // Salvar dados localmente para backup
                    console.log('💾 Backup dos dados:', dadosSupabase);
                }
                
            } catch (error) {
                console.error('Erro geral:', error);
                document.getElementById('error-message').style.display = 'block';
                document.getElementById('error-details').innerHTML = 
                    '❌ Erro de conexão. Verifique sua internet e tente novamente.';
            } finally {
                submitBtn.textContent = 'Confirmar Inscrição';
                submitBtn.disabled = false;
                isSubmitting = false;
            }
        });

        // ===================================
        // INICIALIZAÇÃO
        // ===================================
        
        // Verificar se o Supabase está configurado
        function verificarConfiguracaoSupabase() {
            if (SUPABASE_CONFIG.url.includes('SEU-PROJETO') || SUPABASE_CONFIG.anonKey.includes('SUA-ANON')) {
                console.warn('⚠️ ATENÇÃO: Configure as variáveis do Supabase antes de usar!');
                return false;
            }
            return true;
        }

        // Executar verificações ao carregar
        document.addEventListener('DOMContentLoaded', function() {
            if (verificarConfiguracaoSupabase()) {
                if (initializeSupabase()) {
                    console.log('🎯 Supabase inicializado com sucesso!');
                    buscarContadorInscricoes();
                }
            }
        });

        // ===================================
        // FUNÇÕES DE TESTE
        // ===================================
        
        // Função para testar conexão (execute no console do navegador)
        window.testarSupabase = async function() {
            console.log('🧪 Testando conexão com Supabase...');
            
            try {
                const { count, error } = await supabase
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

        // Função para inserir dados de teste
        window.testeInscricao = async function() {
            console.log('🧪 Testando inserção...');
            
            const dadosTeste = {
                nome: 'TESTE SISTEMA',
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
            
            const result = await submitToSupabase(dadosTeste);
            
            if (result.success) {
                console.log('✅ Teste de inserção OK!');
                alert('✅ Teste de inserção funcionando!');
            } else {
                console.error('❌ Erro no teste:', result.error);
                alert('❌ Erro no teste: ' + result.error);
            }
        };

        console.log('🎯 Sistema Supabase carregado!');
        console.log('🎽 Informações sobre camisa incluídas!');
        console.log('🖼️ Logo configurada - troque o endereço na linha 78!');
        console.log('💡 Para testar a conexão, execute: testarSupabase()');
        console.log('💡 Para testar inserção, execute: testeInscricao()');
        console.log('');
        console.log('📋 ESTRUTURA ATUALIZADA DO BANCO (SQL):');
        console.log(`
-- Estrutura atualizada da tabela inscricoes
CREATE TABLE IF NOT EXISTS inscricoes (
    id SERIAL PRIMARY KEY,
    nome_completo VARCHAR(255) NOT NULL,
    sexo VARCHAR(20) NOT NULL CHECK (sexo IN ('MASCULINO', 'FEMININO')),
    idade INTEGER NOT NULL CHECK (idade >= 12 AND idade <= 100),
    whatsapp VARCHAR(20) NOT NULL UNIQUE,
    email VARCHAR(255) NOT NULL,
    endereco VARCHAR(500) NOT NULL,
    numero VARCHAR(20) NOT NULL,
    bairro VARCHAR(100) NOT NULL,
    cidade VARCHAR(100) NOT NULL,
    comorbidade VARCHAR(10) NOT NULL CHECK (comorbidade IN ('SIM', 'NÃO')),
    comorbidade_qual TEXT,
    gravida VARCHAR(10) NOT NULL CHECK (gravida IN ('SIM', 'NÃO')),
    gravidez_observacao TEXT,
    medicacao VARCHAR(10) NOT NULL CHECK (medicacao IN ('SIM', 'NÃO')),
    medicacao_qual TEXT,
    restricoes_alimentares VARCHAR(10) NOT NULL CHECK (restricoes_alimentares IN ('SIM', 'NÃO')),
    restricoes_quais TEXT,
    alergias VARCHAR(10) NOT NULL CHECK (alergias IN ('SIM', 'NÃO')),
    alergias_quais TEXT,
    limitacao_locomocao VARCHAR(10) NOT NULL CHECK (limitacao_locomocao IN ('SIM', 'NÃO')),
    locomocao_qual TEXT,
    cor_rede VARCHAR(20) NOT NULL,
    vai_servir_receber VARCHAR(20) NOT NULL CHECK (vai_servir_receber IN ('TRABALHO', 'ENCONTRISTA')),
    status_pagamento VARCHAR(50) NOT NULL,
    valor_pago VARCHAR(20),
    forma_pagamento VARCHAR(50) NOT NULL,
    autorizacao_imagem VARCHAR(10) NOT NULL CHECK (autorizacao_imagem IN ('SIM', 'NÃO')),
    data_inscricao TIMESTAMP WITH TIME ZONE DEFAULT NOW(),
    data_confirmacao_pagamento TIMESTAMP WITH TIME ZONE,
    status VARCHAR(20) DEFAULT 'ATIVO',
    created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW(),
    updated_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);

-- Índices para performance
CREATE UNIQUE INDEX IF NOT EXISTS idx_whatsapp_unique ON inscricoes (whatsapp);
CREATE INDEX IF NOT EXISTS idx_sexo ON inscricoes (sexo);
CREATE INDEX IF NOT EXISTS idx_status ON inscricoes (status);
CREATE INDEX IF NOT EXISTS idx_data_inscricao ON inscricoes (data_inscricao);
        `);
    </script>
</body>
</html>
