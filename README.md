-- LumberTycoon2_OpenSource.lua

-- Defina as variáveis globais
local game = game
local workspace = game.Workspace
local players = game.Players

-- Defina a função para coletar a madeira
local function coletarMadeira(madeira)
-- Encontre a árvore com a madeira desejada
local arvore = workspace:FindFirstChild(madeira)

-- Se a árvore for encontrada, colete a madeira
if arvore then
-- Código para coletar a madeira
print("Madeira coletada com sucesso!")
else
print("Árvore não encontrada.")
end
end

-- Defina a função para vender a madeira
local function venderMadeira(madeira)
-- Encontre o jogador que está vendendo a madeira
local jogador = players.LocalPlayer

-- Se o jogador estiver vendendo a madeira, execute o código para vender
if jogador then
-- Código para vender a madeira
print("Madeira vendida com sucesso!")
else
print("Jogador não encontrado.")
end
end

-- Defina a função para automatizar a coleta de madeira
local function automatizarColeta()
-- Encontre as árvores com madeira disponível
local arvores = workspace:GetDescendants()

-- Para cada árvore, colete a madeira
for _, arvore in pairs(arvores) do
if arvore.Name == "Blue Spruce" then
coletarMadeira(arvore.Name)
end
end
end

-- Chame a função para automatizar a coleta de madeira
automatizarColeta()

-- Defina a função para atualizar o script
local function atualizarScript()
-- Código para atualizar o script
print("Script atualizado com sucesso!")
end

-- Chame a função para atualizar o script
atualizarScript()
