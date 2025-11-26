# Calculadora de IMC

Aplicação React para cálculo do IMC (Índice de Massa Corporal) com uma grade de níveis (Magreza, Normal, Sobrepeso, Obesidade).

## Tecnologias

- React + TypeScript
- CSS Modules
- Vite / Create React App (conforme boilerplate usado)
- Node.js / npm

## Instalação (Windows)

1. Abrir terminal na pasta do projeto:
   cd c:\Users\rodri\Desktop\Projeto-React\calc-imc
2. Instalar dependências:
   npm install
3. Rodar em modo de desenvolvimento:
   npm start

## Scripts úteis

- npm start — roda a aplicação em modo de desenvolvimento
- npm run build — build de produção
- npm test — executar testes (se houver)

## Estrutura principal

- src/
  - components/ — componentes (GridItem, etc.)
  - helpers/imc.ts — dados e cálculo de níveis de IMC
  - assets/ — imagens
  - App.tsx, App.module.css — layout principal

## Uso

1. Inserir altura em metros (ex: 1.75) e peso em kg (ex: 75.3).
2. Clicar em "Calcular".
3. O nível correspondente será exibido com cor e informação do IMC.

## Debug rápido (se as cores não aparecerem)

- Verificar se o componente GridItem recebe `item.color`. Inspecionar console para logs e DevTools → Elements para confirmar style inline.
- Garantir que o elemento tenha tamanho visível (GridItem.module.css): adicionar `min-height` ou remover `flex: 1` do pai se necessário.
- Conferir `src/helpers/imc.ts` para não deixar lacunas nos intervalos (usar limites contíguos, ex.: [0, 18.5], [18.5, 24.9], ...). Se calculateImc retornar `null`, nenhum nível será destacado.
- Confirmar que App.module.css não quebra o layout (ex.: .main definido corretamente).
- Reiniciar o dev server se necessário (Ctrl+C → npm start).

## Contribuição

- Abrir issue descrevendo problema ou sugestão.
- Criar branch, implementar e submeter PR.

## Licença

Projeto sem licença especificada. Adicionar LICENSE se necessário.
