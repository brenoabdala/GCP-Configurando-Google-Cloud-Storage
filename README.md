<h1>Guia Passo a Passo: Criando seu Depósito de Arquivos (Cloud Storage)</h1>

<p>Este guia foi feito para quem nunca utilizou o Google Cloud. Vamos criar um "balde" (bucket) onde sua aplicação guardará fotos, documentos ou qualquer arquivo.</p>

<hr />

<h2>Etapa 1: Preparando o Terreno</h2>
<p>Pense no Google Cloud como um grande prédio de escritórios. Primeiro, precisamos dizer ao recepcionista que vamos usar a sala de arquivos.</p>
<ul>
    <li>Acesse o <a href="https://console.cloud.google.com/">Console do Google Cloud</a>.</li>
    <li>No topo da tela, clique em <strong>Selecionar um projeto</strong> (ou no nome do projeto atual) e escolha o seu.</li>
    <li>Na barra de busca (lupa) no topo, digite: <code>Cloud Storage API</code> e clique no primeiro resultado.</li>
    <li>Se aparecer um botão azul escrito <strong>ATIVAR</strong>, clique nele. Se não aparecer, já está pronto!</li>
</ul>



<h2>Etapa 2: Criando o seu "Bucket" (O Balde)</h2>
<p>No Google, chamamos as pastas de armazenamento de <strong>Buckets</strong>. É aqui que os arquivos de fato moram.</p>
<ol>
    <li>No menu lateral esquerdo, procure por <strong>Cloud Storage</strong> e clique em <strong>Buckets</strong>.</li>
    <li>Clique no botão <strong>CRIAR</strong> no topo da página.</li>
    <li><strong>Nome:</strong> Escolha um nome único. Não pode ter espaços ou letras maiúsculas. Dica: use <code>meu-projeto-storage-2024</code>.</li>
    <li><strong>Local:</strong> Escolha <code>Region</code> e selecione uma localização perto de você (ex: <code>southamerica-east1</code> para São Paulo).</li>
    <li><strong>Controle de Acesso:</strong> Desmarque a opção "Impedir acesso público" se você pretende que as fotos sejam vistas por qualquer pessoa na internet, ou deixe marcado para máxima segurança.</li>
    <li>Clique em <strong>CRIAR</strong> até o final.</li>
</ol>



<h2>Etapa 3: Criando a "Chave da Porta" (Credenciais)</h2>
<p>Seu código precisa de uma chave digital para entrar no Google Cloud sem você precisar digitar sua senha toda hora.</p>
<ol>
    <li>Busque por <strong>Contas de Serviço</strong> (Service Accounts) na barra de busca do topo.</li>
    <li>Clique em <strong>+ CRIAR CONTA DE SERVIÇO</strong>.</li>
    <li>Dê um nome simples, como <code>acesso-storage</code>, e clique em "Criar e Continuar".</li>
    <li>Em "Selecionar um papel", escolha <strong>Cloud Storage</strong> > <strong>Administrador de Objetos do Storage</strong>. Isso dá permissão para o código ler e apagar arquivos.</li>
    <li>Clique em "Concluir".</li>
</ol>

<h2>Etapa 4: Baixando o arquivo de chave</h2>
<p>Agora vamos pegar a chave física (um arquivo .json):</p>
<ol>
    <li>Na lista que apareceu, clique no e-mail da conta que você acabou de criar.</li>
    <li>Clique na aba superior chamada <strong>CHAVES</strong>.</li>
    <li>Clique em <strong>ADICIONAR CHAVE</strong> > <strong>Criar nova chave</strong>.</li>
    <li>Deixe marcado <strong>JSON</strong> e clique em <strong>CRIAR</strong>.</li>
</ol>

<hr />

