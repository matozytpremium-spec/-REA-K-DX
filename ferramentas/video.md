# Ferramentas de vídeo

Instaladas pelo dono em 14/11/2026. Conferidas na sessão de nuvem (funciona
igual pelo celular, porque a sessão não roda no aparelho).

## FFmpeg (plugin `ffmpeg-llm`)

- **Estado:** pronta para uso. FFmpeg 6.1.1 instalado no container.
- **Skills:** `ffmpeg-llm:ffmpeg` e `ffmpeg-llm:ffmpeg-command` (geram o
  comando a partir de um pedido em linguagem natural) e o agente
  `ffmpeg-llm:ffmpeg-expert` (filtros complexos, diagnóstico, ajuste de
  qualidade e tamanho).
- **Serve para:** cortar, juntar, redimensionar para 1080x1920 ou 1080x1350,
  aplicar texto e logo, trocar ou tirar áudio, exportar GIF, montar motion a
  partir de imagens.
- **Saída:** arquivos finais vão para `motion/`.

## HyperFrames (HeyGen)

- **Estado:** conectado, mas limitado nas sessões do Claude Code.
- **Funciona aqui:** listar projetos, abrir projeto, consultar status de
  projeto e de render.
- **Não funciona aqui:** criar (`compose`) e renderizar (`render_video`). Esses
  dois ficam bloqueados para clientes com sistema de arquivos local.
- **Como contornar:** usar pelo chat normal do Claude, ou instalar as skills
  locais no repositório com `npx skills add heygen-com/hyperframes`.
